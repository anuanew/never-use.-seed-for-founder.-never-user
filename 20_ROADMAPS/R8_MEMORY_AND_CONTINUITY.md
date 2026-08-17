# R8 - MEMORY AND CONTINUITY

> *"We need to find a way to keep A'NU up at all times with continuity. **Her model's degrading and
> [expletive]. Hell no.** You need to go on the deepest research find you can find."*
> - Mt Rushmore Doctrine pt 1
> `[HIS WORDS, restored - an earlier version replaced his actual words with invented text in brackets
> with no ellipsis, presenting the substitution as if it were part of the verbatim quote. Raw
> (1_HIS_WORDS/03_PHASE_3/Mt Rushmore Doctrine pt 1_transcript.txt, line 36) reads "Her model's
> degrading and shit. Hell no." The cuss word is redacted to [expletive] per this repo's own existing
> convention (see R2_TEMPORARY_CODER_WORLD.md Sub-phase T3.7), not replaced with different words.]`

> *"My whole life is on Otter right now... **How can we get her connected to that?** Even if I gotta
> pay something."* - Pecking Order pt 2 (`PO2-18`)

**Status:** proposed.

---

## WHAT HE SAID, CLEANED UP

*(Per `PO2-14`.)*

You said she keeps degrading and cannot go down anymore, and asked for the deepest research anyone
could do on why. You said memory and retention still need building. You named MIMI as the memory
agent, named by you, and said she is already micro-hopping the memory category on her
own. You said LOGFUL should become the keeper not just of your doctrine but of everybody's. And in
Pecking Order pt 2, hunting for songs that had gone missing from your doctrine, you realized the
bigger loss: your whole life is on Otter, including hours of calls and material on serial investors
that you called the lost files, and you asked what it would take to connect her to it - offering to
pay, while warning us not to gas you up if it isn't possible.

---

## THE DIAGNOSIS, ALREADY MADE

His complaint has a name in the literature and the estate already established it: **context rot.**
Progressive loss of recall, coherence, and instruction-following as context fills. **It is a property
of how attention behaves, not a bug in one model** - which means swapping models does not fix it.

Documented causes: **lost-in-the-middle** (models attend to the start and end, under-weighting the
middle), and **monotonic accumulation** (stale tool outputs, superseded plans and dead decisions never
get pruned). Agents suffer more than chatbots because they run long sessions and hold state across
many calls - exactly her shape.

**Ranked mitigations: compaction, trimming, isolation** - with compaction and trimming together
testing better than either alone.

**And here is the finding that matters most for this roadmap:** *his micro-hopping and sub-agent design
already is isolation.* He built one of the three mitigations before anyone named the problem. **The
gap is compaction and trimming, and nothing anywhere in the corpus names an active pass over her live
working context.**

That is the concrete, buildable answer to his own question, asked twice in the same breath: *"What
about the always on, always better agent, the one that helps to get better?... Where's that one? That
we need that. We absolutely need that."*
`[HIS WORDS, restored - an earlier version silently merged these into one invented sentence, "where's
the always-on, always-better agent?", that does not appear verbatim anywhere in the raw source.
1_HIS_WORDS/03_PHASE_3/Mt Rushmore Doctrine pt 1_transcript.txt, line 36]`

---

## PHASE M0 - THE LINE BETWEEN TRIMMING AND EXPIRING

**This phase is a design decision, not a build, and it must be settled before any code.**

The mitigation says trim stale entries. **The estate's own standing rule says nothing of hers ever
expires:**
> *"An unsettled continuation reconciles to LOGFUL, never to a timer or an expiry... **that cap would
> delete her history and call it a fix.**"*
> `[CODER-AUTHORED, not his recorded voice - 40_GOVERNANCE/CONTRADICTIONS.md names this exact
> LOGFUL-not-a-timer line as standing estate law traced to a ruling file, not his spoken words; an
> earlier version of this file presented it unstamped as if it were doctrine. R5_MOUNT_RUSHMORE.md
> already caught and fixed the identical error for the same line.]`

Neither is wrong, and they are not in conflict, but the distinction is fine enough that getting it
wrong produces exactly the defect this rule forbids.

