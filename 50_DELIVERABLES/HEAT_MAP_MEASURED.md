# THE MEASURED HEAT MAP

> *"I want you to examine how many times I repetitively ask for the same thing over and over again, and
> **turn that into a heat map** for me too, because that will tell you the things I keep begging for.
> Like, **how many times have I asked for agent span** to really be up, agent tastes, agent transcript,
> right?"*
> - The crossover doctrine, session dated 2026-07-25

**This document replaces the guessed bands in `40_GOVERNANCE/HEAT_MAP.md` with counted occurrences.**

That file said, honestly, that its bands were *"reasoned, not measured"* and that the measured version
was owed. This is the measured version. Every number below carries the exact predicate that produced it.
A count with no stated filter is not a receipt.

---

## 1. THE CORPUS OF RECORD

**Scope: his own words only.** The five folders under
`0 ANU_ANEW_OS_use to be call doctrine/1_HIS_WORDS/`: `01_RAW_WORDS`, `02_PHASE_2`, `03_PHASE_3`,
`04_THE_COUNTDOWN`, `05_THE_911s`.

Deliberately excluded: `4_WRITTEN_BY_A_CODER_NOT_HIM/`, `06_OLD_WORLD_HIS_WORDS/`,
`SHIFT_CHANGE_REPORTS/`, and every estate-authored document. If a coder wrote it, it is not an ask.

| Corpus fact | Value | Predicate |
|---|---|---|
| Sessions counted | **110** | `[MEASURED - file count after the dedupe rules in section 2]` |
| Words | **776,734** | `[MEASURED - wc -w over the 110 normalized session files]` |
| Characters | **4,021,043** | `[MEASURED - sum of len() over the 110 normalized session files]` |
| Earliest session | **2026-05-30** | `[MEASURED - 01_RAW_WORDS/01_20260530_HEAT.txt, date from filename]` |
| Latest session | **2026-08-16** | `[MEASURED - 03_PHASE_3/Mt Rushmore Doctrine pt 1_transcript.txt, date from file mtime]` |
| Span | **79 days** | `[MEASURED - 2026-05-30 to 2026-08-16]` |

His own estimate in doctrine was *"~600,000 unique words across the corpus."* Measured total words in
his-words-only: **776,734**. His estimate was the right order of magnitude and slightly low.

---

## 2. THE DEDUPE, STATED

`0 ANU OS Doctrines as of Aug 15th 26/` duplicates `1_HIS_WORDS/` by filename and was **not counted at
all**. Only `1_HIS_WORDS/` was read. Within `1_HIS_WORDS/` there are further internal duplicates, removed
as follows:

| File dropped | Reason | Predicate |
|---|---|---|
| `04_THE_COUNTDOWN/COUNTDOWN_pt1_20260812.txt` | byte-identical to the `03_PHASE_3` copy | `[MEASURED - md5sum match b8750f8a...]` |
| `04_THE_COUNTDOWN/COUNTDOWN_pt2_20260812.txt` | byte-identical to the `03_PHASE_3` copy | `[MEASURED - md5sum match 65b1b6e5...]` |
| `04_THE_COUNTDOWN/COUNTDOWN_pt3_20260812.rtf` | byte-identical to the `03_PHASE_3` copy | `[MEASURED - md5sum match e57fd516...]` |
| `04_THE_COUNTDOWN/COUNTDOWN_pt4_20260813.rtf` | byte-identical to the `03_PHASE_3` copy | `[MEASURED - md5sum match 7276e122...]` |
| `03_PHASE_3/The Countdown doctrine pt 3.rtf` | RTF markup; the plain-text conversion in `04` was used instead | `[JUDGEMENT - stated, not measured]` |
| `03_PHASE_3/The Countdown doctrine pt 4.rtf` | same | `[JUDGEMENT - stated, not measured]` |
| `03_PHASE_3/text.txt` | 24 bytes, a stub | `[MEASURED - wc -c = 24]` |
| `03_PHASE_3/Call with [a partner]/Call with [a partner].md` | 98 bytes, an attachment pointer | `[MEASURED - wc -c = 98]` |

**Net: 118 files present, 8 dropped, 110 counted.** The three PDFs in the corpus were text-extracted and
counted. Nothing else was skipped.

**Known scope gap, declared:** the two *Pecking Order* doctrine transcripts exist in the corpus only
under `0 ANU OS Doctrines as of Aug 15th 26/these are phase 3 doctrines raw words as of 081626 at
11pmest/` and have **no counterpart inside `1_HIS_WORDS/`**. They are therefore **outside the corpus of
record and are not counted anywhere in this document**, even though `40_GOVERNANCE/HEAT_MAP.md` cites
`PO2-14` as evidence. Every count below is short by whatever those two sessions contain. This is a
filing defect in `1_HIS_WORDS/`, not a counting choice.

---

## 3. THE `grep -c` TRAP, DEMONSTRATED

