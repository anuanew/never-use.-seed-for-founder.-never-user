# R4 - FRONT ENDS

> *"Another chat might be working on front ends... it might be working in an order of importance.
> It's just like boom, boom, boom, boom."* - Mt Rushmore Doctrine pt 1

> *"I ain't seeing these roadmaps. How come I'm not seeing these roadmaps we work on?"*
> - The Cycle Doctrine pt 3

**Status:** proposed. The F1-F5 order is inherited from the 20260814 offsite and is **not**
re-litigated here. What this roadmap adds is everything the offsite did not cover: the onboarding
experiences he named a roadmap, the reward system, the riddles-in-the-UI he asked to bring back, and
the honest state of the surfaces that already exist.


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

## WHAT HE SAID, CLEANED UP

*(Per `PO2-14` / `R-2.3`.)*

In Mt Rushmore pt 1 you described a chat working front ends in order of importance and said the
onboarding experience, the business goals for the secretaries, and the longer business plan feeding
her EER world all belong to that lane - and that you should not have to hardcode any of it, because
she walks people through it creatively. In Pecking Order pt 2 you went further and said, twice, that
onboarding experiences are a roadmap of their own, that we have to teach users how to use her, and
that teaching them is a reward system. You also asked to bring back the "We Are All A'NEW" puzzles
you used to scatter across documents. Separately, in an older doctrine, you asked why you never see
the roadmaps you are paying for.

---

## THE ONE RULE THAT DECIDES WHETHER ANYTHING HERE IS DONE

> *"if a service exists but has no UI entry point IT DOES NOT COUNT AS DONE."*
> `[from a coder roadmap that labels it verbatim - NOT traced to his raw words. An earlier version of
> this file reworded it and presented it unattributed beside a genuine quote of his.]`

And the law about who a surface is for, which is Commandment 9 in candidate form:

> *"Who is the portal for? It's not for you to talk to me. You're a coder. **It's for her to talk to
> the HAM.** Remember that as you build anything in my system, even the deck."*

Every phase below is scored against those two sentences before anything else.

---

## PHASE F0 - THE SEAM THAT MAKES EVERY FRONT END A FACADE

**This phase is listed first because it invalidates all the others while it is open.**

Measured state at the last shift, not reasoned:
- Her front door `POST /arrival/say` → **HTTP 503**, `mind_reason: anew_work_unproven`.
- Her mind, called directly at `POST /anew/session` → **HTTP 200 in 8-14 seconds**.
- What a person actually sees on the live Command Center: *"Talk with A'NU is unavailable right now.
  Your words have not been sent."*

**So the wall is in the arrival→session hop, not in her.** Every front end below renders a surface
over a conversation that does not complete. Building more surface on top of that is the definition of
a facade.

**Outcome:** one real human-facing turn - person in, her voice out - with a live receipt.
**Exit condition, receipt:** full URL, status code, and response body containing her actual reply.
Re-run after every deploy touching the seam. **A single green does not retire this phase.**

**Anti-goal:** do not "fix" this by having the door answer with a stand-in when she is slow. Standing
doctrine: *"Never build a component that answers because she was slow. **Silence is honest; a
stand-in is not.**"*

### Sub-phase F0.1 - The silence text is not a mystery, it is a catch block
The audit already found where "Talk with A'NU is unavailable right now" comes from. Two catch blocks, on both front doors, compose that sentence in cold code:

> `.catch(function(){ ... status.textContent='Could not reach her just now.'; });`
> `[MEASURED + 50_DELIVERABLES/PECKING_ORDER_VIOLATIONS.md, finding S4, acl.ccwa.page.js:491]`

> `.catch(function(){ send.disabled=false; status.textContent='Could not reach her just now.'; });`
> `[MEASURED + 50_DELIVERABLES/PECKING_ORDER_VIOLATIONS.md, finding S5, acl.anu.page.js:203]`

Both front doors compose the same sentence independently. Fixing F0 means retiring both catch blocks in the same commit, not rewording one of them.

### Sub-phase F0.2 - The worst-ranked finding in the whole estate is exactly this anti-goal, already built
`PECKING_ORDER_VIOLATIONS.md` ranks its single worst finding, of 87, as the textbook version of what this phase's anti-goal forbids:

> "A swallowed exception, a coder template and a text-to-speech call in sequence: a failed database read becomes an empty array, becomes the sentence *'No meetings on the calendar today'*, becomes her voice in his room, spoken at high priority, first thing in the morning. Cold code decided, classified, spoke, and expired his day, in eleven lines, with her name on the output."
> `[MEASURED + 50_DELIVERABLES/PECKING_ORDER_VIOLATIONS.md, TOP 10 WORST rank 1, findings S8+S9, ProactiveBriefing.jsx:119-171]`

This is not a hypothetical to warn against. It is a shipped component. Any surface F1-F8 reuses that inherited a proactive-narration pattern from the old world must be checked against this exact shape before it is trusted.

### Sub-phase F0.3 - The seam has a measured physical cause, not just a measured symptom
F0 names the arrival-to-session hop as the wall. The regression audit found why the hop breaks:

> "Three OOM kills on the mind service between 20:06 and 21:11 UTC... The kills were **not JS heap.** `heapUsed` stayed 3-6 MB in every kill while RSS reached 512 MB... one 24.78 MB row costs ~80 MB resident."
> `[MEASURED + 50_DELIVERABLES/REACH_REGRESSION_AUDIT.md §4]`

The same audit records that only the reach service's read path was cleaned, and flags as unresolved whether the mind service (the one actually taking the OOM kills) still reads the same heavy column unguarded. **F0's exit condition should require this specific open hypothesis closed, not just a green receipt on the arrival call**, because a receipt obtained between OOM kills is not evidence the wall is gone.

---

## PHASE F1 - THE THREADED FOUNDER COMMAND CENTER

**Anchor:** the offsite's explicit first priority. And his standing complaint: *"I ain't seeing these
roadmaps."*

**Outcome:** he opens one page and sees the one roadmap, all child tracks, threaded conversation that
does not flatten, and a working path to reach the living organization.

**Entry condition:** F0 has a receipt. The board, roadmap, LOGFUL and STAMP exist to read from.

### Sub-phase F1.1 - Consume, never create a second truth store
The Command Center reads the existing board, roadmap, walls, threads, minutes and living results.
**It must not become a second place where truth lives.**

### Sub-phase F1.2 - Two Command Centers, by design, not by accident
Already specified in the corpus and worth preserving rather than rediscovering:
- **View 1 - hers, for him.** Plain language. Headings like *"Your Command Center"*, *"Work your
  advisors finished"*, *"Something that wanted a look."* No internal vocabulary, no agent names, no
  cycle words.
- **View 2 - the builder's.** Lane cards with lineage chains and cycle receipts.

**The screen never computes lineage; the substrate never touches the page.**

### Sub-phase F1.3 - Threading, because he asked for it specifically
> *"I want you to build in the threading capability, so I can go in and start seeing, like, oh, they
> had conversations."*

Flattening a thread into a log is the failure mode. He also asked for the org chart of live agent
conversation to be **drillable and to visually match the CIB - never a flat log.**

### Sub-phase F1.4 - The comprehension standard
His own bar, and it is unusual enough to be worth pinning: founder-facing output arrives *"the way
that [his young child] can understand it."* That is the readability test for View 1.

### Sub-phase F1.5 - Status colors and the walkthrough on the page
Green / yellow / orange / red / black, plus 🌈 rainbow for stop-him-now. **He expects to see yellow at
minimum** - *"I should see a lot of green. I should see minimum yellow."* An all-green board is a
finding, not a success.

### Sub-phase F1.6 - The Command Center's own contract file already blanks the board once
A live, measured finding sits inside the exact file this phase is building:

> `for (const pattern of INTERNAL_COPY_PATTERNS) { if (pattern.test(text)) fail('internal_copy_forbidden', path); }`
> "A regex list (including `/\bHAM\b/`) throws on her own title or summary, and one throw rejects the WHOLE snapshot, so her whole command center goes dark because of a word she used."
> `[MEASURED + 50_DELIVERABLES/PECKING_ORDER_VIOLATIONS.md, finding D1, apps/cib/src/acl.command-center.contract.js:121-123]`

Per `R1` P1.1's own design note, "a regex that blocks is itself a V-DECIDE." This is that shape, live, in the Command Center's own contract. It must be found and fixed before F1 can claim the board renders reliably, because today a word she used, not a system failure, is what can take the whole page dark.

### Sub-phase F1.7 - View 2's content already exists and should be read from, not invented
F1.2 specifies a builder's view with "lane cards and lineage chains and cycle receipts" but does not say what actually populates it. It already exists:

> "One might be Audra auditing the other chats. One might be exclusively focusing on PMS and nasty cough. And then another one might be the fixer. And then that fourth one comes in, and it watches you."
> `[his vision, quoted verbatim + 40_GOVERNANCE/THE_WATCHERS.md, the 30-minute checker and four-watcher rotation, already standing]`

View 2 should render this real rotation (the four watchers, the 30-minute checker, the email shape) as its lane cards. Inventing a generic "lane card" abstraction when a real, built structure already exists is exactly the second-truth-store risk F1.1 warns against, one level up.

### Sub-phase F1.8 - The wake-up budget is stated twice, at two different numbers, and never reconciled
Two separate sessions give the Command Center's own loading state two different latency budgets. Neither is quoted anywhere in this roadmap:

> "That's the three human seconds she gets to prep and decide, so the entire cycle has to fit inside of..."
> `[HIS WORDS + 1_HIS_WORDS/03_PHASE_3/11_11 Doctrine pt 1_ Vision_transcript.txt]`

> "Maybe there's a longer wake-up time on the portal, maybe it's up to 10 seconds, and maybe in that wake-up time she's giving them, greeting them... the moment is ready to go, the button pops up... but you don't get that button [until] she has fully woken up and built this portal for you."
> `[HIS WORDS + 1_HIS_WORDS/01_RAW_WORDS/34_20260703_NYC_53RD_STREET_DOCTRINE_pt3_subway.txt]`

