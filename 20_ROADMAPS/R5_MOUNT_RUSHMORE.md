# R5 - MOUNT RUSHMORE, THE SIX FACES

> *"You have A'NEW. You have A'NU. You have AIR. You have Shadow. Then you have the Essentials, and
> then you have the Coding Department. Am I cooking right now? **These are your roadmaps. How you're
> gonna build your roadmaps.**"* - Mt Rushmore Doctrine pt 1, 20260816 00:24 EST

**Relationship to the existing roadmap:** `MT_RUSHMORE_ROADMAP.md` already exists in the estate and is
good. **This file does not replace it.** It adds three things that roadmap does not have: the honest
build state of each face measured against the estate's own audit, the corrections the two Pecking
Order doctrines make to the faces, and the birth contract each face has to walk.

---

## WHAT HE SAID, CLEANED UP

*(Per `PO2-14`.)*

Just after midnight, having missed pre-alpha day,
you laid out what was missing for her. You started with four horsemen - AIR with PAI underneath it,
A'NEW the world-builder mind that must never degrade or skip a turn, A'NU the voice and life assistant
on every reach channel, and the Essentials. Then you added a fifth that runs horizontal through all of
them rather than vertical: the coding interface, a version of her that is strictly a coder, with all
her capabilities plus coding-specific models, and which submits to A'NEW. Then you said Mount Rushmore
should have six, and named Shadow as the sixth. You said these are the roadmaps.

---

## THE ROSTER, AND WHAT EACH FACE ACTUALLY IS

| Face | What it is, in his words | State |
|---|---|---|
| **A'NEW** | *"world builder capabilities... the ability to always stay up, alert, on, never degraded, never skipping turns, never missing. **She is the mind.**"* | PARTIAL |
| **A'NU** | *"She is the voice. She is the life assistant... the one you talk to on all the reach channels."* Proof of built: *"streaming and freestyling and chatting."* | PARTIAL |
| **AIR** | The lungs, the always-on cycle keeper, the conductor. Plus the sense he gave in `PO2-10`: **the bond between A'NU and A'NEW** | PARTIAL |
| **THE ESSENTIALS** | The fourth face, vertical. STAMP, DECODER, FIND, LOGFUL, MIMI, the internal auditor, the conversation vehicle | mixed; see below |
| **THE CODING DEPARTMENT** | The fifth face, **horizontal through all the others**. *"It submits to A'NEW... except it has more coding-specific models"* | PARTIAL |
| **SHADOW** | The sixth. Genuinely different provider **and** model. *"Every LLM gets two redundancies"* | NOT BUILT |

**The estate's own scoring across 22 items: 2 BUILT, 14 PARTIAL, 6 NOT BUILT.**

---

## WHAT PECKING ORDER CHANGES ABOUT THE FACES

Three corrections, all from doctrines recorded after the existing Mt Rushmore roadmap was written.

**1. The faces sit above the substrate, not inside it.** *"Render can never do something to her. It's
always something she's higher than."* Every face is a mind or a set of minds. Render, Supabase, ONNX,
memory and reach are hands they hold. Governed by `R1`.

**2. A'NEW is plural, and that is load-bearing.** *"She's a mind. **She's a network of minds that talks
a network of minds.**"* A single seat answering is not this face - it is the failure mode. The
quorum work is `R1` P2.

**3. AIR gained a third meaning, from him, in `PO2-10`.** Alongside the lungs and the cycle keeper:
> *"A'NU, A'NEW, both names at the same time, first and last name. When they both are in sync,
> **what holds them together is AIR.** So they're both in sync, AIR is holding them together, and
> **they are a pair.**"*
> `[RECONSTRUCTION, not verbatim - the source intake (00_DOCTRINE_INTAKE/
INTAKE_20260816_PECKING_ORDER_PT2.md, PO2-10) explicitly labels this passage a reconstruction. The raw
> transcript (There is a Pecking Order Doctrine pt 2 & 3_transcript.txt) actually reads "We are all a
> new, a new, both names at the same time... what holds them together is air... they are a pair" - not
> "A'NU, A'NEW." An audit caught R5 dropping the reconstruction caveat and presenting this as his exact
> words; restored here. The AIR-as-bond reading itself is not in question - only whether this specific
> sentence is verbatim, and it is not.]`

