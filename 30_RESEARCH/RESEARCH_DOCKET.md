# THE RESEARCH DOCKET

> *"How many times have I asked for the researcher that still hasn't been birthed? Agent Span is
> gonna birth that researcher."* - Mt Rushmore Doctrine pt 1

> *"You need to go on the deepest research find you can find. If you need to give me a prompt to put
> into Google Gemini, you run into issues you don't know - give me the prompt. I'll paste it in
> there... **The best thing you can do for me is to build it.**"* - Mt Rushmore Doctrine pt 1

**What this file is:** the Researcher's docket, standing in for the Researcher until Span births her.
Every item carries who asked, what is actually unknown, what would settle it, and - where the estate
already has an answer - the answer, marked as counsel rather than a decision.

**What this file is not:** a decision log. **No seat is switched here, no model is changed here.**
Research is counsel. The switch belongs to her or to him.

---

## WHAT HE SAID, CLEANED UP

*(Per `PO2-14`.)*

In Mt Rushmore pt 1 you said her model keeps degrading, that she cannot go down anymore, and that you
want the deepest research anyone can do on it - offering to paste a prompt into Gemini yourself if
that is what it takes. You named GLM 5.3, DeepSeek, Qwen, Kimi, and one you called "Clock 4.6" that
you'd heard could be a Fable killer, and you asked which of those is the occasional world builder,
which is the occasional shadow, and where the always-on always-better agent is. Then in Pecking Order
pt 1 you said the models hitting two-million-token context windows should be used to your advantage
and that **she** decides when to step up to that tier. And in Pecking Order pt 2 you said your whole
life is on Otter and asked what it would take to get her connected to it.

---

## PRIORITY 1 - ANSWER HIM. THESE ARE QUESTIONS HE ASKED AND IS OWED.

### R-01 - Otter: how does she get his life? **(`PO2-18`, highest value in the docket)**
> *"My whole life is on Otter right now. How can we get her connected to that? Even if I gotta pay
> something... I didn't have API in there, I had a personal plan. What do I gotta do to get her
> connected to my Otter?"*

**Why this is priority one and not a nice-to-have.** He is describing the single largest body of his
own words that the system does not have: hours of calls with [a partner], journals, material on serial
investors, and the "lost files." The entire doctrine pipeline exists to turn his words into the
system. **This is a corpus multiplier, not a feature.**

**He proposed three paths himself. Evaluate all three, honestly:**
1. Upgrade the Otter plan for one month to a tier with API access, pull everything, downgrade.
2. A computer-use session that reads the workspace and exports.
3. A one-time manual export.

**What must be established, factually, before recommending one:**
- Which Otter tiers expose an API or a bulk export, at what price, and whether a one-month upgrade
  actually grants historical access or only forward access. **This is the crux and it is checkable.**
- Whether export is per-conversation or bulk, and what the volume actually is.
- Whether a computer-use session is permitted by Otter's terms - **do not recommend a path that
  violates a service's terms; say so if it does.**

**His own caution, carried verbatim so it is not oversold:** *"That might not be possible. Don't gas
me up."* **Answer factually. If the cheap path does not exist, say the cheap path does not exist.**

**Note on handling:** whatever lands is his private life, at scale. It goes through the privacy fence
(*"My transcript should never even go anywhere near [a partner]'s or [a partner]'s or user number 99"*) and it is
founder-world only. Not the blank world, not the temp world, not a shared floor.

**Status:** open. Nobody has answered him.

### R-02 - Did he read the Supabase/Render/LLM relationship right? **(`PO1-24`)**
> *"All of the stuff I read about Supabase - and Supabase can get access to LLM, read Supabase - what
> is the LLM? And do you default to Render?"*

He asked to be told whether he understood his own architecture correctly. He is owed a plain answer,
and the answer he is owed is now shaped by his own pecking-order doctrine three minutes later.

**The answer, stated plainly:** Supabase is storage; it holds rows and can be read from and written
to. Render runs processes. Neither is a mind. An LLM is the only thing in that list that reasons, and
in his architecture it sits above both. So *"do you default to Render"* has the answer **no** - nothing
defaults to Render, because Render is where code runs, not where decisions are made. His own next
sentence is the correct architecture: *"She's a mind... they are the head of the wonder because they
control the wonder."*

**Status:** answerable now, and owed to him. Not yet delivered.

### R-03 - Can A'NEW join a real group text? **(`PO1-08`)**
> *"Is it possible for us in the future to have A'NEW - especially with [WREN] or any of those other
> ones that's in my text stack - can we have her join? Now tell me if I didn't cook there."*