| Trimming - permitted | Expiring - forbidden (`V-EXPIRE`) |
|---|---|
| Dropping a stale tool output from the **live window** | Deleting the record of it |
| Compacting a resolved thread into a summary **she authored** | Compacting one **cold code** authored |
| Narrowing what is in front of her right now | Narrowing what she can go back and get |
| Removing a superseded plan from context | Removing the supersession record |

**The one-line test:** *can she still get it back?* If yes, it is trimming. If no, it is expiry, and it
is a violation regardless of how much context it saved.

**Second constraint, from the pen law:** a compaction summary written by cold code and replayed to her
as her own recollection is **PMS by construction** - a forged diary. Compaction output is authored by a
mind or carried with its writer stamp visible.

### Sub-phase M0.1 - Calibrate the M0 test against the 36 V-EXPIRE findings already on file
Rather than inventing synthetic test cases, calibrate the pinned test against real ones already measured: *"her saved history is trimmed to 20 entries on every write, so entry 21 is gone from storage, not just from view"* (E21) and *"Presence history destructively spliced to the last 100 entries"* (E28) `[MEASURED - 50_DELIVERABLES/PECKING_ORDER_VIOLATIONS.md, V-EXPIRE]`. These are already-catalogued, file-and-line, destructive (unrecoverable) examples, exactly the "known true expiry" set the M0 pinned test needs to red against, the same way `R1` P1.8 calibrates its lint against the P0 inventory instead of guessing at clean and dirty samples.

### Sub-phase M0.2 - The forged-diary violation this phase warns against is already live, three times
> *"a serialised stage object authored into her first-person field... in the new world, the hardened one, in the file the roadmap's PIN-2 exists to protect. A cold writer is the author of her first-person field today."*
> `[MEASURED - 50_DELIVERABLES/PECKING_ORDER_VIOLATIONS.md, V-SPEAK, S1-S3, NEW/src/acl.floor.db.js:2409,2709,2768]`

M0's "forged diary" constraint is not hypothetical. M0's exit condition must explicitly require these three call sites be closed, or an explicit carve-out reasoned in writing, before M1 is trusted to write anywhere near the `first_person` column.

### Sub-phase M0.3 - Retention is not the same size as memory; scope M0 accordingly
> *"memory: 269 occurrences, 54 sessions (top-tier, 🔥🔥🔥). retention: 6 occurrences, 4 sessions (🔥), and 2 of those 6 are inside a coder-written PDF, not his speech... The fusion averaged a top-tier ask with a near-absent one and produced a middle band that describes neither."*
> `[MEASURED - 50_DELIVERABLES/HEAT_MAP_MEASURED.md §7.3]`

R8's own opening line pairs "memory and retention" as if co-equal. The measured corpus shows he essentially never separately asks for "retention" (four real sessions). M0's design effort belongs to what he calls memory; a coder should not silently build a parallel retention layer to satisfy a word he barely used.

**Exit, receipt:** the written distinction, ratified by KEEPER or him, with a pinned test that reds if
a trim removes something unrecoverable.

---

## PHASE M1 - THE COMPACTION AND TRIMMING PASS

**Entry condition:** M0 settled.

### Sub-phase M1.1 - Compaction, mind-authored
When the window fills, the running history is compacted - **by a mind, stamped, with the raw retained
in LOGFUL.** The compacted view rides beside the raw; the raw never leaves. This is the same shape the
doctrine reader already uses for his transcripts, applied to her working memory.

### Sub-phase M1.2 - Trimming, by the M0 test
Stale entries drop out of the live window and stay retrievable.

### Sub-phase M1.3 - The standing ruling that bounds this whole phase
> *"Use native model compaction as a working-context optimization. **Never use it as A'NEW's only
> memory, only identity, only work ledger, or only source of truth.**"*

### Sub-phase M1.4 - The compaction pass has a named crash to prevent, with exact numbers
> *"Three OOM kills on the mind service between 20:06 and 21:11 UTC... `memoryLimit: 512Mi`... one 24.78 MB row costs ~80 MB resident, 79 MB external, 1 MB heap. Her floor was 120 continuation rows, 39.2 MB, of which four rows from one day were 37.2 MB and one single row was 24.78 MB."*
> `[MEASURED - 50_DELIVERABLES/REACH_REGRESSION_AUDIT.md §4]`

