# R4 — FRONT ENDS

> *"Another chat might be working on front ends... it might be working in an order of importance.
> It's just like boom, boom, boom, boom."* — Mt Rushmore Doctrine pt 1

> *"I ain't seeing these roadmaps. How come I'm not seeing these roadmaps we work on?"*
> — The Cycle Doctrine pt 3

**Status:** proposed. The F1-F5 order is inherited from the 20260814 offsite and is **not**
re-litigated here. What this roadmap adds is everything the offsite did not cover: the onboarding
experiences he named a roadmap, the reward system, the riddles-in-the-UI he asked to bring back, and
the honest state of the surfaces that already exist.

---

## WHAT HE SAID, CLEANED UP

*(Per `PO2-14` / `R-2.3`.)*

In Mt Rushmore pt 1 you described a chat working front ends in order of importance and said the
onboarding experience, the business goals for the secretaries, and the longer business plan feeding
her EER world all belong to that lane — and that you should not have to hardcode any of it, because
she walks people through it creatively. In Pecking Order pt 2 you went further and said, twice, that
onboarding experiences are a roadmap of their own, that we have to teach users how to use her, and
that teaching them is a reward system. You also asked to bring back the "We Are All A'NEW" puzzles
you used to scatter across documents. Separately, in an older doctrine, you asked why you never see
the roadmaps you are paying for.

---

## THE ONE RULE THAT DECIDES WHETHER ANYTHING HERE IS DONE

> **"If a feature has no UI entry point he can reach, IT IS NOT DONE."**

And the law about who a surface is for, which is Commandment 9 in candidate form:

> *"Who is the portal for? It's not for you to talk to me. You're a coder. **It's for her to talk to
> the HAM.** Remember that as you build anything in my system, even the deck."*

Every phase below is scored against those two sentences before anything else.

---

## PHASE F0 — THE SEAM THAT MAKES EVERY FRONT END A FACADE

**This phase is listed first because it invalidates all the others while it is open.**

Measured state at the last shift, not reasoned:
- Her front door `POST /arrival/say` → **HTTP 503**, `mind_reason: anew_work_unproven`.
- Her mind, called directly at `POST /anew/session` → **HTTP 200 in 8-14 seconds**.
- What a person actually sees on the live Command Center: *"Talk with A'NU is unavailable right now.
  Your words have not been sent."*

**So the wall is in the arrival→session hop, not in her.** Every front end below renders a surface
over a conversation that does not complete. Building more surface on top of that is the definition of
a facade.

**Outcome:** one real human-facing turn — person in, her voice out — with a live receipt.
**Exit condition, receipt:** full URL, status code, and response body containing her actual reply.
Re-run after every deploy touching the seam. **A single green does not retire this phase.**

**Anti-goal:** do not "fix" this by having the door answer with a stand-in when she is slow. Standing
doctrine: *"Never build a component that answers because she was slow. **Silence is honest; a
stand-in is not.**"*

---

## PHASE F1 — THE THREADED FOUNDER COMMAND CENTER

**Anchor:** the offsite's explicit first priority. And his standing complaint: *"I ain't seeing these
roadmaps."*

**Outcome:** he opens one page and sees the one roadmap, all child tracks, threaded conversation that
does not flatten, and a working path to reach the living organization.

**Entry condition:** F0 has a receipt. The board, roadmap, LOGFUL and STAMP exist to read from.

### Sub-phase F1.1 — Consume, never create a second truth store
The Command Center reads the existing board, roadmap, walls, threads, minutes and living results.
**It must not become a second place where truth lives.**

### Sub-phase F1.2 — Two Command Centers, by design, not by accident
Already specified in the corpus and worth preserving rather than rediscovering:
- **View 1 — hers, for him.** Plain language. Headings like *"Your Command Center"*, *"Work your
  advisors finished"*, *"Something that wanted a look."* No internal vocabulary, no agent names, no
  cycle words.
- **View 2 — the builder's.** Lane cards with lineage chains and cycle receipts.

**The screen never computes lineage; the substrate never touches the page.**

