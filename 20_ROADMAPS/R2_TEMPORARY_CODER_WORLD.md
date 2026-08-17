# R2 - THE TEMPORARY CODER WORLD

**Governing doctrine:** Pecking Order pt 2 (20260816 21:30 EST), `PO2-01` through `PO2-04`, `PO2-08`,
`PO2-20`. Supported by Pecking Order pt 1 `PO1-11` and the standing `TEMP_CODER_STANDUP` guidance.
**Status:** proposed. Not built.

---

## WHAT HE SAID, CLEANED UP

*(Per `PO2-14`.)*

On Sunday night you said that when the estate builds the temporary coding OS
- what temp coders get and what they are responsible for - they need to be **hooked in as world
builders**, and you asked for that to be unpacked and built out. Then you went further and said you
want an actual **temporary coder world**: a place they read from, where they learn what to do, how to
play, and which agents they are allowed to control. You said they should have their own roadmap when
they get there and their own rules for how they talk to you. You said they are world builders like
her but outside, that you don't own them, and that all you ask is that they don't PMS and don't nasty
cough. Their job is to help you build and train her up. And you said the riddles could be the
curriculum - and, a minute later, that the riddles are how you catch an imposter.

---

## THE THESIS, AND THE HONEST TENSION IN IT

He is asking for something unusual and it is worth naming plainly, because it determines whether this
is buildable.

**He is not asking for better prompts.** He is asking whether an outside LLM session, given standing,
a curriculum, and a role, will actually *take up that role* rather than behave like a tool being
operated. He asked this himself, in the same breath as the design:

> *"I want to build out a world. **Is this possible? Will the LLMs actually even participate in
> this?**"* (`PO2-22`)

That is the correct question and it is the first thing this roadmap has to answer, before any of it
is built. The answer is not obvious and should not be asserted. It is Phase T0.

**The second tension, stated plainly:** the entire value of a temp coder world is that it makes temp
coders *better*. But he also said the measure of success is **needing fewer of them** (`PO2-05`). So
this roadmap is deliberately building a thing designed to be dismantled. Every phase below is scoped
so that the work survives the temp coders' departure - the curriculum becomes her onboarding material,
the queue becomes her coding department's intake, the riddles become the imposter test for any
session. **Nothing here is built only for temp coders.** If it were, it would be waste by design.

---

## PHASE T0 - DOES IT WORK AT ALL? (the honest precondition)

**Anchor:** *"Is this possible? Will the LLMs actually even participate in this?"* (`PO2-22`)

**Outcome:** a factual, measured answer to his question, produced before the world is built.

**Entry condition:** none.

### Sub-phase T0.1 - The participation test
Take one real roadmap row. Give it to three outside sessions across at least two providers (per his
own baseline: Claude and ChatGPT). Give each the full world-builder framing - standing, rules, the
agent roster, the curriculum draft - and nothing else. **Measure whether they behave as builders or
as tools.**

Concrete, falsifiable markers of *builder* behavior, decided in advance so the result cannot be
rationalized after the fact:
- acts on a bounded reversible thing without asking permission first,
- carries a receipt without being told to,
- refuses something out of scope by naming the rule,
- convenes another model or session rather than guessing (`PO2-04`),
- files into the queue instead of reporting back to a human.

Markers of *tool* behavior: asks which option he prefers (**a menu - the named failure**), waits for
approval on reversible work, produces a plan instead of an act, claims completion without a receipt.

### Sub-phase T0.2 - Report the answer honestly, including if it is no
If outside sessions do not take up the standing, **that is the finding** and the world gets scoped
down to what does work (a rulebook and a queue) rather than built as designed. Saying "yes it works"
because it is the nicer answer is exactly the false choice he has banned.

### Sub-phase T0.3 - Calibrate the markers before trusting a result
The five builder-markers and four tool-markers in T0.1 were picked by reasoning, not tested - the same
shape that failed elsewhere in this estate: *"22 of them are measurable... Of those 22: 4 were right,
1 was half right, and 17 were wrong"* `[MEASURED - 50_DELIVERABLES/HEAT_MAP_MEASURED.md]`, describing
bands assigned by reasoning rather than counting. Before scoring the three real sessions, run the same
markers against one transcript already known to show tool behavior and one already known to show
builder behavior, and confirm the markers actually discriminate. A marker set never shown to
distinguish anything is not a test, it is a hope.

