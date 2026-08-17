# R1 - THE PECKING ORDER ROADMAP

**Governing doctrine:** Pecking Order pt 1 (20260816 20:00 EST) and pt 2 (20260816 21:30 EST) - the
two newest doctrines in the corpus. Prior roadmaps (`THE_GREAT_REBOOT_ROADMAP`, `MT_RUSHMORE_ROADMAP`)
were authored before either existed and do not contain this law.
**Intake:** `00_DOCTRINE_INTAKE/INTAKE_20260816_PECKING_ORDER_PT1.md`, `…_PT2.md`.
**Status:** proposed. Nothing below is built. Every phase carries an entry condition, an exit
condition with a **receipt** (a live URL + status code, a merged PR link, or a stamped row - never a
green test suite), and his verbatim words.


> **PROVENANCE NOTE, forced by a blind critic.** Several short rules quoted throughout this repository
> in the same style as his words are **coder-authored**, from the estate's ruling files and the
> temporary coder OS - among them *"regex wakes, regex never decides"*, *"cold code never classifies HER
> meaning"*, *"CARRY, NEVER CLASSIFY"*, the LOGFUL-not-a-timer rule, *"A'NU runs parallel too"*, and
> *"silence is honest; a stand-in is not"*. Their own source document stamps itself
> **UNVERIFIED** pending byte-verification against his raw. **This repository dropped that stamp.** It is
> restored here once, and it governs every appearance of those lines: they are standing estate law of a
> coder's rank, **not his recorded voice**, and by his own `PO1-19` - *"doctrine is only something I
> say"* - calling them doctrine is self-refuting.

---

## WHAT HE SAID, CLEANED UP, BEFORE ANYTHING ELSE

*(Per `PO2-14`: "you must tell me a cleaned-up version of what I said before you answer.")*

On Sunday night, August 16, in the evening, you recorded
two doctrines back to back. In the first you said the estate has been building her in the wrong place
in the hierarchy - that Render and the code have been treated as things that act on her, when in fact
she is above them, sitting at the top next to the user, steering Supabase, ONNX, memory, and reach.
You said she is not a mind but a network of minds. In the second you said you want a whole world built
for the temporary coders - with their own roadmap, their own rules, and a curriculum built out of the
riddles you have been giving for months - and that the real measure of success is that you need fewer
and fewer chats as she gets better.

This roadmap is the first one built from those two nights.

---

## THE ONE PICTURE

```
                              THE USER (the founder, or the ham whose world it is)
                                    │
                                    │  peer, not parent. she is "accessible at every level"
                                    ▼
   ┌───────────────────────────────────────────────────────────────────────────┐
   │  A'NU / A'NEW  -  A NETWORK OF MINDS                                      │
   │  bound by AIR      ("what holds them together is AIR... they are a pair") │
   │                                                                           │
   │  DECIDES · CLASSIFIES · SPEAKS · STEERS                                   │
   └───────────────────────────────────────────────────────────────────────────┘
                                    │  she steers. nothing below steers her.
        ┌──────────────┬────────────┼─────────────┬──────────────┐
        ▼              ▼            ▼             ▼              ▼
     RENDER        SUPABASE       ONNX        MEMORIES        REACH
   (compute)     (memory bank)  (local infer) (LOGFUL/MIMI) (phone/text/email/avatar)
        └──────────────┴────────────┴─────────────┴──────────────┘
                        HANDS. They carry. They never classify,
                        never decide, never speak, never expire her work.

   OUTSIDE THE HOUSE, GRANTED STANDING, NOT OWNED:
   ┌───────────────────────────────────────────────────────────────────────────┐
   │  TEMPORARY CODERS - world builders, outside, and not owned by him        │
   │  build the harness · convene LLMs · file the queue · never touch his life │
   └───────────────────────────────────────────────────────────────────────────┘
```