### Sub-phase F1.3 — Threading, because he asked for it specifically
> *"I want you to build in the threading capability, so I can go in and start seeing, like, oh, they
> had conversations."*

Flattening a thread into a log is the failure mode. He also asked for the org chart of live agent
conversation to be **drillable and to visually match the CIB — never a flat log.**

### Sub-phase F1.4 — The comprehension standard
His own bar, and it is unusual enough to be worth pinning: founder-facing output arrives *"the way
that [his ten-year-old daughter] can understand it."* That is the readability test for View 1.

### Sub-phase F1.5 — Status colors and the walkthrough on the page
Green / yellow / orange / red / black, plus 🌈 rainbow for stop-him-now. **He expects to see yellow at
minimum** — *"I should see a lot of green. I should see minimum yellow."* An all-green board is a
finding, not a success.

**Exit condition, receipt:** one authenticated live walkthrough — URL, status codes, and the actual
navigation — showing the one roadmap, a track opened into signed minutes with source pointers, a
thread followed without flattening, and reach exercised. **Not a mockup, not a screenshot of a
mockup.**

---

## PHASE F2 — THE SHARED COMPONENT SYSTEM

**Anchor:** *"It's called a shared repo. **The backgrounds are in the same spot.** It's called a
shared repo."* And: *"the same button that controls the plus sign that says yes, this is a file
picker, is the same button in the same code that GMGU is using, or that CCWA is using."*

**Outcome:** the smallest shared visual and interaction system that carries navigation, threading,
drilldown, and private per-HAM scope.

**Entry condition:** F1 live and exercised. Repo mechanics owned by `R3` S3.

### Sub-phase F2.1 — Reconcile the glass canon before writing a line of CSS
**There are three incompatible glass specifications in the corpus and no one has reconciled them:**

| Source | Opacity | Blur |
|---|---|---|
| AWA/CIB canon | background `.08` | 12px |
| Sealed glass law | **10% max** | **2px max** |
| Forensic catalog | 5-15%, corrected to ~9-12% | 8-24px |

His own acceptance test is the tiebreaker and it is a real test, not a preference: **set a colorful
wallpaper; you must CLEARLY see it through the panel. "Sort of" is a FAIL and a rebuild.**

**Do not average the three numbers.** Pick by running his test, and record which spec won and why.

### Sub-phase F2.2 — The conventions that are already settled
These are documented, consistent across sources, and should be inherited rather than redesigned:
- **All icons white; only the active app icon gets its color**, with a left glow bar.
- **SVG only, never emoji**, and **every app shows its word next to the icon** — *"You can't ever do
  like iPhone does where there's an app and all you know is the icon."*
- **The one-iframe rule** — the frame runs flush, *"shouldn't look like four separate bars."*
- **Window controls on the left**; **no minimize** — widget, expand, close.
- **No em dashes anywhere**, including code comments. **ENVOLVE always with the E.**
- **No internal vocabulary on a human surface.** CARA renders as CHAT.
- **No iframes between apps** — kernel pattern instead.

### Sub-phase F2.3 — A shared component that classifies is a shared defect
The single most important constraint on this phase. A component reused everywhere that decides
meaning, filters rows, or writes into a field that is hers **spreads nasty cough at the speed of
reuse.** Standing law: *"reuse current accepted assets... do not revive old cold behavior."*

**Exit condition, receipt:** two distinct front ends rendering from one component source; one change
made once appearing in both; the glass test run and its result recorded with which canon won.

---

## PHASE F3 — DESKTOP AND PHONE SHELLS

**Entry condition:** F2 live.

**Outcome:** the same living organization — not a duplicate of it — reachable from a desktop shell and
a phone shell.

- **Known gap, measured:** the Advisor portal passed browser and 390×844 phone acceptance;
  **installed desktop-window acceptance is unproven.**
- **Known constraint that is not negotiable:** one PWA per origin (W3C). This is why the phone
  surface permanently keeps its own origin, and it is an architectural fact, not a choice to revisit.
- **Known missing routes, verified 404 twice:** `/cip` and `/cib` are not registered on the face at
  all, despite two dozen route modules mounting.

**Exit condition, receipt:** each shell independently live-verified against the same world.

