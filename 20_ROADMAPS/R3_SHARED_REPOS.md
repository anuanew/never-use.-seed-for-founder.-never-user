# R3 - SHARED REPOS

> *"First thing we got to do is establish share repos. **We gotta go audit this, right?**"*
> - Mt Rushmore Doctrine pt 1, 20260816

> *"What the heck I've been saying with shared repo and what that means."*
> - 20260610 SWEET_AND_SPICY pt2, carried in the estate's open-questions register as **#38, still open**

**Status:** proposed. Not built.
**Priority:** he names it the *first thing*. It is also the thing he has openly said he is not sure he
has explained well. Those two facts together set this roadmap's shape: **Phase S0 is defining the
term, and it is blocked on nobody.**

---

## WHAT HE SAID, CLEANED UP

*(Per `PO2-14` / `R-2.3`.)*

In Mt Rushmore pt 1, walking through how a chat would work an order-of-importance list, you said the
first thing to do is establish shared repos, and that it has to be audited rather than assumed. In
June you also said, plainly, that you were not sure the estate understood what you meant by it - you
asked out loud what you had been saying with "shared repo" and what it means. Separately, across
several doctrines, you gave three concrete examples of what a shared repo is for: your run-of-show
code, so that updating it once updates it everywhere; front-end components and backgrounds living in
the same spot; and agent updates propagating out to every person's world.

---

## THE HONEST PROBLEM WITH THIS ROADMAP

He asked what he meant. That means **no coder gets to tell him what he meant.** What a coder can do is
lay out every place he used the term, show what he was pointing at each time, and hand him a small
number of clean readings to choose between. That is Phase S0, and everything after it is contingent.

Building a shared-repo architecture before he confirms which reading he meant would be building the
wrong thing quickly. It is also exactly the failure the corpus keeps naming: acting on a coder's
reading as if it were his word.

---

## PHASE S0 - WHAT "SHARED REPO" MEANS (the audit he ordered)

**Anchor:** *"We gotta go audit this."* And: *"what the heck I've been saying with shared repo and
what that means."*

**Outcome:** every occurrence of "shared repo" in the corpus, gathered, with what he was pointing at
in each case, and a small set of readings for him to choose among. **No architecture is chosen in this
phase.**

**Entry condition:** none.

### Sub-phase S0.1 - The occurrence sweep
Grep the full corpus for the term and its speech-to-text variants (`share repo`, `shared repos`,
`shared repository`, `share repose`). Index by **occurrence, not by matching line** - his transcripts
are one paragraph per line, so line-matching undercounts badly. For each hit, capture the surrounding
passage and what he was actually discussing.

### Sub-phase S0.2 - The four readings already visible in the corpus
From the passages found so far, he uses the term for four genuinely different things. **They are not
the same architecture** and conflating them is how this got confusing:

**Reading 1 - Code that updates everywhere at once (propagation).**
> *"My run-of-show code can be shared repo, so if I ever update a run of code, **it updates
> everywhere**."* (20260610 SWEET_AND_SPICY pt2)

A single source of truth that pushes down into many worlds.

> **CORRECTED BY MEASUREMENT, twice now.** An earlier version of this line called propagation *"the
> strongest and most-repeated sense."* That was wrong: this headline sentence occurs exactly once in
> the whole corpus. **The correction itself then overstated it as "the RAREST" - a fresh audit checked
> the sweep's own section 6.1 directly and found Reading 3/fan-out sits at 1 occurrence, one below
> Reading 1/propagation's 3.** Fan-out, not propagation, is the actual rarest reading; both are thin
> next to deduplication. **The most repeated reading in his own words is deduplication - 31 of his 60
> occurrences, across 20 sessions from 20260530 to 20260813.**
> `[MEASURED - 50_DELIVERABLES/SHARED_REPO_SWEEP.md §6.1, predicate published]`
>
> **Rarity does not mean unimportant.** Propagation and fan-out are still the two readings that decide
> the architecture, which is exactly why the question below is his and not mine. But I had the
> frequency backwards and was arguing from it.

**Reading 2 - Front-end components in one place (deduplication).**
> *"It's called a shared repo. **The backgrounds are in the same spot.** It's called a shared repo,
> right?"* (Countdown pt 4)