His transcripts are one enormous line per speaking turn. Measured line geometry:

| File | Lines | Longest single line |
|---|---|---|
| `01_RAW_WORDS/13_20260612_SPRING_WATER.txt` | 222 | **4,176 chars** |
| `02_PHASE_2/Banana Pepper Doctrine pt 1.txt` | 134 | **3,904 chars** |
| `03_PHASE_3/Sesame Chicken Doctrine.txt` | 251 | **4,039 chars** |

`[MEASURED - awk 'BEGIN{max=0}{if(length($0)>max)max=length($0)}END{print NR, max}' <file>]`

`grep -c` counts **matching lines**. When he says a word nine times inside one 4,000-character speaking
turn, `grep -c` returns 1. Here is the size of the error, same regex, same files, both ways:

| Ask | Matching LINES (`grep -c` equivalent) | Actual OCCURRENCES (`grep -o` equivalent) | Undercount |
|---|---|---|---|
| advisors | 300 | 836 | **64%** |
| Easter eggs | 23 | 67 | **66%** |
| ACL | 114 | 271 | **58%** |
| world builder | 68 | 163 | **58%** |
| Agent SPAN | 49 | 114 | **57%** |
| roadmaps | 167 | 321 | **48%** |
| coding department | 84 | 160 | **48%** |
| memory | 139 | 251 | **45%** |
| nasty cough family | 66 | 115 | **43%** |
| STAMP family | 115 | 187 | **39%** |

`[MEASURED - per-line re.findall over the 107 plain-text session files, counting matching lines vs summed match counts; the 3 PDF sessions are excluded from this demonstration table only, which is why these figures run slightly below the ranked table]`

**A line-based count of this corpus is wrong by 39% to 66%.** Every band in the guessed heat map was
assigned without this correction being available.

**How the ranked table was actually counted, so it can be re-run:** each session file was normalized by
collapsing every whitespace run (spaces, tabs, newlines) into a single space, making the whole file one
line. Occurrences were then counted with `re.finditer(pattern, text, re.IGNORECASE)`, non-overlapping.
This is the `grep -o | wc -l` result, immune to line geometry.

---

## 4. THE RANKED TABLE

Bands are **measured**, defined on distinct sessions out of 110:
**🔥🔥🔥 = 40+ sessions · 🔥🔥 = 15 to 39 sessions · 🔥 = 2 to 14 sessions · ❄ = 0 or 1 session.**

"Still open" is a **derived** flag, and the derivation is stated: **OPEN** means the ask's last
occurrence falls in the final window 2026-08-12 to 2026-08-16 (the last 11 sessions) **and** at least one
unbuilt-or-demand phrase co-occurs within 220 characters of an occurrence somewhere in the corpus.
The unbuilt-phrase pattern is
`(haven'?t|have not|hasn'?t|has not|didn'?t|did not|never)\s+(been\s+)?(built|build|birthed|done|got|created|made)|still\s+(not|hasn'?t|ain'?t)|we\s+(got|gotta|have)\s+to\s+build|need(s)?\s+to\s+(be\s+)?build|i\s+need\s+you\s+to\s+build|what happened to|how many times have i asked`.
"COLD TAIL" means the last ask predates the final window. "NO DEMAND SIGNAL" means zero unbuilt-phrase
co-occurrences.