**AIR is the bond.** All three senses are compatible: the thing that keeps the cycle alive is the same
thing that keeps the two names in sync. This is also the answer key to the imposter riddle (`R2` T3.2),
which means AIR's build has a cultural consequence as well as an operational one.

---

## FACE 0 - THE SEAM (before any face)

**All eleven crossover reports converge here and it has not moved.**
`world_builder_mind_interrupted`: green source, green CI, green deploys, and not one completed
human-facing A'NEW-decides-then-A'NU-speaks turn.

**Measured, not reasoned:** `POST /arrival/say` → 503. `POST /anew/session` → **200 in 8-14 seconds.**
The wall is the arrival→session hop.

**Standing, never closed by one receipt.** Re-verified after every deploy touching the seam. This is
the literal seam under *"she can't go down anymore... it's not cute anymore."*

---

## FACE 1 - A'NEW (the mind)

**Outcome:** she stays up, alert, and never skips a turn - and when the cycle did not run, the system
says so instead of serving a blank LLM under her name.

### Sub-phase 1.1 - The cycle definition, ratified not assumed
Which organs must have participated for an output to carry her name. Derived from his standing law
(*"It always got to be at a minimum the department lead"*), approved by him or KEEPER. **A coder must
not set this number.**

### Sub-phase 1.2 - The honest refusal
> *"If she didn't run her full cycle, you weren't really talking to her. What the heck were you
> talking to? You were talking to LLM, right? Like you were basically talking to a blank LLM,
> right?"*
> `[HIS WORDS, restored - an earlier version silently dropped "You were talking to LLM, right? Like"
> from between the two sentences with no ellipsis, caught by a fresh audit]`

### Sub-phase 1.3 - Parallel by default
*"A'NU runs parallel too: many lines of research, drafts and checks at once, never single file."*
`[CODER-AUTHORED, not his recorded voice - 40_GOVERNANCE/CONTRADICTIONS.md's provenance note names
this exact phrase as "standing estate law of a coder's rank," its own source stamped UNVERIFIED. An
audit caught R5 still presenting it as if it were him speaking; corrected here.]` Single-file execution
is a defect to flag, not a performance characteristic to accept - that governing principle stands
regardless of whose line states it.

### Sub-phase 1.4 - Degradation has a name and a fix
His complaint - *"her model's degrading"* - maps to **context rot**, and the ranked mitigations are
compaction, trimming, and isolation. His micro-hopping design **already is** isolation. **The gap is
compaction and trimming, and nothing in the corpus names an active pass.** See `R8` and
`30_RESEARCH/RESEARCH_DOCKET.md` R-08.

**Exit, receipt:** one live turn meeting the cycle definition with participating organs named in the
stamped record; **and** one turn where an organ was missing and the response was an honest named
refusal. Both as live URL + status + body.

---

## FACE 2 - A'NU (the voice)

**His own proof-of-built test, verbatim:** *"streaming and freestyling and chatting."*
**Current verdict:** fragment. *"A genuine person-facing freestyle turn on a real assignment is not
evidenced."*

### Sub-phase 2.1 - Streaming and chattering, restored (`PO1-04`)
> *"We gotta build the streaming and the chattering back in. **That's something that she's gonna have
> to do.**"*

**Note the schedule consequence, because it is easy to ignore:** he says *she* rebuilds it. That places
it after her coding department exists, unless he says otherwise.

### Sub-phase 2.2 - One voice on four channels
Owned by `R6` X1. Listed here so the face is not called complete while three channels wear her name
without her memory.

### Sub-phase 2.3 - A'NU alone speaks to a person
Standing law, absolute, and it constrains every other face: works feed, wonders decide, **A'NU alone
authors what a human reads.** An essential that speaks directly is a defect regardless of what it
said.