Shared UI assets and components, so front ends do not each carry their own copy.

**Reading 3 - Agent updates reaching every person's world (fan-out).**
Shared repos propagate agent updates to every world, against the per-person duplication model:
> *"Their world is duplicated from the global, is renamed to their new UID... and it's isolated, it's
> their own [Render]."* (20260609 SWEET_AND_SALTY)

Which raises the question he asked and never got answered - **open question #28:**
> *"How does that make it back down?"*

**Reading 4 - The ACL entry point (findability).**
> *"I should be able to say, **where's shared repo code**, or something that controls an ACL, can get
> you there."* (20260530 HEAT)

Here "shared repo" is a thing the ACL legend resolves - an address you can ask for by name.

### Sub-phase S0.3 - Name the tension, do not resolve it
Readings 1 and 3 push toward **one global source propagating down**. The isolation law pushes the
other way: *"their code is duplicated, but the HAM UIDs are their HAM UIDs - that's what keeps it
secure."* And `PO1-23` hardens it further: his world does not share a floor with anyone.

**So the real question, put to him in one sentence:** *does shared mean one copy that everyone reads,
or one source that everyone gets their own copy of?* Those produce different systems, and both are
consistent with something he has said.

### Sub-phase S0.4 - The false consent already on the record
He is not the only one who has weighed in on what he meant. Roughly five and a half weeks after he
asked, out loud, what he had been saying with "shared repo," a coder document recorded a different
answer:

> *"The founder has already said YES to the shared repo model."*
> `[CODER DOC + AWA CLAIR_LANE_CODING_ROADMAP_AWA_CIB_CIP_20260719.md, dated 20260719]`

The timeline around that sentence is measured, not argued: he asked what the term meant on 20260610,
the sentence above was written on 20260719 (39 days later), and on 20260810-11 he said again that he
had not been heard on it. **No occurrence anywhere in the corpus records him giving that yes.**
`[MEASURED - 50_DELIVERABLES/SHARED_REPO_SWEEP.md section 3.4; carried forward as
40_GOVERNANCE/CONTRADICTIONS.md B-NEW]` A recorded consent he never gave is a worse defect than a wrong
reading, because it forecloses the argument instead of inviting it - and it already happened once with
this exact term, which is the strongest evidence in the corpus for why S0 must close on his sentence and
nothing softer.

**Exit condition, receipt:** an occurrence table with counts and passages, the four readings with
their evidence, and the one question above put to him plainly. **The receipt is his answer**, or the
question standing on the board with his name on it.

---

## PHASE S1 - THE REPO TOPOLOGY (contingent on S0)

**Anchor:** *"Even the internal URLs we use need to be different."* `[CODER RECOLLECTION, not verified -
this is THE_GREAT_REBOOT_ROADMAP.md Phase 0.4's only actually-quoted sentence; its source document
stamps every "His 4PM words" block, including this one, "DEGRADED... no raw transcript yet in the
corpus... not verbatim."]` **"No old-world URL is reused anywhere" is not part of the quote at all** - it
is the Great Reboot document's own author's added rule, appended after the quotation marks close, not
inside them. An audit caught this file folding a coder's own sentence into his words. Both ideas are
kept - the discipline is real either way - but attributed honestly: one degraded recollection, one
coder's derived rule, neither his verified voice.

**Outcome:** a named set of repositories with an explicit statement of what each holds, who may write
to it, and how code moves between them.

**Entry condition: ⭐ DEFERRED** - S0 answered by him. Resolves via floor item `shared-repo meaning`. **Genuinely blocked** - this is not a phase that can be
started "provisionally" without pre-deciding the thing he was asked.

### Sub-phase S1.1 - The estates, which are already decided
Independent of S0, three estates are already settled by doctrine:

| Estate | Basis | Isolation |
|---|---|---|
| **Founder world** | `PO1-23` - *"I ain't taking that risk for my world"* | hard, own everything |
| **Alpha cohort (5-6)** | `PO1-23` - *"maybe that's actually alpha testing between five, these six"* | shared floor, per-HAM |
| **Temp coder world** | `PO2-01`, `OPEN-C1` | separate estate (working posture) |