| # | Ask | Occurrences | Sessions | Band | First | Last | Unbuilt co-occ. | Still open? |
|---:|---|---:|---:|:--:|---|---|---:|---|
| 1 | **advisors** | **844** | **79** | 🔥🔥🔥 | 2026-06-10 | 2026-08-16 | 45 | **OPEN** |
| 2 | reach (bare token, all senses) | 574 | 88 | 🔥🔥🔥 | 2026-05-30 | 2026-08-16 | 29 | OPEN |
| 3 | AIR (bare token) | 478 | 53 | 🔥🔥🔥 | 2026-05-30 | 2026-08-16 | 9 | OPEN |
| 4 | **roadmaps** | **324** | **61** | 🔥🔥🔥 | 2026-05-30 | 2026-08-16 | 13 | **OPEN** |
| 5 | **ACL** | **273** | **51** | 🔥🔥🔥 | 2026-05-30 | 2026-08-15 | 8 | **OPEN** |
| 6 | **memory** | **269** | **54** | 🔥🔥🔥 | 2026-06-08 | 2026-08-16 | 9 | **OPEN** |
| 7 | STAMP (bare token family) | 221 | 51 | 🔥🔥🔥 | 2026-05-30 | 2026-08-16 | 6 | OPEN |
| 8 | **streaming** | **210** | **52** | 🔥🔥🔥 | 2026-06-02 | 2026-08-16 | 3 | **OPEN** |
| 9 | **world builder** | **166** | **21** | 🔥🔥 | 2026-07-30 | 2026-08-16 | 6 | **OPEN** |
| 10 | **coding department** | **160** | **41** | 🔥🔥🔥 | 2026-05-30 | 2026-08-16 | 7 | **OPEN** |
| 11 | SHADOW (bare token family) | 150 | 27 | 🔥🔥 | 2026-05-30 | 2026-08-16 | 0 | NO DEMAND SIGNAL |
| 12 | **nasty cough family** | **124** | **31** | 🔥🔥 | 2026-07-01 | 2026-08-16 | 9 | **OPEN** |
| 13 | **Agent SPAN** | **115** | **31** | 🔥🔥 | 2026-06-09 | 2026-08-16 | 5 | **OPEN** |
| 14 | TASTE (bare token) | 103 | 28 | 🔥🔥 | 2026-06-02 | 2026-08-16 | 3 | OPEN |
| 15 | **reach / "reaching me" (strict)** | **97** | **31** | 🔥🔥 | 2026-05-30 | 2026-08-13 | 5 | **OPEN** |
| 16 | **life modules / life goals** | **91** | **22** | 🔥🔥 | 2026-07-20 | 2026-08-16 | 3 | **OPEN** |
| 17 | KEEPER | 81 | 20 | 🔥🔥 | 2026-06-19 | 2026-08-16 | 1 | OPEN |
| 18 | **penny hustle** | **77** | **23** | 🔥🔥 | 2026-06-13 | 2026-08-11 | 2 | COLD TAIL |
| 19 | **chattering** | **73** | **33** | 🔥🔥 | 2026-06-09 | 2026-08-16 | 3 | **OPEN** |
| 20 | **Wonder Games** | **68** | **20** | 🔥🔥 | 2026-07-01 | 2026-08-16 | 2 | **OPEN** |
| 21 | **Easter eggs** | **67** | **15** | 🔥🔥 | 2026-06-02 | 2026-08-15 | 7 | **OPEN** |
| 22 | **gauntlet** | **62** | **11** | 🔥 | 2026-08-07 | 2026-08-16 | 1 | **OPEN** |
| 23 | Agent SPAN, named form only | 54 | 18 | 🔥🔥 | 2026-06-09 | 2026-08-16 | 3 | OPEN |
| 24 | **freestyling** | **54** | **17** | 🔥🔥 | 2026-07-10 | 2026-08-16 | 1 | **OPEN** |
| 25 | **DECODER** | **54** | **22** | 🔥🔥 | 2026-05-30 | 2026-08-16 | 3 | **OPEN** |
| 26 | TASTE (named agent) | 51 | 21 | 🔥🔥 | 2026-06-03 | 2026-08-16 | 3 | OPEN |
| 27 | **onboarding** | **43** | **20** | 🔥🔥 | 2026-06-17 | 2026-08-16 | 4 | **OPEN** |
| 28 | **shared repos** | **33** | **15** | 🔥🔥 | 2026-05-30 | 2026-08-13 | 1 | **OPEN** |
| 29 | **Coding Cookoff** | **33** | **14** | 🔥 | 2026-07-20 | 2026-08-16 | 2 | **OPEN** |
| 30 | cold code (spelled or spoken) | 31 | 18 | 🔥🔥 | 2026-07-01 | 2026-08-16 | 0 | NO DEMAND SIGNAL |
| 31 | Agent TRANSCRIPT | 31 | 17 | 🔥🔥 | 2026-06-12 | 2026-08-11 | n/a | COLD TAIL |
| 32 | AUDRA | 29 | 14 | 🔥 | 2026-05-30 | 2026-08-16 | 0 | NO DEMAND SIGNAL |
| 33 | Agent FIND | 28 | 15 | 🔥🔥 | 2026-06-08 | 2026-08-11 | 0 | COLD TAIL |
| 34 | LOGFUL | 25 | 18 | 🔥🔥 | 2026-05-30 | 2026-08-16 | 3 | OPEN |
| 35 | **job descriptions** | **21** | **14** | 🔥 | 2026-06-13 | 2026-08-16 | 4 | **OPEN** |
| 36 | **the researcher** | **20** | **10** | 🔥 | 2026-07-11 | 2026-08-16 | 3 | **OPEN** |
| 37 | **PMS / planted memory** | **20** | **4** | 🔥 | 2026-08-12 | 2026-08-16 | 2 | **OPEN** |
| 38 | **purge** | **18** | **7** | 🔥 | 2026-07-20 | 2026-08-16 | 2 | **OPEN** |
| 39 | **bridge builder** | **16** | **3** | 🔥 | 2026-08-09 | 2026-08-12 | 4 | **OPEN** |
| 40 | **false choices** | **15** | **4** | 🔥 | 2026-08-03 | 2026-08-16 | 0 | NO DEMAND SIGNAL |
| 41 | Agent SPAN, speech-to-text "spam" | 12 | 8 | 🔥 | 2026-06-08 | 2026-08-13 | 0 | NO DEMAND SIGNAL |
| 42 | **"she can't go down"** | **7** | **4** | 🔥 | 2026-07-11 | 2026-08-16 | 5 | **OPEN** |
| 43 | **retention** | **6** | **4** | 🔥 | 2026-08-02 | 2026-08-10 | 1 | COLD TAIL |
| 44 | STAMP (named agent) | 4 | 4 | 🔥 | 2026-06-09 | 2026-08-02 | 0 | COLD TAIL |
| 45 | MIMI | 2 | 2 | 🔥 | 2026-08-15 | 2026-08-16 | 0 | NO DEMAND SIGNAL |
| 46 | **conversation vehicle** | **1** | **1** | ❄ | 2026-08-16 | 2026-08-16 | 1 | **OPEN** |
| 47 | **reward system** | **0** | **0** | ❄ | never | never | 0 | **NEVER ASKED** |

