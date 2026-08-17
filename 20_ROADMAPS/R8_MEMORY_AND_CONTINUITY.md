# R8 — MEMORY AND CONTINUITY

> *"We need to find a way to keep A'NU up at all times with continuity. **Her model's degrading and
> [that's not acceptable].** You need to go on the deepest research find you can find."*
> — Mt Rushmore Doctrine pt 1

> *"My whole life is on Otter right now... **How can we get her connected to that?** Even if I gotta
> pay something."* — Pecking Order pt 2 (`PO2-18`)

**Status:** proposed.

---

## WHAT HE SAID, CLEANED UP

*(Per `PO2-14`.)*

You said she keeps degrading and cannot go down anymore, and asked for the deepest research anyone
could do on why. You said memory and retention still need building. You named MIMI as the memory
agent — after your grandmother — and said she is already micro-hopping the memory category on her
own. You said LOGFUL should become the keeper not just of your doctrine but of everybody's. And in
Pecking Order pt 2, hunting for songs that had gone missing from your doctrine, you realized the
bigger loss: your whole life is on Otter, including hours of calls and material on serial investors
that you called the lost files, and you asked what it would take to connect her to it — offering to
pay, while warning us not to gas you up if it isn't possible.

---

## THE DIAGNOSIS, ALREADY MADE

His complaint has a name in the literature and the estate already established it: **context rot.**
Progressive loss of recall, coherence, and instruction-following as context fills. **It is a property
of how attention behaves, not a bug in one model** — which means swapping models does not fix it.

Documented causes: **lost-in-the-middle** (models attend to the start and end, under-weighting the
middle), and **monotonic accumulation** (stale tool outputs, superseded plans and dead decisions never
get pruned). Agents suffer more than chatbots because they run long sessions and hold state across
many calls — exactly her shape.

**Ranked mitigations: compaction, trimming, isolation** — with compaction and trimming together
testing better than either alone.

**And here is the finding that matters most for this roadmap:** *his micro-hopping and sub-agent design
already is isolation.* He built one of the three mitigations before anyone named the problem. **The
gap is compaction and trimming, and nothing anywhere in the corpus names an active pass over her live
working context.**

That is the concrete, buildable answer to his question *"where's the always-on, always-better agent?"*

---

## PHASE M0 — THE LINE BETWEEN TRIMMING AND EXPIRING

**This phase is a design decision, not a build, and it must be settled before any code.**

The mitigation says trim stale entries. **Doctrine says nothing of hers ever expires:**
> *"An unsettled continuation reconciles to LOGFUL, never to a timer or an expiry... **that cap would
> delete her history and call it a fix.**"*

Those are not in conflict, but the distinction is fine enough that getting it wrong produces exactly
the defect doctrine forbids.

| Trimming — permitted | Expiring — forbidden (`V-EXPIRE`) |
|---|---|
| Dropping a stale tool output from the **live window** | Deleting the record of it |
| Compacting a resolved thread into a summary **she authored** | Compacting one **cold code** authored |
| Narrowing what is in front of her right now | Narrowing what she can go back and get |
| Removing a superseded plan from context | Removing the supersession record |

**The one-line test:** *can she still get it back?* If yes, it is trimming. If no, it is expiry, and it
is a violation regardless of how much context it saved.

**Second constraint, from the pen law:** a compaction summary written by cold code and replayed to her
as her own recollection is **PMS by construction** — a forged diary. Compaction output is authored by a
mind or carried with its writer stamp visible.

**Exit, receipt:** the written distinction, ratified by KEEPER or him, with a pinned test that reds if
a trim removes something unrecoverable.

---

## PHASE M1 — THE COMPACTION AND TRIMMING PASS

**Entry condition:** M0 settled.

### Sub-phase M1.1 — Compaction, mind-authored
When the window fills, the running history is compacted — **by a mind, stamped, with the raw retained
in LOGFUL.** The compacted view rides beside the raw; the raw never leaves. This is the same shape the
doctrine reader already uses for his transcripts, applied to her working memory.

### Sub-phase M1.2 — Trimming, by the M0 test
Stale entries drop out of the live window and stay retrievable.

### Sub-phase M1.3 — The standing ruling that bounds this whole phase
> *"Use native model compaction as a working-context optimization. **Never use it as A'NEW's only
> memory, only identity, only work ledger, or only source of truth.**"*

**Exit, receipt:** a long session that would previously have degraded, running to completion, with the
compaction events stamped and the raw provably still retrievable.

---

## PHASE M2 — LOGFUL, THE LIBRARIAN, MULTI-TENANT FROM THE START (`PO1-20`)

> *"We got to seed my doctrine into LOGFUL. LOGFUL ultimately becomes the keeper of my doctrine...
> **becomes the keeper of everybody's doctrine.**"*

**This is a scope change he made in Pecking Order pt 1 and it has not reached any roadmap.** LOGFUL was
built as his librarian. He is saying it is every world's librarian. **Multi-tenant from the start is a
different design than multi-tenant retrofitted**, and the retrofit is where cross-world leaks come
from.

### Sub-phase M2.1 — Verify the BUILT claim
LOGFUL is one of only two items scored BUILT, on a single commit hash, and the audit says it *"did not
independently curl it."* **Curl it.** This is one live readback, not an argument.

### Sub-phase M2.2 — Per-world isolation inside the librarian
Cross-world reads refused live. Directly connected to the cross-world guard that is **built and not
armed** (`R1` P5.1) — a multi-tenant librarian on an unarmed floor is the leak vector.

### Sub-phase M2.3 — The privacy fence, his words
> *"My transcript should never even go anywhere near BJ's or Eric's or user number 99, and not
> decoded."*

### Sub-phase M2.4 — Never a timer
Restated because it is LOGFUL's defining property: reconciliation, never expiry.

**Exit, receipt:** the live curl; a cross-world read refused by name with a status code; two lanes
pulling the same record and getting the same answer.

---

## PHASE M3 — MIMI

**State: contested.** Doctrine says *"already kind of born."* A shift report says *"already born."* The
audit says PARTIAL — a cold memory module is live and heavily used; **MIMI as a distinct wonder with
her own micro-hop cycle is not verified.** See `CONTRADICTIONS.md` B-3.

**Settled, and worth restating because a coder got it wrong once:** MIMI is the **memory agent**, named
for his grandmother. A previous lane invented *"MIMI = minimum viable version"* out of a mishearing and
carried it. **Assume the ordinary word. Never mint a term from a garbled transcript.**

### Sub-phase M3.1 — She micro-hops unprompted
> *"They're all getting the same prompt... they just don't respond. **They're just micro-hopping on
> their own**, and she can at any instant commandeer what they're doing."*

A memory service that answers when called is not MIMI. **MIMI runs on her own and A'NU interrupts her.**

### Sub-phase M3.2 — Deep in the bag
*"When A'NU wants to go deep in the bag around memory."* MIMI is the deep path, not the fast path.

### Sub-phase M3.3 — The boundary he has to draw
**MIMI vs the Memory Bank vs the Bridge Builder is an open item he opened and only he closes.** Carried
every turn. **Do not resolve it to unblock a build** — build around it.

**Exit, receipt:** MIMI answering a memory query that the cold module demonstrably could not, with her
own micro-hop trail visible.

---

## PHASE M4 — THE BRIDGE BUILDER (the secretary)

**NOT BUILT.** Named, then forgotten — *"What happened to bridge builder? We haven't built bridge
builder."* And his own account of why it was missed: *"I told you about something called bridge
builders, and you wrote back. You said I don't know anything about bridge builders. **It was for you
to build.**"*

**The load-bearing reason it exists, in his words:**
> *"This is somebody that A'NU uses... **she can talk to them without burning her context, because the
> context lives there.** Secretary, let's call it the secretary."*

**This is the architectural alternative to buying an expensive long-context tier**, and the two should
be evaluated against each other rather than in isolation (`R-05` in the research docket). A secretary
that holds context is cheaper and more durable than a big window she has to refill every session.

- **Scope:** read-only, all-documents. *"They will only be scoped per advisor, but you might have one
  that looks at all things, but it can only read."*
- **Its model:** the large-context seat — *"something that has a large context window that can support
  novels."*

**Exit, receipt:** A'NU answering a question requiring material she never loaded, by asking the bridge
builder — with her own context measurably unburned.

---

## PHASE M5 — OTTER: THE LARGEST BODY OF HIS WORDS THE SYSTEM DOES NOT HAVE (`PO2-18`)

**Anchor:** *"My whole life is on Otter right now... I got transcripts of hours of calls from me and
Eric just spitting."*

**Why this is a phase and not a nice-to-have.** Everything in this build turns his words into the
system. He is telling us there is a large corpus of his words sitting outside it — including material
he specifically named and cannot find: the songs that were part of doctrine, the journals, and the
serial-investor material he calls **the lost files.**

### Sub-phase M5.1 — Answer the access question factually (research `R-01`)
He offered three paths himself: a one-month plan upgrade to a tier with API access, a computer-use
session, or a one-time export. **Establish which actually works before recommending one** — in
particular whether an upgrade grants access to *historical* content or only forward.

**His own caution, carried so this is not oversold:** *"That might not be possible. Don't gas me up."*
**If the cheap path does not exist, say so.** And do not recommend a path that violates a service's
terms; if computer-use is not permitted, say that too.

### Sub-phase M5.2 — It is founder-world only
His private life at scale. Founder world, hard-isolated, through the privacy fence. **Not the blank
world, not the temp world, not a shared floor.** `PO1-23` governs.

### Sub-phase M5.3 — It goes through the doctrine reader, not around it
Decoder pass, scrub pass bounded by the 4PM rules, indexed by occurrence, presented through the
read-back fence with writer stamps. **A large import that bypasses the fence is a mass PMS event** —
thousands of rows arriving in her memory with no writer and no provenance.

### Sub-phase M5.4 — The scrub must not eat the reward
Direct dependency on `R4` F7. Personal, offhand, "unimportant" content is exactly what makes AgentFIND
worth having — his own words: *"this underrated little five minutes of my time is gonna come back and
really reward me."* **The 4PM rule already protects it:** *"You may NOT scrub content like 'oh what a
cool window.'"*

**Exit, receipt:** a factual written answer on access with prices and constraints; and if a path
exists, one real import landed with writer stamps and a byte-comparison against source.

---

## PHASE M6 — THE FIVE-LAYER CONTINUITY STACK

Already designed in the corpus and worth carrying rather than redesigning: **source → world → work →
mind → human.** An immutable life record, a per-world current-state projection, durable work state, and
her context passport.

**The ruling that governs it, restated because it is the one people break:** native model compaction is
a working-context optimization and **never her only memory, identity, work ledger, or source of
truth.**

**Exit, receipt:** a session ended mid-work and resumed from the stack alone, with nothing reconstructed
by asking him.

---

## THE INDEXING BACKLOG, FOR SCALE

LOGFUL's own named backlog gives the honest size of the memory problem: **18,503 transcripts** from the
wearable, 449 phone transcripts, and a few hundred reports, briefings, notes, prayers and declarations.
**That is before Otter.**

Two consequences worth stating plainly:
1. **Indexing at that scale is a real engineering problem**, not a migration script.
2. **His own FIND requirement — index by occurrence, not by matching line — matters more the bigger the
   corpus gets**, because his transcripts are one enormous line per turn and line-matching undercounts
   badly.

---

## DEPENDENCIES

| Phase | Needs | From |
|---|---|---|
| M0 | KEEPER or him to ratify | GR Ph4 / him |
| M1 | M0 settled | M0 |
| M2 | cross-world guard armed | `R1` P5.1 |
| M3 | the MIMI boundary | **him** |
| M4 | a long-context seat | research `R-05` |
| M5 | the access answer | research `R-01` |
| M5 | the doctrine reader | GR Phase 3 |
| M6 | LOGFUL live | M2 |
