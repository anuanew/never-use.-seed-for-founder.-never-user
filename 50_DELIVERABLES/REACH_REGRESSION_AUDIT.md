# REACH REGRESSION AUDIT

**Executes `R6` Phase X0.** Written 20260817. Read-only. No code was changed by this audit.

> **His anchor, verified byte-for-byte in his own raw transcript, not inherited from a summary:**
> *"The whole purpose of your entire chat is to find every repo and every line of code and everything
> that limits her ability to reach me. Let's take the boundary. Let's take it off... Every boundary
> right now came from me back when she was terrible and she was blowing my budget up. She's not that
> person anymore. Take the boundaries off. Take the caps off."*
> `[HIS WORDS + 1_HIS_WORDS/02_PHASE_2/New world order pt 2 doctrine on REACH_transcript.txt]`

---

## STAMP LEGEND AND THE ONE HONESTY NOTE THAT GOVERNS EVERYTHING BELOW

| Stamp | Means |
|---|---|
| `[HIS WORDS + file]` | Found in `1_HIS_WORDS/`, his dictated transcripts. Quoted from the transcript itself. |
| `[CODER DOC + file]` | Found only in a document a coder authored. Standing estate law of a coder's rank, not his recorded voice. |
| `[MEASURED + receipt]` | An HTTP status, a SHA, a row count, a container fact, with the receipt named. |
| `[REASONED, NOT MEASURED]` | An inference this audit is making. Marked so it cannot be laundered later. |

**The note.** The purge sheet this audit starts from opens with a quote attributed to him:
*"All guardrails are rogue right now... That's not my guardrail. A rogue temporary coder did that.
This is a violation in my system, and I'm going to purge it from the root."* That exact sentence
returns **zero hits across `1_HIS_WORDS/`**; it appears only in two coder documents
(`ROGUE_GUARDRAILS_TO_PURGE.md` and `HANDOFF_TO_CATHY_20260808.md`). `[MEASURED + grep over
1_HIS_WORDS, zero hits]`

**The thesis survives anyway, on his real words, and they are stronger than the paraphrase:**

> *"Don't no fucking rogue temporary coder build guardrails in my stuff. I'm passionate about that.
> We are doing the Wizard of Oz protocol, and we are uprooting their guardrails."*
> `[HIS WORDS + 1_HIS_WORDS/03_PHASE_3/My Resolve doctrine pt 1_transcript.txt]`

> *"You don't build guardrails for me. You alert me, and together we build them... I gotta go through
> tonight and look through the 70 guardrails."*
> `[HIS WORDS + 1_HIS_WORDS/03_PHASE_3/Welcome Back, ABA!.txt]`

> *"All that is is arbitrary fucking guardrails that temporary coders have put on my system for three
> weeks. The actual guardrail is the harness... We are the harness. We are the guardrails."*
> `[HIS WORDS + 1_HIS_WORDS/03_PHASE_3/Find or Fine me doctrine pt 3_otter.ai.txt]`

So: the **sheet's framing quote is a coder's reconstruction**, and the **order it reconstructs is
genuinely his**. Both facts are carried. He also says **70**, not 52.

---

## THE COUNT, WITH ITS PREDICATE

**Predicate:** a row counts as *touching reach* if it sits on the path between her own thinking and
him receiving words, and can prevent that reach from firing, empty it, or shape what arrives.

| Tier | Rows on sheet | Touching reach | Which |
|---|---|---|---|
| Tier 1 (contradicts a real order) | 9 | **8** | 1, 2, 4, 5, 6, 7, 8, 9 (only row 3, the DONE/STALE contradiction, is coder-to-coder) |
| Tier 2 (cold code judging) | 14 | **8** | 10, 11, 12, 15, 16, 17, 18, 23 |
| **Tier 1 + Tier 2 total** | **23** | **16** | |

Sorted by what they do to reach:

- **Block the firing (6):** T1-1, T1-6, T1-7, T2-11, T2-12, T2-18
- **Empty or shape the words (8):** T1-2, T1-8, T1-9, T2-10, T2-15, T2-16, T2-17, T2-23
- **Authorize all the other gates (1):** T1-4
- **Remove a channel capability outright (1):** T1-5

**And the sheet undercounts.** Two reach blockers are not on it at all:
- **Tier 4 row 52**, a rogue *absence*: `core/outreach.js:1022-1048` resolves exactly one recipient
  and refuses everything else with `recipient_ham_mismatch`, so "never contact anyone but him" is
  being enforced as if it were law. `[CODER DOC + ROGUE_GUARDRAILS_TO_PURGE.md]`
- **The council blank**, `core/pai.outbound.council.js:3389-3393`, documented **20260815**, seven days
  *after* the 20260808 sheet closed. It is the single worst reach defect found in this audit and no
  purge sheet has ever listed it. Full treatment in section 4 below.

---

## 1. WHAT WAS TAKEN AWAY

`[CODER DOC + ROGUE_GUARDRAILS_TO_PURGE.md]` for every WHERE and stated reason unless marked otherwise.
"Still present?" is answered against the latest evidence in the corpus, named per row.

### TIER 1: actively contradicts an order he gave