### 4.1 The predicate for every row

Every row above was produced by `re.finditer(<pattern>, <normalized session text>, re.IGNORECASE)`.
`[MEASURED - patterns as listed]`

| # | Ask | Exact pattern |
|---:|---|---|
| 1 | advisors | `\badvisors?\b` |
| 2 | reach (bare) | `\breach\w*` |
| 3 | AIR (bare) | `\bair\b` |
| 4 | roadmaps | `\broadmaps?\b` |
| 5 | ACL | `\bacl\b` |
| 6 | memory | `\bmemor(y\|ies)\b` |
| 7 | STAMP family | `\bstamp\w*\b` |
| 8 | streaming | `\bstream\w*` |
| 9 | world builder | `\bworld\s?builders?\b` |
| 10 | coding department | `coding\s+department` |
| 11 | SHADOW family | `\bshadow\w*` |
| 12 | nasty cough family | `nasty\s+(coughs?\|coughed\|coughing\|calls?\|colds?\|codes?\|c\b\|c'?s\b\|seas\|seeds\|cop\|copper\|coffeeer\|sneeze)` |
| 13 | Agent SPAN | `\bspans?\b` |
| 14 | TASTE (bare) | `\btastes?\b` |
| 15 | reach / reaching me | `reach\w*\s+(me\|him\|us\|out to me)\|(can'?t\|cannot\|couldn'?t\|isn'?t\|not\|won'?t)\s+(be\s+)?(able\s+to\s+)?reach\w*` |
| 16 | life modules / life goals | `life\s+modules?\b\|life\s+goals?\b` |
| 17 | KEEPER | `\bkeepers?\b` |
| 18 | penny hustle | `\bpenny\s?hustl\w*` |
| 19 | chattering | `\bchatter\w*` |
| 20 | Wonder Games | `wonder\s+games?\b` |
| 21 | Easter eggs | `easter\s?eggs?\b` |
| 22 | gauntlet | `\bgauntlets?\b` |
| 23 | Agent SPAN named | `\bagents?\s+spans?\b` |
| 24 | freestyling | `\bfreestyl\w*` |
| 25 | DECODER | `\bdecoders?\b` |
| 26 | TASTE named | `\bagents?\s+tastes?\b` |
| 27 | onboarding | `\bonboard\w*` |
| 28 | shared repos | `shared\s+repos?\b` |
| 29 | Coding Cookoff | `\bcook\s?offs?\b` |
| 30 | cold code | `\bc\s*o\s*l\s*d\s*[\.,]?\s*c\s*o\s*d\s*e\b` |
| 31 | Agent TRANSCRIPT | `\bagents?\s+transcripts?\b` |
| 32 | AUDRA | `\baudra\b` |
| 33 | Agent FIND | `\bagents?\s+finds?\b` |
| 34 | LOGFUL | `\blog\s?ful\w*\b\|\blogfel\b\|\bl\s*g\s*f\s*u\s*l\b\|\blog\s+full\b` |
| 35 | job descriptions | `job\s+descriptions?\b` |
| 36 | the researcher | `\bresearchers?\b` |
| 37 | PMS / planted memory | `\bPMS\b\|planted\s+memor\w*` |
| 38 | purge | `\bpurg\w+` |
| 39 | bridge builder | `bridge\s?builders?\b` |
| 40 | false choices | `false\s+choices?` |
| 41 | SPAN as "spam" | `\bspams?\b` |
| 42 | she can't go down | `(can'?t\|cannot\|never\|won'?t\|not)\s+(go\|going\|goes\|went)\s+down\|go(ing)?\s+down\s+(again\|anymore\|on me)` |
| 43 | retention | `\bretention\b` |
| 44 | STAMP named | `\bagents?\s+stamp\w*` |
| 45 | MIMI | `\bmimi\b` |
| 46 | conversation vehicle | `conversation\s+vehicles?\b` |
| 47 | reward system | `\brewar\w*` |

---

## 5. FOOTNOTES ON CONTAMINATED PREDICATES