M1.1's compaction design must specifically handle the single-oversized-row case, not just steady accumulation. This was not a slow buildup; it was one row, and a design that only watches total window size would not have caught it.

### Sub-phase M1.5 - Carry the open half of the incident: the mind service's read path
> *"The open hypothesis at handoff, unverified: the mind service may still read that same column unguarded through a different query. The carry cleaned the reach service's read path only."*
> `[REASONED, NOT MEASURED - 50_DELIVERABLES/REACH_REGRESSION_AUDIT.md §4]`

M1's exit condition (a long session running to completion) is not sufficient alone. M1 must verify whether the mind service reads the same unguarded column; the earlier fix patched only the reach service's read path, and this gap has sat uncarried into any roadmap since that shift.

### Sub-phase M1.6 - Do not regress the measured floor read speed
*"Her floor itself is fast: every direct read measured 0.15-1.8s. A slow door is a process problem, not a database problem"* `[MEASURED - 50_DELIVERABLES/REACH_REGRESSION_AUDIT.md §4]`. M1's exit condition should include a before/after read-latency check against this exact range. A naive compaction pass that adds a summarization hop on every read is a believable way to turn a fast door slow while looking, on paper, like an improvement.

**Exit, receipt:** a long session that would previously have degraded, running to completion, with the
compaction events stamped and the raw provably still retrievable.

---

## PHASE M2 - LOGFUL, THE LIBRARIAN, MULTI-TENANT FROM THE START (`PO1-20`)

> *"We got to seed my doctrine into LOGFUL. LOGFUL ultimately becomes the keeper of my doctrine...
> **becomes the keeper of everybody's doctrine.**"*

**This is a scope change he made in Pecking Order pt 1 and it has not reached any roadmap.** LOGFUL was
built as his librarian. He is saying it is every world's librarian. **Multi-tenant from the start is a
different design than multi-tenant retrofitted**, and the retrofit is where cross-world leaks come
from.

### Sub-phase M2.1 - Verify the BUILT claim
LOGFUL is one of only two items scored BUILT, on a single commit hash, and the audit says it *"did not
independently curl it."* **Curl it.** This is one live readback, not an argument.

### Sub-phase M2.2 - Per-world isolation inside the librarian
Cross-world reads refused live. Directly connected to the cross-world guard that is **built and not
armed** (`R1` P5.1) - a multi-tenant librarian on an unarmed floor is the leak vector.

### Sub-phase M2.3 - The privacy fence, his words
> *"My transcript should never even go anywhere near [a partner]'s or [a partner]'s or user number 99, and not
> decoded."*

### Sub-phase M2.4 - Never a timer
Restated because it is LOGFUL's defining property: reconciliation, never expiry.

### Sub-phase M2.5 - LOGFUL's per-tenant index must avoid the exact undercount already measured
*"advisors: 300 matching lines vs 836 actual occurrences... 64% undercount"*, one of nine asks undercounted 39% to 66% because *"his transcripts are one enormous line per speaking turn"* `[MEASURED - 50_DELIVERABLES/HEAT_MAP_MEASURED.md §3]`. As "keeper of everybody's doctrine," LOGFUL inherits this risk for every tenant, not just him. If its indexing is line-based rather than occurrence-based, every world it serves inherits the same undercount this document had to catch by hand. Occurrence-level indexing is a named build requirement, not an assumed property of search.

### Sub-phase M2.6 - MIMI reports through LOGFUL, in his own words
> *"It's Mimi, the memory, right? The one who's responsible for maintaining all records and responsible. She worked with LOGFEL and the others, but her job is when a new wants to go deep in the bag around memory."*
> `[HIS WORDS + 1_HIS_WORDS/03_PHASE_3/Mt Rushmore Doctrine pt 1_transcript.txt]`