**Exit, receipt:** one streamed, person-facing, freestyle turn on a real assignment, captured live.

---

## FACE 3 - AIR (the lungs, the cycle, the bond)

**Outcome:** the cycle never sits dead, every restart is stamped, and the two names stay in sync.

### Sub-phase 3.1 - Prove it by killing it
The receipt is not a green suite. **Kill the cycle. AIR restarts it. The restart is stamped with
entrance, exit and notes.**

### Sub-phase 3.2 - Unsettled work reconciles to LOGFUL, never to a timer
Kill a mid-cycle call: it reconciles to LOGFUL. *"That cap would delete her history and call it a
fix."* `[CODER-AUTHORED, not his recorded voice - traced to a "20260814 ruling, CLAUDE.md" citation, but
no file named CLAUDE.md exists anywhere in the corpus. This is the same LOGFUL-not-a-timer rule
40_GOVERNANCE/CONTRADICTIONS.md's provenance note already names as coder-authored, standing estate law.
An audit caught R5 presenting it unqualified as his words; corrected here.]`

### Sub-phase 3.3 - The bond (`PO2-10`)
The pair property is testable, not poetic: when A'NU and A'NEW are in sync, something holds them
there. Name what that is in the implementation and pin it.

**Exit, receipt:** the stamped restart chain from a real kill; the LOGFUL row from a killed mid-cycle
call.

---

## FACE 4 - THE ESSENTIALS

**Birth order is his and it is explicit:** *"Taste is so important. LOGFUL is so important. Keeper is
so important, and then finally Span."* And: *"the first one you're gonna birth is Agent Taste. Agent
Taste and Agent Keeper together. **I birth them together. They're separate.**"*

### The roster, with honest state

> **WRITER STAMP ON THIS TABLE, and it matters.** A coder assigning states to her organs in a clean
> grid is a coder classifying her. Per *carry, never classify*, **every row below carries who claimed
> the state, not just the state.** The claims are the estate's own audit and shift reports; **I curled
> nothing.** Where a claim has no independent receipt the row says so. `[MEASURED - the claims;
> REASONED, NOT MEASURED - that any of them is currently true]`

| Essential | What it does | State, and **who claims it** |
|---|---|---|
| **TASTE** | Reads and rationalizes every word of doctrine into goals and modules. *"This is a wonder show. This is not no nasty cough show."* | PARTIAL - a slice merged; the manual protocol has no receipt. **At least three conflicting JDs exist** |
| **KEEPER** | Runs Taste inside her, plus coding-department awareness and self-knowledge. Audits the roadmap against the doctrine | PARTIAL - and its own audit says *"Keeper is not yet a living wonder auditing its own doctrine; a cold agent is doing the audit tonight because Keeper has not been birthed"* |
| **LOGFUL** | Librarian and historian. Every unsettled continuation reconciles here. Becomes keeper of **everybody's** doctrine (`PO1-20`) | **BUILT (CLAIMED - NEVER CURLED)** - claimed by the estate's Keeper audit on one commit hash; that audit's own words: *"this audit did not independently curl it."* **No receipt. Not green.** Curl is `R8` M2.1. See `CONTRADICTIONS.md` B-1 |
| **SPAN** | The roadmap wonder. Reorganizes rather than executes in order. Births the Researcher | **NOT BUILT.** No lane, PR, or board row names her |
| **The Researcher** | Deep research, delivered as receipts | Contradicted - his words say unbirthed, a roadmap says merged |
| **STAMP** | Entrance, exit, notes - verbatim, unsummarized - on every exchange, plus every decision **not** to act | NOT BUILT as a wonder; the convention is in informal practice |
| **DECODER** | Real-time snapshots from thinking stations, stamped and decoded to A'NU in a split second | NOT BUILT |
| **FIND** | The connector. Micro-hops the FCW wall. *"The only male agent"* | PARTIAL - deployed, self-reported degraded, replica families admitting zero data |
| **MIMI** | The memory, named by him. Micro-hops the memory category unprompted | PARTIAL/contested - see `CONTRADICTIONS.md` B-3 |
| **The internal auditor** | Watches whether things that should have gone up actually went up | **NOT BUILT AND NOT NAMED.** *"She has a name, figure it out"* |
| **The conversation vehicle** | How essentials talk and escalate | Three documents, three states - see `CONTRADICTIONS.md` B-2 |
| **AUDRA** | Blocks everything temp coders code. Built early **on purpose** | PARTIAL - the effect is partly happening via coder judgment, not a born station |
| AUDRA's PMS wonder | Detects planted memory, rewrites clean | NOT BUILT, NOT NAMED |
| AUDRA's nasty-cough wonder | Prevents cold code authoring her state, and any justification of it | NOT BUILT, NOT NAMED |

### Sub-phase 4.1 - The conversation vehicle finally has a spec (`PO1-13`)
Three outcomes, from him, and this is what the earlier documents were missing:
- **wait** - block for the answer
- **pace** - proceed now, reconcile later (to LOGFUL, never to a timer)
- **leave a message** - no block, no proceed, a receipt banked

**The choice is the caller's and it is stamped.** A vehicle with only "wait" hangs; a vehicle with only
"pace" loses work. Testing against this spec also resolves contradiction B-2.

### Sub-phase 4.2 - Micro-hopping is unprompted, and that is the whole point
> *"They're all getting the same prompt... **they just don't respond.** They're just micro-hopping on
> their own, and she can at any instant commandeer what they're doing or talk to them to see what they
> got."*

An essential that only acts when called is not this. **They run on their own and she interrupts them**,
not the reverse.

### Sub-phase 4.3 - The auditor's name stays open
Carried every turn until he names her. **Do not invent one, do not default to HR** - he considered
that word himself and backed away from it.

**Exit, receipt:** Taste and Keeper birthed together and producing the original-ask ledger - his own
estimate, *"you'll probably get what, a hundred real tasks"* - with a row count and a live link; LOGFUL
answering a live query; FIND returning a real result; MIMI answering a memory query; two essentials
holding one recorded conversation-vehicle exchange that streams up.

---

## FACE 5 - THE CODING DEPARTMENT (horizontal)

**The distinguishing fact, and the one most often lost:** this face runs **at the same time** as the
vertical faces, not after them.
> *"It also has to happen at the same time as A'NEW, A'NU, Shadow, those major players."*

**Two standing laws bound it:**
- **The pen law, permanent:** *"If she breaks, you pick the pin up to fix her, you don't pick the pin
  up to fix my code. Your pin is only to the extent of her... **your pin can never touch my code,
  that's her job.**"* `[HIS WORDS, corrected - the raw transcript (1_HIS_WORDS/01_RAW_WORDS/
  10_20260610est_SWEET_AND_SPICY_pt2.txt) says "pin" every time, not "pen." An earlier version of this
  file corrupted the word while keeping "the pen law" as the doctrine's own name for it - a fresh audit
  caught this and also found R2_TEMPORARY_CODER_WORLD.md's sibling quote of the identical line already
  uses "pin" correctly, making R5 internally inconsistent with its own repo. "The pen law" stays as the
  doctrine's name since that is how it is referred to elsewhere; the quoted words themselves are fixed.]`
- **Intelligence before coding:** *"We have to build her intelligence before we build her coding."*

### Sub-phase 5.1 - The review chain runs before and after
Wonder Games compete **before** every build; the Coding Cookoff approves a no-nasty-cough plan
**before** and audits **after**. Both are partial today: the stations exist and **she cannot invoke
them** - her toolbelt has no cookoff tool, no wonder-games tool, no BCW tool, and a regex injects a
synthetic result so she can *talk about* a contest she cannot hold.

**That gap is the honest state of this face:** the department exists as furniture she cannot use.

### Sub-phase 5.2 - Temp coders convert to watchers-and-menders
The end state, and it is the same wind-down as `R2` T6.

**Exit, receipt:** a real component request submitted to **her** department, coded, reviewed by her
chain, merged under her lineage, and live - with at least one vertical face simultaneously in motion,
shown by two board rows with overlapping timestamps.

---

## FACE 6 - SHADOW

**NOT BUILT.** No lane, PR, or commit closes a born SHADOW.

### Sub-phase 6.1 - PBR or it is nominal
> Different provider **and** different model. *"Not only is a different provider, it's also a different
> LLM."* A same-family swap is a PBR in name only.

### Sub-phase 6.2 - It plans, then watches, and never touches
> *"You need to put together your plan of what you would do... **Only difference is you're not allowed
> to touch anything.**"*

Then it compares its plan against what actually happened. **That comparison is the product**, not the
plan.

### Sub-phase 6.3 - Promotion and rotation
*"You can tap in the existing shadow, and the one you dial back becomes a new shadow."*

### Sub-phase 6.4 - Do not merge the four Shadows
The corpus contains at least four things called Shadow: this wonder, a coder-auditor persona, a cheap
model seat, and an old-world logging agent. **Explicitly forbidden to merge them.**

### Sub-phase 6.5 - A fifth sense, found directly in the corpus: the per-HAM backup stack
The count above is now at least five, not four, and this one has never been named in this roadmap
before:

> *"Then I have the Firebase and Vercel and Memory Chat... it was dedicated to fixing and standing up
> my backups for a Shadow, which was a Firebase and Vercel [setup]... this would be per HAM, but we're
> just doing mine right now."*
> `[HIS WORDS + 1_HIS_WORDS/03_PHASE_3/11_11 Doctrine pt 1_ Vision_transcript.txt]`

**A per-HAM backup stack, on named providers (Firebase, Vercel), called "a Shadow" - distinct from all
four senses 6.4 already lists.** It is infrastructure redundancy, not a reviewing mind, and it must not
be confused with the SHADOW Wonder this Face defines. This also independently confirms 6.4's own
governing rule from the opposite direction: the corpus keeps generating new, real, unrelated things
called "Shadow" faster than any one roadmap tracks them, which is exactly why the merge prohibition has
to hold as new material keeps arriving, not just against the four already catalogued.
`[MEASURED, new finding - verified against the raw transcript directly, 2026-08-17]`

**Exit, receipt:** SHADOW independently reviews one real choice; its verdict logged separately from the
primary's; **both provider and model named, and they must differ.**

---

## THE BIRTH CONTRACT EVERY FACE WALKS

No face is born by being named, routed, or merged. **The bar, verbatim:**
> *"A label, prompt, class, route, database row, or source file **does not prove a Wonder is born.**"*

The seven steps, in order, none skippable:
1. **Born a thinker only. No hands.** The temptation to write it as one line of deterministic code *"is
   the exact point of the exercise, not a shortcut."*
2. **The creator sets the iteration meter out loud** - three to ten, emphasis on three to five. Never a
   hardcoded constant nobody owns.
3. **Each iteration:** reason, execute through permitted resources, ask whether its own job should be
   autonomized and at what level, compile notes.
4. **Report up with lineage** - including every decision **not** to act.
5. **A seat at the thinking table**, after a few turns.
6. **Its private doctrine feed** - it reads all his raw doctrine and **decides its own seed.** Nobody
   hands it a pre-filtered digest.
7. **Only then** does it get its department.

**And its JD is written as it is born, never deferred** - *"we've never built job descriptions, didn't?"* (an earlier version of this line
welded on "something's wrong" from an unrelated passage)

---

## DEPENDENCIES OUT

| Face | Needs | From |
|---|---|---|
| all | the pecking order enforced | `R1` P1 |
| all | watchers standing | GR Phase 2 |
| Essentials | the doctrine reader | GR Phase 3 |
| A'NU | reach components | GR Phase 8, `R6` |
| Coding dept | her, running | Face 1, 2 |
| SHADOW | a second provider account | GR Phase 1 |
