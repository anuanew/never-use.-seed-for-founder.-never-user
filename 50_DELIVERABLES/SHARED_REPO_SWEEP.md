# SHARED REPO OCCURRENCE SWEEP

**Executes:** `20_ROADMAPS/R3_SHARED_REPOS.md` phase S0, sub-phases **S0.1** (the occurrence sweep)
and **S0.2** (the readings already visible in the corpus).

**The order this answers:**
> *"First thing we got to do is establish share repos. **We gotta go audit this.**"*
> [HIS WORDS + `1_HIS_WORDS/03_PHASE_3/Mt Rushmore Doctrine pt 1_transcript.txt`]

**The question this is built to let him answer:**
> *"Please explain to me what the heck I've been saying with shared repo and what that means,
> because I came up with that on a whim, and you just been like, yeah, share repo, but we haven't
> actually instituted this, so I don't know what this means."*
> [HIS WORDS + `1_HIS_WORDS/01_RAW_WORDS/10_20260610est_SWEET_AND_SPICY_pt2.txt`]

**Status of this document:** evidence only. **No reading is chosen here.** R3's founding premise
governs: he asked what he meant, so no coder gets to tell him what he meant.

---

## 0. CONVENTIONS IN THIS FILE

- Every row and quote is stamped **[HIS WORDS + file]** or **[CODER DOC + file]**.
- Personal names inside quotes are replaced with bracketed roles. Substitutions used:
  `[the founder]`, `[alpha tester A]`, `[alpha tester B]`, `[a brother]`, `[a sister]`,
  `[an advisor]`, `[founder-handle]`, `[founder-first-name]`. Every other word inside quote marks is
  verbatim. One source **filename** (row A58) carries a personal name and is shown with the
  bracketed role substituted in place; the on-disk name is unchanged and the rest of the path is
  exact.
- No credentials, tokens, keys or secret values appear here. Where a source document contained
  hardcoded keys, that fact is noted and the values are not reproduced.
- Speech-to-text noise is left as found. Where he says "share repo" the transcript is quoted as
  "share repo", not silently corrected to "shared repo".

---

## 1. METHOD AND PREDICATES

### 1.1 What was searched

Whole corpus at `corpus/`, both parts (`0 pt 1 TEMP OS New World LLM`, `1 pt 2 TEMP OS New World
LLM`). **1,399 files present. 1,165 machine-readable text files** matching extensions
`.md .txt .rtf .jsonl .json .html .js .jsx .tsx .py .csv`.

**Not searched: 185 PDF files, 3 .docx, 3 .xlsx, 10 .zip, 4 .png.** This is a known gap in this
sweep, declared rather than hidden. Two of the un-searched PDFs sit inside `1_HIS_WORDS`
(`05_THE_911s/Failed Lessons - Agent Cook - IRIS - interview.pdf`,
`05_THE_911s/Failed Lessons - Agent Cook - Strat Plan - BDIF.pdf`) and one is
`03_PHASE_3/TEMP CODER .md.pdf`. If a shared-repo passage lives in a PDF it is not in this table.

### 1.2 Patterns, and the raw predicate for each

Case-insensitive. Counted by **occurrence, not by matching line**, because his transcripts run one
paragraph per line and line-matching undercounts badly. Raw counts before any deduplication:

| Pattern | Raw occurrences | Note |
|---|---|---|
| `shared repo` | 186 | includes the 51 `shared repos` |
| `share repo` | 48 | includes the 18 `share repos` |
| `shared repository` | **0** | the variant the roadmap anticipated does not appear |
| `share repose` | **0** | the speech-to-text variant the roadmap anticipated does not appear |
| `run of show` | 250 | plus 19 as `run-of-show` |
| `tattoo` | 43 | his renaming order, plus unrelated senses |

The unified regex used for the sweep table below is `shared?[\s\-_]repos?`, which catches
`shared repo`, `share repo`, `shared repos`, `share repos`, `shared-repo`, `share-repo`,
`shared_repo`, and the shouted `SHARED repo`. **234 raw occurrences** before deduplication.

### 1.3 The deduplication predicate

The corpus carries whole mirrored trees. `0 ANU OS Doctrines as of Aug 15th 26/` mirrors
`1_HIS_WORDS/`; `4_WRITTEN_BY_A_CODER_NOT_HIM/06_OLD_WORLD_CODER_BUILT/` mirrors
`1 pt 2 .../ACW WALL .../`. Counting those twice would inflate every number in this document.

**Predicate:** files were hashed with sha256; byte-identical files collapsed to one canonical copy;
the canonical copy is the one whose path contains `1_HIS_WORDS/`, else the shortest path.
**710 unique files out of 1,165.** All counts below are post-deduplication.

Post-deduplication: **131 occurrences** of the shared-repo family.

### 1.4 The HIS versus CODER predicate

**Primary predicate, path only:** an occurrence is HIS if its canonical path contains
`0 ANU_ANEW_OS_use to be call doctrine/1_HIS_WORDS/`. Everything else is a coder's. This is the
folder law stated by the corpus itself:

> *"`1_HIS_WORDS/` - the Origin Story. 138 files. 1,143,878 words. Every one spoken or written by
> the founder. Byte-identical to source. Nothing summarised, condensed, reworded or written on his
> behalf."*
> [CODER DOC + `0 ANU_ANEW_OS_use to be call doctrine/00_READ_ME_FIRST.md`]

**The predicate does not fully hold, and section 3 documents where it breaks.** Three published
splits, so nothing is hidden behind one number:

| Predicate | HIS | CODER | Total |
|---|---|---|---|
| **P1** folder path only | 66 | 65 | 131 |
| **P2** P1 corrected for authorship of the document | 62 | 69 | 131 |
| **P3** P2 corrected for format-twin duplicates and one misfiled transcript | **60** | **68** | **128** |