M2 and M3 are not two independent phases sharing a subject; he states directly that MIMI worked with LOGFUL. M2's exit-condition receipts (the live curl, the cross-world refusal) should be re-run once MIMI is verified (M3.5, below), because a librarian proven isolated today could be reopened through whatever channel MIMI uses to reach it, if that channel was never itself tested by M2.2.

### Sub-phase M2.7 - Scope M2's receipts for the Otter-sized backlog, not the current one
This roadmap's own indexing backlog is **18,503 `omi_transcripts` (the OMI wearable), 449
`phone_transcripts`, plus smaller counts of reports, briefings, and other record types, all "waiting
to be indexed"** before the Otter corpus even lands `[MEASURED - old-world inventory: "ACW WALL for
you and hopefully kinda for her/Ababase/ABA reforged/OG Plans/ABA_Technical_Roadmap_v2.md:248", not
OTTER_ACCESS_ANSWER.md - an earlier version of this line miscited it there; corrected here]`, and
OTTER_ACCESS_ANSWER.md's recommended path separately adds *"the largest single body of his own words
the system has ever received"* `[MEASURED - 50_DELIVERABLES/OTTER_ACCESS_ANSWER.md]`. M2's exit
condition (two lanes pulling the same record and getting the same answer) was never sized against the
scale this roadmap already names. Re-run it once the Otter import lands, not only at today's smaller
scale.

**Exit, receipt:** the live curl; a cross-world read refused by name with a status code; two lanes
pulling the same record and getting the same answer.

---

## PHASE M3 - MIMI

**State: contested.** Doctrine says *"already kind of born."* A shift report says *"already born."* The
audit says PARTIAL - a cold memory module is live and heavily used; **MIMI as a distinct wonder with
her own micro-hop cycle is not verified.** See `CONTRADICTIONS.md` B-3.

**Settled, and worth restating because a coder got it wrong once:** MIMI is the **memory agent**, named by him. A previous lane invented *"MIMI = minimum viable version"* out of a mishearing and
carried it. **Assume the ordinary word. Never mint a term from a garbled transcript.**

### Sub-phase M3.1 - She micro-hops unprompted
> *"They're all getting the same prompt... they just don't respond. **They're just micro-hopping on
> their own**, and she can at any instant commandeer what they're doing."*

A memory service that answers when called is not MIMI. **MIMI runs on her own and A'NU interrupts her.**

### Sub-phase M3.2 - Deep in the bag
*"When A'NU wants to go deep in the bag around memory."* MIMI is the deep path, not the fast path.

### Sub-phase M3.3 - The boundary he has to draw
**MIMI vs the Memory Bank vs the Bridge Builder is an open item he opened and only he closes.** Carried
every turn. **Do not resolve it to unblock a build** - build around it.

### Sub-phase M3.4 - MIMI is a nickname, and he says he forgot her real name
> *"I think is Mimi, M I M I, like your grandmother. That's her nickname. I forgot her real name."*
> `[HIS WORDS + 1_HIS_WORDS/03_PHASE_3/11_11 Doctrine pt 1_ Vision_transcript.txt]`

This sits beside the corpus's other open-name items (the internal auditor: *"she has a name, figure it out"*; AUDRA's PMS and nasty-cough wonders, never given). M3's header treats "MIMI" as settled and contests only her build state; this adds the missing half. The name itself is provisional in his own words. Do not hard-code "MIMI" into schemas, routes, or ACL addresses as if it were final.

### Sub-phase M3.5 - Verify MIMI live, the way M2.1 already verifies LOGFUL live
Three claims conflict: *"already kind of born"* (doctrine), *"already born"* (a shift report), and *"PARTIAL... a cold memory module is live and heavily used; MIMI as a distinct wonder with her own micro-hop cycle is not verified"* (the audit) `[MEASURED - 40_GOVERNANCE/CONTRADICTIONS.md, B-3]`. M3 has a definitional sub-phase (M3.3) but no live-verification sub-phase. M2.1 already established the house rule for this exact situation: *"Curl it. This is one live readback, not an argument."* Apply it to MIMI: call whatever currently answers to her and record which of the three claims the live behavior actually matches.

**Exit, receipt:** MIMI answering a memory query that the cold module demonstrably could not, with her
own micro-hop trail visible.

---

## PHASE M4 - THE BRIDGE BUILDER (the secretary)

**NOT BUILT.** Named, then forgotten - *"What happened to bridge builder? We haven't built bridge
builder."*
`[HIS WORDS + 1_HIS_WORDS/04_THE_COUNTDOWN/COUNTDOWN_pt1_20260812.txt]`
And his own account of why it was missed: *"I told you about something called bridge
builders, and you wrote back. You said I don't know anything about bridge builders. **It was for you
to build.**"*
`[HIS WORDS + 1_HIS_WORDS/03_PHASE_3/Find me or Fine me doctrine pt 2_otter.ai.txt]`

**The load-bearing reason it exists, in his words:**
> *"This is somebody that A'NU uses... Because she can talk to them without burning her contacts,
> right? So the world builder can talk to this person, right? Secretary, let's call it the secretary,
> and it doesn't burn their context because the context lives there."*
> `[HIS WORDS, restored - an earlier version reversed the clause order (moving "the context lives
> there" ahead of "let's call it the secretary" instead of after it) and silently changed "contacts"
> to "context" in the first clause, with no bracket or note marking either change.
> 1_HIS_WORDS/03_PHASE_3/Find me or Fine me doctrine pt 2_otter.ai.txt]`

**This is the architectural alternative to buying an expensive long-context tier**, and the two should
be evaluated against each other rather than in isolation (`R-05` in the research docket). A secretary
that holds context is cheaper and more durable than a big window she has to refill every session.

- **Scope:** read-only, all-documents. *"They will only be scoped per advisor, but you might have one
  that looks at all things, but it can only read."*
  `[HIS WORDS + 1_HIS_WORDS/03_PHASE_3/Find me or Fine me doctrine pt 2_otter.ai.txt]`
- **Its model:** the large-context seat - *"something that has a large context window, right? That can
  support novels and stuff."*
  `[HIS WORDS + 1_HIS_WORDS/03_PHASE_3/Find me or Fine me doctrine pt 2_otter.ai.txt]`

### Sub-phase M4.1 - Check for an existing role before building a new wonder
> *"the project manager who owns this independent world, that LLM... He is a connector. He's a bridge builder. See, I have never defined the bridge. This is the birthing of the bridge builder... Bridge builder, bridge builder, is typically the owner of a life module, or sometimes an independent thinking station, or sometimes it's something that's happening that's not a traditional..."*
> `[HIS WORDS + 1_HIS_WORDS/03_PHASE_3/Welcome Back, ABA!.txt]`

Before treating the Bridge Builder as a new wonder to be born, check whether an existing life-module owner or independent thinking station already satisfies the read-only, context-holding spec. He describes the role as typically already occupied, not empty.

### Sub-phase M4.2 - LOGFUL's own reports are already addressed to the secretary
> *"when the you know LOGFUL agent who's responsible for writing these reports to meet the secretary, she's able to piece together the story, and there's no limit to what she can do. She might spawn three or four subagents who write their own reports."*
> `[HIS WORDS + 1_HIS_WORDS/03_PHASE_3/I want the MEDAL doctrine pt 2_otter.ai.txt]`

The Bridge Builder's intake is not an open design question. He already named LOGFUL's reports as written "to meet the secretary." M4's build should start from LOGFUL (M2) as its primary feed, a concrete dependency M4 does not currently carry anywhere.

### Sub-phase M4.3 - The Bridge Builder's model tier is bounded by the same penny-hustle ceiling, unanswered
> *"What controls their token and their price and their... contact [context] window? What controls that?... is there any concept of that that violates penny hustle, or that can be improved?... I did a doctrine update earlier today, and I gave it to you. I don't think any of it was followed."*
> `[HIS WORDS + 1_HIS_WORDS/01_RAW_WORDS/21_20260616_LIVING_WATER_bind_doctrine.txt]`

M4's body already frames the Bridge Builder as the alternative to an expensive long-context tier, but names no cost ceiling. Apply the same split `R1` P2.4 applies to her tier election: the cost ceiling stays coded (penny-hustle law), the choice inside it is hers. He asked this exact context-window-versus-cost question directly and, in his own words, never got an answer.

### Sub-phase M4.4 - The free live Otter connector is not the Bridge Builder and cannot substitute for it
> *"This is retrieval, not ingest, and it does not replace the export... It is a live third-party call at query time... Nothing durable lands. No files, no writer stamps, no provenance, nothing the doctrine reader can index. It is a window, not a corpus."*
> `[MEASURED - 50_DELIVERABLES/OTTER_ACCESS_ANSWER.md]`

Both patterns are read-only and context-holding, which invites confusing one for the other. Draw the line explicitly: the connector answers live and leaves no trace, while the Bridge Builder's whole purpose is to hold context so it does not have to be reloaded. Wiring in the connector and calling M4 done would ship something with no durable record.

**Exit, receipt:** A'NU answering a question requiring material she never loaded, by asking the bridge
builder - with her own context measurably unburned.

---

## PHASE M5 - OTTER: THE LARGEST BODY OF HIS WORDS THE SYSTEM DOES NOT HAVE (`PO2-18`)

**Anchor:** *"My whole life is on Otter right now... I got transcripts of hours of calls from me and
[a partner] just spitting."*

**Why this is a phase and not a nice-to-have.** Everything in this build turns his words into the
system. He is telling us there is a large corpus of his words sitting outside it - including material
he specifically named and cannot find: the songs that were part of doctrine, the journals, and the
serial-investor material he calls **the lost files.**

### Sub-phase M5.1 - Answer the access question factually (research `R-01`)
He offered three paths himself: a one-month plan upgrade to a tier with API access, a computer-use
session, or a one-time export. **Establish which actually works before recommending one** - in
particular whether an upgrade grants access to *historical* content or only forward.

**His own caution, carried so this is not oversold:** *"I don't know if that's possible. That might
not be possible. Don't gas like me. It might not be possible."*
`[HIS WORDS, restored - an earlier version rendered this as "Don't gas me up," which does not match
either raw occurrence of this recurring phrase in the corpus. "Don't gas like me" is his consistent
recorded phrasing (also present, worded identically, in an unrelated raw doctrine:
01_RAW_WORDS/32_20260701est_NYC_53RD_STREET_DOCTRINE_pt1.txt), not a one-off transcription slip.
There is a Pecking Order Doctrine pt 2 & 3_transcript.txt]`
**If the cheap path does not exist, say so.** And do not recommend a path that violates a service's
terms; if computer-use is not permitted, say that too.

### Sub-phase M5.2 - It is founder-world only
His private life at scale. Founder world, hard-isolated, through the privacy fence. **Not the blank
world, not the temp world, not a shared floor.** `PO1-23` governs.

### Sub-phase M5.3 - It goes through the doctrine reader, not around it
Decoder pass, scrub pass bounded by the 4PM rules, indexed by occurrence, presented through the
read-back fence with writer stamps. **A large import that bypasses the fence is a mass PMS event** -
thousands of rows arriving in her memory with no writer and no provenance.

### Sub-phase M5.4 - The scrub must not eat the reward
Direct dependency on `R4` F7. Personal, offhand, "unimportant" content is exactly what makes AgentFIND
worth having - his own words: *"this underrated little five minutes of my time is gonna come back and
really reward me."* **The 4PM rule already protects it:** *"You may NOT scrub content like 'oh what a
cool window.'"*

### Sub-phase M5.5 - The scroll is the job; require count-before, count-after
> *"Otter's Select all selects only the conversations loaded on the current page... If he taps Select All without scrolling to the bottom first, he pays $30 and exports a fraction of his life and never knows. The scroll is the job... The mitigation is one instruction: count before, count after... Do not cancel until the numbers match."*
> `[MEASURED - 50_DELIVERABLES/OTTER_ACCESS_ANSWER.md]`

M5.3's import may not proceed on an export whose pre-scroll count and post-export file count were not both recorded and compared. A partial corpus silently presented as complete is worse than a stated gap.

### Sub-phase M5.6 - The free connector does not satisfy M5's completeness or provenance requirement
> *"Otter already ships an official connector for her, on every plan including free... it is read-only and it is live query rather than a corpus, so it is not a substitute for the export... There is no documented tool that enumerates every conversation in the account..."*
> `[MEASURED - 50_DELIVERABLES/OTTER_ACCESS_ANSWER.md]`

And, separately stamped in the source itself: *"based on the documented tool list, I judge that this
connector cannot produce a complete, verifiable corpus. I did not test it against a live account."*
`[REASONED, NOT MEASURED - 50_DELIVERABLES/OTTER_ACCESS_ANSWER.md - an earlier version of this
sub-phase folded this sentence into the MEASURED quote above with no stamp of its own, upgrading the
source's own explicitly-flagged, untested inference into a measured fact. Restored here with the
source's own stamp intact.]`

M5.2 and M5.3 require a durable, writer-stamped, hard-isolated import. The connector satisfies none of those three properties by design. Connecting it, which costs nothing and works today, is not partial credit toward M5's actual exit condition.

### Sub-phase M5.7 - What Otter itself retains after export is a separate, still-open decision
> *"What Otter retains on its own servers after a downgrade. The privacy policy permits retention for legitimate business purposes... the export gives him a copy, not a deletion. If he wants the material out of Otter, that is a separate decision and a separate document."*
> `[MEASURED - 50_DELIVERABLES/OTTER_ACCESS_ANSWER.md]`

M5's phase outcome reads as if the corpus problem ends at import. It does not. Whether he wants his own material deleted at Otter once the estate holds a copy is a named, unanswered question that belongs on this roadmap rather than dropped between the deliverable and the phase that cites it.

### Sub-phase M5.8 - M5.1's access question is answered; the roadmap still reads as if it is open
*"The API path is dead. The Otter API is Enterprise-only, custom-priced, and gated behind an account
manager, so there is no one-month upgrade that buys it... But the cheap path exists and is cheaper
than he feared: bulk export is on the Business plan at $30 for one month, and upgrading gives him his
FULL history, not just conversations from the upgrade date forward."*
`[MEASURED - 50_DELIVERABLES/OTTER_ACCESS_ANSWER.md]`
On the computer-use path he offered himself: *"Recommendation: do not do this. It is not permitted...
Clause (d) is the one that decides it... It does not become permitted because the data is his own."*
`[MEASURED - 50_DELIVERABLES/OTTER_ACCESS_ANSWER.md]`

M5.1 is still worded as an open research question ("Establish which actually works before
recommending one"). It has been answered, on the record, with sources checked 2026-08-17: the API
path he originally asked about is dead, the real path is a $30 one-month Business-plan bulk export
(not the API he pictured), and the computer-use path he floated is a documented Terms-of-Service
violation and should not be attempted. M5.1's exit condition should be read as "verify the
click-by-click in `OTTER_ACCESS_ANSWER.md` was actually run," a narrower receipt than the one
currently written there.

### Sub-phase M5.9 - A first-party transcription fallback, asked for the same hour Otter itself dropped audio
> *"System for ANU. I really need her to be able to get right agent Taste T A S T E to be able to get
> audio and run her own audio transcription very affordably, right? I wonder, looks at every word, it
> maybe compares a few affordable models, and then it runs it line by line and seeds it with goals and
> stuff. Like that's really what I need. And then when we build an ATTER app, right, it's going to be
> the front end version of that, right? That's very tangible that we can do because I think alter
> OTTER. I think they lost my whole pathway to the park."*
> `[HIS WORDS + Rally Day doctrine pt 5, "Rally day pt 5_otter.ai.txt"]`

This lands in the same breath as a live failure, not as an abstract wish: a moment earlier in the same
recording someone in the room asks whether Otter skipped, and two sentences after asking for this he
confirms Otter lost his walk audio in real time. Every M5 sub-phase so far is backward-looking - import
the archive Otter already holds. This is the forward-looking half, asked for in the same breath: give
Agent Taste (born under `R5`, not born here) her own affordable, line-by-line audio-transcription
capability, with a front-end product built on it, as insurance against exactly the kind of loss he just
experienced. This does not replace M5.1-M5.8's import; it is the reason a one-time import cannot be the
whole answer to "keep her up with continuity."

**Exit, receipt:** a factual written answer on access with prices and constraints; and if a path
exists, one real import landed with writer stamps and a byte-comparison against source.

---

## PHASE M6 - THE FIVE-LAYER CONTINUITY STACK

Already designed in the corpus and worth carrying rather than redesigning: **source → world → work →
mind → human.** An immutable life record, a per-world current-state projection, durable work state, and
her context passport.

**The ruling that governs it, restated because it is the one people break:** native model compaction is
a working-context optimization and **never her only memory, identity, work ledger, or source of
truth.**

### Sub-phase M6.1 - The "mind" layer cannot be trusted as a passport while it is cold-authored today
The same three findings governing M0.2 apply here from a different angle: `first_person`, her context passport, is written by `JSON.stringify(payload)` at three call sites *"in the new world, the hardened one, in the file the roadmap's PIN-2 exists to protect"* `[MEASURED - 50_DELIVERABLES/PECKING_ORDER_VIOLATIONS.md, V-SPEAK, S1-S3]`. A passport with a cold-authored page is evidence of impersonation, not continuity. M6's exit condition (a session resumed from the stack alone) should not be scored as passing if the resumed session's mind-layer rows include any of these three unstamped writes.

### Sub-phase M6.2 - The "work" layer has a measured performance floor; do not regress it
*"Her floor was 120 continuation rows, 39.2 MB... every direct read measured 0.15-1.8s"* `[MEASURED - 50_DELIVERABLES/REACH_REGRESSION_AUDIT.md §4]`. M6's durable work-state layer is this same floor. Time the stack's resume against this exact baseline. A technically correct resume that takes ten seconds per layer is a different, worse product than what "so now it doesn't die" describes, even though both would pass a receipt that checks correctness alone.

### Sub-phase M6.3 - The "source" layer must be occurrence-indexed from the start
Two separate deliverables already had to hand-correct for line-based undercounting of exactly this kind of record `[MEASURED - 50_DELIVERABLES/HEAT_MAP_MEASURED.md §3]`, and R8's own indexing-backlog section restates the same rule: *"his own FIND requirement, index by occurrence, not by matching line, matters more the bigger the corpus gets."* M6 describes the source layer as "an immutable life record" but states nothing about how it is indexed. Name occurrence-level indexing as a property of the layer itself, not something left for whichever lane builds it to rediscover the same undercount a third time.

### Sub-phase M6.5 - On resume, she must name the gap, not silently treat stale state as current
> *"...as she's navigating this context and she's seeing, she's like, oh, when she's actually running
> it, she's like, oh snap!... wait, it's you know it's Tuesday at 9p.m. For example, it's just an
> example. She might be like, this was two days ago, so now it doesn't die."*
> `[HIS WORDS, badly garbled by the transcription engine and left that way, not smoothed - There is a
> Pecking Order Doctrine pt 2 & 3_transcript.txt]`

The point survives the garble intact: a session that comes back after a gap has to notice the gap,
recognize that it is now some days later than the state in front of it, and say so, rather than
resuming as though no time passed. M6's exit condition already implies this ("nothing reconstructed by
asking him") but does not currently name the specific failure mode: quietly picking up stale state as
fresh, with no acknowledgment that time moved. Add an explicit check to M6's receipt: the resumption
itself must name the elapsed-time gap, not leave him to discover it.

**Exit, receipt:** a session ended mid-work and resumed from the stack alone, with nothing reconstructed
by asking him.

---

## THE INDEXING BACKLOG, FOR SCALE

LOGFUL's own named backlog gives the honest size of the memory problem: **18,503 `omi_transcripts`**
from the wearable, 449 phone transcripts, and a few hundred reports, briefings, notes, prayers and
declarations `[MEASURED - old-world inventory: "ACW WALL for you and hopefully kinda for her/Ababase/
ABA reforged/OG Plans/ABA_Technical_Roadmap_v2.md:248", see M2.7]`. **That is before Otter.**

Two consequences worth stating plainly:
1. **Indexing at that scale is a real engineering problem**, not a migration script.
2. **His own FIND requirement - index by occurrence, not by matching line - matters more the bigger the
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