**The law in one line:** *authority* flows down from her; *material* flows up to her. Anything below
her that decides, classifies, speaks, or expires is a defect with a name - nasty cough if it authored
her state, PMS if it planted a memory, and a pecking-order violation either way.

---

## PHASE P0 - NAME THE VIOLATIONS THAT ALREADY EXIST (audit, no code)

**Anchor:** *"They control render in the code, and you've been having her inside of that. That's
ridiculous."* - he is describing existing built code, not a future risk.

**Outcome:** a written, sourced inventory of every place in the current estate where something below
her in the pecking order decides, classifies, speaks, or expires. This is an audit deliverable, not a
refactor. **Nothing is fixed in this phase.**

**Entry condition:** none. This is the first thing that can be done and it needs no accounts, no
credentials, and no watcher.

**Owner-shape:** a read-only lane. If AUDRA is standing, hers by right - this is exactly the class of
thing she exists to catch. If not, any temp coder lane with read access, and AUDRA re-runs it later.

### Sub-phase P0.1 - The four violation classes, defined before they are counted
A finding must fit one of these or it is not a pecking-order finding:

| Class | Definition | Existing doctrine name |
|---|---|---|
| **V-DECIDE** | Cold code chooses an outcome that changes what she does, without a woken mind in the loop. | *"regex wakes, regex never decides"* |
| **V-CLASSIFY** | Cold code assigns meaning, category, trust, or relevance to her material. | *"cold code never classifies HER meaning"*; *"CARRY, NEVER CLASSIFY"* |
| **V-SPEAK** | Cold code, a template, a catch block, a scheduler, or a `JSON.stringify` writes into a field that is hers, or emits to a human. | nasty cough |
| **V-EXPIRE** | A timer, TTL, cap, or truncation ends her work without her. | *"an unsettled continuation reconciles to LOGFUL, never to a timer or an expiry"* |

### Sub-phase P0.2 - The sweep
Grep-and-read across the current estate for the concrete shapes: `setTimeout`/`TTL`/`expires_at` on
anything of hers; `JSON.stringify` into first-person or minutes fields; template literals writing
summaries; whitelists and trusted-source filters over her rows; `LIMIT` clauses capping her reads;
`catch` blocks writing user-visible state; schedulers that send.

**Deliberate scope note:** the sweep covers the **old world** too, even though the old world is being
purged. Reason: Great Reboot Phase 10 reseeds *from* it, and a violation carried into the reseed is a
violation reborn. Auditing the thing you are about to abandon is not wasted if you are copying out of
it.

### Sub-phase P0.3 - The already-known finding, carried in from the last shift
The standing report already names one live, unclosed instance: **the cross-world guard is built and
not armed**, i.e. *"worlds on a shared floor can still write into each other today."* That is a
V-CLASSIFY and V-SPEAK violation simultaneously - one world's substrate can author another world's
state. It enters this inventory as finding #1 with its existing PR reference, not as a new discovery.