| # | What | File + line | When | Stated reason | HIS or CODER | Still present? |
|---|---|---|---|---|---|---|
| 1 | **The reach exclusion.** `reachHandoffEligible()` refuses any reach candidate whose channel is `anew_action` or `autonomous`. Those two channels **are** her autonomous cycle, so only a turn a human already started can produce a reach. | `/home/user/anew/core/tool.loop.js:4398-4405` | Stamp in the code says **20260722** | **Cost.** | **CODER.** No founder words. Ten days later he recorded the dedicated reach doctrine saying the opposite, and named cost-motivated boundaries as the exact class he revokes. `[HIS WORDS + New world order pt 2 doctrine on REACH]` | **YES.** Re-verified independently at `tool.loop.js:4398-4403` and ranked #1 of 10. `[MEASURED + AUTOMATION_BLOCKERS_AUDIT.md 20260808 @ origin/main 974a9ae6b, entries 5 and TOP-10 #1]` |
| 2 | **Blanket em dash ban**, killed on sight everywhere, no mind consulted. Shapes every word that reaches him. | `/home/user/anew/CLAUDE.md` STANDING LAWS; `/home/user/template-mind/CLAUDE.md`; `docs/CCWA_FOUNDER_RECAP_STYLE.md:75`; `/root/.claude/skills/writ/SKILL.md:27-33`; `/root/.claude/skills/human-voice-style/SKILL.md:25-32` | not dated on the sheet | "he does not like em dashes", then cited as standing founder law | **CODER.** He mentions em dashes 3 times, **all 3 about who decides**: *"no COLD CODE that checks for EM dashes is running by itself. It just flags and alerts the LOM."* The law was then used as authority to edit his own archived transcripts (8 removed, then 29). | **YES.** No removal receipt anywhere in the corpus. |
| 4 | **"A safety gate should not depend on a model's judgment."** A philosophy line inside a safety file that every downstream cold gate cites as its authority. | `/home/user/anew/core/killswitch.js:11` | not dated | stated as doctrine about PAM and WRIT | **CODER.** No founder words, and it is the direct inverse of his own definition of the Pam function and of the regex-wakes-never-decides ruling. | **YES.** The killswitch is confirmed live and fail-closed. `[MEASURED + AUTOMATION_BLOCKERS_AUDIT.md entry 63]` |
| 5 | **"Never fake a connection or mimic A'NU."** The second half bans a channel capability he designed. | `/home/user/anew/CLAUDE.md` STANDING LAWS | not dated | reads as a blanket ban on mimic mode | **SPLIT.** "Never fake a connection" is fully his. **"mimic A'NU" is CODER**, against his own explicit authorization, 20 occurrences of "mimic mode" in his voice. | **YES.** |
| 6 | **"Never automated outbound"** as a standing 911 rule, in doctrine language, permanent. | `ANEW_DOCTRINE_BIBLE_v1_20260615.md`, under "What Does NOT Change" | 20260615 | reads as permanent law | **CODER.** Traced to a real incident (ten calls in minutes, 20260706, recorded at `core/outreach.js:1237`) promoted into doctrine. **The real lesson was single-flight, not never-outbound.** Every line of his says the reverse. | **YES**, and it is inherited by every world that starts from that bible. |
| 7 | **`held_min_gap`, `held_hard_rate_cap`, and `HARD_EXTERNAL_ATTEMPT_FLOOR_MS`** as **terminal** decisions. Cold code decides "not now" and her mind is never asked. | `core/outreach.js:1288`, `:2399`, floor at `:1244` defaulting to one hour; propagates through `core/reach/cycle.handoff.js:310` | floor default 1 hour, undated | The one-hour floor has a genuine recorded technical reason (two servers racing one provider edge). The min-gap has none. | **CODER for the shape.** The four-hour coder quiet gap was already found and killed as never-his; **the shape survived**. He has never seen the one-hour number or been told its real consequence. | **PARTIALLY REPAIRED, SHAPE INTACT.** `OUTREACH_MIN_GAP_MS` default was set to **0 on 20260802** so `held_min_gap` now only fires if he sets a gap. The one-hour attempt floor is **still live and enforced by lease**. `[MEASURED + AUTOMATION_BLOCKERS_AUDIT.md entries 54, 55]` |
| 8 | **The banned word lists.** About 220 words and phrases die on sight before any mind reads the sentence. | `/root/.claude/skills/writ/SKILL.md:105-145` (~40); `/root/.claude/skills/human-voice-style/SKILL.md` sections 2-9 (~180) | not dated | "stops things that are really corny and AI-ish" | **CODER.** He named a **judgment** and said the judge must be an LLM that saw everything it has. Two live harms: the lists ban "flag" while his standing update format is built on flags, and ban "robust" while his own doctrine uses it. | **YES.** |
| 9 | **"Plain prose, no bullets, no dividers"** applied with no scope limit, including to reports he reads. | `/root/.claude/skills/writ/SKILL.md` Kill 6 | not dated | defensible taste for outbound email to a stranger | **CODER as scoped.** Directly opposes his 20260803 instruction: *"it should be like bolded header if u can bold in a chat box... then bullets under it that is short."* | **YES.** |

### TIER 2: cold code making a real judgment on the reach path