Three rows in the table are token counts, not clean ask counts. Stated, not hidden.

**S1 - Agent SPAN.** `\bspans?\b` returns 115. Manual inspection of all 115 found **5 ordinary English
uses** (*"in the span of a day"*, *"span out 10 phases"*, *"a span of message"*, *"roadmap span type"*,
*"in the span of like a week"*). Clean agent-sense count: **110**.
`[MEASURED - \bspans?\b = 115, minus 5 hand-classified English-sense hits]`

Separately, `\bspams?\b` returns **12 occurrences in 8 sessions**, of which **8 are speech-to-text for
SPAN** and 4 are genuine junk-mail sense. He corrects the machine himself in one of them: *"So if I say
at agent spam, right, or I'm sorry, at spam s at no, I'm not saying spam. I'm saying span s p a n,
right?"*
`[MEASURED - \bspams?\b = 12, hand-classified 8 SPAN / 4 junk-mail]`

**Best single figure for Agent SPAN: 118 occurrences across 31 of 110 sessions**
(110 clean `span` + 8 speech-to-text `spam`). `[DERIVED from the two MEASURED figures above]`

**R1 - reach.** `\breach\w*` returns 574 across 88 sessions, but that token carries *outreach*, *reach a
channel*, *reach out to them*, and *reach the goal*. The strict ask predicate (row 15) returns **97
across 31 sessions**. The honest statement is a range: **97 strict, 574 loose.** The guessed heat map's
🔥🔥🔥 band for REACH survives only on the loose predicate.

**A1 - AIR.** `\bair\b` returns 478. AIR is the name of the mega-LLM in his system, so most hits are the
agent, but the token also carries *"in the air"*, *"on air"*, and *"air quotes"*. Attempts to build a
false-positive filter kept catching genuine agent references (*"on air server"*, *"the air cycle"*,
*"the air router"*). **AIR cannot be counted reliably by token and is listed in section 8.**

---

## 6. NAMED-AGENT DISAMBIGUATION

Several wonders are named with ordinary English words. Both the loose token count and the strict
`agent <name>` count are given so nobody quotes the wrong one.

| Wonder | Bare token | Sessions | `agent <name>` form | Sessions |
|---|---:|---:|---:|---:|
| TASTE | 103 | 28 | **51** | 21 |
| STAMP | 221 | 51 | **4** | 4 |
| SHADOW | 150 | 27 | **2** | 1 |
| KEEPER | 81 | 20 | **12** | 2 |
| SPAN | 115 | 31 | **54** | 18 |
| FIND | n/a | n/a | **28** | 15 |
| DECODER | 54 | 22 | **0** | 0 |
| AUDRA | 29 | 14 | **0** | 0 |
| MIMI | 2 | 2 | **0** | 0 |

`[MEASURED - \b<token>s?\b vs \bagents?\s+<token>\w*, re.IGNORECASE, over the 110 normalized sessions]`

**Reading:** TASTE and SPAN are genuinely and repeatedly named as agents. STAMP is overwhelmingly the
**verb** (*"stamp these chats"*, *"time stamp"*), which is a doctrine about stamping, not a request for a
wonder called Stamp. DECODER, AUDRA and MIMI are **never once** prefixed with the word "agent".

---

## 7. WHAT THE MEASURED MAP CHANGES vs THE GUESSED ONE

`40_GOVERNANCE/HEAT_MAP.md` published 28 banded entries. **22 of them are measurable with the ask list
counted here. Of those 22: 4 were right, 1 was half right, and 17 were wrong.** Six were outside this
counting pass. Every disagreement, named:

### 7.1 The guess was RIGHT (4)

| Guessed | Measured | Verdict |
|---|---|---|
| ROADMAPS at 🔥🔥🔥 | 324 occurrences, 61 sessions, band 🔥🔥🔥 | **Right.** |
| THE ADVISORS at 🔥🔥🔥 | 844 occurrences, 79 sessions, band 🔥🔥🔥 | **Band right, rank badly wrong.** See 7.5. |
| SHARED REPOS at 🔥🔥 | 33 occurrences, 15 sessions, band 🔥🔥 | **Right, at the very bottom edge of the band.** |
| bridge builder at 🔥 | 16 occurrences, 3 sessions, band 🔥 | **Right.** |

### 7.2 The guess was HALF right (1)

**REACH at 🔥🔥🔥.** Measured 574 occurrences in 88 sessions on the bare token (🔥🔥🔥) but only 97 in
31 sessions on the strict *"reach me / reaching me / can't reach"* predicate (🔥🔥). The band is
defensible only if you count every use of the word. **The guess published no predicate, so the band was
unfalsifiable.** That is the exact failure this document exists to end.

### 7.3 The guess ran TOO HOT (7 wrong)