**The reading tally in section 6 uses P3.** P1 and P2 are published so the correction is auditable.

---

## 2. HEADLINE COUNTS

- **128 distinct occurrences** of "shared repo" and its variants across the corpus (P3).
- **60 are his own spoken words. 68 are a coder's writing.**
- His 60 occurrences fall in **31 files across 30 distinct sessions**, from 20260530 to 20260816.
- **The reading his own words support most is R2 DEDUPLICATION: 31 of 60.**
- **R1 PROPAGATION, which the roadmap calls "the strongest and most-repeated sense," is supported by
  3 of his 60 occurrences, and its headline quote occurs exactly once in the entire corpus.**
- **R3 FAN-OUT is supported by exactly 1 of his 60 occurrences.**
- **16 of his 60 occurrences are him asking what it means, ordering it audited, complaining he was
  never answered, or announcing he is about to explain it. He is the largest single voice in the
  corpus asking this question.**

---

## 3. THREE DEFECTS FOUND IN THE CORPUS ITSELF

These are audit findings, not readings. They change the counts, so they come before the table.

### 3.1 Four coder documents are filed inside `1_HIS_WORDS/`

All four sit in `1_HIS_WORDS/06_OLD_WORLD_HIS_WORDS/AbaServer 2/`. Each names a literal GitHub
repository and specifies file paths and packages, which is coder writing, not speech:

| File | Occurrences | Why it is a coder document |
|---|---|---|
| `BRAINDUMP ABASERVER/AOA_CONTEXT_POOL_10K.md` | 1 | *"in the aba-shared repo. Currently 400+ lines - violates the under-100-lines rule."* |
| `BRAINDUMP ABASERVER/LOGFUL_AGENT_ROADMAP.md` | 1 | *"New package: @aba/logful-core in aba-shared repo."* |
| `BRAINDUMP ABASERVER/WRITES_AGENT_ROADMAP_v1.md` | 1 | *"In: aba-shared repo (`[founder-handle]/aba-shared`)"* |
| `logful abaserver/doctrine/CLABA_CODING_PROJECT_INSTRUCTIONS.md` | 1 | *"the Triplet Rule says fix the shared repo unless [the founder] scoped one surface"* |

The same folder also carries the "run of show" mismatch: `BDIF_BRAIN_EXTRACTION_20260531.md` (8
occurrences) and `doctrine/SWEETEST_HEAT_VISION.md` (7 occurrences) are both coder extraction and
compilation documents sitting under `_HIS_WORDS`. **In that one folder the rule that actually holds
is file extension: the `.txt` transcripts are his, the `.md` documents are a coder's.** This matters
beyond this sweep, because any seeding or search that trusts the folder label will teach a coder's
summary of him as his word, which is the exact failure `00_READ_ME_FIRST.md` says the folder split
exists to prevent.

### 3.2 One of his transcripts is filed inside the coder tree

`1 pt 2 .../Ababase/ABA reforged/OG Plans/ALL OF ABA rules especially for coding.txt` opens
*"[The founder] 0:03 Okay, so here's my issue with you. You have been coding ccwa For about two
whole days now."* It is a verbatim session transcript. It contains one shared-repo occurrence
(C35 in table B) and it is **his**, not a coder's. It is counted as his under P3.

### 3.3 The Countdown pt 4 exists as an `.rtf` and a `.txt` of the same session

`1_HIS_WORDS/03_PHASE_3/The Countdown doctrine pt 4.rtf` and
`1_HIS_WORDS/04_THE_COUNTDOWN/COUNTDOWN_pt4_20260813.txt` carry the same three utterances. They are
not byte-identical, so sha256 deduplication did not catch them. **3 occurrences are a format twin,
not three more times he said it.** P3 counts them once. This is the R2 headline quote, so the
inflation would have landed on the most load-bearing evidence in the file.

### 3.4 A coder document claims he already approved the thing he later asked about

Not a counting defect. It is the finding that most bears on why S0 exists.

> *"The founder has already said YES to the shared repo model."*
> [CODER DOC + `1 pt 2 .../Anew bootstrap/BOOTSTRAPS for new Anew coding/AWA CLAIR_LANE_CODING_ROADMAP_AWA_CIB_CIP_20260719.md`, dated 20260719]

The timeline against that sentence, from his own words:

| Date | Who | What |
|---|---|---|
| 20260610 | **him** | *"Please explain to me what the heck I've been saying with shared repo and what that means... we haven't actually instituted this, so I don't know what this means."* |
| 20260719 | a coder | *"The founder has already said YES to the shared repo model."* |
| 20260810-11 | **him** | *"the notion of shared repos - I don't think you still have hurt [heard] me yet on that, or really like entertained me on share repos."* |
| 20260816 | **him** | *"First thing we got to do is establish share repos. We gotta go audit this."* |

A coder recorded consent in July for a term he said in June he could not define, and in August he
said he still had not been heard on it. **No occurrence anywhere in the corpus records him choosing
a reading.** Section 7 states the question that closes this.

---

## 4. TABLE A: HIS OCCURRENCES

60 occurrences. All stamped **[HIS WORDS]**. `#` is occurrence index, not line number. Files are
relative to `1_HIS_WORDS/` except A60, noted.

Reading legend: **R1** propagation, one source that updates everywhere. **R2** deduplication,
shared components and assets in one place. **R3** fan-out, updates reaching every person's world.
**R4** findability, an ACL address you can ask for by name. **R5** other, including him asking what
it means.