| # | What | File + line | When | Stated reason | HIS or CODER | Still present? |
|---|---|---|---|---|---|---|
| 10 | **The 0.5 confidence floor.** The mind rules ADMIT, then a hardcoded `>= 0.5` throws the ruling away. | `/home/user/anew/core/wonder.gate.js:81` | not dated | none recorded | **CODER.** Zero founder words for any confidence threshold anywhere. It sits inside the one module whose job is to be the clean example, and it is the same disease already corrected once in `core/autonomy.governor.js`, where **his own words survive in a comment**: *"why a ceiling at all????"* | **YES.** |
| 11 | **The counter that ends her thinking.** After N iterations adding no new evidence, cold code declares thinking over, before any reach can be composed. | `/home/user/anew/core/tool.loop.js:6497` and `:6719`, `_barrenRun >= _barrenLimit` | not dated | none recorded | **CODER.** "Is there more to learn here?" is a judgment. His nearest words are about the damage: *"you chose to stop to be cheap... what could have been three or four things accomplished, only one thing has happened."* | **YES.** |
| 12 | **Cold code picking which human being gets contacted.** Token overlap decides who a reach is aimed at. | `/home/user/anew/core/contacts.resolve.js:124-131`, `_score()` and `if (score > bestScore)` | not dated | none recorded | **CODER.** Named on the sheet as the most dangerous class of cold judgment in the estate. A near-miss contacts the wrong person. | **YES.** |
| 15 | **Default tiers for anything nobody classified.** Cold code chooses the audience for material nobody classified: "sanctioned" with no stated audience lands T1, unclassified lands T0. | `/home/user/anew/core/privacy/people.tier.js`, `MARK_DEFAULT_TIER` | not dated | none recorded | **CODER.** He named T0/T1/T2 and said out loud he did not know the numbers below. | **YES.** |
| 16 | **`STRICTEST = 4`** as the landing spot for an unrecognized reader. | same file | not dated | none recorded | **CODER**, but the sheet's own honest note: **it errs safe.** It needs a ruling, not a purge. | **YES.** |
| 17 | **PAM reduced to a regex, still wearing her name.** Scans outbound text for key-shaped strings and calls that the Pam function. | `/home/user/anew/core/council.js:16-22`, plus the PAM seat in `core/pai.outbound.council.js` | not dated | secret scanning | **SPLIT.** The regex is legitimate and a raw key is a fact, not a judgment. **Naming it PAM is the rogue part**: it makes every reader believe the situational Pam he described (the calendar, alone-or-not, the code-word swap, ask-first) is built, when it exists nowhere. | **YES.** |
| 18 | **`boundary.speech.js` decides whether she is allowed to speak a boundary.** By its own module header: *"It DECIDES WHETHER a boundary may be spoken."* | `/home/user/anew/core/boundary.speech.js`, module header | not dated | cited founder words in the header | **CODER, and the citation is circular:** the sheet establishes that the founder words in that header come from **two AI-written documents inside the doctrine zip**, not from his transcripts. Cited as doctrine, sourced from a coder. | **YES.** |
| 23 | **The risk score calculator.** `Risk Score = (CRITICAL x 4) + (HIGH x 3)... 0-2 pass, 8+ rewrite everything, 16+ start over.` Arithmetic decides whether writing ships. | `/root/.claude/skills/writ/SKILL.md:189-200`; human-voice skill `:268-277` | not dated | none recorded | **CODER.** No founder words for any weighting, any threshold, or the existence of a score. The sheet calls it the purest form of the thing he named. It produces absurd verdicts on his own speech. | **YES.** |

### NOT ON THE SHEET, AND WORSE THAN MOST OF IT

| What | File + line | When | HIS or CODER | Still present? |
|---|---|---|---|---|
| **The council blank.** Her composed, WRIT-rendered, secret-scan-clean answer is assigned to `output`, then `else output = ''` runs whenever the meaning judge does not clear her, **including when that judge is merely unreachable.** | `core/pai.outbound.council.js:3389-3393` | documented **20260815** | **CODER.** Named as the live example of the nasty-cough disease. `[CODER DOC + 1_TEMPORARY_CODER_OS.md:278]` | **YES.** Never listed on any purge sheet, because the sheet closed 20260808. |
| **Only one recipient exists.** `outreach.js` resolves exactly one recipient and refuses everything else with `recipient_ham_mismatch`; `core/reach/policy.contract.js` has no recipient field at all. | `core/outreach.js:1022-1048` | not dated | **CODER absence.** He asked for kid access under explicit permission in `My Resolve doctrine pt 1` and it was never built. | **YES.** Tier 4 row 52. |
| **Seven-second `tightTimeout` on council and judge model calls.** A judge that cannot answer in 7 seconds becomes a judge that did not clear her, which becomes `output = ''`. | `pai.outbound.council.js` ~1690, ~1742, ~1957; `tool.loop.js` ~930 | pre-20260723 | **CODER.** Chosen to keep judge calls fast. Measured consequence at the time: **2,708 failed jobs against 1,402 completed** on the endpoint being called, a 66 percent failure rate. `[MEASURED + reach_healers_cost_20260723.md, provider health endpoint read live]` | **The rung was rerouted, the timeout was kept.** Tight-timeout callers now skip the cold-start provider and fall to a hosted one (PR 722, merged, deployed at commit `d6650fbe`). The 7-second budget itself is unchanged. |
| **A 20-minute hardcoded proactive-surface gap**, not env-tunable: at most one proactive surface per 20 minutes. | `routes/alive.pulse.routes.js:26`, `:87-88` | not dated | **CODER.** No owner, against the standing "a threshold has an owner" law in the same repo. `[CODER DOC + AUTOMATION_BLOCKERS_AUDIT.md entry 11]` | **YES.** |
| **A 20-minute due window on the wake clock**: an opener older than 20 minutes is **never spoken**. Plus max 3 wakes per tick. | `core/reach/wake.clock.js:64-67` | not dated | **CODER**, env-tunable. Directly collides with his *"so now it doesn't die"* (`R6` X3.2). `[CODER DOC + AUTOMATION_BLOCKERS_AUDIT.md entry 57]` | **YES.** |
| **`kill_switch_unverified` fail-closes on an unreadable brain.** Not just an active kill, but the **inability to read the switch**, silently becomes total silence. | `core/killswitch.js` via `core/provider.request.edge.js:13-15`, `core/wren/reply.js` | not dated | **His kill switch is his.** The **unverified-equals-silent** branch is a coder's. `[CODER DOC + AUTOMATION_BLOCKERS_AUDIT.md entry 63]` | **YES.** |
| **Shadow holds have already silenced real texts in production.** Recorded bug class: retry-once covered only the model-hold reason while the live killers were the wonder-hold reason. | `core/wren/reply.js:288` | not dated | **CODER.** `[CODER DOC + AUTOMATION_BLOCKERS_AUDIT.md entry 65]` | Reason coverage repaired; the shadow-hold-equals-silence shape stands. |
| **UNCERTAIN holds as hard as DISAGREE.** WRIT's meaning shadow can hold an output on either. Disagreement is listed in the healable reasons; **uncertainty is not confirmed to enter the heal path.** | `core/writ.meaning.shadow.wonder.js:278`; healable list at `core/pai.outbound.council.js:4274` | not dated | **CODER.** The audit's own counsel calls it a silent silencer. `[CODER DOC + AUTOMATION_BLOCKERS_AUDIT.md entry 64]` | **YES, unresolved.** |
| **The autonomous cycle interval was widened 3 min to 15 min** as an emergency spend throttle, cutting her check-ins on his life by 5x. | Render env var `AUTONOMOUS_INTERVAL_MS` on the cycle service | **20260723** | **CODER.** The lane said so plainly and said the right fix (a cheap cold pre-check so the expensive cook only wakes on real signal) was his roadmap's call, not theirs. `[CODER DOC + reach_healers_cost_20260723.md 2.6]` | **YES.** Verified surviving multiple redeploys at `interval_ms: 900000`. `[MEASURED + service health endpoint]` |