| Guessed | Measured | How wrong |
|---|---|---|
| **NO NASTY COUGH, NO PMS at 🔥🔥🔥**, called *"the most-repeated constraint in the entire corpus"* and said to appear in *"nearly every doctrine session"* | nasty cough family: **124 occurrences, 31 of 110 sessions (28%)**. Band 🔥🔥. | **Wrong on the band and categorically wrong on the superlative.** It is not the most-repeated constraint. It is not close. Advisors outrank it 844 to 124 and 79 sessions to 31. "Nearly every session" is measurably 28% of sessions. |
| **PMS at 🔥🔥🔥**, fused into the same entry and implied to run *"since June"* | **20 occurrences, 4 of 110 sessions.** First appearance **2026-08-12**. Band 🔥. | **Wrong by two bands, and wrong about the age.** PMS does not exist in this corpus before 2026-08-12. It is a **late** ask, not an old one. Fusing it with nasty cough hid that completely. |
| **THE RESEARCHER at 🔥🔥🔥** | **20 occurrences, 10 of 110 sessions.** Band 🔥. | **Wrong by two bands.** The guess promoted it because he counts it out loud in one session. Him counting it once does not make it frequent. It makes it *conspicuous*, which is a different signal, and the guess conflated the two. |
| **NO FALSE CHOICES at 🔥🔥🔥** | **15 occurrences, 4 of 110 sessions.** First appearance 2026-08-03. Band 🔥. | **Wrong by two bands.** The guess quoted *"I'm going to paste that in every chat"* as evidence of frequency. He said he *would* paste it; the corpus shows he said it in 4 sessions. An intention to repeat is not repetition. |
| **AGENT SPAN at 🔥🔥🔥** | **115 occurrences (118 with the speech-to-text variant), 31 of 110 sessions.** Band 🔥🔥. | **Wrong by one band.** SPAN is real, sustained (2026-06-09 to 2026-08-16) and still open, but it is not in the top tier by frequency. It is the **example he happened to reach for** while ordering the heat map, and the guess mistook the example for the answer. |
| **THE CONVERSATION VEHICLE at 🔥🔥**, described as *"asked repeatedly across several sessions"* | **1 occurrence, 1 session, 2026-08-16.** Band ❄. | **Flatly wrong.** He said it once, in the most recent session in the corpus. The guessed band's own written definition ("several sessions") is falsified by the guessed band's own cited quote. |
| **JOB DESCRIPTIONS at 🔥🔥** | **21 occurrences, 14 sessions.** Band 🔥. | **Wrong by one band.** Also: the guess claimed *"first 20260603, last 20260814."* Measured **first 2026-06-13, last 2026-08-16.** Both endpoints in the guess are wrong. |

Two further too-hot calls inside compound entries:

| Guessed | Measured | How wrong |
|---|---|---|
| **SHE CANNOT GO DOWN at 🔥🔥** | **7 occurrences, 4 sessions.** Band 🔥. | **Wrong by one band.** Note it has the **highest unbuilt-phrase density in the entire corpus** (5 demand co-occurrences against 7 occurrences). Low frequency, maximum pressure. Frequency alone would have buried it. |
| **CODELESS / PURGE THE CODE at 🔥🔥** | purge: **18 occurrences, 7 sessions.** Band 🔥. | **Wrong by one band.** |
| **MEMORY AND RETENTION at 🔥🔥** | memory: **269 occurrences, 54 sessions (🔥🔥🔥)**. retention: **6 occurrences, 4 sessions (🔥), and 2 of those 6 are inside a coder-written PDF, not his speech.** | **Wrong in both directions at once.** The fusion averaged a top-tier ask with a near-absent one and produced a middle band that describes neither. Memory is understated by a band; retention is overstated by a band. |

### 7.4 The guess ran TOO COLD (10 wrong)

| Guessed | Measured | How wrong |
|---|---|---|
| **ACL at 🔥**, bottom tier, bundled as *"ACL as legend and decoder"* | **273 occurrences, 51 of 110 sessions**, spanning 2026-05-30 to 2026-08-15. Band 🔥🔥🔥. | **Wrong by two bands. The single largest miss in the guessed map.** ACL is the fifth most repeated ask in his entire corpus and the guess filed it in the bottom tier of a bullet list. |
| DECODER, bundled into that same 🔥 line | **54 occurrences, 22 sessions.** Band 🔥🔥. | **Wrong by one band**, and it should never have been bundled with ACL: DECODER is never once said as "agent decoder". |
| **THE CODING DEPARTMENT at 🔥🔥** | **160 occurrences, 41 of 110 sessions**, from 2026-05-30 to 2026-08-16. Band 🔥🔥🔥. | **Wrong by one band.** It is one of only two asks present in both the first and the last session of the corpus with 40+ session coverage. |
| **STREAMING, FREESTYLING, CHATTERING at 🔥🔥** | streaming **210 / 52 sessions (🔥🔥🔥)**, chattering **73 / 33 (🔥🔥)**, freestyling **54 / 17 (🔥🔥)**. | **Wrong by one band on the streaming half.** The compound entry hid that streaming alone is a top-tier ask. |
| **Easter eggs at 🔥** | **67 occurrences, 15 sessions.** Band 🔥🔥. | **Wrong by one band.** |
| **The Wonder Games at 🔥** | **68 occurrences, 20 sessions.** Band 🔥🔥. | **Wrong by one band.** (The Coding Cookoff half, 33 / 14, band 🔥, was right.) |
| **Life modules and life goals at 🔥** | **91 occurrences, 22 sessions.** Band 🔥🔥. | **Wrong by one band.** |
| **Model tiering and penny hustle at 🔥** | penny hustle **77 occurrences, 23 sessions.** Band 🔥🔥. | **Wrong by one band.** |
| **Onboarding experiences at 🔥** | **43 occurrences, 20 sessions.** Band 🔥🔥. | **Wrong by one band.** |