| # | File | What he was pointing at | Reading |
|---|---|---|---|
| A01 | `01_RAW_WORDS/01_20260530_HEAT.txt` | front-end roadmap history: *"even in the minimum front ends we use different shared repos"* | R2 |
| A02 | `01_RAW_WORDS/01_20260530_HEAT.txt` | ACL as decoder and legend: *"I should be able to say, where's shared repo code, or something that controls an ACL, can get you there"* | **R4 anchor** |
| A03 | `01_RAW_WORDS/02_20260602_SPICY_HEAT.txt` | the arm and the skin: *"if you're an arm, right, you have these tattoos. I want, I want, I want shared repos to be called tattoos"* | R2 + naming order |
| A04 | `01_RAW_WORDS/02_20260602_SPICY_HEAT.txt` | *"the tattoos basically are for shared repos, right, for that, for this section... how to make the perfect this and that"* | R2 |
| A05 | `01_RAW_WORDS/04_20260605est_SWEETER_HEAT.txt` | work summaries as a shared reading shelf: *"the agents who are responsible for catching shared repos and shadow"* | R5 (a watcher beat, not an architecture) |
| A06 | `01_RAW_WORDS/05_20260608_SWEETEST_HEAT_oG.txt` | file-name addressing: *"how we did share repos and how those will be pulling up the same files is broken up just like that"* | R4 (+R2) |
| A07 | `01_RAW_WORDS/07_20260609_SWEETEST_HEAT_pt2_long.txt` | rebuild scope: *"we have front ends, we have shared repos, we have all of this stuff right now, and it just all of that will have to be redone"* | R5 (inventory) |
| A08 | `01_RAW_WORDS/08_20260609_SWEET_AND_SALTY.txt` | UI he is dictating: *"Again, these are shared repos I'm giving you. You're going to import them in"* | R2 |
| A09 | `01_RAW_WORDS/08_20260609_SWEET_AND_SALTY.txt` | *"we're going to talk more about share repos in a second"* | R5 (announcement) |
| A10 | `01_RAW_WORDS/08_20260609_SWEET_AND_SALTY.txt` | *"because I'm a cook on shared repos, I promise you that"* | R5 (announcement) |
| A11 | `01_RAW_WORDS/08_20260609_SWEET_AND_SALTY.txt` | after listing his backgrounds: *"Everything I just said is a shared repo"* | R2 |
| A12 | `01_RAW_WORDS/08_20260609_SWEET_AND_SALTY.txt` | *"But what a shared repo means is..."* | **R5, the definitional question** |
| A13 | `01_RAW_WORDS/08_20260609_SWEET_AND_SALTY.txt` | *"...is that a shared repo?"* | **R5, the definitional question** |
| A14 | `01_RAW_WORDS/08_20260609_SWEET_AND_SALTY.txt` | *"There got to be a way for you to update stuff, because in my mind, a shared repo is so the back end knows exactly what's going on in that mood"* | **R1** |
| A15 | `01_RAW_WORDS/08_20260609_SWEET_AND_SALTY.txt` | *"for me the value of the shared repo is... those backgrounds... whenever our coder is coding, she goes in to the library"* | R2 |
| A16 | `01_RAW_WORDS/08_20260609_SWEET_AND_SALTY.txt` | *"I talked about the share repos, right? So that was the other thing I had highlighted"* | R5 (agenda note) |
| A17 | `01_RAW_WORDS/10_20260610est_SWEET_AND_SPICY_pt2.txt` | *"that same front end code, though, can literally be merged to share repo, right? Like this is all can be connected... we'll be able to update as need be"* | **R1** |
| A18 | `01_RAW_WORDS/10_20260610est_SWEET_AND_SPICY_pt2.txt` | *"a run of show is all code, but again, my run of show code can be shared repo, so if I ever update a run of code, it updates everywhere"* | **R1 anchor** |
| A19 | `01_RAW_WORDS/10_20260610est_SWEET_AND_SPICY_pt2.txt` | *"that dynamic variable, a shared repo that's loaded in. We know what glass is, we know what percentage Ken Burns animations run on, we know what backgrounds are imported in"* | R2 |
| A20 | `01_RAW_WORDS/10_20260610est_SWEET_AND_SPICY_pt2.txt` | *"the problem with code is, is that it's hard to update it everywhere for everyone, but not underneath this new model... if we ever decide to update Agent Cook, and we change Agent Cook's name to be Agent Cooking, guess what? Just updated [alpha tester A]s, [the founder], [alpha tester B]s, everyone"* | **R3 anchor, and the only one** |
| A21 | `01_RAW_WORDS/10_20260610est_SWEET_AND_SPICY_pt2.txt` | *"my whole Share Repo moving backgrounds are imported in Ken Burns Animations, Glass Frost, everywhere"* | R2 |
| A22 | `01_RAW_WORDS/10_20260610est_SWEET_AND_SPICY_pt2.txt` | *"and all of this is shared repo"* | R5, immediately preceding the question |
| A23 | `01_RAW_WORDS/10_20260610est_SWEET_AND_SPICY_pt2.txt` | *"Please explain to me what the heck I've been saying with shared repo and what that means, because I came up with that on a whim"* | **R5, THE QUESTION** |
| A24 | `01_RAW_WORDS/10_20260610est_SWEET_AND_SPICY_pt2.txt` | *"you just been like, yeah, share repo, but we haven't actually instituted this, so I don't know what this means"* | **R5, THE QUESTION** |
| A25 | `01_RAW_WORDS/10_20260610est_SWEET_AND_SPICY_pt2.txt` | *"that code is darn near identical on every move, so that's why it's a shared repo, right? And we can just dynamically import it"* | R2 |
| A26 | `01_RAW_WORDS/10_20260610est_SWEET_AND_SPICY_pt2.txt` | *"those components are streamed in from the share repo source, so the same button that controls the plus sign... is the same button in the same code that G and G U is using"* | R2 |
| A27 | `01_RAW_WORDS/12_20260611_HOP_WATER_2.txt` | naming discipline: *"I know that this is backslash, you know, reach backslash front and cold share repo live, you know, ACL name"* | R4 |
| A28 | `01_RAW_WORDS/13_20260612_SPRING_WATER.txt` | *"If it's something that feels like it should be a shared repo item, right, something that others know how to do, they must draw from it, like we perfect the chat box"* | R2 |
| A29 | `01_RAW_WORDS/13_20260612_SPRING_WATER.txt` | signing into a portal: *"the front ends at a service is all the same, it's just Share Repo front in the service, but the back end is all of my stuff"* | R2, with the isolation contrast attached |
| A30 | `01_RAW_WORDS/13_20260612_SPRING_WATER.txt` | advisor mode: *"because front end code share repo lives underneath that identified channel, so it says, oh yeah, it has a chat box, same chat box"* | R2 |
| A31 | `01_RAW_WORDS/32_20260701est_NYC_53RD_STREET_DOCTRINE_pt1.txt` | the merit directory of ACL: *"This is how they build. This is when we make shared repos"* | R4 |
| A32 | `01_RAW_WORDS/32_20260701est_NYC_53RD_STREET_DOCTRINE_pt1.txt` | *"You're going to have to import some shared repo"* | R2 |
| A33 | `01_RAW_WORDS/32_20260701est_NYC_53RD_STREET_DOCTRINE_pt1.txt` | *"Think about how much better my system will be when we're actually using shared repos, but then take the layer of ACL on top of it... Harder to steal"* | R4 |
| A34 | `02_PHASE_2/Banana Pepper Doctrine pt 1.txt` | *"track works on CIP and merging shared repos and making sure it all works, and then does what what auditor is making sure that somebody didn't just break... the C I B version"* | R2 |
| A35 | `02_PHASE_2/Banana Pepper Doctrine pt 1.txt` | agent job descriptions: *"generated a lot of that assignment from something like a template, like a share repo or something, something that's like stampable, that's findable"* | R4 |
| A36 | `02_PHASE_2/Demo Day doctrine.txt` | the migration plan he wanted told to him: *"I'm gonna move this to share repos. I'm already working on it"* | R2 |
| A37 | `02_PHASE_2/Governor's Doctrine pt 1_otter.ai.txt` | *"when it gets ready to act, they can use code. It can touch shared repo. Can also be coded summons"* | R5 (an agent action surface) |
| A38 | `02_PHASE_2/Great reset doctrine pt 4_otter.ai.txt` | the real chat imported into the portal: *"that would be what is dynamically imported there, but just more in a miniaturized version... A UI specific for that, but it's still shared repo"* | R2 |
| A39 | `02_PHASE_2/Life assistant Doctrine pt 5 (budget...).txt` | sky writing: *"some actual coding of animations that would be shared repo. All of my apps can kind of have that strategic look"* | R2 |
| A40 | `02_PHASE_2/Pre governor doctrine ELECTROLYTES_otter.ai.txt` | *"we need to be building this to be portable... It has to be shared repo, right? Even as you're building this, now is the perfect time to work on that dynamic"* | R2 |
| A41 | `02_PHASE_2/Pre governor doctrine ELECTROLYTES_otter.ai.txt` | the things she must learn to hate: *"judging for scaffold, for non-dynamic dynamic variables, things that are not shared repos, tracks that are stalled, bleeds, leaks"* | R5 (a defect signal) |
| A42 | `02_PHASE_2/Rebirth Doctrine - Times Square.txt` | live mode inserting a widget: *"you share repo because you' gonna be able to insert that shit"* | R2 |
| A43 | `02_PHASE_2/Rebirth Doctrine - Times Square.txt` | *"share repos are a must. But what you're gonna have to do? You have to go look for [them]... I think we put these all in GitHub"* | R4 |
| A44 | `02_PHASE_2/Rebirth Doctrine - Times Square.txt` | *"got to share repos to be able to import everything that you need"* | R2 |
| A45 | `02_PHASE_2/Rebirth doctrine pt 6 Clair command center, usage, tools.txt` | *"you rob me the honor of not having a fully flushed and functional UI because you refuse to truly make every element a share repo"* | R2 |
| A46 | `02_PHASE_2/Rebirth doctrine pt 6 Clair command center, usage, tools.txt` | *"Almost every code in the share repo should have that ACL should define it"* | R4 |
| A47 | `02_PHASE_2/The Cycle Doctrine pt 3.txt` | *"We got to lean back into the share repo model that was really important, and we just kind of left it down"* | R2 |
| A48 | `02_PHASE_2/The Cycle Doctrine pt 3.txt` | *"the share repo model was always supposed to kind of help with that... cinematic moving backgrounds. That's not something that you gotta keep recreating. That's something that we import"* | R2 |
| A49 | `02_PHASE_2/Why do people scaffold_ doctrine pt 1_transcript.txt` | *"I love pink smoke and wet city share repo backgrounds with nice big bold font"* | R2 |
| A50 | `03_PHASE_3/Find me or Fine me doctrine pt 1_otter.ai.txt` | *"the notion of shared repos - I don't think you still have hurt [heard] me yet on that"* | **R5, never answered** |
| A51 | `03_PHASE_3/Find me or Fine me doctrine pt 1_otter.ai.txt` | *"or really like entertained me on share repos"* | **R5, never answered** |
| A52 | `03_PHASE_3/Find me or Fine me doctrine pt 1_otter.ai.txt` | *"That was a while ago when I used to preach that. I used to live and breathe by share repos, bro. I've kind of let my foot off the gas a little bit on it, but that's important"* | **R5, never answered** |
| A53 | `03_PHASE_3/Mt Rushmore Doctrine pt 1_transcript.txt` | *"It might be working on in an order of importance... First thing we got to do is establish share repos. We gotta go audit this, right?"* | **R5, THE ORDER** |
| A54 | `03_PHASE_3/My Resolve doctrine pt 1_transcript.txt` | the form builder: *"having the Cam Burns polish on it the glass all of that share repo easy"* | R2 |
| A55 | `03_PHASE_3/The Countdown doctrine pt 4.rtf` | *"if you're gonna have a button to dial her, it's in the exact same spot, right? As all of the other front ends. It's called a shared repo"* | R2 |
| A56 | `03_PHASE_3/The Countdown doctrine pt 4.rtf` | *"The backgrounds are in the same spot. It's called a shared repo, right? I've went on and on about this"* | **R2 anchor** |
| A57 | `03_PHASE_3/The Countdown doctrine pt 4.rtf` | *"You then start to build in components into them that are shared repo, right? You build a C A R A"* | R2 |
| A58 | `06_OLD_WORLD_HIS_WORDS/AbaServer 2/BRAINDUMP ABASERVER/[founder-first-name] on friday may 22nd 2026 Code Audit Instructions_transcript.txt` | *"that's the whole model of shared reposing and 90% back in, 10% front end"* | R2 |
| A59 | `06_OLD_WORLD_HIS_WORDS/AbaServer 2/BRAINDUMP ABASERVER/lots of thoughts on life apps and moods...txt` | *"I thought that Trace should have a whole entire subgraph dedicated to the content of the apps and the shared repos and stuff, like from a data standpoint"* | R4 |
| A60 | **filed in the coder tree**: `1 pt 2 .../Ababase/ABA reforged/OG Plans/ALL OF ABA rules especially for coding.txt` | *"if you do a major breakthrough on GMG, you right, I tell you change the iframe layout to pink... You're going to change the shared repo, unless I specifically ask for only GMG"* | R2, and the origin of the coders' Triplet Rule |