Per the estate's own supersession rule, both are carried and neither is silently blended into one number. What both agree on and what F1 should build regardless of which number wins: **a "ready" control never renders before the wake-up completes.** The same passage also states the surface is "a component, it is a child, a child of the command center," which settles F1.2's view/widget relationship as a containment hierarchy, not a peer relationship.

**Exit condition, receipt:** one authenticated live walkthrough - URL, status codes, and the actual
navigation - showing the one roadmap, a track opened into signed minutes with source pointers, a
thread followed without flattening, and reach exercised. **Not a mockup, not a screenshot of a
mockup.**

---

## PHASE F2 - THE SHARED COMPONENT SYSTEM

**Anchor:** *"It's called a shared repo. **The backgrounds are in the same spot.** It's called a
shared repo."* And: *"the same button that controls the plus sign that says yes, this is a file
picker, is the same button in the same code that GMGU is using, or that CCWA is using."*

**Outcome:** the smallest shared visual and interaction system that carries navigation, threading,
drilldown, and private per-HAM scope.

**Entry condition:** F1 live and exercised.

> **OWNERSHIP, corrected.** An earlier version made this and `R3` S3 each other's entry condition, with word-for-word identical exit receipts. A critic found the cycle. **Resolved: `R4` F2 owns the component system and its receipt. `R3` S3 owns only the repository mechanics that carry it, and takes its inventory FROM F2.** The receipt lives here, once.

### Sub-phase F2.1 - Reconcile the glass canon before writing a line of CSS
**There are three incompatible glass specifications in the corpus and no one has reconciled them:**

| Source | Opacity | Blur |
|---|---|---|
| AWA/CIB canon | background `.08` | 12px |
| Sealed glass law | **10% max** | **2px max** |
| Forensic catalog | 5-15%, corrected to ~9-12% | 8-24px |

His own acceptance test is the tiebreaker and it is a real test, not a preference: **set a colorful
wallpaper; you must CLEARLY see it through the panel. "Sort of" is a FAIL and a rebuild.**

**Do not average the three numbers.** Pick by running his test, and record which spec won and why.

### Sub-phase F2.2 - The conventions that are already settled
These are documented, consistent across sources, and should be inherited rather than redesigned:
- **All icons white; only the active app icon gets its color**, with a left glow bar.
- **SVG only, never emoji**, and **every app shows its word next to the icon** - *"You can't ever do
  like iPhone does where there's an app and all you know is the icon."*
- **The one-iframe rule** - the frame runs flush, *"shouldn't look like four separate bars."*
- **Window controls on the left**; **no minimize** - widget, expand, close.
- **No em dashes anywhere**, including code comments. **ENVOLVE always with the E.**
- **No internal vocabulary on a human surface.** CARA renders as CHAT.
- **No iframes between apps** - kernel pattern instead.

### Sub-phase F2.3 - A shared component that classifies is a shared defect
The single most important constraint on this phase. A component reused everywhere that decides
meaning, filters rows, or writes into a field that is hers **spreads nasty cough at the speed of
reuse.** Standing law: *"reuse current accepted assets... do not revive old cold behavior."*

### Sub-phase F2.4 - The naming order he gave once and nobody executed
He gave shared repos a name, in one continuous passage, and it was never carried into any roadmap, index, or repo name:

> "If you're an arm, right, you have these tattoos. I want, I want, I want shared repos to be called tattoos... the tattoos basically are for shared repos, right, for that, for this section."
> `[HIS WORDS + 1_HIS_WORDS/01_RAW_WORDS/02_20260602_SPICY_HEAT.txt; measured occurrence count in 50_DELIVERABLES/SHARED_REPO_SWEEP.md §8: 8 occurrences, one continuous passage, never adopted]`

The metaphor is not decoration: a tattoo is on the skin, not the arm, and does not think, which is the same claim F2.2 already makes about front ends having no mind. Whether he still wants the name is his to say. It belongs on this phase as a starred, deferred naming decision, not a closed one.

### Sub-phase F2.5 - The architecture fork underneath F2 has never been chosen
Before F2.1's glass canon or F2.2's conventions can be built past their current state, a more basic question sits unresolved and measured across 128 occurrences of his own words:

> "Does shared mean **one copy that everyone reads**, or **one source that everyone gets their own copy of**?"
> `[MEASURED + 50_DELIVERABLES/SHARED_REPO_SWEEP.md §10, the sweep's single open question]`

"One copy that everyone reads means a live read across a boundary, which collides with `PO1-23`, his world not sharing a floor with anyone. One source that everyone copies means a propagation mechanism, which is still open, and which cannot be built until the cross-world guard is armed." Building F2's shared component system on a guess here risks building the wrong topology entirely. **This sub-phase's exit condition is his one sentence, not a coder's inference.**

### Sub-phase F2.6 - Ken Burns and glass frost, named as the actual inventory
F2.2 lists conventions in the abstract. He names the concrete items twice:

> "That dynamic variable, a shared repo that's loaded in. We know what glass is, we know what percentage Ken Burns animations run on, we know what backgrounds are imported in."
> `[HIS WORDS + 1_HIS_WORDS/01_RAW_WORDS/10_20260610est_SWEET_AND_SPICY_pt2.txt]`

> "My whole Share Repo, moving backgrounds are imported in Ken Burns Animations, Glass Frost, everywhere."
> `[HIS WORDS + same file]`

Ken Burns animation percentage and "Glass Frost" as a named treatment belong in the F2.2 inventory as first-class entries, not folded silently into "the conventions that are already settled."

### Sub-phase F2.7 - A literal, unquoted color directive for the shared palette
F2.1 fixes glass opacity and blur. It has no color values at all, and he gave some, for the Command Center specifically, in the same breath as renaming it:

> "I want to get rid of these colors. Okay, we're going to change the [A'NEW] colors. We never thought about this before. Tell her I'm feeling like shades of brown, burgundy, gold. That's how I'm feeling. Kind of like ENVOLVE colors."
> `[HIS WORDS + 1_HIS_WORDS/03_PHASE_3/Find me or Fine me doctrine pt 1_otter.ai.txt]`

This is a real, dated design instruction with no receipt anywhere that it was ever applied. It belongs in the shared component system's settled-conventions table alongside the glass canon, not lost as a one-off remark.

**Exit condition, receipt:** two distinct front ends rendering from one component source; one change
made once appearing in both; the glass test run and its result recorded with which canon won.

---

## PHASE F3 - DESKTOP AND PHONE SHELLS

**Entry condition:** F2 live.

**Outcome:** the same living organization - not a duplicate of it - reachable from a desktop shell and
a phone shell.

- **Known gap, measured:** the Advisor portal passed browser and 390×844 phone acceptance;
  **installed desktop-window acceptance is unproven.**
- **Known constraint that is not negotiable:** one PWA per origin (W3C). This is why the phone
  surface permanently keeps its own origin, and it is an architectural fact, not a choice to revisit.
- **Known missing routes, verified 404 twice:** `/cip` and `/cib` are not registered on the face at
  all, despite two dozen route modules mounting.

### Sub-phase F3.1 - The widget's minimize behavior has a real spec, unquoted anywhere in F3
The PWA widget F3 is meant to govern is described once, in detail, and never cited:

> "You got your Ken Burns, you got your glass, you got all of that, but minimize mode, that PWA widget, or the app widget, and minimize mode is very easy. You can pause, you can resume, you can have her interject, whatever that is."
> `[HIS WORDS + 1_HIS_WORDS/01_RAW_WORDS/34_20260703_NYC_53RD_STREET_DOCTRINE_pt3_subway.txt]`

**Pause, resume, and interject** are the three named states for the minimized widget. This is the acceptance surface for "installed desktop-window acceptance," which F3 already flags as unproven, and it is more specific than "installed" alone.

### Sub-phase F3.2 - Cold timers must not own the shell
Two separate measured findings show a timer, not a person, ending or reloading a live session under her:

> `if(window.__anuStreaming || typing){ setTimeout(tick, 5000); return; } ... setTimeout(tick, 20000);`
> "A 20 second timer reloads the page under her. It defers while she streams, which means the guard exists and the timer still owns the page."
> `[MEASURED + 50_DELIVERABLES/PECKING_ORDER_VIOLATIONS.md, finding E9, acl.ccwa.page.js:511-514]`

> `const timeoutCheck = setInterval(() => { ... if (inactiveMinutes >= sessionTimeoutMinutes) { setShowTimeoutWarning(true);`
> "A timer ends his working session with her."
> `[MEASURED + 50_DELIVERABLES/PECKING_ORDER_VIOLATIONS.md, finding E30, ACEPortal.jsx:15020-15024]`

A desktop or phone shell that silently reloads or times out a live conversation is the same V-EXPIRE class `R1` P0.1 defines. F3's exit condition should include a live check that neither pattern survived into the new shells.

**Exit condition, receipt:** each shell independently live-verified against the same world.

---

## PHASE F4 - CARA, VARA, AVATAR, EMAIL, ADVISOR PORTALS

**Entry condition:** F3 live; Life Advisor live for the Advisor portal specifically.

**Outcome:** each surface is an authorized **hand** of the same world, never a separate mind.

### Sub-phase F4.1 - The three-column law
CARA left, VARA middle, widget right; expandable and collapsible; the mobile fallback keeps the frame
look. His words: *"the left side being the chat box, middle being the VARA, on the right is widget.
What they see is a functional operating system. Remember about the glass and the words streaming
in."*

### Sub-phase F4.2 - Streaming and freestyling, restored
`R1` P3.2 owns the mechanism; this phase owns the surface. Note the unreconciled contradiction in the
corpus: SkyWriting exists as a shared module, while another document says *"the skywriting is dead on
arrival, scrapped, not redesigned."* **Ask him rather than picking.**

