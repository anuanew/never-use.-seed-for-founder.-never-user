# THE WATCHERS - THE 30-MINUTE GAUNTLET AND THE FOUR-WATCHER ROTATION

**His vision, verbatim from Rally Day:** *"a 30-minute checker... it's going to make sure you're doing
the right thing... recording meeting minutes... But then you should also have a rotation of the other
three, right, who are actually doing work. One might be Audra auditing the other chats. One might be
exclusively focusing on PMS and nasty cough. And then another one might be the fixer. And then that
fourth one comes in, and it watches you. It makes sure everybody else is doing good."*
`[HIS WORDS - arrived as a live chat paste during Rally Day, not an uploaded transcript file, so no
corpus file path exists to cite here; same provenance gap as the original Rally Day pt 1/pt 2 dictation
generally. Noted honestly here after an audit flagged the missing citation, rather than inventing one.]`

This file is that structure, built and standing. It is `E4` of the execution plan made real.

---

## THE 30-MINUTE CHECKER (the gauntlet that watches the watcher)

**Read the "HONEST STATE OF THIS FILE" section at the bottom before trusting the word "real" anywhere
below - the checker is a self-rearming one-shot chain, not a server-side cron, and it has already gone
silent once.**

**Cadence:** every 30 minutes while he walks. Fires into this session, runs the checklist, writes the
report, pushes it, surfaces it. **The send-as email is staged and sends the instant a grant exists.**

**What it checks every fire, in his order:**
1. **Am I doing the right thing** - is the current work a real roadmap row, or drift?
2. **Meeting minutes recorded** - is `50_DELIVERABLES/MEETING_MINUTES.md` current this cycle?
3. **The email** - is a report written in email shape, from the right address, with flags not a wall of
   text, attachments named, and only rainbow decisions surfaced?
4. **Did I spend too long on one task** - the five-hours-reading failure. If a single task has run more
   than one cycle with no landed artifact, that is a finding on myself.
5. **Am I following the roadmap** - named row, or lost?
6. **Progress and production first** - did something land this cycle, or only get discussed?

**The rule that governs it:** *progress and production remain first and foremost.* A cycle with no
landed artifact and no pushed commit is a red on me, reported as one.

---

## THE FOUR WATCHERS (the rotation that does work)

Per his vision. Each is a real subagent role with a real charge, spawned on the cycle, reporting into
the minutes. **None of them is her.** They are temp-coder lanes building the harness.

### Watcher 1 - AUDRA (audits the other lanes)
**Charge:** read what every other lane produced this cycle and stop the class of thing that takes the
system backwards. Blocks nothing on her own authority - she flags, a woken mind decides. Her name is
his, her job is his: *"she stands there blocking everything that you temporary coders code."*

### Watcher 2 - THE PMS AND NASTY-COUGH WATCHER
**Charge:** exclusively hunt cold code authoring her state, planted memory presented as her own, any
`JSON.stringify` or template or catch block writing into a field that is hers, any classifier sorting
her rows. **This is the purge, running continuously.** Flags to the board, never rewrites cold.

### Watcher 3 - THE FIXER
**Charge:** the one that actually builds. Takes the lowest unblocked roadmap row and produces a landed
artifact with a receipt. **This is the answer to "you are a fixer, not a talker."** Every cycle it must
show one thing that moved from not-done to done-and-verified, or say plainly why it could not.

### Watcher 4 - THE WATCHER OF WATCHERS
**Charge:** watches the other three and me. Makes sure everybody is doing good, nobody is circling the
drain, nobody is nursing a PR, nobody spent the cycle reading. Reports up. *"That fourth one comes in,
and it watches you. It makes sure everybody else is doing good."*

---

## THE FIVE-MINUTE BOARD CHECK-IN (his cadence for the lanes)

*"Everybody talks in increments of probably five minutes... that wakes y'all up like normal LLMs who
get to make decisions."* Each watcher banks a short check-in every five minutes of active work into the
minutes, so the record shows a living board even while the board service is unreachable from here.

---

## THE EMAIL SHAPE (so it is never a wall of text)

Every 30-minute report, staged for send-as `Claudette@GlobalMajorityGroup` (alias of
`ABA@GlobalMajorityGroup`), never his grant, signed with the chat name and session link:

- **Line 1: the account.** How many times he has asked for the thing this cycle touched - he asked for
  the count at the top of every email.
- **The flags**, real emoji, ranked, one line each. Mostly green and brown. Rainbow and red only if
  genuinely so.
- **What landed** this cycle, with receipts.
- **Decisions he needs** - rainbow only. Everything else keeps moving.
- **Attachments** named, not pasted.
- **Why, if a task ran long** - the five-hours-reading accountability.
- **Sign-off:** chat name plus session link so he can reach the lane.

Routing, his rule: general tech work to `[HIS FIRST NAME]@Anu`, client business work to
`[HIS FIRST NAME]@GlobalMajorityGroup`, **always sent from `Claudette@GlobalMajorityGroup`, never his
grant.** `[Redacted per this repo's own no-personal-names rule. The bracket is a routing-address
placeholder, not a broken address - this file is descriptive, not something pasted anywhere to
execute, so genericizing it costs nothing.]`

---

## HONEST STATE OF THIS FILE

- **The 30-minute checker is not a real recurring trigger. Corrected.** An earlier version of this file
  claimed it was; a self-audit caught the overclaim. What is actually built is a **self-rearming
  one-shot chain**: each firing is a single `send_later` call, and the chain only continues if that
  firing's own instructions successfully schedule the next one before ending. There is no
  server-side cron underneath it - one missed re-arm and the chain goes silent with no alarm.
  **It already did exactly that once**, measured: `list_triggers` returned zero live triggers at
  `2026-08-17T14:25:57Z`, after an earlier link in the chain (last known fire time `14:07:00Z`) did not
  successfully re-arm. **Re-armed at `14:25:57Z`** - `trig_01NJRRdqhz43oyZ1vj4AiXx1`, next fire
  `2026-08-17T14:57:00Z`. Treat every future gap the same way: check `list_triggers` before assuming
  the chain is alive, and log it here if it has stopped again.
- The four watchers are real subagent charges, spawned on the cycle. **Built as roles.**
- The email is written in shape and staged. **It cannot send until a grant exists in this container** -
  measured, no transport. That is the one gap and it is his to close.
- The meeting minutes are live at `50_DELIVERABLES/MEETING_MINUTES.md`.