**Occurrences removed from table A and why:**

| Removed | Reason | Now counted as |
|---|---|---|
| 3 occurrences in `04_THE_COUNTDOWN/COUNTDOWN_pt4_20260813.txt` | format twin of A55, A56, A57 (section 3.3) | not counted |
| 4 occurrences in `06_OLD_WORLD_HIS_WORDS/AbaServer 2/` `.md` files | coder documents misfiled under `_HIS_WORDS` (section 3.1) | table B, C66 to C69 |

**"Cam Burns," A54 and its Table B echo, resolved.** A self-audit flagged `A54` and the form-builder row
in Table B (§5) as a possible unredacted private name, since neither reads as an obvious real term.
**Checked against the raw transcript directly:** `03_PHASE_3/My Resolve doctrine pt 1_transcript.txt`
itself contains the literal string *"having the Cam Burns polish on it"* - this is exactly what is in
the source file, not an error introduced by this sweep. Separately, **"Ken Burns" (the pan-and-zoom
photo effect, a real, well-known, non-private cinematography term) appears correctly 14 other times
across `1_HIS_WORDS/`**, including twice for this identical concept (shared-repo background
animations). The single "Cam Burns" instance is almost certainly that file's own transcription engine
mishearing "Ken Burns" on one occasion, the same class of error already documented elsewhere in this
estate for "MIMI"/"minimum viable version" and "LGF UL"/"LOGFUL." **Reading: not a name, not PII,
carried faithfully. No redaction needed.** `[MEASURED, not just re-asserted]`