### 7.5 The guess carried an ask he has never made (1)

**"Onboarding experiences and the reward system" at 🔥.**

> **`\brewar\w*` returns 0 occurrences across all 110 sessions and 776,734 words.**
> `[MEASURED - re.finditer(r'\brewar\w*', text, re.I) over the 110 normalized session files]`

He has **never once** used the word "reward", "rewards" or "rewarding" in his own words in this corpus.

Meanwhile the estate carries it in **six documents**: `20_ROADMAPS/R4_FRONT_ENDS.md` (7 mentions
including a section heading), `20_ROADMAPS/R8_MEMORY_AND_CONTINUITY.md`, `10_SPINE/DEPENDENCY_GRAPH.md`,
`00_DOCTRINE_INTAKE/INTAKE_20260816_PECKING_ORDER_PT2.md`, `README.md`, and
`40_GOVERNANCE/HEAT_MAP.md` itself.
`[MEASURED - grep -rion "reward[a-z]*" --include='*.md' over the repository]`

**This is the finding that justifies the exercise.** A guessed heat map does not just mis-rank real asks.
It can invent one, and once invented it propagates into roadmaps, the dependency graph, and the README,
where it competes for build capacity against things he actually said 844 times. The reward system is
either an inheritance from the Pecking Order intake or a coder's idea wearing his voice. **Either way it
is not in his words and must not be ranked as an ask until someone produces the sentence where he asks
for it.**

### 7.6 The guess did not band things he says constantly (10 omissions)

Never appeared in any band of the guessed map, measured here:

| Ask | Occurrences | Sessions | Band |
|---|---:|---:|:--:|
| **world builder** | 166 | 21 | 🔥🔥 |
| **STAMP family** | 221 | 51 | 🔥🔥🔥 |
| **SHADOW family** | 150 | 27 | 🔥🔥 |
| **TASTE** | 103 (51 as "agent taste") | 28 | 🔥🔥 |
| **KEEPER** | 81 | 20 | 🔥🔥 |
| **gauntlet** | 62 | 11 | 🔥 |
| **Agent TRANSCRIPT** | 31 | 17 | 🔥🔥 |
| **AUDRA** | 29 | 14 | 🔥 |
| **Agent FIND** | 28 | 15 | 🔥🔥 |
| **LOGFUL** | 25 | 18 | 🔥🔥 |
| **MIMI** | 2 | 2 | 🔥 |

**Two of these are named in the sentence that ordered the heat map.** He said: *"how many times have I
asked for agent span to really be up, **agent tastes, agent transcript**."* He named three asks. The
guessed map banded one of them and omitted the other two entirely.

### 7.7 What the guess could not be checked against (6)

Not in this counting pass, so no verdict is issued: THE WALKTHROUGH, *"a new Supabase and a new Render,
clean"*, per-HAM isolation, *"sign your name"*, *"never end a turn without someone up"*, *"shift change
reports every turn"*. These are behavioural standing orders rather than named asks and would need a
different predicate (they have no stable keyword). **Not estimated.**

---

## 8. WHAT I COULD NOT COUNT RELIABLY

Declared rather than estimated.

1. **AIR.** `\bair\b` = 478 occurrences in 53 sessions, but the token is his mega-LLM's name **and** an
   ordinary English word. Every filter I built to remove *"in the air"* also removed genuine agent
   references such as *"on air server"* and *"the air cycle"*. **No clean number is available.**
   `agent air` plus `air server|air code|air wall` gives **29 in 10 sessions**, which is certainly an
   undercount. The honest statement is: AIR is somewhere between 29 and 478, and the corpus cannot
   currently separate them.

2. **The two Pecking Order sessions.** They have no copy inside `1_HIS_WORDS/` (section 2). Every count
   in this document is short by their contents. **The fix is a filing fix, not a counting fix.**