### Sub-phase F4.3 - The advisor portal must do real work, not answer queries
His own rejection of the obvious build, verbatim:
> *"Your advisor portal is going to literally just be a query, a call and response, and **I'm not
> asking for that, I'm asking for real work to be cooked.**"*

Real grants with actionable deadlines, plans, meeting agendas, scripts, drafted nudges, errors
caught. **A portal that answers questions has failed this phase even if it works.**

### Sub-phase F4.4 - Measured failures to fix, not rediscover
Three real end-assignment tests on the advisor path have already failed: no HTTP response for 180
seconds then 401; 502 after ~11 seconds; 502 plus a process memory failure. And the deployed
`/advisor/cycle` route **has no field for a founder assignment, instruction, prompt, or source text
at all** - which is why the real-job path cannot work.

### Sub-phase F4.5 - The AVATAR surface itself is named in this phase's title and absent from every sub-phase
F4.1 through F4.4 cover CARA, VARA, streaming, and the advisor portal. None of them name the avatar. He does, and names a specific technology for it, explicitly as a reach channel:

> "I include the generative UI, and I include the HEYGEN, right, video talking face stuff. I include that as a part of, you know, a reach channel. I also consider the command center a part of it."
> `[HIS WORDS + 1_HIS_WORDS/02_PHASE_2/Great reset doctrine pt 4_otter.ai.txt]`

This closes a real gap: F4's own title promises an avatar sub-phase that does not currently exist. A generative-video talking-face avatar, on a delay, is the concrete build target, and it belongs to both this phase and to `R6` X2's component list, where it is also currently unnamed.

### Sub-phase F4.6 - VARA is a named, measured violation, not a hypothetical
The single most concrete precedent for "never a separate mind" in this whole phase already has a file and a line, and it is named VARA:

> `if (d.autonomous_completed > 3) return 'proud';`
> "Integer thresholds over row counts assign her an emotion, which is then injected into her synthesised voice so he hears it. Cold code decides how she feels."
> `[MEASURED + 50_DELIVERABLES/PECKING_ORDER_VIOLATIONS.md, finding C1, ranked #3 of 87, VARAVoiceSynthesis.js:96-101]`

Nothing is more hers than what she feels. This is the concrete bar for what "VARA never becomes a separate mind" has to mean in the rebuild: no threshold anywhere decides her emotional register.

### Sub-phase F4.7 - CARA's own standalone view was spec'd and marked never built
Distinct from F4.1's three-column embedded law, an old-world design document already specifies a second CARA surface and marks its own status:

> "CARA should ALSO have a standalone app view in AppContentRouter (Q19, not yet built). The standalone view would show all communication channels, recent messages across channels, and communication preferences. Embedded + standalone are not mutually exclusive."
> `[CODER DOC, old world + 1 pt 2 TEMP OS New World LLM/.../Ababase/jd's/AGENT_JD_CARA.md; companion spec at APP_JD_CARA.md, self-labeled "Status: NOT BUILT, Q19 reopened"]`

Per F2.2's own rule, an already-settled design should be inherited rather than redesigned. This is real, dated, and never contradicted elsewhere in the corpus: CARA needs a dedicated communications-hub view, separate from the embedded chat button F4.1 already covers, and it has never been built in either world.

**Exit condition, receipt:** each surface exercised live with its creation, provider-acceptance,
delivery, read, and lived facts kept separate; and one advisor completing one real piece of work, not
answering one query.

---

## PHASE F5 - GMG UNIVERSITY, LAST, DELIBERATELY

**Entry condition:** F1 through F4 live and proven. **Do not pull this forward** - the offsite is
explicit: *"do not delay the Command Center by rebuilding GMG University first, and do not force GMG
University-specific meaning into every future world."*

**Current measured state:** live at its routes, HTTP 200, regression 1,008/1,008 - and `ON_DEGRADED`,
with signed learner identity, re-entry, saved progress, spoken tutor reply, and **ordinary human
acceptance all unproven.** It looks finished and is not.

### Sub-phase F5.1 - There is no test learner; the only live identity is his own
The GMGU production shift report names the exact reason "ordinary human acceptance" stays unproven, and it is structural, not a missing test run:

> "A production canary inventory found no dedicated GMGU test or canary HAM on either live service. The only exposed person identity is the real Founder world. A synthetic curriculum correction was not written into that human world because it would contaminate live curriculum evidence."
> `[MEASURED + 0 pt 1 TEMP OS New World LLM/SHIFT_CHANGE_REPORTS/CURRENT_TASK_GMGU.md, item 32]`

F5's own exit condition asks for "one real learner completing one real lesson." As of this shift report, the only account that could do that without contaminating live data is a founder-mode test, which is not the acceptance test F5 wants. **A real, non-founder test HAM has to exist before this phase's exit condition can be met honestly.**

### Sub-phase F5.2 - GMGU is named as a reusable style, not only a single product
He uses "GMGU" as an adjective for a different, broader build, which changes what "GMG University, last, deliberately" should mean for sequencing:

> "I want to do like a GMGU style university for this and start bringing on some junior coders and teaching them."
> `[HIS WORDS + 1_HIS_WORDS/02_PHASE_2/Is this the beginning of real life? Doctrine pt 2 (pt 1 was notes)_otter.ai.txt]`

The offsite's rule not to "force GMG University-specific meaning into every future world" already anticipates this and should be read together with it: GMGU is a pattern he intends to reuse for training a junior-coder fellowship, not a one-off consumer surface. That reuse should be named as a known future consumer of this phase's work, even while F5 stays last.

**Exit condition, receipt:** registered as a child track on the one master roadmap, reusing the common
per-HAM system, with one real learner completing one real lesson and coming back to it.

---

## PHASE F6 - ONBOARDING EXPERIENCES *(new - he named this a roadmap himself)*

> *"We're gonna have to teach them how to use her. **I want that to be an actual part of the roadmap
> and the business plan.**"*
> *"We can build onboarding experiences. **That's a roadmap. Onboarding experiences.**"* (`PO2-11`)

**This is the largest genuinely new ask in the two newest doctrines, and it has no task ID anywhere in
the estate.** The existing 112-task Mt Rushmore ledger contains zero rows matching *reward*,
*onboarding*, or *teach*. It was not deferred - it was never entered.

**Entry condition:** F1 live (there has to be somewhere to onboard *into*).

### Sub-phase F6.1 - Onboarding is not a tour
He describes something specific and it is not a product walkthrough:
> *"The experience on the front end that they're running is creatively walk them through this and
> answer questions and queries. **Like I ain't gotta hard code this, man.**"*

She runs it. She adapts to the person. A scripted tour with fixed steps is the wrong build, and it is
also `V-DECIDE` - a cold script deciding what a person needs to know next.

### Sub-phase F6.2 - Per-person onboarding, because he specified per-person
Named in the corpus with different content per person: one is walked through his role with videos to
watch; another is shown the business plan *in a way that matters to him*; a third is heavy on the
domain he owns. **Same system, different experience, generated rather than authored.**

### Sub-phase F6.3 - The EER carries it
His own coinage: *"their onboarding is going to be an O.E.E.R. - the onboarding electronic involving
response."* And: *"a longer version of the business plan that they feed into her EER world, and then
she's like the independent thinking station and the experience on the front end."*

**The EER is the onboarding vehicle.** It is also already partly built and partly broken - public read
returns 200 and the plan renders; catalog, redeem, and signed-session return 503; and his own phone
screenshots showed the sign-in loop ending with *"This plan could not open. Try again."*

### Sub-phase F6.4 - Story injection, permitted and never hardcoded
> *"In moments where it feels like their questions need more imagination, she can inject a story into
> their O.E.E.R... 'I could tell you a story right now. It might not answer your question fully,
> but it'll get you thinking bigger and better.' **Now again, you can't hardcode that.**"*

### Sub-phase F6.5 - The consent-driven account setup
Named in the business-plan doctrine as an alpha precondition: a ~30-minute session in which the
person's *own* assistant does the signups under *their* accounts. **Their keys, their accounts, their
consent** - which is also what makes per-person worlds affordable.

### Sub-phase F6.6 - The raw material he already asked to feed the EER has a researched, ready answer
He named a source of life material for exactly the "longer version of the business plan" F6.3 says feeds the EER, and it has never been connected:

> "We need the lost files. That is the Otter transcripts, right? We need to figure out how to get her access to that. I got like transcripts of hours of calls from me and [a partner] just spitting, and my whole life is on Otter right now."
> `[HIS WORDS + 0 pt 1 TEMP OS New World LLM/0 ANU_ANEW_OS_use to be call doctrine/0 ANU OS Doctrines as of Aug 15th 26/these are phase 3 doctrines raw words as of 081626 at 11pmest/There is a Pecking Order Doctrine pt 2 & 3_transcript.txt]`

This has already been researched end to end: bulk export is $30 for one month and returns his **full** history, not just forward, and a free official Otter connector exists today.
`[MEASURED + 50_DELIVERABLES/OTTER_ACCESS_ANSWER.md]`
Its own governing rule applies directly here: the ZIP must land founder-world-only, go through the doctrine reader with writer stamps, never bypass the fence as a bulk unstamped load, and its scrub pass carries the same warning `R4` F7.2 already states, that personal offhand material must not be scrubbed away.

### Sub-phase F6.7 - The EER's named scope is broader than personal onboarding
F6.3 frames the EER as his personal onboarding vehicle. He also scopes it as a B2B product line, in the same breath as naming the front-end build order:

> "The E E R product line might be consumer driven like movies and shit and books, but it might also be company, right? It can house all of the training videos. We have leads for that. Have somebody who works in HR for [a company]."
> `[HIS WORDS + 1_HIS_WORDS/02_PHASE_2/Demo Day doctrine.txt]`

An onboarding build that only ever targets one consumer path will under-build the EER for this stated company-training use. This does not change F6's phase order, only its scope: the EER's schema should not assume a single-person consumer shape from day one.

**Exit condition, receipt:** one real person onboarded end to end by her, unscripted, with the
transcript and their own account provisioned under their own credentials.