---

## 5. TABLE B: CODER OCCURRENCES

68 occurrences, all stamped **[CODER DOC]**. Grouped, because the coder corpus repeats one thing.

| Group | Files and counts | What the coder documents say | Reading |
|---|---|---|---|
| **The Triplet Rule**, restated across five near-identical architecture one-pagers | `ABA Architecture v6.md` 2, `ABA Architecture v7.md` 1, `ABA_ARCHITECTURE_ONE_PAGER.md` 2, `ABA_Architecture_One_Pager_v4.md` 2, `ABA_Architecture_v5.md` 2 | *"If you make a breakthrough on one surface, change the SHARED repo unless [the founder] explicitly asked for that one surface only. Don't copy code platform-to-platform."* Traced to A60, his own words | **R2** x9 |
| **The `aba-shared` monorepo**, as a physical GitHub repository | `ABA_DIALS_MASTER_PLAN.md` 4, `WRAPSMITH_logful_build_20260531.md` 2, `WRAPSMITH_gmg_formation_portal_build_20260528.md` 1, `⬡B-logful.bootstrap...We Are All ABA.md` 2, `CLABA_BOOTSTRAP_MESA_IRIS_20260531.md` 1, `GMGU_VISUAL_RESTORATION_ROADMAP.md` 1, `writ_subgraph_offline.jsonl` 2, plus the 4 misfiled files from section 3.1 | *"dial-core.js lives in aba-shared repo. CIP, CIB, and standalone all import from the core."* *"The aba-shared repo has 14 cores."* Named packages, named branches, named paths | **R2** x17 |
| **Monorepo consolidation planning** | `ABA_Technical_Roadmap_v2.md` 4, `aba_technical_roadmap_v2.jsonl` 3, `aba roadmap may9 v1.jsonl` 5 of 6, `aba_manual_v1_6.jsonl` 1 as noted below, `brainstorm/text.txt` 2, `00_MASTER_CONVERSION_PLAN.md` 1 | *"The shared-repo consolidation (aba-shared monorepo exists with 3 packages, needs to absorb mesa-core, iris-core, gmgu-core..."* *"Shared repo, not monolith... No copy-paste"* | **R2** x14 |
| **Component and asset inventories** | `DOCTRINE_INTAKE_PACKET_20260814.md` 2, `THE A'NU APP - Master Roadmap to the Index.md` 1, `ENVOLVE_CORONATION_ROADMAP_20260721.md` 1, `ANEW_DOCTRINE_BIBLE_v1_20260615.md` 1 of 3, `ALIVE_JARVIS_2046_BOOTSTRAP_AND_ROADMAP.md` 1 of 2 | *"Ken Burns cinematic moving backgrounds as share-repo components"*, *"every element a share-repo component"*. The intake packet also records that a legacy surface *carries hardcoded keys for three providers, rotate before any reuse*. Values not reproduced here | **R2** x6 |
| **The form builder order, carried forward twice** | `DOCTRINE_RESOLVE_PT1_LEDGER.md` 2, `MASTER_ONE_STOP_20260808.md` 2 | carries A54 forward as an instruction: *"glass theme, Cam Burns polish, tested, good URL or a generic one, shared repo"* | **R2** x4 |
| **Sub-total R2** | | | **50** |
| **The Shared Repo Law**, a coder's formulation | `ANEW_DOCTRINE_BIBLE_v1_20260615.md` 2 of 3 | *"The Shared Repo Law. Every component that appears on more than one front end lives in ONE shared repo... When it updates, it updates everywhere. The ACL file name IS the import path."* Written **in his voice**, in the folder the corpus flags for exactly that | R2 x1, **R1** x1 |
| **Quoting his R1 sentence back** | `THE_GREAT_REBOOT_ROADMAP.md` 2 | *"Run of show is enforceable code, shared repo: 'my run of show code can be shared repo, so if I ever update a run of code, it updates everywhere'"* | **R1** x2 |
| **Sub-total R1** | | | **3** |
| **Fan-out asserted** | `THE_GREAT_REBOOT_ROADMAP.md` 2, `ALIVE_JARVIS_2046_BOOTSTRAP_AND_ROADMAP.md` 1 of 2 | *"shared repos propagate agent updates to every world"*; *"Global shared-repo propagation: 'how does that make it back down?'"* carried as open question 28; *"update once, deploy everywhere, so she can mass-update all HAMs overnight"* | **R3** x3 |
| **Findability** | `THE_GREAT_REBOOT_ROADMAP.md` 1, `HAS ALL THIS BEEN DONE ANU BOOSTRAP CHECK - ANU_APP_INDEX_FULL.md` 1, `aba roadmap may9 v1.jsonl` 1 of 6 | quotes A02 back to him; *"this is how shared repos plus the ACL layer make the system harder to steal and easier to build"*; *"Grep across... and shared repos"* as an acceptance criterion | **R4** x3 |
| **A watcher role, not an architecture** | `CLABA_CODING_LATCH_VIGIL.md` 1, `CLABA_CODING_v9_MERGE_MODEL_ARCHIVED.md` 1, `CLAIR_ORIGIN_PERSONA_MEETING_MINUTES.md` 1 | three restatements of A05: *"that same place is where MACE and the bug-catcher and the shared-repo watchers and SHADOW draw from"* | **R5** x3 |
| **A scoping rule that touches the one question** | `aba_manual_v1_6.jsonl` 1 | *"MACE is global because it operates on shared repos, not HAM-private data."* A coder document defining shared repo as the not-per-person tier | **R5** x1 |
| **His open question, registered** | `THE_GREAT_REBOOT_ROADMAP.md` 1 | *"38. 'what the heck I've been saying with shared repo and what that means'"* carried as open, correctly | **R5** x1 |
| **The consent claim** | `AWA CLAIR_LANE_CODING_ROADMAP_AWA_CIB_CIP_20260719.md` 2 | *"The founder has already said YES to the shared repo model."* See section 3.4 | **R5** x2 |
| **Sub-total R3 / R4 / R5** | | | **3 / 3 / 7** |

