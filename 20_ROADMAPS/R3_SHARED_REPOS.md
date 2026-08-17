# R3 - SHARED REPOS

> *"First thing we got to do is establish share repos. **We gotta go audit this.**"*
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

A single source of truth that pushes down into many worlds. This is the strongest and most-repeated
sense.

**Reading 2 - Front-end components in one place (deduplication).**
> *"It's called a shared repo. **The backgrounds are in the same spot.** It's called a shared repo."*
> (Countdown pt 4)

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

**Exit condition, receipt:** an occurrence table with counts and passages, the four readings with
their evidence, and the one question above put to him plainly. **The receipt is his answer**, or the
question standing on the board with his name on it.

---

## PHASE S1 - THE REPO TOPOLOGY (contingent on S0)

**Anchor:** *"Even the internal URLs we use need to be different. No old-world URL is reused
anywhere."* (Great Reboot 0.4) - the same discipline governs repo names.

**Outcome:** a named set of repositories with an explicit statement of what each holds, who may write
to it, and how code moves between them.

**Entry condition:** S0 answered by him. **Genuinely blocked** - this is not a phase that can be
started "provisionally" without pre-deciding the thing he was asked.

### Sub-phase S1.1 - The estates, which are already decided
Independent of S0, three estates are already settled by doctrine:

| Estate | Basis | Isolation |
|---|---|---|
| **Founder world** | `PO1-23` - *"I ain't taking that risk for my world"* | hard, own everything |
| **Alpha cohort (5-6)** | `PO1-23` - *"maybe that's actually alpha testing between five, these six"* | shared floor, per-HAM |
| **Temp coder world** | `PO2-01`, `OPEN-C1` | separate estate (working posture) |

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

The reading that fits both: **the global is the source; each world holds a materialized copy; a sync
channel pushes updates down; the UID stays local and is never overwritten.** That is a coder's
reading, marked as one, and it is offered to him as an answer to his own question rather than assumed
as settled.

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
Reinforced: *"Don't give me yet another app... anything you need to build and design should always be
inside the CIB."* (MEDAL pt 2)

**Outcome:** front ends stop duplicating and start sharing. Detail lives in `R4_FRONT_ENDS.md`; this
phase owns only the **repository mechanics**.

### Sub-phase S3.1 - One component source, per Great Reboot F2
The smallest shared visual and interaction system that carries navigation, threading, drilldown, and
private per-HAM scope.

### Sub-phase S3.2 - Do not revive old cold behavior
Standing offsite law: *"reuse current accepted assets... do not revive old cold behavior."* Reusing a
component means reusing its appearance, not its cold decision-making. **A shared component that
classifies is a shared defect** - the most efficient way to spread nasty cough ever devised.

### Sub-phase S3.3 - Backgrounds and assets: an open question of his, still open
> *"Backgrounds as image URLs or self-hosted?"* (open question #31, 20260609)

Unanswered. Carried into `30_RESEARCH/RESEARCH_DOCKET.md`, not decided here.

**Exit condition, receipt:** two distinct front ends rendering from one component source; a change
made once appearing in both; the no-cold-behavior check passing on the shared set.

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