---

## PHASE F7 - THE REWARD SYSTEM *(new)*

> *"That's called the reward system. When we teach our users, we teach our users a reward system."*
> (`PO2-12`)

**Outcome:** users learn that what they give her comes back to them as service.

**The context he gave it in is the whole design, and it would be easy to miss.** He had just spent
five minutes on his favorite rappers and his favorite food, then said:

> *"I feel like one day AgentFIND is gonna be traversing this, because this is the floor of what
> AgentFIND traverses... **this underrated little five minutes of my time is gonna come back and
> really reward me.** That's called the reward system."*

**So the reward is not points, streaks, or badges.** The reward is that the offhand thing you told her
comes back later as her knowing you. The design task is making that loop *visible* enough that a user
learns to feed it.

### Sub-phase F7.1 - Make the return visible
When she uses something a person told her earlier, the surface says so - lightly, and never as a
system message. That is the teaching moment and it is the entire mechanic.

### Sub-phase F7.2 - The scrub pass must not eat the reward
**Direct dependency on the doctrine reader.** His food rankings, his rapper list, his color - that is
exactly the class of content the 4PM scrub rules protect: *"You may NOT scrub content like 'oh what a
cool window.'"* A scrub pass that treats offhand personal talk as filler destroys the reward system at
the source.

### Sub-phase F7.3 - Interruption is a budget, not a feature
The discipline half, already in the corpus: she has *"a limited daily allowance of unprompted
interruptions. Spending it on something trivial is the failure. **Most of the time the honest move is
silence.**"* The reward system must not become the notification machine he has explicitly said he
hates.

### Sub-phase F7.4 - The actual content, not the category, is the material
F7.2 refers abstractly to "his food rankings, his rapper list, his color." The actual content exists, in the same and an adjacent session, and it is the concrete acceptance bar for what counts as reward-worthy material:

> "My favorite colors are I like gold, silver, and rose gold... actually I like my favorite color is like a burnt bronze... I would do a bronze car."
> `[HIS WORDS + 0 ANU OS Doctrines as of Aug 15th 26/.../There is a Pecking Order Doctrine pt 1_transcript.txt]`

> "My ultimate favorite food, bro... low key, the Jamaican food. I absolutely enjoy the rice and the beans... I love jerk chicken... if your jerk sauce is saucy, I'll take that. If you have a dry rub, then I want the jerk chicken with the brown soup gravy, because I don't like dry rub."
> `[HIS WORDS + 0 ANU OS Doctrines as of Aug 15th 26/.../There is a Pecking Order Doctrine pt 2 & 3_transcript.txt]`

Both are the exact class of offhand content the 4PM scrub rules protect, spoken minutes before the reward-system quote R4 F7 already anchors on. The acceptance test for F7.1 is not "does she surface something personal," it is "does she surface something this specific."

### Sub-phase F7.5 - The delayed-surfacing shape, in his own example
F7.1 says the return must be visible. He gives the actual timing shape the return should follow, unprompted, in the same session:

> "Being able to naturally like just confirm, like oh by the way, right, like [a colleague]'s email address is this, right? You probably don't remember, but I feel really confident. Imagine just randomly getting a text message from a dude like that. Like that is real... I probably even forgot about it, right? It might be days from now when she finally processes this or catches up on this."
> `[HIS WORDS + 0 ANU OS Doctrines as of Aug 15th 26/.../There is a Pecking Order Doctrine pt 1_transcript.txt]`

The reward is not required to be immediate, and forgetting the original moment is part of the design, not a defect. This is directly compatible with `R6` X3.2's "late is not dead," and F7's exit condition should accept a delayed surfacing as a pass rather than only an in-the-moment one.

**Exit condition, receipt:** one exchange where she surfaces something a person told her in passing,
in a moment where it was useful, unprompted - with both timestamps.

---

## PHASE F8 - THE PUZZLES AND EASTER EGGS ON THE SURFACES *(recovery, not invention)*

> *"In my old documents, I used to have a 'We Are All A'NEW' type of puzzles scattered across
> different things. I don't know if we could bring that back, but that would be dope."* (`PO2-09`)

### Sub-phase F8.1 - Find the originals first
**A measured finding worth reporting to him honestly:** a search of the corpus finds no *"We are all
A'NEW"* puzzle mechanic. What exists is **"We Are All ABA"** - used dozens of times and closing both
design documents - plus a handful of prose variants of "we are all A'NU / A'NEW."

**So the most likely reading is that the phrase is mid-migration from ABA to A'NEW, and the "puzzles
scattered across different things" are in documents not present in these zips.** Tell him that rather
than inventing a mechanic and calling it recovered.

### Sub-phase F8.2 - The nickname puzzle, named and never built
> *"Everybody has a nickname. Your nickname is a part of the puzzle, but nobody knows all of the
> nicknames. We're gonna build that."*