**Total table B: 50 + 3 + 3 + 3 + 7 = 66, plus the 2 counted inside the Shared Repo Law row = 68.**

---

## 6. THE TALLY

### 6.1 By reading, HIS words only (predicate P3, 60 occurrences)

| Reading | His occurrences | Share | Distinct sessions |
|---|---|---|---|
| **R2 DEDUPLICATION** shared components and assets in one place | **31** | 52% | 20 |
| **R5 OTHER**, of which 11 are him asking, ordering, or complaining | **16** | 27% | 8 |
| **R4 FINDABILITY** an ACL address you can ask for by name | **9** | 15% | 8 |
| **R1 PROPAGATION** one source that updates everywhere | **3** | 5% | 2 |
| **R3 FAN-OUT** updates reaching every person's world | **1** | 2% | 1 |

### 6.2 By reading, CODER documents only (68 occurrences)

| Reading | Coder occurrences | Share |
|---|---|---|
| **R2 DEDUPLICATION** | **52** | 76% |
| **R5 OTHER** | 7 | 10% |
| **R1 PROPAGATION** | 3 | 4% |
| **R3 FAN-OUT** | 3 | 4% |
| **R4 FINDABILITY** | 3 | 4% |

### 6.3 What the tally does and does not say

**It says R2 is what he pointed at most often.** By a wide margin, in the most sessions, over the
longest span, and it is the reading the coder corpus built on.

**It does not say R2 is what he meant.** Three things cut against reading the tally as an answer:

1. **Frequency is not authority, by his own supersession rule.** The newest doctrine controls. The
   Countdown pt 4, 20260813, is the newest shared-repo passage in the corpus, and it is R2
   (*"The backgrounds are in the same spot"*). But Mt Rushmore pt 1, 20260816, is newer still, and
   what it contains is not a reading. It is the order to audit.
2. **R1 and R3 are rare but load-bearing.** They are the readings that decide the architecture.
   A02 and A56 describe where files live. A18 and A20 describe what happens to every world when one
   file changes. **A single occurrence that changes the system is not outvoted by thirty that do
   not.** R1's headline sentence occurs exactly once in 128 occurrences, and R3's exactly once.
3. **R2, R4, R1 and R3 are not alternatives in his usage.** In A26 one sentence carries R2 and R4
   together. In A11 through A15 one passage carries R2, R1 and the definitional question. He was
   not choosing between four architectures. He was naming one thing whose consequences a coder
   never traced.