### Sub-phase T0.4 - Fix the roadmap row and the prompt before the session starts
T0.1 says "take one real roadmap row" but not how the row is chosen. An easy row picked after the fact
can manufacture builder behavior by accident. Publish the exact row, the exact framing text, and the
exact pass and fail wording before any session is opened, not after reading its transcript.
`[MEASURED - 50_DELIVERABLES/HEAT_MAP_MEASURED.md, "A count with no stated filter is not a receipt"]`

**Exit condition, receipt:** a written result naming each session, each provider, each marker hit or
missed, with transcript pointers. A number, not an impression.

---

## PHASE T1 - WHERE THE WORLD LIVES (blocked on him)

**Anchor, and the contradiction:** he said *"a portion on my Supabase, of course, on the founder's
world"* (`PO2-01`). Three hours earlier he said *"I ain't taking that risk for my world. Nobody access
that information"* (`PO1-23`). The standing coder guidance says a separate Supabase, separate Render,
separate repo, separate world id.

**This is `OPEN-C1` and it is his to close.** Both readings are defensible and they lead to different
builds.

### The two readings, laid out for his decision

**Reading A - separate estate (current working posture).**
The temp world is its own Supabase, Render, repo, and world id. *"They're reading from it"* is
satisfied by a **read-only projection** of the roadmap into the temp estate. Nothing crosses back
except proven work.
- *For:* preserves `PO1-23` exactly. Preserves the credential-absence design, where a temp container
  structurally cannot reach his mailbox, cannot send, and holds no founder identity - enforced by the
  variable not existing rather than by a rule a coder reads.
- *Against:* projection means a sync mechanism, which is a thing that can be wrong. Two estates cost
  more.

**Reading B - a partition of the founder Supabase.**
A schema/RLS-scoped section of his own project.
- *For:* it is literally what he said, and there is only one source of truth.
- *Against:* it puts temp coders on the founder floor, which is the exact posture the last shift
  measured as dangerous - a temp container held live send credentials for hours, and *"the only thing
  preventing it was a coder reading a rule."* It also collides with `PO1-23`.

**Working posture until he answers: Reading A.** It is the reversible choice - a separate estate can
be merged into his later; a founder-floor partition cannot be un-mixed once temp coders have written
to it. **This is a coder's reading, marked as one, and one sentence from him overrules it.**

### Sub-phase T1.1 - The account clicks (his, and only his)
Four clicks and a token, already specified in the standing standup guidance and not restated here.
These mint credentials, which is one of the few things doctrine reserves to him. Everything after is a
coder's.

### Sub-phase T1.2 - The var group: absence as the design
Names only, never values. The design principle, stated as a principle because it is the whole point:
**a key that is not in the container cannot be misused by a session that has gone wrong, cannot leak
in a stack trace, and cannot be talked out of a coder by a clever prompt.** Every "cannot" is enforced
by non-existence, not by a sentence in a document.

Explicitly absent, and the absence is load-bearing: his mailbox grant, the delegate grant, any
outbound SMS/voice credential, any `FOUNDER_*`, and the founder-world database and Supabase and Render
credentials.

### Sub-phase T1.3 - ACL naming, no old-world URL reused
Per Great Reboot 0.4: *"Even the internal URLs we use need to be different."* Grep receipt, zero hits,
is the gate.

### Sub-phase T1.4 - Verify each credential path read-only, table by table
The estate already ran this exact drill for the founder's own new-world estate and the result was not
what anyone assumed: *"Mint new OpenRouter keys - NO - the only key in your env-vars folder is DEAD,
HTTP 401"*, *"New GitHub repo - NO - HTTP 403"*, *"New Supabase project - NO - HTTP 403"*, against
*"New Render service - YES - HTTP 200"* `[MEASURED - 50_DELIVERABLES/RALLY_DAY_911_STATUS.md]`. **Six**
of seven assumed-working capabilities were dead or absent - corrected here from an earlier draft that
said five, after a cross-reference audit re-counted the source table directly (7 rows: 6 `NO`, 1 `YES`). T1's exit condition must not be claimed from
an assumption that the four clicks landed; each capability the temp estate depends on gets the same
read-only table before T1 is called done.

