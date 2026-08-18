# KEEPER FRONTEND VISUAL VERDICT

Seat: `OTJT.KEEPER.FRONTEND-VISUAL-CRITIC`. One finite review. Read-only. No em dashes.

**Target, verified before opening.** `OTJT_CODA_FRONTEND_STUDIO_PACKAGE_20260818.zip`
SHA-256 `f1c9eb925f2e8c87cb80f60f782fa4ca3d6e84b66f002c44ed0726c94148a334`, size 6,168,737 bytes.
**Both the expected hash and the expected size matched exactly.** Writer: max SPAN, separate lane.
Nothing in the package was edited, repackaged, or rebuilt.

---

# VERDICT: **DEFECT**

**Exact ZIP hash: `f1c9eb925f2e8c87cb80f60f782fa4ca3d6e84b66f002c44ed0726c94148a334`**

**Two material defects. Both have small repairs. The package is not to be thrown away, and most of it
is ready to hand to the Codex visual integration successor exactly as it stands.**

I want the proportion stated plainly before the defects, because a two-item defect list read cold can
sink work that does not deserve it: **this is not a generic frontend and it is not ugly.** It is a
considered, coherent, warm system with real hierarchy, and its honesty discipline is the best I have
reviewed in this program.

---

## DEFECT 1. The smallest text carries the truthfulness copy and fails contrast

**Exact paths:** `skin/skin-0001/tokens-hearth.css:82-83`, `tokens-atrium.css:81-82`,
`tokens-slate.css:82-83`, applied at `skin/skin-0001/skin.css:170-173`, `:308-310`, `:347-350`.
**Visible in renders:** `renders/desktop-hearth.png`, `renders/phone-slate.png`.

**What I measured, not eyeballed.** I composited the glass card over its ground and computed WCAG
contrast:

| Direction | Token | Colour | On card | Verdict |
|---|---|---|---|---|
| Hearth | `--ink` | `#F4E9DA` | 10.59 | passes |
| Hearth | `--ink-dim` | `#CBB49B` | 6.37 | passes |
| **Hearth** | **`--ink-faint`** | **`#9C836B`** | **3.55** | **fails AA for normal text** |
| Atrium | `--ink` | `#FBF3E7` | 10.48 | passes |
| Atrium | `--ink-dim` | `#DCC7AE` | 7.04 | passes |
| **Atrium** | **`--ink-faint`** | **`#AE9679`** | **4.09** | **fails AA for normal text** |

AA requires 4.5:1 for normal-size text. `--ink-faint` is used only at `--fs-xxs` and `--fs-xs`, which
are **10px and 11.5px in Hearth, 10.5px and 12px in Atrium, and 9.5px and 11px in Slate**. That is the
smallest type in the package at the lowest contrast in the package, which is the wrong pairing in both
directions at once.

**Why this is material rather than a polish note.** `--ink-faint` is the colour of `.state-note`, and
`.state-note` is where this package keeps its honesty. It is the line that reads *"No count,
identifier, or preview is shown, by design"*, *"Studio placeholder. Not a real figure"*, and *"The
living runtime is not composed yet. This surface will not invent words while it waits."* Those
sentences are the entire reason the shell is trustworthy. If the Founder cannot comfortably read them,
the truthfulness becomes decorative while the confident numbers stay perfectly legible. A shell that
renders `$4,120` at full strength and "not a real figure" at 3.55:1 is quietly doing the opposite of
what it claims.

**Doctrine citation.** `docs/07_ACCESSIBILITY.md` commits that "State is never carried by colour
alone." I verified that claim is **true**, every state pill carries its own word. This defect is the
adjacent one the document does not address: legibility of the explanatory line under the pill. The
document makes no contrast claim anywhere, so it does not overclaim, and I am not scoring it as a
false statement.

**Smallest successor repair.** Raise `--ink-faint` in all three token files until it measures at least
4.5:1 against the composited card, or promote `.state-note` to `--ink-dim`, which already passes at
6.37 and 7.04. Either is a one-value change per file and touches no layout, no component, and no
structure. Do not shrink the type further in Slate while doing it.

---

## DEFECT 2. A Founder quotation is cited to a roadmap file rather than his own words

**Exact path:** `docs/04_CHROME_VS_STATION_MATRIX.md`, the pull quote in the opening section.

**Triggering wording:** the package prints
*"If you're an arm, right, you have these tattoos. I want shared repos to be called tattoos."* and
attributes it `[HIS WORDS, R4_FRONT_ENDS.md F2.4]`.

**What I verified, both directions.** The **words are genuinely his.** I found them in the raw corpus:
*"tattoos. I want, I want, I want shared repos to be called tattoos, yeah."* I am not alleging
fabrication and this is not a stolen-voice finding.

The **citation is the problem.** `R4_FRONT_ENDS.md` is a roadmap file, which is secondary. My own copy
of `20_ROADMAPS/R4_FRONT_ENDS.md`, 399 lines, contains **zero** occurrences of "tattoo". My branch
records the primary source instead, at `50_DELIVERABLES/SHARED_REPO_SWEEP.md:195`, which cites
`01_RAW_WORDS/02_20260602_SPICY_HEAT.txt` for exactly this line.