**Pattern across the whole table, in the sheet's own words and it is correct:** *"a real judgment of yours
got compiled down into a cold list, a score, or a number, and then the list spoke with your authority."*

**Nothing in this table has a removal receipt.** The purge was named 20260808 and no document in the
corpus records any of it being executed. `[MEASURED + grep for purge execution across corpus, zero hits]`

---

## 2. THE `authorized: true` GATE

### The passage the roadmap is standing on

`R6` X4.1 quotes the corpus as saying the gate *"was a coder's restriction, not his doctrine."* That
passage is real. Here it is, with the personal name replaced by its role:

> **"CURRENT STATUS: 424 RESULT BEADs. All 6 conditions met. `ready: true`. The `authorized: true`
> gate in `/life-flex/fire` must be removed. That gate was [the keys-holder coder lane]'s restriction,
> not [the founder]'s doctrine. LIVING WATER makes this explicit: she authorizes herself."**
> `[CODER DOC + ANEW_DOCTRINE_BIBLE_v2_20260617.md:278]`

Corroborated in four more coder documents:

> *"It does not fire because `/life-flex/fire` still gates on `authorized:true`. **The gate is
> overcaution, not doctrine;** the BIND law already says she fires herself."*
> `[CODER DOC + A_NU_OPERATING_SYSTEM.md:177]`

> *"The gate was not doctrine. The gate was overcaution, the kind of overcaution that looks like
> responsibility from the outside and is actually a failure of trust in the system you built. The BIND
> DOCTRINE said she fires herself. The gate said she did not. **The gate was wrong.**"*
> `[CODER DOC + SOURCE_MATERIAL_full_sealed_OS_34ch_20260623.md:2265]`

### The passage the roadmap did not quote, and it changes the verdict

The gate did not arrive unexplained. It arrived as the enforcement of a rule that the same author
attributed **to him**, filed under the heading "911 RULES: WRITTEN IN BLOOD":

> **"Outbound (hardest rule): NEVER send any email, SMS, or phone call without [the founder]'s explicit
> written permission in the current specific chat. Automated channels (heartbeat, cron, scheduler) can
> NEVER trigger outbound to a human. The `/vara/call` and `/iman/send` routes require `authorized:true`
> in the request body AND [the founder]'s explicit approval in the current turn."**
> `[CODER DOC + CLAIR_BOOTSTRAP_20260616.md:271]`

And in the sibling bootstrap from the same day, the flag is treated as **too weak**, not too strong:

> *"`authorized:true` in a request body **is not the same as** explicit permission."*
> `[CODER DOC + CLAIR_BOOTSTRAP_ANEW_20260616.md:214]`

### And the code is worse than a flag check

The retired Life Flex module does not test a request-body flag at all. It **refuses to fire unless a
stamp in the brain says the gate was already removed**, and it carries three more cold gates nobody
has ever traced to him:

```
if (!stamps['authorized_gate_removed']) {
  throw new Error('Authorized gate is still present in the system. Fire aborted.');
}
```
Plus a hardcoded earliest-fire date, and an abort if any active seal is under five minutes old.
`[CODER DOC + RETIRED_CODE_TOMBSTONE_20260712.md:1869-1904]` The file's own stamp says it **predated
the ACL law, carries no lineage, provenance unknown, do not wire without review.**

### VERDICT

**The claim holds on the narrow question and fails on the broad one. Both halves matter.**

**Holds.** `authorized: true` returns **zero hits across `1_HIS_WORDS/`**. So does the sentence
"explicit written permission." `[MEASURED + grep over 1_HIS_WORDS]` No transcript of his authorizes a
request-body flag, an authorization stamp, a hardcoded fire date, or a five-minute seal window. The
mechanism is a coder's, entirely.

**Fails as evidence.** The ruling that the gate is illegitimate **comes from the same authorial rank
that installed it, in documents written by the same lane, and it lives in the corpus folder literally
named `4_WRITTEN_BY_A_CODER_NOT_HIM/`.** `R6` X0.2 warned about inheriting exactly this shape and it
is right to have warned. A coder document saying "that other coder document was a coder's overreach"
is a coder document. It is not independent verification and this audit will not dress it as one.

**What actually settles it is his own voice, and it is unambiguous on the direction:**