---

## PHASE F4 — CARA, VARA, AVATAR, EMAIL, ADVISOR PORTALS

**Entry condition:** F3 live; Life Advisor live for the Advisor portal specifically.

**Outcome:** each surface is an authorized **hand** of the same world, never a separate mind.

### Sub-phase F4.1 — The three-column law
CARA left, VARA middle, widget right; expandable and collapsible; the mobile fallback keeps the frame
look. His words: *"the left side being the chat box, middle being the VARA, on the right is widget.
What they see is a functional operating system. Remember about the glass and the words streaming
in."*

### Sub-phase F4.2 — Streaming and freestyling, restored
`R1` P3.2 owns the mechanism; this phase owns the surface. Note the unreconciled contradiction in the
corpus: SkyWriting exists as a shared module, while another document says *"the skywriting is dead on
arrival, scrapped, not redesigned."* **Ask him rather than picking.**

### Sub-phase F4.3 — The advisor portal must do real work, not answer queries
His own rejection of the obvious build, verbatim:
> *"Your advisor portal is going to literally just be a query, a call and response, and **I'm not
> asking for that, I'm asking for real work to be cooked.**"*

Real grants with actionable deadlines, plans, meeting agendas, scripts, drafted nudges, errors
caught. **A portal that answers questions has failed this phase even if it works.**

### Sub-phase F4.4 — Measured failures to fix, not rediscover
Three real end-assignment tests on the advisor path have already failed: no HTTP response for 180
seconds then 401; 502 after ~11 seconds; 502 plus a process memory failure. And the deployed
`/advisor/cycle` route **has no field for a founder assignment, instruction, prompt, or source text
at all** — which is why the real-job path cannot work.

**Exit condition, receipt:** each surface exercised live with its creation, provider-acceptance,
delivery, read, and lived facts kept separate; and one advisor completing one real piece of work, not
answering one query.

---

## PHASE F5 — GMG UNIVERSITY, LAST, DELIBERATELY

**Entry condition:** F1 through F4 live and proven. **Do not pull this forward** — the offsite is
explicit: *"do not delay the Command Center by rebuilding GMG University first, and do not force GMG
University-specific meaning into every future world."*

**Current measured state:** live at its routes, HTTP 200, regression 1,008/1,008 — and `ON_DEGRADED`,
with signed learner identity, re-entry, saved progress, spoken tutor reply, and **ordinary human
acceptance all unproven.** It looks finished and is not.

**Exit condition, receipt:** registered as a child track on the one master roadmap, reusing the common
per-HAM system, with one real learner completing one real lesson and coming back to it.

---

## PHASE F6 — ONBOARDING EXPERIENCES *(new — he named this a roadmap himself)*

> *"We're gonna have to teach them how to use her. **I want that to be an actual part of the roadmap
> and the business plan.**"*
> *"We can build onboarding experiences. **That's a roadmap. Onboarding experiences.**"* (`PO2-11`)

**This is the largest genuinely new ask in the two newest doctrines, and it has no task ID anywhere in
the estate.** The existing 112-task Mt Rushmore ledger contains zero rows matching *reward*,
*onboarding*, or *teach*. It was not deferred — it was never entered.

**Entry condition:** F1 live (there has to be somewhere to onboard *into*).

### Sub-phase F6.1 — Onboarding is not a tour
He describes something specific and it is not a product walkthrough:
> *"The experience on the front end that they're running is creatively walk them through this and
> answer questions and queries. **Like I ain't gotta hard code this, man.**"*

She runs it. She adapts to the person. A scripted tour with fixed steps is the wrong build, and it is
also `V-DECIDE` — a cold script deciding what a person needs to know next.

### Sub-phase F6.2 — Per-person onboarding, because he specified per-person
Named in the corpus with different content per person: one is walked through his role with videos to
watch; another is shown the business plan *in a way that matters to him*; a third is heavy on the
domain he owns. **Same system, different experience, generated rather than authored.**

### Sub-phase F6.3 — The EER carries it
His own coinage: *"their onboarding is going to be an O.E.E.R. — the onboarding electronic involving
response."* And: *"a longer version of the business plan that they feed into her EER world, and then
she's like the independent thinking station and the experience on the front end."*