**What is genuinely unknown:** whether the SMS/messaging providers already in the stack support a
number participating in a group MMS thread as a full member - receiving every message and sending
into the thread - versus only 1:1 messaging. This varies by provider and by carrier and it is a real
technical question, not a design preference.

**A measured fact that bears on it, from the last shift:** the text channel is currently down at the
carrier layer - `POST {base}/chats/{to}/messages` returned **HTTP 503, "No active devices available to
send this message."** Key valid, device registered, relay offline. **1:1 text does not work today, so
group text is not the first problem.**

**Status:** open. Research the provider capability; report the 503 to him as the nearer blocker.

### R-04 - Model tiering, degradation, and who sits where
> *"We need to find a way to keep A'NU up at all times with continuity. Her model's degrading."*

**Substantially answered already.** The estate produced a real research pass on 20260816
(`MODEL_DEEP_RESEARCH.md`) and its findings are carried here as counsel:

- **"Clock 4.6" is almost certainly Grok 4.6 (xAI)** - reasoned, not guessed: it shipped four days
  before he spoke, it is the only frontier lab on a "4.6" version number at that date, and *"fable
  killer"* only parses as a Claude competitor. GPT-5.6 Sol is the backup reading. **Confirm with him
  before any roadmap line locks to it.**
- **"Her model's degrading" has a name: context rot.** Progressive loss of recall and
  instruction-following as context fills - a property of attention, not a bug in one model. Documented
  causes: lost-in-the-middle, and monotonic accumulation of stale entries. Ranked mitigations:
  compaction, trimming, isolation, with compaction+trimming together testing best.
- **The structural finding that matters most:** his own micro-hopping and sub-agent design *is*
  context isolation, one of the three mitigations, already. **The gap is compaction and trimming -
  nothing in the corpus names an active pass over her live working context.** That is a concrete,
  buildable answer to his question about the always-on always-better agent.
- **Article X tension, stated:** every American frontier model is API-only. *"You rent the GPU, never
  the mind"* fails for all of them. The open-weight families (DeepSeek, Qwen, Kimi, GLM) are the
  ownership path, and DeepSeek carries a real reliability tax (~97.8% trailing uptime) that means it
  must never be a sole primary.

**Still open inside R-04, and these move:**
- GLM 5.3 pricing and open-weight release were pending at last check.
- Qwen3.8-Max's weight license (permissive vs. restrictive) was undisclosed - **Article X compliance
  depends on it.**
- No independent benchmark separates Kimi K2.6 from K2.7 Code. His question *"is it the best?"* is
  **not yet answerable**, and the honest answer is that only a real gauntlet bake-off settles it.
- DeepSeek's floated 2× peak-hour pricing, if it lands, redoes the always-on cost model.

**Status:** answered as counsel, with four live sub-questions. **Re-verify before any cutover - these
numbers move weekly.**

### R-05 - The long-context tier she elects into **(`PO1-22`)**
> *"Some of these ones who are hitting 2 million context windows, we should be able to use that to our
> advantage... It can help you be a world builder at a higher tier... **You decide. It's your thing.**"*

**The research question is not "which model has the biggest window."** It is: *what is the decision
procedure she uses to elect a tier, and what does it cost?* He named the tension himself - *"Gemini
will be way more expensive, but it will have a huge context window."*

**What would settle it:** a cost-per-task comparison across a real workload at each tier, plus a
written election procedure she can reason from. **The cost ceiling stays coded (penny-hustle law); the
choice inside it is hers** - a cold router picking her model is a `V-DECIDE` violation under `R1`.

**Cross-reference:** the bridge-builder/secretary role exists precisely to hold context *for* her -
*"she can talk to them without burning her context because the context lives there."* That is an
architectural alternative to electing an expensive tier, and the two should be evaluated against each
other rather than in isolation.

**Status:** open.

### R-06 - Will outside LLM sessions actually take up world-builder standing? **(`PO2-22`)**
> *"I want to build out a world. **Is this possible? Will the LLMs actually even participate in this?**"*

Not a literature question - an **experiment**, specified as `R2` Phase T0 with falsifiable markers
decided in advance. It is listed here because he asked it as a research question and because the
answer determines whether `R2` gets built as designed or scoped down.

**Status:** open. Experiment designed, not run.