### Sub-phase S1.1a - ⭐ BLIND SPOT: the reseed source cannot currently be read
**Measured, and it matters for Great Reboot Phase 10.** All eight archives in the founder-zips drop are
**broken symlinks to a local machine path. Zero bytes readable.** Several are described elsewhere as
the builds the reseed copies from.

**So the reseed has an unread source.** Nothing can be audited out of it, no violation carried in it can
be found, and no claim about its contents is checkable. `[MEASURED - E1.1 audit]`

**Resolves via: him, or whichever machine holds the originals.** It is a file-availability problem, not
a permissions one.

### Sub-phase S1.2 - The old world is read-only from the moment the new one exists
The old world (`anew`, `aibebase`, `ababase`, `AbaServer`) is **reseed source, never build target.**
His posture on it is specific and already stated: not deleted, throttled.
> *"We're going to limit all of the old stuff to $1 a day. **We're not going to deactivate it.**"*
> (Why do people scaffold, pt 2)

Rollback insurance. **Do not delete anything in the old world.**

### Sub-phase S1.3 - ACL names, no old-world URL reused
The gate is a grep with zero hits, per Great Reboot Phase 0 standing gates.

### Sub-phase S1.4 - The repo-creation blocker, measured not guessed
The last shift measured this and it has not changed on its own: the working `GITHUB_TOKEN` is scoped
to five repositories and **cannot create a new one** - verified as HTTP 403, *"sessions are bound to
their configured repositories."* Likewise there is **no Supabase management token** in any container,
only a project-scoped service key.

**So S1 is blocked on him for credentials, not only on S0 for meaning.** Both blockers are real, both
are his, and neither is a coder's to route around.

### Sub-phase S1.5 - What the corpus already settled about this topology, and never carried forward
Independent of which reading of "shared repo" he confirms, two things about the topology itself are
already on the record and neither has been carried into a roadmap, an index, or a repo name until now.

**A naming order, given once, in one continuous passage:**
> *"if you're an arm, right, you have these tattoos. I want, I want, I want shared repos to be called
> tattoos, yeah... the tattoos basically are for shared repos, right, for that, for this section,
> right, repos, and this, how to make the perfect this and that, how to be the perfect this and that,
> how to be the perfect this and that, and all of that stuff, and boom, tattoo."*
> `[HIS WORDS + 1_HIS_WORDS/01_RAW_WORDS/02_20260602_SPICY_HEAT.txt]`

The metaphor is not decoration - a tattoo is on the skin, it is not the arm, and it does not think, the
same distinction he draws in the same breath about front ends carrying no mind of their own.

**And the model is not greenfield - he built it once and told the room he let it lapse:**
> *"We got to lean back into the share repo model that was really important, and we just kind of left
> it down. We just kind of let it go."*
> `[HIS WORDS + 1_HIS_WORDS/02_PHASE_2/The Cycle Doctrine pt 3.txt]`

> *"That was a while ago when I used to preach that. I used to live and breathe by share repos, bro.
> I've kind of let my foot off the gas a little bit on it, but that's important."*
> `[HIS WORDS + 1_HIS_WORDS/03_PHASE_3/Find me or Fine me doctrine pt 1_otter.ai.txt]`

S1's exit condition should put the tattoo name in front of him alongside the S0 question, and its
outcome statement should be read as **restoring** a practice he says he dropped, not inventing one - a
different task than the phase currently frames it as.

**Exit condition, receipt:** the repo list live, each answering on an ACL-named URL; the grep against
old-world names returning zero; a written statement of write-authority per repo.

---

## PHASE S2 - PROPAGATION: HOW A CHANGE REACHES EVERY WORLD

