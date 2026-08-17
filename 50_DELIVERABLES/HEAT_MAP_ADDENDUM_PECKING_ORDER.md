# ADDENDUM TO HEAT_MAP_MEASURED.md - THE TWO PECKING ORDER SESSIONS, COUNTED

**Closes the gap the measured heat map declared against itself.** Every count in
`HEAT_MAP_MEASURED.md` was short by the contents of Pecking Order pt 1 and pt 2 - both live outside
`1_HIS_WORDS/` and were never in the 110-session count. This file adds them with the identical method
(one line normalized, `re.finditer` non-overlapping, same 47 patterns, unretuned) and changes nothing
already published - it is an addendum, not a rewrite.

Corpus grows from 110 sessions / 776,734 words to **112 sessions / 785,417 words.** `[MEASURED]`

---

## THE TOP 5 - UNCHANGED IN MEMBERSHIP AND ORDER

| Rank | Ask | Corrected | Was | Delta |
|---|---|---:|---:|---:|
| 1 | advisors | **844** | 844 | +0 |
| 2 | reach (bare token) | **577** | 574 | +3 |
| 3 | AIR (bare token) | **480** | 478 | +2 |
| 4 | roadmaps | **327** | 324 | +3 |
| 5 | ACL | **273** | 273 | +0 |

**advisors and ACL are genuine zeros in both new sessions** - independently re-verified with a second
tool (`grep -oi`), not a script artifact. No band changes anywhere across all 47 tracked asks; new
sessions moved totals, not tiers.

---

## THE REWARD SYSTEM - THE QUESTION SETTLED, BOTH NUMBERS TRUE

Two correct answers exist and both are reported rather than one being picked:

- **The literal phrase "reward system":** exactly **2** occurrences, both in pt 2, zero in pt 1.
  *"That's called the reward system... we teach our users a reward system."*
- **The full-word predicate `\brewar\w*`** (the row this file's tracker actually uses): **3** - the
  same two, plus the verb three words earlier in the same breath, *"gonna come back and really reward
  me."*

**Both confirm the earlier correction: the reward system is his, said in one breath, in the newest
doctrine in the corpus.** `R4` F7 stands, unchanged.

**One honest distinction worth keeping:** by session count (the tracker's own banding rule) it stays
banded coldest (present in 1 of 112 sessions) with zero demand-phrase co-occurrence nearby - so
*existing* and *being pressed for repeatedly* are not the same finding, and neither contradicts the
other. He said it once, clearly, and it is real.

---

## WHAT MOVED BELOW THE TOP 10

- **world builder** gained the most, +11 (166 -> 177) - expected, since pt 2 is explicitly about
  building a temporary coder world of world builders.
- **coding department** +7 (160 -> 167), all first-person.
- **PMS / planted memory** rises to 25 occurrences across 6 sessions, overtaking "job descriptions" and
  "the researcher" in raw count - a real reordering, though not in the top 10.
- **purge** rises to 21, now tied with "job descriptions."
- **Easter eggs** last-occurrence date moves 2026-08-15 to 2026-08-16 - already flagged OPEN, status
  unchanged.

**29 of 47 tracked asks (62%) appear in neither new session and are completely unchanged**, including
the current #1 and #5.

---

## METHOD NOTE, CARRIED FORWARD

The same undercount this whole exercise exists to correct reproduces itself live in this addendum:
`grep -c "reward system"` against pt 2 returns 1 (one matching line, because a whole speaking turn is
one line). The actual count is 2. Same file, same phrase, two different answers depending on which
tool is trusted. `grep -c` is never used for occurrence counting in this repository, for exactly this
reason.