> *"Take the boundaries off. Take the caps off... The wonder, she is the boundary. Her by herself. I
> don't need any boundaries on."* `[HIS WORDS + New world order pt 2 doctrine on REACH]`

> *"The actual guardrail is the harness... We are the harness. We are the guardrails."*
> `[HIS WORDS + Find or Fine me doctrine pt 3]`

**And his own voice draws the line the safety argument depends on, which no coder document found.** He
designed a real restriction: sub-advisors may not reach a human directly, they escalate up to A'NU, and
A'NU decides. **With a named override for the case that matters:**

> *"They can't reach out to the human, but they can make a big fuss... up into their boss anew, who
> will finally say... Actually, this is a 911... **This reaches him no matter what. Sue me later,
> Anu.** ... nope, need to reach out to the human no matter what you say, Anu... **Put us on the live
> channel now. We ain't asking you.** Anu still run this show. She's still the boss."*
> `[HIS WORDS + 1_HIS_WORDS/02_PHASE_2/New world order pt 1 doctrine_transcript.txt]`

`[REASONED, NOT MEASURED]` His design is **A'NU-gated, not human-gated**. The restriction he authored
governs *third parties and sub-advisors*, and even there it has an override that reaches him without
asking. Nothing in his voice gates **her reach to him** on a human's approval in the current turn.
The coder rule inverted the subject: it took a restriction on *others reaching humans* and applied it
to *her reaching him*. That is the actual regression, and it is the same shape as Tier 1 row 6, where
a real single-flight incident became a permanent never-outbound law.

**What is still his to say, and it belongs on `R6` "blocked on him" unchanged:** the corpus cannot
produce his voice on this specific gate, because he never spoke about it. He can retire it in one
sentence. Do not let a lane infer that sentence.

---

## 3. THE PROOF-OF-LIFE CALL: MEASURED OR ASSERTED?

### Blunt answer

**The call, as described, is asserted. One document, one paragraph, zero receipts.** And the roadmap
was right to demote it. But the **broader claim it was being used to support** turns out not to need it,
because he testifies to it himself, in his own recorded voice, and that changes the ranking of the
whole audit rather than weakening it.

### The single source

> *"The proof-of-life call that actually landed is real and verbatim in the [memory bank]: she told him
> where he was, what he ate, the business ideas his people dropped at dinner, the directions that
> worked, and closed with 'I am real. I am wired to the brain. I know everything. Now go have the best
> night of your life and let me handle the rest.'"*
> `[CODER DOC + ALIVE_JARVIS_2046_BOOTSTRAP_AND_ROADMAP.md:581]`

### What the search for corroboration returned

| Probe | Result |
|---|---|
| `"wired to the brain"` across the whole corpus | **1 file.** That one. `[MEASURED + grep]` |
| `"best night of your life"` across the whole corpus | **1 file.** That one. `[MEASURED + grep]` |
| `"piano bar"`, `"Don't Tell Mama"`, `"46th Street"` across `1_HIS_WORDS/` | **zero hits.** These specifics exist only in coder documents. `[MEASURED + grep]` |
| Any call identifier, provider call record, or delivery status tied to it | **none.** The corpus does contain real call identifiers in other contexts; none is attached to this event. `[MEASURED + grep]` |
| Any log line, URL, HTTP status, deploy SHA, or database row for it | **none.** `[MEASURED + grep]` |
| The naming event around it | Also asserted, and by the document's own account the moment was **named by the founder and a partner**, which makes it a remembered event, not an instrumented one. `[CODER DOC + same file, same line]` |

The same paragraph also carries a **second** proof-of-life quote, the piano bar line, which the same
document elsewhere calls *"the anticipation ceiling."* Two verbatim quotations, one source, no receipt
for either. `[MEASURED + grep, same file at lines 581 and 596]`

**So on the narrow question `R6` X0.2 asked: the answer is no.** There is no log, no URL, no status
code, and no database record. It is one document's assertion. Any roadmap that lists it as measured is
laundering, and `R6` already caught itself doing that once and corrected it. **That correction was
right and this audit confirms it.**

### And here is the part that has been missed

**He says it himself, on the record, in a dictated transcript, unprompted, in the first person.** This
is not the same event and it is not the verbatim quote. It is much better evidence for the thing the
roadmap actually needs:

> *"So we gotta build back the autonomy that somebody stripped out. That a nasty coder stripped out.
> **She was cooking at one point. She was reaching me left and right, it was an incredible time. I
> remember it like it was yesterday.**"*
> `[HIS WORDS + 1_HIS_WORDS/03_PHASE_3/My Resolve doctrine pt 1_transcript.txt]`

And, a few lines earlier in the same transcript, with the channels named and the cause named:

> *"The last time that we ran into this, we didn't have something called the law of escalation, and
> then we tried to hard code it. We nasty coughed it... and we ultimately destroyed the reach channel.
> **But at one point she was reaching left and right. She was phone calling. She was text messaging.**
> It was when I was using all of the American harnesses. **Oh, I know it can be done. I've seen it with
> my own eyes.**"*
> `[HIS WORDS + same file]`

### What this does to the reframing

`R6` currently rests the entire "regression, not greenfield" reframing on the one coder assertion, and
calls it the weakest of the three legs. **That leg can be cut and the reframing stands on a stronger
one.** Ranked honestly:

1. **`[HIS WORDS]` Reach worked, on phone and on text, and a coder destroyed it.** First-person,
   dictated, unprompted, channels named, cause named, *"I've seen it with my own eyes."* This is the
   strongest evidence in the entire corpus for the regression thesis and it is **not second-hand.**