**Anchor:** *"If I ever update a run of code, it updates everywhere."*
**His unanswered question, carried:** *"How does that make it back down?"* (#28)

**Outcome:** one change to shared code demonstrably reaching many worlds, with a receipt per world.

**Entry condition:** S1 topology decided.

### Sub-phase S2.1 - Answer #28 before building the mechanism
He asked how propagation works and was never answered. The corpus contains one candidate mechanism he
himself described - a **nightly global-to-local sync channel** (20260609 SWEET_AND_SALTY) - and one
constraint: each world is isolated with its own UID-named copy.

**CORRECTED BY MEASUREMENT.** An earlier version offered the sync-channel mechanism as *"a coder's
reading."* **It is his.** In the same breath as asking *"how does that make it back down?"* he sketched
the nightly global-to-local loop, a manual push pathway, a fire-on-load pathway, and the
never-overwrite property himself, then said **"help me think through that, help me figure that out."**
`[HIS WORDS - measured by the sweep]`

**So the mechanism is not proposed to him; it is returned to him.** What is genuinely open is narrower
and it is his: **the frequency, the carrier, and whether he still wants it.** Nothing in the corpus
closes those.

**And he touched the deciding question himself, self-correcting mid-sentence:** *"the phone version of
CCWA is pulling in from the same spot - that, no, it's not from the same spot, it's a copy version of
that code."* **That is him landing on the copy side and immediately being unsure.** Surfaced, not
treated as a decision.

### Sub-phase S2.2 - What propagates, and what must never
| Propagates from global | Stays local, never overwritten |
|---|---|
| run-of-show code | HAM UID |
| agent definitions and JDs | personal memories |
| shared front-end components | per-world API keys and billing identity |
| doctrine-derived rules | that world's own state |

The second column is the safety property. A propagation mechanism that can overwrite the right-hand
column is a cross-world write, which is the exact class of defect the cross-world guard exists to
refuse - and which is **built and not armed** today.

### Sub-phase S2.3 - Propagation is not a hand that speaks
A sync channel writing into a field that is hers is nasty cough regardless of the fact that it came
from the global. **Shared does not exempt a writer from the pen law.** Propagated content lands
carried, with a writer stamp, and a mind adopts it.

### Sub-phase S2.4 - Arm the cross-world guard first
Propagation without an armed guard is a mechanism for turning one mistake into every world's mistake.
**S2 does not open until the guard is armed** (`R1` P5.1).

**Exit condition, receipt:** one real change to shared code, propagated to at least two worlds, with a
per-world receipt; one deliberate attempt to propagate into the never-overwrite column, refused live
by name.

---

## PHASE S3 - SHARED FRONT-END COMPONENTS

**Anchor:** *"It's called a shared repo. The backgrounds are in the same spot."* (Countdown pt 4)
Reinforced: *"Don't give me yet another app. Don't you build any scaffolds? Anything you need to build
and design should be always inside the CIB computer and a browser."* `[HIS WORDS, restored - an earlier
version silently reworded "should be always inside the CIB computer and a browser" to "should always be
inside the CIB" and dropped the preceding "Don't you build any scaffolds?" sentence with no ellipsis,
caught by a fresh audit]` (MEDAL pt 2)

**Outcome:** front ends stop duplicating and start sharing. Detail lives in `R4_FRONT_ENDS.md`; this
phase owns only the **repository mechanics**.

### Sub-phase S3.1 - One component source, per `R4` F2

**Corrected here** - an earlier version attributed this to "Great Reboot F2," but
`THE_GREAT_REBOOT_ROADMAP.md` has no phase numbered F2 anywhere (its phases run 0 through 10, no
F-prefix). The actual owner, correctly named fourteen lines below in this same file's S3 exit condition,
is `R4_FRONT_ENDS.md` Phase F2 - "THE SHARED COMPONENT SYSTEM."
The smallest shared visual and interaction system that carries navigation, threading, drilldown, and
private per-HAM scope.

### Sub-phase S3.2 - Do not revive old cold behavior
Standing offsite law: *"reuse current accepted assets... do not revive old cold behavior."* Reusing a
component means reusing its appearance, not its cold decision-making. **A shared component that
classifies is a shared defect** - the most efficient way to spread nasty cough ever devised.

### Sub-phase S3.3 - Backgrounds and assets: an open question of his, still open
> *"Backgrounds as image URLs or self-hosted?"* (open question #31, 20260609)

Unanswered. Carried into `30_RESEARCH/RESEARCH_DOCKET.md`, not decided here.

### Sub-phase S3.4 - Why this phase's scope line is drawn where it is
He drew the boundary this phase's outcome statement depends on - shared front end, isolated back end -
himself, in one sentence:

> *"the front ends at a service is all the same, it's just Share Repo front in the service, but the
> back end is all of my stuff."*
> `[HIS WORDS + 1_HIS_WORDS/01_RAW_WORDS/13_20260612_SPRING_WATER.txt]`

This is what licenses S3's own line above - "this phase owns only the repository mechanics" - as his
distinction rather than a coder's convenient split between R2 dedup and the isolation law. A shared
front-end component set sitting over backends that stay per-world isolated is the shape he already
described, not a compromise invented to reconcile S0.3's tension.

**Exit condition, receipt:** the no-cold-behavior check passing on the shared component set, and the repo mechanics proven to carry it. **The two-front-ends receipt belongs to `R4` F2 and is not duplicated here** - an earlier version restated it word for word, which a critic correctly read as two roadmaps claiming one deliverable.

---

## PHASE S4 - SHARED REPO AS AN ACL ADDRESS

**Anchor:** *"I should be able to say, where's shared repo code, or something that controls an ACL,
can get you there."* (20260530 HEAT)

**Outcome:** "shared repo" is a name the legend resolves, not a folder someone remembers.

### Sub-phase S4.1 - Register shared surfaces in the legend
Every shared repository and shared component set has an ACL name that resolves through the decoder,
per Great Reboot 0.1-0.2.

### Sub-phase S4.2 - The findability test is his own sentence
Ask the system in plain language *"where's shared repo code"* and get taken there. That is the
acceptance criterion, and it is his, verbatim.

### Sub-phase S4.3 - Why ACL-over-shared-repo is not only about findability
Two more places he returns to this pairing, and both make a claim past "you can find it by name":

> *"Almost every code in the share repo should have that ACL should define it."*
> `[HIS WORDS + 1_HIS_WORDS/02_PHASE_2/Rebirth doctrine pt 6 Clair command center, usage, tools.txt]`

> *"Think about how much better my system will be when we're actually using shared repos, but then
> take the layer of ACL on top of it. Now, does it make more sense to you? Harder to steal."*
> `[HIS WORDS + 1_HIS_WORDS/01_RAW_WORDS/32_20260701est_NYC_53RD_STREET_DOCTRINE_pt1.txt]`

The first quote sets near-total coverage, "almost every code," not an opt-in tag for a few surfaces.
The second states the reason it matters as security, not convenience. S4's exit condition should
demonstrate both: a name the legend resolves, and what it denies to a reader who does not hold the ACL
for it.

**Exit condition, receipt:** the query run live, the answer returned with its ACL name resolving
through the legend.

---

## PHASE S5 - THE CI THAT KEEPS IT HONEST

**Anchor:** the last shift's measured finding - a missing CI package was *"the common cause behind
four PRs failing or going dark, including one where all six tests of a pin - the entire reason that PR
existed - skipped under a green check."*

**Outcome:** shared code cannot regress silently across worlds.

### Sub-phase S5.1 - A skip is not a pass
The single most important rule here, and it is already a measured failure in this estate: **a suite
can be dark rather than passing** (failure shape #1), and **a decline can turn a code defect into a
green skip** (failure shape #6). Every shared-repo suite reports RAN / PASS / FAIL / **SKIP**
separately, and a skip on a pinned property fails the build.

### Sub-phase S5.2 - Pins must be shown red
Every pin protecting the never-overwrite column of S2.2 is demonstrated failing against a broken
build before it is trusted green (failure shape #2).

### Sub-phase S5.3 - A merged PR is not a deploy
Standing estate law. Live readback with a status code, per world, or it did not ship.

**Exit condition, receipt:** the red-run and green-run pair for each pin; a live readback per world
after one shared change.

---

## DEPENDENCIES

| Phase | Needs | From |
|---|---|---|
| S0 | nothing | - |
| S1 | S0 answered | **him** |
| S1.4 | repo-creation credentials | **him** |
| S2 | cross-world guard armed | `R1` P5.1 |
| S2 | S1 topology | S1 |
| S3 | component inventory | `R4` |
| S4 | ACL legend | Great Reboot Phase 0 |
| S5 | CI on the new estate | Great Reboot Phase 1 |

## WHAT IS BLOCKED ON HIM, PLAINLY

1. **Which reading of "shared repo" did he mean?** (S0.3) - one sentence unblocks S1 through S4.
2. **Repo-creation credentials.** Measured 403, not a guess.
3. **A Supabase management token**, if a new project is to be created by a coder rather than by him.

Everything else in this roadmap can be worked without him.