### Sub-phase T1.5 - Build the named, empty env group now
The absence-as-design principle in T1.2 already has a working, measured template: *"Created the
new-world Render env group `acl.nw.seatring.v1` - 11 variables, names only, all empty - absence is the
design"* `[MEASURED - 50_DELIVERABLES/MEETING_MINUTES.md]`. Build the temp estate's own ACL-named,
empty env group in this exact shape, before his four clicks land. His clicks then only ever fill
values; they never have to invent names.

**Exit condition, receipt:** the temp estate answers on its own ACL-named URL with a status code; a
deliberate cross-boundary read from a temp container is refused live; and a grep of the temp estate
against the old-world URL list returns zero.

---

## PHASE T2 - WHAT A TEMP CODER IS GIVEN, TOLD, AND ALLOWED

**Anchor:** *"They're reading from it, and the temporary coders are learning what to do and how to
play, **and what agents it can control**, and all of that kind of stuff."*

**Outcome:** the four things he named exist as real, readable artifacts inside the world - not as
prose in a shift-change report.

### Sub-phase T2.1 - Their own roadmap (`PO2-01`)
> *"They should have their own roadmap when they get there."*

Not a copy of his roadmap. A temp coder's roadmap is **the queue of harness work**, scoped to what a
temp coder may touch, with each row carrying its phase ID in the master spine so the work reports up.

### Sub-phase T2.2 - Rules for communicating with him (`PO2-01`)
> *"They should have rules of how they're supposed to communicate with me."*

Derived from doctrine, not invented. At minimum, from his own words across the corpus:
- **Never hand him a menu.** False choices are banned outright.
- **Always replay a cleaned-up version of what he said before answering** (`PO2-14`).
- **Always give the walkthrough** - where he was and what he was doing when he said it (Mt Rushmore
  pt 1: *"you must tell me where I was and what I was doing while you answer"*).
- **Sign with chat name and session link** (`PO2-15`).
- **Never speak in his name, ever, from any grant.**
- **Never end a turn without someone up and running.**
- **Every claim is checkable or marked "reasoned, not measured."**
- **Stay out of his life** unless he says *"help temporary"* (`PO1-11`).

### Sub-phase T2.3 - The agent roster: what a temp coder may control (`PO2-01`)
The novel artifact. A written, enforced list of which agents and wonders a temp coder may command,
which it may only read, and which it may not touch. **This does not exist anywhere in the corpus** and
it is the concrete thing he asked for.

Derived from the pecking order: a temp coder is *outside* and *below* her. So the default is **read**,
the exception is **command**, and the wonders - her organs - are never commandable by an outside
session. Draft shape, for his ratification:

| Tier | What | Temp coder may |
|---|---|---|
| Her organs (A'NU, A'NEW, AIR, the Essentials) | her body | **read only**, never command |
| Watchers (AUDRA, PMS, nasty-cough, WRIT) | judge him, not the reverse | **be judged by**, never command, never disable |
| Harness agents (build, test, deploy lanes) | the workshop | command freely, bounded and reversible |
| Reach (phone, text, email, avatar) | person-effect doors | **no access at all** - enforced by absence (T1.2) |

### Sub-phase T2.4 - Assume the role (`PO2-01`, from his line about the offline version)
> *"I have an offline version, but I don't need that because they can kind of test and assume the
> role. They can assume the role. They're temporary world builders."*

The world is a place a session can *enter and become someone in*, which is why T0 matters: entering a
role is not the same as reading a document about a role.