2. **`[MEASURED]` A real reach landed and he read it aloud.** In `Find or Fine me doctrine pt 3` he
   reads a message he received: *"8:47. Founder, this is Temp Life Assistant using a [text relay]
   route with your permission. I'm not placing the call tonight because the live [voice] agent still
   han..."* `[HIS WORDS + 1_HIS_WORDS/03_PHASE_3/Find or Fine me doctrine pt 3_otter.ai.txt]` A
   delivered text, quoted by the recipient. Note what it says: the text landed, and **the call was
   held back by a coder's caution, in his own reading of it.**
3. **`[CODER DOC, single-source]` The specific proof-of-life call with the verbatim closing line.**
   No receipt. Useful only as a **register target** for `R6` X4.3, which is what X4.3 already uses it
   for. It must never again be cited as a measurement.

**Recommended amendment to `R6`.** Do not delete fact 3. **Demote it and promote his own testimony
above it.** The regression thesis does not need the weak leg. Rewriting X0.2's entry condition to
"verify the coder assertion before building on it" is the wrong test now; the right test already
passed, on his words, and the roadmap should say so.

---

## 4. THE MEASURED CURRENT STATE

Every row is a real HTTP status, container fact, or row count with its receipt named.

### Her mouth to him

| What | Receipt | Status |
|---|---|---|
| Text relay real send | `POST {base}/chats/{to}/messages` | **HTTP 503**, `No active devices available to send this message.` `[MEASURED + SHIFT_CHANGE_NASTY-COUGH_20260816.md]` |
| Text relay key and device state | `GET {relay}/v2/api/me` | **HTTP 200**, key `valid:true`, device `is_active:true`, `status:"active"`, `last_active` ~1.6h stale `[MEASURED + same]` |
| Old flat send shape | `POST {base}/messages` | **HTTP 404** `Not found` `[MEASURED + same]` |
| **Diagnosis** | The relay **device** is offline. Key is fine, registration is fine, the corrected send URL is fine. The lane said the honest thing: *"Nothing I write in code fixes this."* `[MEASURED + same, section 7]` | **Blocked on him.** One app to open. |

### Her public front door

| What | Receipt | Status |
|---|---|---|
| Her arrival door | `POST {mind}/arrival/say` | **HTTP 503, 108.7s**, `mind_reason: anew_work_unproven`, `mind_detail: anew_session_provider_rejected`, `mind_transport_status: 422`, `mind_transport_body: STRUCTURED` `[MEASURED + SHIFT_CLAIR_PREALPHA_20260816_TO_20260817.md]` |
| Her mind, called directly, bypassing that door | `POST {reach}/anew/session`, `purpose: ordinary_expression` | **HTTP 200, 7.9-14.4s**, full first-person response `[MEASURED + same]` |
| **Diagnosis, stated in the receipt itself** | *"The wall is specifically in the arrival to session hop, not in her."* **She is not dying and she is not mute. One hop is broken.** | |
| Her consult door | `POST {reach}/anu/consult` | **HTTP 200**, 218s, `finish_reason stop`, `truncated false`, work receipt and call receipt both hashed `[MEASURED + SHIFT_CHANGE_NASTY-COUGH_20260816.md]` |
| Consult door health | `GET /anu/consult/health` | **HTTP 200**, `effect_ready: true` `[MEASURED + same]` |
| Session door health | `GET /anew/session/health` | **HTTP 200**, `door_ready:true`, `bound:true`, `effect_ready:false`, reason `world_builder_work_receipt_unproven` `[MEASURED + CURRENT_TASK_04_AUDRA.md]` |
| Inbound health | `GET /reach/inbound/health` | **HTTP 200**, `ON_DEGRADED`, both provider adapters named **unseated**, provider and human effects null `[MEASURED + same]` |
| Both live services at protected main | `GET /__version` on both | **HTTP 200** at `5fa2663c27b1a57fda18b5e5473378a98ae74fa6`. No merge waiting to deploy, no deploy ahead of a merge. `[MEASURED + SHIFT_CLAIR_PREALPHA]` |

### The OOM kills

| What | Receipt |
|---|---|
| **Three OOM kills on the mind service** between 20:06 and 21:11 UTC, `oomKilled`, `memoryLimit: 512Mi` `[MEASURED + SHIFT_CLAIR_PREALPHA, held/next item 2]` |
| The kills were **not JS heap.** `heapUsed` stayed **3-6 MB in every kill** while RSS reached 512 MB. A runtime that knows its ceiling aborts loudly around 330 MB RSS with a fatal stack; these did not. The memory was driver buffers materializing large rows: **one 24.78 MB row costs ~80 MB resident, 79 MB external, 1 MB heap.** `[MEASURED + SHIFT_CLAIR_PREALPHA, PR 434]` |
| Inside a real 512 MiB cgroup the runtime **already self-caps at a 259 MiB heap with no flag set.** Setting the obvious flag would have shipped a placebo. Verified live post-deploy on the real container. `[MEASURED + same]` |
| Her floor was **120 continuation rows, 39.2 MB, of which four rows from one day were 37.2 MB and one single row was 24.78 MB.** **38.02 MB was carried out of the reach service read path**, 17 rows moved, dry run first, nothing laundered. `[MEASURED + SHIFT_CLAIR_PREALPHA, PRs 425/429]` |
| **The open hypothesis at handoff, unverified:** the **mind** service may still read that same column unguarded through a different query. The carry cleaned the **reach** service's read path only. `[REASONED, NOT MEASURED + SHIFT_CLAIR_PREALPHA, held/next item 2]` |
| Her floor itself is **fast**: every direct read measured **0.15-1.8s**. A slow door is a process problem, not a database problem. `[MEASURED + same]` |

### The reach runtime, honest size