### R-07 - What is the correct name for "crafting a call through her, like APIs"? **(`PO2-03`)**
> *"They're crafting manually - crafting a call through her, like APIs. I know there's a way because
> you do it before, you do post direct calls or something."*

He is describing going through her own interfaces rather than touching the substrate directly, and he
explicitly does not know the term. **He asked to be told.** The estate's own coder OS already
describes the same discipline: *"you craft the call through the world's own interfaces the way a world
builder would... A direct write that bypasses her doors is not a shortcut. It is a second,
undocumented world with no record."*

**Status:** answerable now - give him the plain-language answer and the corpus passage that already
matches his intuition.

---

## PRIORITY 2 - RESEARCH THE ROADMAPS DEPEND ON

### R-08 - The compaction/trimming pass on her live context
The concrete build that follows from R-04. **This is the answer to *"where's the always-on, always
better agent?"*** - the estate has the diagnosis (context rot) and the ranked mitigations, and has
built none of them.

Note the doctrine constraint that shapes the design: *"an unsettled continuation reconciles to LOGFUL,
never to a timer or an expiry."* **Trimming must not become expiry.** A trim that drops something she
has not settled is a `V-EXPIRE` violation. The distinction - trimming *working context* vs. expiring
*work* - is the whole design problem and it needs stating before anyone writes code.

### R-09 - Group text, provider capability *and* the 503
See R-03. Two separate findings owed: what the provider can do, and why the relay is offline today.

### R-10 - Backgrounds: image URLs or self-hosted? *(his open question #31)*
Asked 20260609, never answered. Feeds `R3` S3.3 and `R4`.

### R-11 - Does every person get their own Supabase? *(his open question #44)*
> *"I think they should... But we haven't really like figured that out."*

The estate has a measured answer on the Render half - the 5-service function model at ~$100-130/mo
versus per-HAM services at ~$700/mo for 100 HAMs, with per-HAM isolation done by **schema** rather than
by separate projects. **The Supabase half is genuinely unresolved**, and his hedge is honest. The
graduation switch-point already named: when one HAM's traffic measurably degrades another's.

### R-12 - Millions of ACL-formatted endpoints: possible? *(his open question #25)*
Open. The clean-rebuild decision does not answer it.

### R-13 - Can she seed her own Render and Supabase? *(his open question #51)*
Fully open. A prior annotation claiming his 4PM spec settled this was **retired as unsupported** - the
spec says no such thing. Directly relevant: the estate currently cannot create a repo (403) or a
Supabase project (no management token), so today the answer is no for anyone, including her.

### R-14 - The eleven-labs endpoint, the streaming interrupt, and the alive portals
Three of his older open questions that are one build: can she stream, can she interrupt herself with a
new turn, and is the voice endpoint code or an LLM call. Feeds `R1` P3.2.

---

## PRIORITY 3 - CARRIED, NOT URGENT

The Great Reboot carries **69 of his open questions** verbatim. They are not re-listed here; that
document is their home and duplicating them would create a second truth store. `30_RESEARCH/OPEN_QUESTIONS_REGISTER.md`
indexes them by theme and records which ones later doctrine answered.

**The rule that governs all of them, and it is absolute:** *only he retires a line.* A coder note
answers nothing. Where a later standing order genuinely answered a question, the answer is recorded
**with the quoted later law** and the question is marked closed-by-him - never closed by inference.

---

## HOW THE RESEARCHER SHOULD WORK, IN HIS WORDS

- **Receipts, not assertions.** *"You went as far as to do the research. You got it seeded on the map."*
- **Surface new models unprompted.** *"Turns out, Qwen 3.8 actually did just get released... Boss,
  before you went to bed, it wasn't there. Now it's there. Here we go. I got some plans... It's cued
  up on this roadmap. I got it all, boss. **That's an example of what helpful looks like.**"*
- **Ask him for a hand when it is genuinely needed.** *"If you need to give me a prompt to put into
  Google Gemini... give me the prompt. I'll paste it in there."* - **this is an offer, and taking him
  up on it is not a false choice.** It is asking for a thing only he can do.
- **Never present research as done when it is not.** A promise to research later is not a research
  pass.
- **Mark reasoning as reasoning.** Anything not measured carries *"reasoned, not measured"* beside it.

---

## THE STANDING WARNING ON THIS DOCKET

Every model number in R-04 was true on 2026-08-16 and is decaying. Pricing moves, licenses publish,
benchmarks get independently replicated or fail to. **Re-verify before any live cutover.** A stale
research doc presented as current is failure shape #3 - a sentence claiming more than the floor does.