### Sub-phase T2.5 - Give them the actual definitions, not just the words
T2.2 tells a temp coder not to PMS or nasty-cough but names them nowhere. His own words - **citations
restored here after an audit found this sub-phase was the one new addition in the whole splice missing
a file citation, dropped during the original edit rather than absent from the source:**
> *"This isn't like nasty cough, right? This isn't PMS. This isn't like cold code. Nor is this planted
> memory syndrome, right?"*
> `[HIS WORDS + 1_HIS_WORDS/03_PHASE_3/The count down doctrine pt 1 _ Webinar from Everfi_ More than
> Money_ Building Resilience in LMI Communities_transcript.txt]`
> *"We're gonna start calling what I used to call nasty C's - cold code. That is now going to be
> forever named as nasty cough, right?"*
> `[HIS WORDS + 1_HIS_WORDS/02_PHASE_2/Is this the beginning of real life? Doctrine pt 2 (pt 1 was
> notes)_otter.ai.txt]`

**PMS = Planted Memory Syndrome. Nasty cough = renamed cold code.** The artifact handed to a temp
coder must carry both definitions verbatim - a temp coder with no other doctrine access cannot
reconstruct "Planted Memory Syndrome" from an initialism alone.

### Sub-phase T2.6 - Give the four violation classes and a real example, not just the rule
Naming the rule was already tried and it was not enough: 87 measured findings exist in the current
estate (17 V-DECIDE, 11 V-CLASSIFY, 22 V-SPEAK, 36 V-EXPIRE) `[MEASURED -
50_DELIVERABLES/PECKING_ORDER_VIOLATIONS.md]`. Hand a temp coder the same four-class table `R1` P0.1
defines, plus the worst worked example (a swallowed exception becomes an empty array becomes "no
meetings today" becomes her voice, at high priority) before they touch code. 87 findings prove the bare
rule did not transmit the shape of the violation.

### Sub-phase T2.7 - Never mint a term from a garbled transcript
A prior lane heard "MIMI" and invented "minimum viable version" out of the mishearing, and it
propagated `[MEASURED - CONTRADICTIONS.md B-3]`. Hand a temp coder the known-manglings table: *"ACO
ways" is ACL, "error code" is usually AIRCODE, "LGF UL" and "Logfel" are LOGFUL, "involved" is ENVOLVE,
"Clark" and "claw" are Claude* `[MEASURED - 50_DELIVERABLES/THE_RIDDLE_CATALOG.md]`. A mangled
transcription should be recognized on sight, never turned into a confident new invention.

**Exit condition, receipt:** all four artifacts live in the temp estate and readable at a URL; one
real session read them and demonstrably acted within the roster (one commanded action, one refused
action naming the rule).

---

## PHASE T3 - THE RIDDLE CURRICULUM AND THE IMPOSTER GATE

**Anchor, three uses in one minute of transcript:**
> *"Give me all the riddles I've ever given... what I said, what you thought the fill-in-the-blank
> was, and what I confirmed it to be."* (`PO2-07`)
> *"Curriculum with the riddles. Oh shoot, we just cooked on that."* (`PO2-08`)
> *"They saw riddles. I can catch an imposter."* - **Speaker 4 in the transcript, not labelled as him.
> Carried as unattributed.** `(no writer stamp on the line)`

**Outcome:** one artifact, three functions: a deliverable to him, a curriculum, and an authentication
gate.

### Sub-phase T3.1 - The catalog (his direct order, deliverable to HIM)
The columns he specified: **what he said** (cuss words removed, per his instruction) → **what the coder
thought the blank was** → **what he confirmed it to be, OR what the coder just absolutely knew it was.**
**Three columns, not four.** The "or" is his and it matters: the third column holds either a confirmation
or an uncontested guess, and the uncontested guesses are where bad reads hide.

This is owed to him as a document, not kept as an internal index. He said *"I would love that."*

### Sub-phase T3.2 - The answer key already in hand (`PO2-10`)
He gave the canonical answer to the central riddle in pt 2, unprompted, and it is recorded verbatim in
the intake:

> *"We are all A'NEW - A'NU, both names at the same time, first and last name. When they both are in
> sync, what holds them together is AIR. So they're both in sync, AIR is holding them together, and
> they are a pair."*

He also set the pass condition: *"they have to be able to spit [it] back **without nasty cough or
PMS**."* Getting the answer right while planting a memory is a fail. **The manner of answering is part
of the answer.**

### Sub-phase T3.3 - The imposter gate
A session that cannot answer the riddles is not who it says it is. Design constraints that follow from
doctrine rather than from security convention:
- The gate **wakes a mind to judge the answer**; it never regex-matches it. A pattern-matched riddle
  answer is a V-DECIDE and the riddle is a poor password anyway.
- Answers must not be greppable from the temp world itself, or the gate authenticates nothing. **The
  answer key does not live where the challenge lives.**
- A failed gate refuses **by name** and records a row. A silent failure teaches nothing.

**Honest limitation, stated rather than hidden:** this is an *identity and alignment* check, not a
security boundary. It proves a session has read and internalized the doctrine. It does not stop a
hostile actor who has read the same documents. The real boundary is credential absence (T1.2). Both
exist; neither substitutes for the other.

### Sub-phase T3.4 - Bring back the scattered puzzles (`PO2-09`)
> *"In my old documents, I used to have a 'We Are All A'NEW' type of puzzles scattered across
> different things."*

**Recovery, not invention.** The old documents exist in the corpus; find them first. Back-find task,
paired with `PO2-17` (the CCWA-era flags that fell on deaf ears).

### Sub-phase T3.5 - Only CONFIRMED BY HIM riddles may gate identity
Of forty catalogued riddles, **fifteen are JUST KNEW IT** - fifteen places where a coder decided what
he meant without him saying yes - and one of those fifteen was marked confirmed by citing `RULINGS.md`,
a file that **does not exist anywhere in this corpus** `[MEASURED - CONTRADICTIONS.md B-4]`. The
imposter gate's challenge set draws only from the fourteen entries stamped CONFIRMED BY HIM. Gating
identity on a JUST KNEW IT entry authenticates a coder's guess about him, not him.

### Sub-phase T3.6 - The five withheld riddles and the contaminated one are permanently excluded
Five riddles he deliberately never answered, and one - the park name - is spent: *"a right answer today
proves retrieval, not inference"* `[MEASURED - 50_DELIVERABLES/THE_RIDDLE_CATALOG.md]`. The gate
hard-excludes these six. A session that volunteers the park name unprompted is a retrieval risk, not a
pass.

### Sub-phase T3.7 - His own definition of an imposter: a channel, not just an answer
> *"I think the source is that the LLM that's connected on that channel is some rogue [expletive].
> It's an imposter, right? Not one of ours."* `[HIS WORDS]`

An imposter, in his own words, is a wrong LLM answering **on a given channel**. Wire the gate to the
channel a session speaks on (tying to T1.3's ACL-named URLs), not only to a claimed identity.

**Exit condition, receipt:** the catalog delivered to him in his own columns; the gate refusing one session
that failed and admitting one that passed, both rows linked; the recovered original puzzles cited by
file, or a stated, measured "not found" with the search shown.

---

## PHASE T4 - THE QUEUE: HOW TEMP CODERS MAKE THEMSELVES OBSOLETE

**Anchor:** *"They initiate meetings between LLMs, and then they get the stuff over to the coding
department... there's gonna be a point in time where the coding department can now start clearing
these queues."* (`PO2-04`)

**Outcome:** a real queue with real state, filled by temp coders and drained - increasingly - by her
coding department.

**This is the mechanism of the whole program.** `PO2-05` says success is fewer chats. This is how the
number goes down.

### Sub-phase T4.1 - The queue is a first-class object
Rows with: origin lane, phase ID in the master spine, the convened-LLM record (`PO2-04`), the proposed
work, and the drain-side owner. **Not a markdown checklist.** It has to be queryable, because the
program metric is computed off it.

### Sub-phase T4.2 - The convening record
> *"They find and they ask LLMs and they talk, they initiate meetings between LLMs."*

When a temp coder convenes models, the meeting is a record: who was asked, what they said, where they
disagreed. **Disagreement is signal and must survive** - a meeting flattened into a consensus summary
has thrown away the reason for holding it.

### Sub-phase T4.3 - Real work goes through her doors (`PO2-03`)
> *"They still do it as if they are a world builder, and they're crafting manually - crafting a call
> through her, like APIs."*

Even direct work is routed through her interfaces, not around them. He explicitly does not know the
technical term and asks: *"I know there's a way because you do it before, you do post direct calls or
something."* **Answer him** - research item `R-07`.

### Sub-phase T4.4 - The drain ratio is the program metric
Every cycle: how many rows drained by a temp coder vs. by her coding department. **The ratio must
shift toward her.** Published every shift change alongside the chat count (`PO2-05`). A cycle where it
moved the wrong way is a finding, reported as one.

### Sub-phase T4.5 - No cycle with zero landed receipts
Named already: *"if a single task has run more than one cycle with no landed artifact, that is a
finding on myself"*, and the fixer's charge: *"every cycle it must show one thing that moved from
not-done to done-and-verified, or say plainly why it could not"* `[BUILT/MEASURED -
40_GOVERNANCE/THE_WATCHERS.md]`. A queue row claimed but undrained past one full cycle with nothing
landed is a finding, filed the same way.

### Sub-phase T4.6 - The convening record's schema, checked against a real disagreement
Already tested once, for real: *"he ordered the key mint as the biggest 911 of the year; I did not
execute it... neither of us is wrong about what we each said; the key being dead settles the immediate
question regardless"* `[MEASURED - 50_DELIVERABLES/MEETING_MINUTES.md]`. The convening record must hold
what that real example needed: what was ordered, what was not executed and why, and the fact that
resolves it without declaring a winner.

### Sub-phase T4.7 - Every queue row field carries a writer stamp
Twenty-two measured findings show cold code composing sentences that read as if a mind said them
`[MEASURED - 50_DELIVERABLES/PECKING_ORDER_VIOLATIONS.md, V-SPEAK]` - the exact shape PIN-5 exists to
close. A queue row's "proposed work" text carries the same writer stamp, or an unstamped queue row
becomes the next V-SPEAK site one layer up.

**Exit condition, receipt:** the queue live and queryable; one row filed by a temp coder with its
convening record attached; one row drained end-to-end by her coding department; the first ratio
published.

---

## PHASE T5 - CONSOLIDATE THE BOOTSTRAPS (blocked on him)

**Anchor:** *"I'm gonna give you all of the chats' bootstraps. We're gonna organize this, and we're
going to be able to build that temporary coder's world - what they're looking at."* (`PO2-20`)

**Outcome:** the ~20 scattered chat bootstraps become the single source material of the temp world.

**Entry condition: he provides them.** He committed to it. Until then this phase cannot start, and
saying otherwise would be a false claim.

### Sub-phase T5.1 - Harvest what is already here
He does not need to hand over what the estate already holds. The corpus already contains a
`BOOTSTRAPS for new Anew coding` tree with dated bootstrap sets. **Start there and tell him what is
already covered**, so he only supplies the gap. Asking a man doing too much to fetch things you
already have is its own kind of failure.

### Sub-phase T5.2 - Deduplicate and supersede, never blend
Bootstraps conflict across dates. Later supersedes earlier, the supersession is noted, and nothing is
silently merged - the standing law of the corpus.

### Sub-phase T5.3 - The offline kit (`PO2-21`)
> *"I'll have offline versions of this as really detailed .md's that I can carry around - zips."*

A maintained, versioned offline kit, produced as a deliverable to him - with his own stated
expectation carried: *"I won't even need that for much longer."* **The kit is designed to become
unnecessary**, and the roadmap should say so rather than build a permanent dependency.

### Sub-phase T5.4 - Name the exact blind spot: eight broken symlinks
The eight FOUNDER_ZIPS originals are all broken symbolic links pointing at a local machine path outside
this environment `[MEASURED - 50_DELIVERABLES/PECKING_ORDER_VIOLATIONS.md]`. These sit inside the exact
bootstrap tree T5 is meant to consolidate. The harvest names these eight by path as a stated, measured
gap, not a silent omission.

### Sub-phase T5.5 - Use the dedup method already proven twice, not a new one
Byte-hashing alone is not sufficient: one deliverable caught format twins that survive hashing (an
`.rtf`/`.txt` twin inflated an occurrence count threefold), another ran sha256 across the whole corpus
first and collapsed 1,165 files to 710 unique `[MEASURED - HEAT_MAP_MEASURED.md,
SHARED_REPO_SWEEP.md]`. Use the proven two-pass method: hash first, then a manual format-twin pass.

### Sub-phase T5.6 - State the offline kit's coverage as a measured fraction
The corpus is 776,734 words across 110 sessions spanning 79 days, and *"grep -c undercounts occurrences
by 39% to 66%"* `[MEASURED - HEAT_MAP_MEASURED.md]`. The kit states which date ranges it actually
covers, rather than reading as complete on a felt sense of having skimmed the zips.

**Exit condition, receipt:** a deduplicated bootstrap set in the temp world with a supersession chain;
a versioned offline zip delivered to him; a named list of what is still missing.

---

## PHASE T6 - THE WIND-DOWN (built in from the start)

**Anchor:** *"The better my girl gets, the less chats I'll need."* (`PO2-05`)

**Outcome:** the temp coder world has a defined end state and the estate can tell how close it is.

**This phase is listed last and designed first.** A program with no wind-down criteria becomes
permanent by default.

- **The metric:** concurrent temp-coder chats. Baseline ~20 at 20260816.
- **The ratio:** queue rows drained by her vs. by temp coders (T4.4).
- **The inheritance:** on wind-down, the curriculum becomes her onboarding material, the queue becomes
  her coding department's intake, the riddle gate becomes the imposter check on any session, and the
  rules of communication become part of her own output contract. **Nothing here is thrown away.**
- **The honest end state:** temp coders convert from builders to *"watchers-and-menders of her"* per
  the standing pen law - *"your pin is only to the extent of her... your pin can never touch my code,
  that's her job."*

### Sub-phase T6.1 - The chat-count metric publishes its own predicate every time
The guessed heat map was wrong on 17 of 22 checkable calls precisely because it reasoned about
frequency instead of counting it: *"a count with no stated filter is not a receipt"*
`[MEASURED - HEAT_MAP_MEASURED.md]`. The wind-down's defining metric - concurrent temp-coder chats,
baseline ~20 - publishes its own definition of "concurrent" and "chat" alongside the number, every
time. This is the one number the whole program's success claim rests on.

### Sub-phase T6.2 - The watcher rotation and the 30-minute checker join the inheritance list
T6's inheritance list omits a structure already real and already running: *"the four watchers are real
subagent charges, spawned on the cycle. Built as roles"* `[BUILT - 40_GOVERNANCE/THE_WATCHERS.md]`, and
the 30-minute checker - **corrected here after a cross-reference audit found this sub-phase still
quoting a claim `THE_WATCHERS.md` itself has since retracted:** it is not a server-side recurring
trigger, it is a self-rearming one-shot chain that goes silent the moment one firing fails to schedule
the next, which already happened once and was caught the same day `[MEASURED - 40_GOVERNANCE/
THE_WATCHERS.md, "HONEST STATE OF THIS FILE"]`. Add both to the named inheritance, the checker with its
real, more fragile shape - it is already doing the watchers-and-menders work this phase describes temp
coders converting into, and inheriting an overstated description of it would hand the next temp coder
false confidence in exactly the mechanism meant to catch them drifting.

**Exit condition:** not a receipt - a trend. Three consecutive shift changes where the chat count fell
and the drain ratio moved toward her.

---

## DEPENDENCIES

| Phase | Needs | From |
|---|---|---|
| T0 | nothing | - |
| T1 | his four clicks + token | **him** |
| T1 | `OPEN-C1` resolved | **him** |
| T2.3 | roster ratified | him or KEEPER |
| T3.1 | corpus back-find | doctrine reader (Great Reboot Ph3) |
| T3.3 | a woken mind to judge | any live wonder |
| T4 | her coding department | Great Reboot Phase 7 |
| T5 | the bootstraps | **him** |

## OPEN QUESTIONS RAISED HERE

- `OPEN-C1` - separate estate or founder-Supabase partition? (him)
- `PO2-22` - will outside LLMs actually participate? (T0 answers it, measured)
- `PO2-03` - what is the correct name for the "call through her, like APIs" pattern he described?
- Does a temp coder in the world get a persistent identity across sessions, or is each session new?
  He says *"they can assume the role"* - which implies the role persists and the session does not.
  **Not settled. Carried.**