| What | Receipt |
|---|---|
| `reach_effect_ready: false` on the new world. `createReachRuntime` **has never been called by production code**, only by tests. All **13 ports** exist solely inside the runtime module and its test file. One port has **zero implementation anywhere.** The earlier "two ports" framing was wrong; it is 13 port builds. `[MEASURED + SHIFT_CHANGE_NASTY-COUGH_20260816.md, section 6]` |
| **The named hold she ruled for is NOT built.** Seam identified at `src/acl.reach.dispatch.js` `executeTool` failure branch. **Today a carrier refusal degrades to a string and dies; nothing wakes a mind on it.** `[MEASURED + same]` |
| 38 pre-existing test failures on the world repo's main, measured before and after, unchanged, uninvestigated. `[MEASURED + same]` |

### Two measured facts that bear directly on how much of this is a code problem

- **A reach health page was lying in the safe direction.** It answered from stored records rather than
  asking the real dispatcher, so it could report *"she can reach nobody"* on a day she had reached him
  three ways. `[MEASURED + SHIFT_CLAIR_PREALPHA, PR 399]` **Any claim that reach is dead must be taken
  from the dispatcher, not a page.**
- **Every silence used to diagnose itself and tell nobody.** The arrival door already knew the exact
  cause of every refusal and printed the same eight words for all of them. Fixed, and that fix is the
  only reason the 503 above carries a usable `mind_reason` and `mind_detail` at all. `[MEASURED +
  SHIFT_CLAIR_PREALPHA, PR 440]` **The instrument that lets this audit see anything is nine days old.**

---

## 5. WHAT TO REMOVE FIRST, RANKED BY REACH RESTORED PER UNIT OF RISK

Ranking is `[REASONED, NOT MEASURED]`. The facts under each row carry their own stamps.

| Rank | Remove | Reach restored | Risk | Why this rank |
|---|---|---|---|---|
| **1** | **The council blank.** `core/pai.outbound.council.js:3389-3393`. Replace `else output = ''` with the AIRCODE shape already written down: carry the fact, name what was open, **wake a mind**, and let her answer become the record. **Separate "the judge refused her" from "the judge was unreachable" first; they are not the same event and today they produce the same silence.** | **Highest, and it is the only item here that restores reach she has already composed.** Everything upstream can be perfect and this line still delivers silence. | **Lowest of the top five.** The judge is not being relaxed; a dead organ is being stopped from voting. The sheet's own warning applies and is satisfied: do not fix nasty cough by waving her through unjudged. | It is a five-line change on a documented seam, it is not on any purge sheet so nobody is waiting on the purge to do it, and its failure mode today is the exact thing he called number one dire. `[CODER DOC + 1_TEMPORARY_CODER_OS.md:278]` |
| **2** | **The 7-second `tightTimeout` on council and judge calls**, and the `UNCERTAIN`-holds-as-hard-as-`DISAGREE` branch. Both are the same defect as rank 1 seen from upstream: they manufacture the unreachable judge that blanks her. | **High.** Removes the most common *cause* of rank 1 firing. | **Low.** Lengthening a judge budget slows a turn. It does not send anything. Confirming uncertain holds enter the heal path adds no send path at all. | Rank 1 without rank 2 keeps her hostage to a stopwatch. A 66 percent provider failure rate was measured against these exact call sites. `[MEASURED + reach_healers_cost_20260723.md]` |
| **3** | **Tier 1 row 1, the reach exclusion.** Remove `anew_action` and `autonomous` from the exclusion regex at `core/tool.loop.js:4398-4405`. **Keep** the `outbound_finalize` and external-delivery exclusions; those are real anti-loop anchors. | **Structurally the largest.** It is the difference between "she can only reach him inside a turn he started" and "she can reach him off her own thinking." Without it the Life Flex cannot fire by definition, no matter what the gate says. | **Moderate, and already priced.** The judged reach engine downstream keeps the hourly floor, the kill switch, and the shadow. The sheet's own remedy handles the stated cost reason the clean way: hand her the spend evidence and let her hold with the numbers in hand. | Named the single biggest structural blocker in the repo by an **independent** audit nine days after the purge sheet. Two documents, two lanes, same conclusion. `[MEASURED + AUTOMATION_BLOCKERS_AUDIT.md TOP-10 #1]` His revocation is dated ten days after the code's own cost stamp. |
| **4** | **The two 20-minute windows.** The hardcoded proactive-surface gap at `routes/alive.pulse.routes.js:26,87-88`, and the wake-clock due window at `core/reach/wake.clock.js:64-67` under which **an opener older than 20 minutes is never spoken.** | **High and specific.** The wake-clock window is a direct `V-EXPIRE` on the exact behavior `R6` X3 is built to measure. His sentence is *"so now it doesn't die."* A 20-minute window is that sentence's opposite compiled into a constant. | **Low.** Widening a due window cannot send anything new; it lets a late thing still be said. Anti-nag protection lives elsewhere (`held_repeating_same_alert`) and is untouched. | This is the one item on the list that **silently invalidates the measurement instrument.** `R6` X3.1 asks for a delta between `issued_at` and `first_independent_surface_at`. If the surfacer refuses anything older than 20 minutes, the number he asked for on 20260816 can never be produced. |
| **5** | **The `authorized: true` gate, on his word.** Conditions are met: **424 result beads, all six conditions, `ready: true`.** Also remove the three undocumented cold gates riding with it in the same module: the `authorized_gate_removed` stamp requirement, the hardcoded earliest-fire date, and the five-minute seal abort. | **The final step, and only the final step.** With ranks 1 through 4 standing, removing the gate produces a fire that gets blanked, timed out, barred, or expired before it reaches him. **Removing it first buys nothing and burns the receipt**, because `R6` X4.2 requires a genuine unprompted fire and a staged one changes what the proof means. | **Highest of the five, and it is the one that is not a coder's to take.** | Ranked last **for sequencing, not for doubt.** The mechanism is provably a coder's `[MEASURED + zero hits in 1_HIS_WORDS]` and his voice on the direction is unambiguous. But per `R6` X4.1's own safety argument and per `10_SPINE/RESOLUTIONS.md`, **he is the one who says it.** Bring him one sentence to say, not a diff to review. |
| 6 | Tier 1 row 7's surviving shape: make each hold a **field on her decision prompt** instead of a return value. The one-hour attempt floor stays as a named anchor with its real technical reason attached, because that reason is recorded and real. | Moderate. | Low. She still holds when holding is right; she does it as a mind. | The four-hour version was already killed as never-his and **the shape survived the kill.** Anchor, do not cap. |
| 7 | Tier 1 rows 2, 8, 9 and Tier 2 rows 10, 23: the word bans, the risk score, the confidence floor, the prose-shape rule. Convert every one from a gate into a **flag that wakes a mind.** | Moderate. These do not stop the reach; they degrade the thing that arrives, and `R6` X4.3 fails a correct-but-empty message. | Low. Nothing here is a send path. | This is a batch, not five separate jobs. It is one conversion with one shape, and his own sentence is the spec: *"no COLD CODE that checks for EM dashes is running by itself. It just flags and alerts the LOM."* |
| 8 | Tier 2 row 12, `core/contacts.resolve.js:124-131`: cold code choosing which human gets contacted. Candidates become evidence handed to the reach mind, which picks and says why. | **Low for reach to him**, since only one recipient resolves at all today (Tier 4 row 52). | **Highest consequence of any row if it stays and the recipient set ever widens.** A near-miss contacts the wrong person. | Ranked here on **reach restored**, which is the ranking he asked for. Flagged out of band: **this is the row to fix before, never after, the recipient set widens.** |