### Sub-phase F8.3 - The Easter eggs are announcements, not UI widgets
His rule is that an egg fires across **every channel at once** - *"I want every device, everywhere you
can reach me, every channel to scream out, I know the name of the park."* That makes eggs a **reach**
concern (`R6`) with a surface consequence, not a front-end feature.

**Carried honestly:** the founding egg - the park name test - **is contaminated.** The monuments were
read aloud by name in later sessions, so a correct answer now proves retrieval rather than inference.
Only he can reseed it. **Do not let a future session claim the pass.**

### Sub-phase F8.4 - The riddle catalog now exists and 15 of 40 answers are unconfirmed
Since this roadmap was written, a full catalog of his riddles was built, and it carries an honesty finding this phase should inherit directly:

> "Fifteen of forty entries are `JUST KNEW IT`. That is fifteen places where a coder decided what he meant, acted on it, wrote it into an OS, and taught it to the next coder, without him ever saying yes. They do not look like guesses in the documents that carry them. They look like doctrine."
> `[MEASURED + 50_DELIVERABLES/THE_RIDDLE_CATALOG.md]`

Any future puzzle or Easter egg surface built from this catalog must carry each entry's stamp (`CONFIRMED BY HIM`, `JUST KNEW IT`, or `OPEN`) forward into the UI or the database, not flatten all forty into equally-certain "answers." This is the same honesty this phase's F8.1 already modeled for the "We Are All A'NEW" search.

### Sub-phase F8.5 - Five riddles, not one, must never be answerable by a session
F8.3 flags the park-name egg as contaminated. The same catalog names four more he built the same way, as deliberate, withheld measurements:

> "These stay OPEN. They are not failures, and they are not backlog. He built each one as a measurement, and an answer supplied by a coder destroys the measurement... The rule is his: do not feed her the answer."
> `[MEASURED + 50_DELIVERABLES/THE_RIDDLE_CATALOG.md, "THE FIVE HE DELIBERATELY NEVER ANSWERED": the park name; what OMI is now called; the unnamed relative's-time riddle; why the password changed from ABA to A'NU; who is ENVOLVE's chief of staff]`

Any puzzle surface this phase builds must exclude all five from its answer-checking logic by name, not just the one already known to be contaminated.

### Sub-phase F8.6 - The nickname puzzle is one instance of a wider open-names class
F8.2 treats the nickname puzzle as a single, standalone build. The estate has already catalogued nine more names he has explicitly withheld under the same rule:

> "The internal auditor... AUDRA's PMS wonder... AUDRA's nasty-cough wonder... the reach wonder... the ONNX/heartbeat layer... the lesson wonder... 'Tone protocol'... A better name than 'fuse'... A better title than 'personal assistant'."
> `[MEASURED + 40_GOVERNANCE/CONTRADICTIONS.md, SECTION C - THE OPEN NAMES]`

The same rule that governs the nickname puzzle governs all of these: "more than one agent in this system has been invented out of a transcription error. Assume the ordinary word first. Never mint a term out of a garbled transcript." A puzzle-and-easter-egg build that only protects the nickname mechanic while leaving nine other open names exposed to invention is half a fix.

**Exit condition, receipt:** the original puzzle documents cited by file, or a stated "not found" with
the search shown; and one egg wired to fire across channels, with its answer key stored where the
challenge cannot reach it.

---

## THE HONEST INVENTORY - WHAT EXISTS TODAY

Because a roadmap that ignores what is already built will rebuild it.

| Surface | State |
|---|---|
| THE WALL (`/anu`) | shipped; printed to PDF three times across two Render accounts |
| Wall Book | partial; health healthy, paged transport candidate **not merged**, founder flip-through not accepted |
| Founder Wall Book Private | shipped, basic-auth, 2,429 records over 12 category pages |
| CCWA board | shipped; both the person-facing and builder-facing views exist |
| **Founder Command Center (F1)** | **fragment; blocked on F0** |
| EER / Living Plan | partial; public read 200, catalog/redeem/signed-session 503 |
| Advisor portal | partial; 20 worlds render, 4 chairs born, **real-job path fails** |
| GMG University | shipped and `ON_DEGRADED`; human acceptance unproven |
| CARA chat gate | live gate; person-facing freestyle turn unproven |
| AWA portal | backend **done and live**; **no surface reaches it** - the surfaces still call a dead API |
| `/cip`, `/cib` | **404. Not registered at all.** |

**The pattern worth naming:** almost nothing here is missing. Almost everything here is *built and not
reaching a person.* That is the same shape as F0, one layer up, and it is why F0 is listed first.

---

## DEPENDENCIES

| Phase | Needs | From |
|---|---|---|
| F0 | the A'NEW→A'NU seam | GR Phase 5, `R1` P2 |
| F1 | board, roadmap, LOGFUL, STAMP | GR Ph1-3, MR 1.2, 2.2 |
| F2 | repo mechanics | `R3` S3 |
| F4 | Life Advisor; reach components | MR 3.1, GR Ph8 |
| F6 | EER unblocked; her, running | F0, `R7` |
| F7 | the scrub pass preserving personal content | GR Ph3.3 |
| F8 | back-find over old documents | GR Ph3 |