### 6.4 The one place he touched the real question himself

In the same passage as A11 to A15, immediately after them, unprompted:

> *"the phone version of CCWA is pulling in from the same spot that not it's not from the same spot,
> **it's a copy version of that code**, but my question is, even if we did that, then how, when you
> update one thing, how does it all get updated"*
> [HIS WORDS + `1_HIS_WORDS/01_RAW_WORDS/08_20260609_SWEET_AND_SALTY.txt`]

He starts to say the surfaces pull from the same spot, **stops himself mid-sentence, and corrects it
to a copy.** That self-correction is the single most load-bearing sentence in this sweep, because it
is him arriving at the exact fork stated in section 7 and choosing the copy side out loud, and then
immediately treating the consequence as an unsolved problem rather than a settled design. **It is not
a decision.** It is one sentence in one session in June, it is followed by *"help me think through
that, help me figure that out,"* and he later said he had never been heard on the term at all. It is
put in front of him here because it is his, not because it settles anything.

---

## 7. OPEN QUESTION #28: "HOW DOES THAT MAKE IT BACK DOWN?"

**He did answer it. Partially, in the same breath, and then handed it straight back.** The roadmap
records #28 as unanswered. That is not quite right, and the correction matters, because the answer
`R3_SHARED_REPOS.md` phase S2.1 offers him as *"a coder's reading, marked as one"* turns out to be
substantially **his own words**, which changes its standing.

The full passage, verbatim, [HIS WORDS + `1_HIS_WORDS/01_RAW_WORDS/08_20260609_SWEET_AND_SALTY.txt`]:

> *"my question is, even if we did that, then how, when you update one thing, how does it all get
> updated, that gotta be the job of span or something, or not span, or or trace of something,
> greping the entire database and changing it, right, but then when we change things, know that
> that's at the global level. When we change things, so while we won't ever change their data, that
> stuff is a global level. **So, how does that make it back down?** Because basically, there should
> always be a nightly loop between the global, let me cook, let me cook, let me cook. There should be
> a nightly loop between the global ABCA, ABA, CIA, which we might need a new name for that, by the
> way, between that and the in the in the local brain. So let's say my brain, for example, right? Or
> [an advisor]'s brain, and so maybe it's isn't once a day, yeah, it could be once a day, or we could
> ever, if as a coder, I ever wanted to send a manual update, I can respond, I can make it, you know,
> a pathway that fires, right, every time somebody loads up, that's easy for the most part, just be a
> nightly update, or something like that, and if there's any new global updates, if we want to change
> an app or change something, want to do something right. It has what I'm saying is it should be a
> connection point for her to get it. Maybe it's a messenger agent, maybe it's a cell LLMs. **Help me
> think through that, help me figure that out.** But I know I just cook hard."*

### 7.1 What that passage establishes, in his words, not a coder's

| Element | His words | Standing |
|---|---|---|
| The mechanism class | *"there should always be a nightly loop between the global... and the local brain"* | **his**, stated twice in one breath |
| A second channel | *"if as a coder, I ever wanted to send a manual update... a pathway that fires... every time somebody loads up"* | **his** |
| The safety property | *"while we won't ever change their data, that stuff is a global level"* | **his**, and it is the never-overwrite column of S2.2 |
| Who carries it | *"Maybe it's a messenger agent, maybe it's a cell LLMs"* | **his**, but offered as two guesses, not a choice |
| What each world holds | *"it's not from the same spot, it's a copy version of that code"* | **his**, and it is section 6.4 |
| The frequency | *"maybe it's isn't once a day, yeah, it could be once a day"* | **open on its face** |
| Whether this is the design | *"Help me think through that, help me figure that out"* | **explicitly handed back** |

### 7.2 So the honest status of #28

**Not "never answered." Answered by him as a sketch, in June, and then explicitly returned as a
request for help that no document in the corpus answers.** The sweep found no occurrence anywhere,
his or a coder's, that closes it. The only coder documents that touch it either carry it as an open
question, which is correct, or restate it as a decided law:

> *"update once, deploy everywhere, so she can mass-update all HAMs overnight"*
> [CODER DOC + `1 pt 2 .../ALIVE_JARVIS_2046_BOOTSTRAP_AND_ROADMAP.md`]

That sentence answers #28 by assertion. It is a coder's, it is not marked as one in its own
document, and it picks the fan-out side of a fork the founder had left open. **It is exactly the
failure this repo exists to stop, and it is recorded here as an occurrence, not adopted.**

`R3_SHARED_REPOS.md` S2.1 should be amended: the *"nightly global-to-local sync channel"* is not a
coder's reading offered to him. **It is his own June sketch, carried back to him with its open ends
still open**, which are the frequency, the carrier, and whether he still wants it.

---

## 8. THE "TATTOO" NAMING ORDER

He gave a naming order for shared repos. **It was given once, in one passage, and no document in the
corpus adopts it.**

**43 raw occurrences of "tattoo". 20 after deduplication. 15 in the HIS tree, 5 in coder documents.**
Broken out by sense:

| Sense | Count | Where | Note |
|---|---|---|---|
| **The naming order for shared repos** | **8** | `1_HIS_WORDS/01_RAW_WORDS/02_20260602_SPICY_HEAT.txt`, one continuous passage | *"if you're an arm, right, you have these tattoos. **I want, I want, I want shared repos to be called tattoos**, yeah... the tattoos basically are for shared repos"* |
| Work-parallelism metaphor | 1 | `1_HIS_WORDS/02_PHASE_2/Governor doctrine pt 2` | *"four or five tattoo spa right that are working"*, speech-to-text noise |
| Literal tattoos, personal | 4 | `CFPMFP weekly meeting`, `The Countdown pt 3` | *"freedom to get a hand tattoo"*, and two lines of speech-to-text noise |
| A coder using the word as if adopted | 1 | `06_OLD_WORLD_HIS_WORDS/.../CODING_COMMANDMENT.md` | *"ACL surrounds everything - the tattoos, the grafts, the agents"*. A coder document, per section 3.1 |
| Unrelated, in coder documents | 5 | agent job descriptions, client notes, one transcript of lyrics | tattoo shops as an errand example, and similar |