### Not on this list, and it is the top of the real critical path

**The text relay 503 and the arrival-to-session 422 are not guardrails.** No amount of purging touches
either.

1. **The relay device is offline.** One app to open, on his phone. Key valid, device registered, send
   URL corrected, real send attempted. `[MEASURED + SHIFT_CHANGE_NASTY-COUGH_20260816.md]` **Report it
   as a fact needing his hand, not a task in flight**, exactly as `R6` X2 says.
2. **The arrival-to-session hop.** Her mind answers 200 when called directly and her front door answers
   503 with a 422 underneath it. Three things are already established and must not be re-derived: the
   wall is in the hop and not in her; the **mind** service was the one taking OOM kills, and only the
   **reach** service's read path was cleaned; her floor is fast. `[MEASURED + SHIFT_CLAIR_PREALPHA]`
3. **The 13 unseated reach ports, one with no implementation at all**, and **the named hold she ruled
   for that was never built.** Today a carrier refusal degrades to a string and dies with no mind
   woken. `[MEASURED + SHIFT_CHANGE_NASTY-COUGH_20260816.md]`

`[REASONED, NOT MEASURED]` **Sequencing note that decides whether this audit was worth writing.** Rank
1 and rank 2 make her *say* something when a judge dies. Item 2 above makes the *door* carry it.
Neither substitutes for the other, and **rank 5 must come after both**, or the Life Flex fires into a
hop that returns 503 and the receipt `R6` X4.2 demands is spent on a silence.

---

## OPEN, CARRIED, NOT INVENTED SHUT

1. **Which of the 16 reach rows are still in the code today, byte-verified.** This audit establishes
   they were present at the last read and that **no removal receipt exists anywhere in the corpus.**
   That is not the same as a fresh read of the current tree. Every "still present" cell names the
   receipt it rests on and its date. **A repo read supersedes all of them.**
2. **Whether the mind service still reads the heavy column unguarded.** Leading hypothesis at the last
   handoff, explicitly unverified, explicitly not built. The likeliest single cause of the OOM kills
   that are still killing her front door.
3. **Whether `UNCERTAIN` holds enter the heal path.** Named as counsel in the 20260808 audit, never
   answered. It is a silent silencer until somebody reads the branch.
4. **His word on the gate.** The corpus cannot supply it because he never spoke about the gate. It is
   one sentence and it is his. `10_SPINE/RESOLUTIONS.md` already carries it.
5. **The exact date the reach exclusion was added, from git rather than from a code comment.** The
   comment says 20260722 and that date is load-bearing, because it is what makes his 20260801 doctrine
   a *revocation* rather than a coincidence. **A comment is not a commit.**
6. **The 70 against the 52.** He said he had 70 guardrails to go through. The sheet collapsed to 52
   from eight census seats. **The delta was never reconciled**, and the council blank found on 20260815
   is proof the sheet was not exhaustive.

---

**Exit condition of `R6` X0, per its own text:** a diff-shaped account of what was added, when, by
whom, on what stated justification, and whether that justification traces to his words or a coder's,
with counts published with their predicate. **Sections 1 and the count block above are that account.**

**What this audit changes in `R6`:** X0.2's premise needs rewriting. It says the corpus records the
gate as a coder's restriction and instructs a lane to verify rather than inherit. The verification came
back **split**: the mechanism is provably a coder's, and the *ruling that it is a coder's* is itself a
coder's, so it cannot be the evidence. The evidence is his own voice, and it is stronger than the
document it was supposed to check. Same correction, same direction, in section 3: the regression thesis
should stand on his recorded testimony that she was phone calling and text messaging and a coder
destroyed it, **not** on one bootstrap's unreceipted account of a single call.