**Stated fairly, because max SPAN works from a different repository:** its `R4` is on branch
`claude/doctrine-roadmap-planning-tog781` at a head I do not hold, so its F2.4 section may genuinely
carry this quote. I am **not** claiming the citation is false. I am reporting that it **cannot be
resolved from the corpus this seat holds**, and that a Founder quotation should point at his recorded
words rather than at a roadmap that quotes them.

Secondary, same line: the package renders the quote as "I want shared repos to be called tattoos"
where the raw is "I want, I want, I want shared repos to be called tattoos, yeah." The stutter and
tail are removed with no ellipsis. His hesitation is part of how he talks and the smoothing is silent.

**Smallest successor repair.** Change the attribution to the primary raw file and restore the exact
words or mark the elision. One line in one document. The matrix's argument does not depend on the fix.

---

## WHAT IS SAFE TO HAND TO THE CODEX VISUAL INTEGRATION SUCCESSOR

Everything below I checked directly. It needs no rework.

**The chrome and station law holds, and it is the best thing in the package.**
`docs/04_CHROME_VS_STATION_MATRIX.md` assigns window controls, frame, crown, rail, slot frame,
navigation, focus order, and the entire colour and type vocabulary to the **shell**, and leaves a
station able to declare only its name, icon key, state from a closed enum, and an already authorized
projection. A station cannot add, rename, or reorder itself. That is the skin and arm reading made
enforceable rather than aspirational.

**No cold surface pretends to decide meaning.** I grepped the shared skin for identity, memory,
persona, classification, ranking, relevance, and priority. The only hits are the files' own
prohibitions: `skin.css:15` "THIS FILE MAY NOT: classify, decide meaning, hold identity", and
`kernel.js:13` and `:107` repeating it. The constraint is written into the headers of the files it
governs.

**No A'NU words are simulated anywhere.** The Talk station renders
*"This surface is not running right now. The living runtime is not composed yet. This surface will not
invent words while it waits."* That is the correct behaviour, stated in the shell's own voice, and it
is exactly what a partner rather than a software product looks like when she is not there yet.

**The refusal state does not leak.** Advisor Portal shows *"Not authorized for this surface. No count,
identifier, or preview is shown, by design."* No row count, no identifier, no preview.

**Accessibility is real work, honestly self-audited.** Roving tabindex on the rail so it is one tab
stop, skip link first, focus ring never removed, motion fully stopped under reduced-motion with the
loading shape still legible, icons `aria-hidden` with the word as accessible name, and every state
pill carrying its own text so no state depends on colour. The document then names its own gaps rather
than hiding them: no real screen reader pass, no focus trap yet, tight phone targets past seven
surfaces. Naming those is a mark of quality, not a defect.

**Phone layout is sound.** I initially read the Talk card in `renders/phone-slate.png` as occluded by
the tab bar and checked the source before reporting it. The phone rail is a grid row, not a fixed
overlay, and it carries `env(safe-area-inset-bottom)`. The render is a mid-scroll position. **No
defect. Withdrawn before it left this file.**

**Zero external requests.** Wallpapers are CSS gradients, icons are inline SVG, type is system stacks.
Nothing phones home, which is the correct posture for a skin that is meant to be shared across worlds.

**Three directions, not one compromise.** Hearth, Atrium, and Slate are three real readings of the
brown, burgundy and gold instruction, built to be looked at rather than averaged. The colour
directive is carried as an open Founder ruling rather than silently resolved.

---

## THE MISSING LOGO, CLASSIFIED PER YOUR OWN RULE

**Not a defect. An exact source input the next visual row needs.**

`docs/09_ASSET_INVENTORY.md` states plainly that "No logo is invented anywhere in this package" and
lists the ENVOLVE wordmark and any real logo asset as missing, with the Founder named as the only one
who can supply them. **The package therefore claims no fidelity it does not have.**

I also searched the corpus this seat holds for a real logo or brand asset file and **found none**. No
wordmark, no brand image, no vector asset. Per the standing rule I will not claim a legacy asset
exists without an exact source, so I am recording it as **not established** rather than as something
the package failed to use.

**On CARA, anu-anew.com, and CIB, the package handles all three correctly and is not ignoring them.**
`README.md:89` keeps CARA off human surfaces as internal vocabulary, which matches the corpus line
about never revealing acronyms externally. `docs/08_MIGRATION_FROM_F1.md:37` and
`docs/10_CODEX_CONTINUATION_CHECKLIST.md:15` both carry `/cip` and `/cib` forward as verified 404
twice and blocked on nobody. These are live items on the checklist, not omissions.

**What the next row genuinely needs from the Founder, and nobody else can supply:** the real wordmark
or logo, the final colour ruling, real photographic wallpapers if he wants them over gradients, and
his pick among the three glass canons. Four minutes of looking, not a work order.

---

## SEAT CONDUCT

Nothing built, edited, repackaged, committed, or deployed. No key, account, or timer. No structural
work reopened for polish. No logo invented and no legacy asset claimed without a source. One finding
was withdrawn after I checked the source rather than shipping it.

Passed acceptance is honoured. Two material defects, both with one-line repairs, and no
could-be-better veto attached to either.

**STOP.**

Signed **KEEPER**.