**The finding: he named it, one coder echoed the word once inside a document that is itself
misfiled, and the naming order was never carried into any roadmap, index, or repo name.** The
metaphor is not decoration. It is a reading in itself: a tattoo is on the skin, it is not the arm,
and it does not think. It sits directly alongside his front ends *"can't have a mind... all they
project is this skin that they're in"*, in the same breath, in the same passage. Whether he still
wants the name is his to say. It is surfaced here because he ordered it and nobody executed it.

---

## 9. THE "RUN OF SHOW" SWEEP

Included because R1's anchor sentence is a run-of-show sentence, so the phrase had to be checked in
case R1 was better supported than table A shows. **It is not.**

**269 raw occurrences. 147 after deduplication.** Corrected for the two misfiled coder documents in
section 3.1: **20 his, 127 a coder's.** His 20 carry three unrelated senses:

| Sense | Count | Note |
|---|---|---|
| The agent orchestration sequence, the order the cycle fires in | 18 | the dominant sense, and it is about agents firing, not about repositories |
| **Tied to shared repo** | **2** | both inside the single sentence A18, *"a run of show is all code, but again, my run of show code can be shared repo"* |
| Literal event production documents | 0 in his files after correction | the 8 golf tournament and awards ceremony run-of-show occurrences are in a coder extraction document, section 3.1 |

**So R1's evidence base is one sentence, twice matched.** The roadmap's claim that R1 is *"the
strongest and most-repeated sense"* is not supported by the sweep and should be corrected to
*"the reading with the widest consequences and the narrowest evidence."* That correction does not
weaken R1. It relocates why it matters.

---

## 10. THE ONE QUESTION FOR HIM

Everything above exists to let this be asked cleanly, and it is the exit condition of S0.3.

> ### Does shared mean **one copy that everyone reads**, or **one source that everyone gets their own copy of**?

Both are consistent with something he has said. The first is A02, A26, A56 and the whole R2 and R4
weight of table A: one spot, one button, one background, addressed by ACL name, read from wherever
you are. The second is A18, A20 and his own mid-sentence correction in 6.4: not the same spot, a
copy version, and a nightly loop that pushes changes down into each isolated world.

**They produce different systems.** One copy that everyone reads means a live read across a
boundary, which collides with `PO1-23`, his world not sharing a floor with anyone. One source that
everyone copies means a propagation mechanism, which is #28, which is still open, and which cannot
be built until the cross-world guard is armed.

**One sentence from him unblocks S1 through S4.** No coder answers it in this file, and no coder
should.

---

## 11. WHAT THIS DELIVERABLE DELIBERATELY DOES NOT DO

- **It does not pick a reading.** R3's premise governs.
- **It does not resolve the R1 and R3 versus isolation tension.** That is S0.3, and S0.3 says name
  the tension, do not resolve it.
- **It does not propose a repo topology, a propagation mechanism, or a component set.** S1, S2 and
  S3 are contingent on his answer and, for S1.4, on credentials that are his.
- **It does not treat the four coder documents in section 3.1 or the consent claim in section 3.4 as
  authority.** They are logged as occurrences.
- **It does not search the 185 PDFs, 3 .docx, 3 .xlsx, or 10 .zip files.** Declared in 1.1.

---

## 12. REPRODUCTION

Every count in this file is reproducible. From the corpus root:

```
# raw occurrence count, the shared-repo family, before deduplication
grep -rEioa --include=*.md --include=*.txt --include=*.rtf --include=*.jsonl \
  --include=*.json --include=*.html --include=*.js --include=*.jsx --include=*.tsx \
  --include=*.py --include=*.csv -- 'shared?[[:space:]_-]repos?' . | wc -l

# per-file occurrence counts, which is what the tables are built from
grep -rEioa <same includes> -- 'shared?[[:space:]_-]repos?' . \
  | awk -F: '{c[$1]++} END {for (f in c) printf "%5d  %s\n", c[f], f}' | sort -rn

# the HIS predicate
#   HIS   iff path contains  0 ANU_ANEW_OS_use to be call doctrine/1_HIS_WORDS/
#   CODER otherwise
# then apply the three corrections in section 3
```

The dedup-and-context script used for this sweep indexes by byte offset rather than by line, which
is the S0.1 requirement. `fold -w 120 -s` gives the same occurrence count when piped per file and is
the simpler check by hand:

```
fold -w 120 -s FILE | grep -Eioa 'shared?[[:space:]_-]repos?' | wc -l
```

---

## 13. RECEIPT

**S0.1 complete.** 128 distinct occurrences, indexed by occurrence, each with its file, its HIS or
CODER stamp, its surrounding passage, and what he was pointing at.

**S0.2 complete.** All four readings evidenced from the passages found, each with a count and a
named anchor, plus **R5** for the 23 occurrences that fit none of the four, which the roadmap did not
anticipate and which turn out to be the second-largest group in his own words.

**S0.3 partially discharged.** The tension is named in 6.3 and 10 and is not resolved. The one
question is on the board.

**The receipt is his answer.** Until then, the question stands on the board with his name on it, and
S1 through S4 stay shut.

---

*Predicates published with every count. Personal names replaced with bracketed roles. No credentials
or secret values reproduced. Occurrence-indexed, not line-indexed. Sources stamped [HIS WORDS] or
[CODER DOC] on every row.*