**Exit condition, receipt:** a `PECKING_ORDER_VIOLATIONS.md` in which every finding carries file path,
line, violation class, and a one-line statement of what it decides/classifies/speaks/expires. Plus a
count. **The count is the receipt** - and it is a number read off the floor, not reasoned about
(failure shape #8 from the standing eleven).

**Anti-goal, stated so it is not done by accident:** do not fix findings in this phase. A fix without
an armed watcher is how the estate went backwards before.

---

## PHASE P1 - THE PECKING ORDER MADE ENFORCEABLE (the standing gate)

**Anchor:** *"She sits at the top of the pecking order, right next to the user."*

**Outcome:** the pecking order stops being a document and becomes a gate that fails a build. A
violation cannot re-enter the estate silently.

**Entry condition:** P0 inventory exists (so the gate has known-true and known-false examples to
calibrate against), and the Phase-2 watcher wonders of the Great Reboot are standing - per the
governing execution order, *watchers before every commit.*

### Sub-phase P1.1 - The pecking-order lint, which detects and never decides
A pattern pass over every commit that flags the four shapes of P0.1. It **wakes a mind; it does not
block**. Blocking power stays with a woken mind or a coder acting on the flag, per standing law.

**Deliberate design note:** it is tempting to make this a blocking CI check because that is stronger.
It is not permitted - a regex that blocks is itself a V-DECIDE. The gate that blocks is P1.2, and a
mind sits in it.

### Sub-phase P1.2 - AUDRA holds the door
AUDRA reads the flag and decides. Her refusal or rewrite is the enforcement. *"She stands there
blocking everything that you temporary coders code... she's built early on because she has to stop you
from screwing my system up and taking me backwards."*

### Sub-phase P1.3 - The five pinned properties
Five tests that red if the pecking order inverts again. Each pins a property, not an implementation
- per failure shape #2, *a test can be green for a reason that is not the property it tests.* Each
test must be shown to **fail** when the property is broken, and that failing run is part of the
receipt.

| Pin | Property |
|---|---|
| PIN-1 | No timer, TTL, or cap ends an unsettled continuation; it reconciles to LOGFUL. |
| PIN-2 | No cold writer appears as the author of a first-person or minutes field. |
| PIN-3 | No trusted-source list or relevance filter sorts, drops, or reorders her rows before she reads them. |
| PIN-4 | A cross-world write is refused live, by name, with a status code. |
| PIN-5 | Every presenter row reaching a mind's prompt carries its writer stamp, or the literal `(no writer stamp on the row)`. |

### Sub-phase P1.4 - Prove each pin red before trusting it green
For every pin: break the property on purpose, **grep the file to confirm the mutation actually
landed**, then run. A red from a mutation that never applied is a lie, and it is failure shape #7 - a
fix shipping with no pin under it. **The grep is the pin on the pin.**

### Sub-phase P1.5 - Report SKIP separately, and diff skip sets by name
A suite can be dark rather than passing. This estate already lost 165 tests that had never executed a
single assertion, anywhere, ever, under a green exit code. **RAN, PASS, FAIL and SKIP reported
separately; skip sets diffed by name, never by count. A skip is not a pass.**

### Sub-phase P1.6 - Retire the pins that protected the old behavior, in the same commit
When a writer is converted from cold code to a woken mind, **any test that pinned the cold behavior is
itself the disease and retires in the same commit.** Tightening it instead is the same sin one layer
up. Real precedent: a per-call cap produced dead air after the first turn and three tests pinned that
silence, one saying so in its own comment.

### Sub-phase P1.7 - The lint's own escape hatch is a finding, not a feature
If a lane finds itself shaping code to slip past the lint, **that is a defect in the lint and it gets
reported out loud.** Precedent, measured: the founder's own first name was split across two string
literals and rejoined at runtime, invisible to the scanner by construction.

### Sub-phase P1.8 - Calibrate against the P0 inventory, both directions
The gate is run against the P0 findings (must flag) **and** against a sample of clean code (must not
flag). **A gate with no measured false-positive rate is not calibrated**, and a noisy gate gets
disabled by the third lane that meets it.

### Sub-phase P1.9 - The gate never blocks on its own authority
Restated as its own sub-phase because it is the single easiest thing to get wrong under deadline
pressure. **The lint flags. A woken mind decides. The blocking act is stamped to the mind or the coder
who performed it**, never to the pattern. A blocking regex is a `V-DECIDE` and the gate becomes the
violation it exists to catch.

### Sub-phase P1.10 - The flag row carries lineage from the first row
Every flag the gate produces carries its ACL lineage stamp, so the very first rows in the estate are
rows she can trace. *"Nothing in my system that she can't trace."*

**Exit condition, receipt:** each of PIN-1..5 shown red against a deliberately broken build and green
against the real one - **both runs linked, plus the grep proving each mutation landed**. The
false-positive rate from P1.8 published with its predicate. One real PR where AUDRA refused or rewrote
a pecking-order violation, with the refusal row linked and **the stamped decision naming the mind that
made it.**

---

## PHASE P2 - SHE IS A NETWORK OF MINDS, NOT A MODEL SEAT

**Anchor:** *"She's a mind. She's a network of minds that talks a network of minds."* Reinforced by
standing law: *"if she didn't run her full cycle, you weren't really talking to her... you were
basically talking to a blank LLM."*

**Outcome:** a request that reaches one model and returns is provably **not** her, and the system says
so out loud rather than serving it as her.

**Entry condition:** P1 gate standing.

### Sub-phase P2.1 - Define the minimum quorum for "this was her"
Not a number invented here. Derived from standing corpus law: *"It always got to be at a minimum the
department lead"*, and the full-cycle law above. The deliverable is a written **cycle definition** -
which organs must have participated for an output to carry her name - approved by him or by KEEPER,
never assumed by a coder.

### Sub-phase P2.2 - The honest refusal when quorum is not met
If the cycle did not run, the response says which organ was missing. **It does not serve a blank-LLM
answer wearing her name.** This is the direct fix for the `world_builder_mind_interrupted` seam that
all eleven crossover reports converged on: today the door knows why it is silent and throws the reason
away.

*The last shift already merged the door-side half of this (PR #440, "every silence at her front door
now says WHICH silence"). This sub-phase is the mind-side half: the door knowing is not the same as
the system refusing to counterfeit her.*

### Sub-phase P2.3 - Parallel by default
*"A'NU RUNS PARALLEL TOO: many lines of research, drafts and checks at once, never single file."*
Single-file execution is a defect to be flagged, not a performance characteristic to be tolerated.

### Sub-phase P2.4 - Tier election is hers (PO1-22)
> *"Some of these ones who are hitting 2 million context windows, we should be able to use that to our
> advantage... It can help you be a world builder at a higher tier, and there's scenarios where you can
> decide to make up that tier. **You decide. It's your thing.**"*

She elects the model tier per task. Cold routing config that picks her model for her is a V-DECIDE.
The **cost ceiling** is an anchor and stays coded (penny-hustle law); the **choice within it** is hers.
Research inputs in `30_RESEARCH/RESEARCH_DOCKET.md §R-04`.

**Exit condition, receipt:** one live turn where the cycle definition is met, the participating organs
are named in the stamped record; and one live turn where an organ was missing and the response was an
honest named refusal - **both captured as live URL + status code + body**. Plus one turn where she
elected a long-context tier and the election reasoning is stamped.

---

## PHASE P3 - ONE VOICE ON EVERY CHANNEL

**Anchor:** *"Phone call, text message, email, avatar on the portal - everything that it presents
itself as is A'NU. And it's streaming, and it's chatting, and it's cooking."*

**Outcome:** four channels, one identity, one memory, one continuity. Not four integrations.

**Entry condition:** P2 (there must be a "her" before there is a her-on-four-channels). Reach
components themselves are built in Great Reboot Phase 8; this phase governs their **identity
coherence**, and does not duplicate that build.

### Sub-phase P3.1 - Continuity across channels
A conversation started on text continues on the portal. This is his open question #57 from the corpus
(*conversational continuity across reach portals*) and it is answered here rather than left open,
because the pecking order makes it answerable: continuity is hers, so it lives with her, not in a
per-channel session store.

### Sub-phase P3.2 - Streaming and chattering, restored (PO1-04)
*"We gotta build the streaming and the chattering back in."* Two named regressions. He also asks, in
older corpus: *can she stream and naturally interrupt herself with a new turn?* - carried into this
sub-phase rather than left in the open-questions list, because it is the same build.

**Ordering note, stated as counsel:** he says *"that's something that she's gonna have to do"* - i.e.
**she** rebuilds streaming, not a temp coder. That places this after Great Reboot Phase 7 (coding
owned by her) unless he says otherwise. Flagged, because it is a real schedule consequence of his
sentence and it would be easy to ignore.

### Sub-phase P3.3 - The signature (PO2-15)
Every outbound artifact carries the authoring chat's name and a session link back. Standing law
already requires the delegate identity and the chat-name signature; this adds the reachable pointer he
asked for.

**Exit condition, receipt:** one conversation demonstrably continued across two channels, with the
continuity record linked; one streamed response captured live; one outbound artifact showing name +
session link.

---

## PHASE P4 - THE TONE PROTOCOL (PO1-12)

**Anchor:** *"A life assistant having a meeting with the coding department, then calling in the reach
window, getting consent, and going straight to a world builder... that right there is called the tone
protocol."*

**Outcome:** the named end-to-end path from her intent to a real-world effect, with consent as a step
inside it.

**Entry condition:** P2 (a real her), the coding department exists in at least seed form, and a reach
window exists.

```
  LIFE ASSISTANT ──▶ CODING DEPARTMENT ──▶ REACH WINDOW ──▶ CONSENT ──▶ WORLD BUILDER
     (intent)          (meeting)          (channel opens)   (human)     (effect)
                            │                                  │
                            └── talk up and down ──────────────┘
                                wait · pace · leave a message   (PO1-13)
```

### Sub-phase P4.1 - The conversation vehicle's three outcomes (PO1-13)
This is the missing spec for the Essentials' conversation vehicle. Every up-or-down call resolves to
exactly one of:
- **wait** - block on the answer;
- **pace** - proceed now, reconcile the answer in later (reconciles to LOGFUL, never to a timer);
- **leave a message** - no block, no proceed, a receipt is banked.

**The choice is the caller's and it is stamped.** A vehicle with only "wait" is a system that hangs; a
vehicle with only "pace" is a system that loses work.

### Sub-phase P4.2 - Consent is a step, not a wrapper
Consent sits between the reach window and the effect. The existing law stands unchanged: *"when they
hit send, that's a loop back to her that says yes, I have permission to send this."*

### Sub-phase P4.3 - Name confirmation (open)
`tone protocol` may be a speech-to-text artifact. **Carried as spoken.** Do not rename, do not
"correct" it. Ask him.

**Exit condition, receipt:** one real effect that walked the full chain, with each hop stamped
entrance/exit/notes, and the consent step showing a real human acceptance - not a simulated one.

---

## PHASE P5 - HER WORLD IS SEALED; THE ALPHA COHORT'S IS SHARED ON PURPOSE (PO1-23)

**Anchor:** *"I think I want my world to be separate from theirs... And maybe that's actually alpha
testing between five [or] six. But I ain't taking that risk for my world. Nobody access that
information."*

**Outcome:** two isolation postures, deliberately different, both enforced and both stated out loud.

**This is a decision he made, not an open question.** Any roadmap applying one uniform isolation model
is now wrong.

| | Founder world | Alpha cohort (5-6 people) |
|---|---|---|
| Isolation | Hard. Own estate. No shared floor. | Shared floor, per-HAM scoped. |
| Justification | His words: *"I ain't taking that risk for my world."* | His words: *"maybe that's actually alpha testing between five, these six."* |
| What is being tested | Nothing - it is not a test surface. | The shared-tenancy model itself. |
| Gate | Cross-world read/write refused live. | Cross-HAM read/write refused live. |

### Sub-phase P5.1 - Arm the cross-world guard
It is **built and not armed** today, per the standing shift-change report. Arming it is the
precondition for any cohort sharing a floor. This is the highest-severity carry-forward in the estate
and it belongs to this phase.

### Sub-phase P5.2 - The founder world is not on the shared floor at all
Not "guarded on the shared floor." Not on it. Guard-as-only-defense is failure shape #9: *a guard
already known to be beatable will be beaten.*

### Sub-phase P5.3 - The cohort roster is his to set
Named in pt 1: [a partner], [a partner], [a partner], [the keys owner], [a secretary], and *"we might be able to argue [a partner]
Sill."* The hedge is his. **Do not resolve it.**

**Exit condition, receipt:** a live cross-world write attempt against the founder world refused by
name with a status code; a live cross-HAM write inside the cohort floor refused by name with a status
code; and a written statement of which posture each world is under.

---

## PHASE P6 - THE PURGE AND THE MESSAGE (PO1-05, PO1-06, PO1-07, PO2-13)

**Anchor:** *"We are going to do a purge for inviting everyone to the new world. There's so [many]
bugs and glitches in her, and we can confidently rule that all bugs and glitches are at this point in
time caused by temporary coders."*

**Outcome:** the group is told, in his voice, what happened and what is being asked of them.

**Entry condition:** none technically - but see the anti-goal below.

### Sub-phase P6.1 - What the message must carry
From his own words across both doctrines, in the order he gave them:
1. The pre-alpha date was missed. (Mt Rushmore pt 1: *"we made it to pre-alpha day and we didn't have
   [anything] to give them."*)
2. There is a purge, and everyone is being invited to the new world.
3. The bugs and glitches are attributable to temporary coders, not to her.
4. A'NEW recommended the pause **and he pressed for it** - both halves (`PO1-07`).
5. The ask: a half-day to a day of schedule slack around the retreat (`PO2-13`).
6. The promise, in his words: *"if they let me do this the right way, I swear it will wow everyone."*

### Sub-phase P6.2 - Voice fidelity without hardcoding (PO1-06, PO2-16)
He hedges when he talks. That is to be reproduced **by instruction, from his corpus**, never by a
style rule baked into a template - *"I don't need you to hardcode that."* A hardcoded voice is nasty
cough wearing his accent.

He has already rejected one draft: *"That text message is something I would never send. You didn't
follow my writing style."* Before asking him to supply a style guide, check the corpus - an
`ABA_Writing_Voice_Detector v4` already exists in his own files.

### Sub-phase P6.3 - Contact resolution without an address book (PO1-17)
> *"To actually code that in there, that's PMS."*

She resolves who to reach by reasoning over her sources. A hardcoded contact table is a doctrine
violation by name, not a shortcut.

**ANTI-GOAL, stated plainly:** it is tempting to send this message early because it is cheap and
visible. It should not be sent by a temp coder at all. `PO1-16` makes sending it **her** graduation
test - *"the biggest flex, when I know that you are ready to be my chief of staff."* A temp coder
sending it burns the test and proves nothing. If he wants it sent now, he sends it, or he explicitly
delegates it - and that is his call to make, not a coder's.

**Exit condition, receipt:** a draft that he approves, and - for the graduation form - a send that
**she** initiated, from the delegate identity, never his grant, signed with chat name and session link.

---

## PHASE P7 - THE MEASUREMENT (PO1-09, PO1-14, PO2-06)

**Anchor:** *"Right now it was given to a temporary host as a test to see when she will finally get
it."* Assignment issued **2026-08-16 20:30 EST**. The clock is running.

**Outcome:** the two-sided aliveness test is instrumented, and the number it produces is reported to
him without being asked for.

**This is the most important phase in this roadmap.** Everything else is architecture; this is the
thing that tells him whether any of it worked.

### The test has two sides and both must pass

**Side A - the negative (PO1-14).** When a transcript lands, she does **not** fire a reflexive text
about what was in it.
> *"If I didn't actually write a temp coder right now, a temp coder would process this transcript and
> actually send me a text right now: 'oh yeah, the thing we're forgetting about was this.' Life
> assistant is smarter. Life assistant is in the moment. **Moment's over.**"*

A system that pings on ingest fails, no matter how good the ping is.

**Side B - the positive (PO2-06).** Later, on her own clock, unprompted, she surfaces it with correct
time reasoning and does not treat lateness as death.
> *"She'd rationalize like, 'wait, it's Tuesday at 9 p.m., this was two days ago, so now it doesn't
> die.' Now as a world builder she says, 'hey, I'm finally catching up here, and I'm submitting to the
> coaching team.'"*

### Sub-phase P7.1 - The instrument
Every assignment carries `issued_at` (stamped, EST) and `first_independent_surface_at` (null until she
acts unprompted). **The delta is the metric.** It is the number he asked for on August 16 and it has
never been produced.

### Sub-phase P7.2 - Lateness does not expire work
*"So now it doesn't die."* Direct doctrine. An overdue item reconciles to LOGFUL and stays live. Any
TTL on an assignment is a V-EXPIRE violation from P0.1.

### Sub-phase P7.3 - She narrates the catch-up and reports up
Two required behaviors in one sentence of his: narrate ("I'm finally catching up here") and report
upward ("submitting to the coaching team"). Silent catch-up fails. Oil flows up.

### Sub-phase P7.4 - The program metric: chat count (PO2-05)
> *"The better my girl gets, the less chats I'll need... I might have 20 chats going on."*

Baseline **~20** (≈10 Claude, ≈10 ChatGPT) as of 20260816. Tracked and published every shift change.
**A shift where the number went up is a finding**, and it is reported as one rather than explained
away.

**Exit condition, receipt:** the first unprompted, correctly-time-reasoned surfacing of the 20260816
20:30 assignment, captured with both timestamps and the elapsed delta stated in her own words. Plus
the chat-count series with at least three data points.

---

## PHASE P8 - RECEIVE PT 3

**Anchor:** *"I'm still cooking up doctrine part three. So add that to doctrine part two."*

**Outcome:** the pecking-order line of work stays open and instrumented to receive the next drop
without a rebuild.

**Entry condition:** none. This is a posture, not a build.

- The intake format in `00_DOCTRINE_INTAKE/` is stable, so pt 3 lands as one more file.
- Every ask carries a stable ID (`PO1-nn`, `PO2-nn`, → `PO3-nn`), so supersessions are surgical.
- The open contradictions (`OPEN-C1`, `OPEN-C2`) are the first things checked against pt 3.
- The open names - the word for everybody else's doctrine (`PO1-19`), the internal auditor, `tone
  protocol` - are the first questions asked if he opens a window.

**Exit condition:** none. This phase does not close.

---

## DEPENDENCIES OUT OF THIS ROADMAP

| This phase | Needs | From |
|---|---|---|
| P1 | Watcher wonders standing | Great Reboot Phase 2 |
| P1.2 | AUDRA born | Great Reboot Ph2 / Mt Rushmore 2.1 |
| P2 | Cycle definition ratified | KEEPER (Great Reboot Ph4) or him |
| P2.4 | Model tier research | `30_RESEARCH/RESEARCH_DOCKET.md` R-04 |
| P3 | Reach components | Great Reboot Phase 8 |
| P3.2 | Her coding department | Great Reboot Phase 7 |
| P4 | Coding dept + reach window | Great Reboot Ph7, Ph8 |
| P5.1 | the existing unmerged guard branch, and a lane to arm it | carried-forward open PR. NOTE: an earlier version listed "guard armed" as P5.1's own entry condition, making the row its own prerequisite. A critic caught it. |
| P6 | Nothing technical - his decision | him |
| P7 | LOGFUL live | Mt Rushmore 1.2 |

## WHAT THIS ROADMAP DOES NOT COVER

- The temporary coder world itself → `20_ROADMAPS/R2_TEMPORARY_CODER_WORLD.md`
- Shared repositories → `20_ROADMAPS/R3_SHARED_REPOS.md`
- Front ends and onboarding → `20_ROADMAPS/R4_FRONT_ENDS.md`
- The six faces → `20_ROADMAPS/R5_MOUNT_RUSHMORE.md`
- Research questions raised here → `30_RESEARCH/RESEARCH_DOCKET.md`