3. **Session dates for 72 of the 110 sessions.** 38 sessions carry a date in the filename; the other 72
   were dated from **file modification time**, which is a proxy for the recording or export date and can
   be wrong. `[MEASURED - 38 filename-derived, 72 mtime-derived]` This affects the "first" and "last"
   columns for every ask whose endpoints fall on a `02_PHASE_2`, `03_PHASE_3` or `05_THE_911s` session.
   **Occurrence counts and session counts are unaffected.** Ordering within a single day is unreliable.

4. **Turn attribution.** The counts do not separate his speech from the other speaker's in the
   transcripts. Otter-style files mark "Speaker 1" and "Speaker 2" inconsistently across the corpus and
   several files have no speaker markers at all. **Every count above is corpus-level, not
   founder-utterance-level.** For the doctrine sessions this is a small error, since he does nearly all
   the talking; for the meeting recordings and the two partner calls it may not be. This is the single
   biggest available improvement to the measured heat map and it needs the transcripts normalized to a
   speaker-tagged format first.

5. **"The walkthrough" and the other standing behavioural orders** (section 7.7). No stable keyword,
   therefore no predicate, therefore no number.

6. **Semantic restatement.** Every count is lexical. When he asks for the same thing in different words
   ("she has to have a researcher" vs "birth the researcher" vs "who is going to find things for her"),
   only the ones containing the counted token are counted. **All counts here are lower bounds on the ask,
   and upper bounds on the phrase.**

---

## 9. WHAT THE MEASURED MAP SAYS THAT THE GUESSED ONE DID NOT

**1. The advisors ask is not merely hot, it is the corpus.** 844 occurrences across 79 of 110 sessions,
with 45 unbuilt-phrase co-occurrences, the highest raw demand pressure of anything counted. The next
genuinely clean ask (roadmaps) is 324. **The advisors ask is 2.6 times larger than anything else he
says.** The guessed map listed it seventh of seven in its top band.

**2. The advisors ask has a birthday, and it is not the start.** Zero occurrences in the first ten
sessions (2026-05-30 through the morning of 2026-06-10). It begins in one session on 2026-06-10 with
*"advisors, this is the advisors department, that's what this is"* and never stops.
`[MEASURED - \badvisors?\b returns 0 for sessions 01 through 10 and 25 for session 11]`
**The heat is not evenly spread through the corpus, and a map that cannot show onset is missing half the
signal.** The guessed map had no onset column.

**3. Heat does not correlate with age, which is the opposite of what the guessed map concluded.** The
guessed map's headline finding was *"the hottest items are the oldest."* Measured: the top ask by
occurrence starts on day 12 of 79. PMS, banded hottest by the guess, starts on day 75 of 79. Meanwhile
ACL, present from the first session to nearly the last, was banded coldest. **There is no age
correlation. The guess found one because it was reasoning from memory of what felt loud.**

**4. Frequency and pressure are two different measurements, and both are needed.** *"She can't go down"*
is said 7 times but 5 of those 7 sit inside a demand phrase. *SHADOW* is said 150 times with **zero**
demand phrases anywhere near it. A pure frequency map would promote SHADOW and bury the contract. The
unbuilt-phrase column is the correction, and it is measurable.

**5. He counts out loud exactly twice, and both times it is about a wonder that was never born.**
`[MEASURED - "how many times (have|did) i (asked|ask|been asking)" returns 2 occurrences in 2 sessions]`
Once on 2026-07-25 (*"how many times have I asked for agent span to really be up, agent tastes, agent
transcript"*) and once on 2026-08-16 (*"She has to have a researcher. How many times have I asked for the
researcher that still hasn't been birthed?"*). **Three weeks apart, and the second one is the last
session in the corpus.** He was still running the count manually on the last day of the record, which
means the heat map he ordered on 2026-07-25 was not delivered in the 22 days before the corpus ends.

**6. The guessed map was wrong 17 times out of 22 checkable calls, and it invented one ask outright.**
Not because the reasoning was careless, but because **reasoned bands over 776,734 words cannot be right**.
The failure mode is not sloppiness, it is the method. This is why he ordered a count and not an opinion.

---

## 10. REPRODUCING THIS

1. Build the corpus of record: the five folders under `1_HIS_WORDS/`, minus the 8 files listed in
   section 2. Extract text from the 3 PDFs.
2. Normalize each file: collapse every whitespace run to a single space, making the file one line. This
   is what defeats the line-geometry problem in section 3.
3. Count with `re.finditer(pattern, text, re.IGNORECASE)`, non-overlapping, summed across files. Record
   the set of files with at least one hit as the session count.
4. Date each session from its filename where a `20\d{6}` string is present, else from file mtime, and
   **mark which**.
5. For the demand column, search the unbuilt-phrase pattern in section 4 within 220 characters either
   side of each occurrence.
6. Publish the pattern next to every number. **A count with no stated filter is not a receipt.**

**When this map and a roadmap disagree about what matters, this map is evidence and the roadmap is
opinion. When this map and the guessed map disagree, the guessed map is retired.**