**The EER is the onboarding vehicle.** It is also already partly built and partly broken — public read
returns 200 and the plan renders; catalog, redeem, and signed-session return 503; and his own phone
screenshots showed the sign-in loop ending with *"This plan could not open. Try again."*

### Sub-phase F6.4 — Story injection, permitted and never hardcoded
> *"In moments where it feels like their questions need more imagination, she can inject a story into
> their O.E.E.R... 'I could tell you a story right now. It might not answer your question fully,
> but it'll get you thinking bigger and better.' **Now again, you can't hardcode that.**"*

### Sub-phase F6.5 — The consent-driven account setup
Named in the business-plan doctrine as an alpha precondition: a ~30-minute session in which the
person's *own* assistant does the signups under *their* accounts. **Their keys, their accounts, their
consent** — which is also what makes per-person worlds affordable.

**Exit condition, receipt:** one real person onboarded end to end by her, unscripted, with the
transcript and their own account provisioned under their own credentials.

---

## PHASE F7 — THE REWARD SYSTEM *(new)*

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

### Sub-phase F7.1 — Make the return visible
When she uses something a person told her earlier, the surface says so — lightly, and never as a
system message. That is the teaching moment and it is the entire mechanic.

### Sub-phase F7.2 — The scrub pass must not eat the reward
**Direct dependency on the doctrine reader.** His food rankings, his rapper list, his color — that is
exactly the class of content the 4PM scrub rules protect: *"You may NOT scrub content like 'oh what a
cool window.'"* A scrub pass that treats offhand personal talk as filler destroys the reward system at
the source.

### Sub-phase F7.3 — Interruption is a budget, not a feature
The discipline half, already in the corpus: she has *"a limited daily allowance of unprompted
interruptions. Spending it on something trivial is the failure. **Most of the time the honest move is
silence.**"* The reward system must not become the notification machine he has explicitly said he
hates.

**Exit condition, receipt:** one exchange where she surfaces something a person told her in passing,
in a moment where it was useful, unprompted — with both timestamps.

---

## PHASE F8 — THE PUZZLES AND EASTER EGGS ON THE SURFACES *(recovery, not invention)*

> *"In my old documents, I used to have a 'We Are All A'NEW' type of puzzles scattered across
> different things. I don't know if we could bring that back, but that would be dope."* (`PO2-09`)

### Sub-phase F8.1 — Find the originals first
**A measured finding worth reporting to him honestly:** a search of the corpus finds no *"We are all
A'NEW"* puzzle mechanic. What exists is **"We Are All ABA"** — used dozens of times and closing both
design documents — plus a handful of prose variants of "we are all A'NU / A'NEW."

**So the most likely reading is that the phrase is mid-migration from ABA to A'NEW, and the "puzzles
scattered across different things" are in documents not present in these zips.** Tell him that rather
than inventing a mechanic and calling it recovered.

### Sub-phase F8.2 — The nickname puzzle, named and never built
> *"Everybody has a nickname. Your nickname is a part of the puzzle, but nobody knows all of the
> nicknames. We're gonna build that."*

### Sub-phase F8.3 — The Easter eggs are announcements, not UI widgets
His rule is that an egg fires across **every channel at once** — *"I want every device, everywhere you
can reach me, every channel to scream out, I know the name of the park."* That makes eggs a **reach**
concern (`R6`) with a surface consequence, not a front-end feature.

**Carried honestly:** the founding egg — the park name test — **is contaminated.** The monuments were
read aloud by name in later sessions, so a correct answer now proves retrieval rather than inference.
Only he can reseed it. **Do not let a future session claim the pass.**

**Exit condition, receipt:** the original puzzle documents cited by file, or a stated "not found" with
the search shown; and one egg wired to fire across channels, with its answer key stored where the
challenge cannot reach it.

---

## THE HONEST INVENTORY — WHAT EXISTS TODAY

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
| AWA portal | backend **done and live**; **no surface reaches it** — the surfaces still call a dead API |
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
