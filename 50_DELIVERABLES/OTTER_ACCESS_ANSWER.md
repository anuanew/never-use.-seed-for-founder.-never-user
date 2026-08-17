# OTTER ACCESS: THE ANSWER

**Answers research docket `R-01`. Serves `R8` sub-phase `M5.1`.**
**All sources checked 2026-08-17.** Every factual claim below carries a source URL.
Anything not verified against a primary source is marked **[REASONED, NOT MEASURED]**.

The founder's caution governs this document: *"That might not be possible. Don't gas me up."*
So: one thing he asked for is dead, one thing he asked for works and costs less than he feared, and
there is a fourth thing he did not ask about that is free and that he should do today.

---

## THE ANSWER IN THREE SENTENCES

1. **The API path is dead.** The Otter API is Enterprise-only, custom-priced, and gated behind an
   account manager, so there is no one-month upgrade that buys it. Source: `https://help.otter.ai/hc/en-us/articles/4412365535895-Does-Otter-offer-an-open-API` (checked 2026-08-17).
2. **But the cheap path exists and is cheaper than he feared: bulk export is on the Business plan at
   $30 for one month, and upgrading gives him his FULL history, not just conversations from the
   upgrade date forward.** That was the crux question and it is answered in Otter's own documentation,
   not inferred. Source: `https://help.otter.ai/hc/en-us/articles/26011568967447-Will-I-still-have-access-to-my-conversations-if-I-cancel-downgrade-or-change-plans` (checked 2026-08-17).
3. **Separately, and at zero dollars: Otter already ships an official connector for her, on every plan
   including free.** It is read-only and it is live query rather than a corpus, so it is not a
   substitute for the export, but it is one setup and he should do it today.
   Source: `https://help.otter.ai/hc/en-us/articles/35287607569687-Otter-MCP-Server` (checked 2026-08-17).

**Total to get everything: $30, one time, one month.** He can cancel the same day he exports.

---

## THE CRUX QUESTION, ANSWERED

He asked the right question without knowing it was the right question. The whole decision turned on
whether a one-month upgrade gives him his archive or only gives him going forward.

**It gives him the archive. This is documented, not inferred.**

Otter's help center, article title verbatim, *"Will I still have access to my conversations if I
cancel, downgrade, or change plans?"*, states:

> "Your conversations will remain in your account, regardless if you downgrade, upgrade, or cancel
> your plan. You have full control over your conversations, and they will only be deleted if you
> choose to delete them, delete your account, or an admin deletes your account if you are part of a
> Workspace."

And on the archive specifically:

> "Currently, users on the Basic free plan will be limited to the most recent 25 conversations. All
> other conversations will be archived but remain in your account."

And the FAQ on that same page, verbatim:

> "If my conversations are archived, how do I access conversations past the 25 limit?
> Upgrade to a paid plan to unarchive and access all conversations."

> "Will my conversations be deleted after a certain period of being archived?
> No. Your conversations will remain in your account regardless if you downgrade, upgrade, or cancel
> your subscription."

Source: `https://help.otter.ai/hc/en-us/articles/26011568967447-Will-I-still-have-access-to-my-conversations-if-I-cancel-downgrade-or-change-plans` (page last updated 2026-08-10, checked 2026-08-17).

Corroborated on the pricing page comparison table, row *"Conversation history"*: Basic reads
`25 most recent`, and Pro, Business, and Enterprise all read `Unlimited`.
Source: `https://otter.ai/pricing` (checked 2026-08-17).

**There is no date-forward restriction anywhere in Otter's plan documentation.** Nothing in the bulk
export article limits export by date, by age, or by which plan the conversation was recorded under.
Export acts on what is in the account, and what is in the account is everything he ever recorded.

**One honesty flag, because he asked not to be gassed up.** Otter puts this warning on that same
article, verbatim:

> "Note: This article may not be up-to-date. The most accurate and up-to-date limits and features can
> be found on our pricing page. Limits and features may be changed at any time."

The pricing page agrees with the article on the point that matters, so two sources agree. But the
answer is Otter's own to change, and he should confirm the conversation count is what he expects
before he cancels, not after.

---

## WHAT EACH PLAN ACTUALLY EXPOSES

Verified directly against the pricing page comparison table markup on 2026-08-17.
Source: `https://otter.ai/pricing`.

| | Basic | Pro | Business | Enterprise |
|---|---|---|---|---|
| Price, billed monthly | Free | $16.99 / user / mo | **$30 / user / mo** | Custom |
| Price, billed annually | Free | $8.33 / user / mo | $19.99 / user / mo | Custom |
| Conversation history | **25 most recent** | Unlimited | Unlimited | Unlimited |
| Export formats | mp3, txt | mp3, txt, pdf, docx, srt | mp3, txt, pdf, docx, srt | mp3, txt, pdf, docx, srt |
| **Bulk export** | No | **No** | **YES** | YES |
| **Otter API and webhooks** | No | No | **No** | **YES only** |
| **MCP connector for AI assistants** | **YES** | **YES** | YES | YES |

Two rows in that table decide everything, and I checked both against the raw page markup rather than
trusting a summary:

- **"Otter API and Webhooks"** carries a checkmark in the Enterprise column only. Three empty cells,
  one check. The API is not a Business feature. It is not a Pro feature.
- **"MCP server integration for AI assistants"** carries a checkmark in all four columns, including
  Basic. Zero empty cells. The connector is free-plan inclusive.

Bulk export tier requirement, quoted verbatim from the help center:

> "Plan: The bulk export feature is only available on the Otter Business and Enterprise plans."

Source: `https://help.otter.ai/hc/en-us/articles/13829342669079-Bulk-export-conversations-audio-or-Takeaways` (last updated 2026-08-03, checked 2026-08-17).

And on Pro, verbatim from the per-conversation export article:

> "Note: Learn how to bulk export multiple conversations on our Business and higher plans."

Source: `https://help.otter.ai/hc/en-us/articles/360047733634-Export-conversations` (last updated 2026-07-22, checked 2026-08-17).

**Which plan is he on.** He said *"I had a personal plan."* Otter's personal paid plan is Pro. If he
is on Pro, all of his conversation history is visible to him right now and the $30 month buys him
only the bulk export button. If he has lapsed to Basic, only his 25 most recent are reachable and
everything older is archived but intact, and the upgrade unarchives it. **He should check
`Account Settings > Plan` before paying anything.** Either way the answer and the price are the same.

---

## THE API, IN DETAIL, SO NOBODY REOPENS THIS

The API is real, it is well documented, and it would do exactly what he imagined. He simply cannot buy
access to it for one month.

Verbatim: *"Otter's Public API is available for all Enterprise workspaces. If you do not see this
feature for your workspace, contact your Otter account manager."*

- Auth model: Bearer token in the `Authorization` header. API keys created under
  `Integrations > Developer > Create key`. Limit of 2 API keys per user. Key shown once only.
- Rate limit: 10 requests per second, `429` on exceed.
- Pagination: cursor based, `meta.has_more` and `meta.next_cursor`.
- It **can** list and fetch past conversations. `GET /conversations` returns conversations in reverse
  chronological order with cursor pagination, and the API retrieves "channels, conversations,
  transcripts, audio, action items, insights, outlines, and workspace details."
- Base URL `https://api.otter.ai/v1`.

Sources: `https://help.otter.ai/hc/en-us/articles/36130822688279-Otter-ai-Public-API` (last updated 2026-04-23) and `https://help.otter.ai/hc/en-us/articles/4412365535895-Does-Otter-offer-an-open-API` (last updated 2026-07-04). Both checked 2026-08-17.

**Why this closes the door.** Enterprise has no self-serve price and no buy button. The pricing page
offers only "Schedule a demo." The upgrade article says Enterprise requires contacting the sales team.
Enterprise is a custom contract with an account manager, which is not a thing a single person turns on
for thirty days and turns off. Source: `https://help.otter.ai/hc/en-us/articles/360048593553-Upgrade-to-a-paid-subscription` (checked 2026-08-17).

**Do not chase this.** The API would give a cleaner pull than a ZIP of text files, and it is the
correct long-term shape if he is ever on Enterprise for other reasons. It is not worth a sales call to
solve a problem that $30 and one afternoon solves.

---

## THE THREE PATHS

### PATH 1: Upgrade one month, pull everything, downgrade

**As he framed it, aiming at the API: this fails.** No self-serve tier carries the API. Business does
not have it. Enterprise is a custom contract.

**Reframed to aim at bulk export instead: this works, and it is the answer.**

**What it costs.** $30 for one seat for one month, billed monthly on the Business plan. He is one
user, so one seat. There is a promotional `$24 /user/month` with "20% off for 3 months" displayed on
the pricing page, which is a three-month commitment framing rather than a cheaper single month, so
budget $30. Source: `https://otter.ai/pricing` (checked 2026-08-17).

Subscriptions are non-refundable per Otter's terms, so the $30 is spent the moment he clicks.
Source: `https://help.otter.ai/hc/en-us/articles/23346776714903-Cancel-an-Otter-subscription` (checked 2026-08-17).

**What it gets him.**
- The bulk export button, which is the only thing standing between him and his archive.
- **His entire history, not just forward.** Established above with two agreeing sources.
- A single ZIP file, delivered by an emailed download link on the web flow.
- Formats: TXT, DOCX, PDF, SRT for text, and MP3 for audio. TXT is the right choice for the doctrine
  reader. SRT is worth taking as a second copy because it carries timestamps, and the doctrine reader
  indexes by occurrence.
- Unlimited conversation history stays unlocked while he is on the plan.

**What it does not get him.**
- Not the API. He gets a ZIP of files, not an endpoint. For a one-time corpus pull that is fine.
- Not structured metadata in any guaranteed schema. A ZIP of TXT and SRT is text and timings, not the
  rich object the API returns.
- Not Takeaways from the mobile app. Verbatim: *"Takeaways cannot be exported on the mobile app. To
  export or bulk export Takeaways, sign into the web browser version of Otter."*
- Not bulk audio out of Channels or Direct Messages. Verbatim: *"Bulk exporting audio is not available
  in Channels or Direct Messages at this time."* Both from the bulk export article, checked 2026-08-17.
- Not Action Items or the Outline as files. Per the export article, Action Items and the Outline cannot
  be exported directly and must be copied by hand.

**Is it permitted.** Yes. It is the product working as sold. Upgrading, exporting, and cancelling are
each first-class documented flows with their own help articles.

**The one trap, and it is the single most likely way this fails.** From the bulk export article's own
FAQ, verbatim:

> "I clicked 'Select all', but it did not bulk export all conversations in my account. How do I bulk
> export all conversations in my account?
> 'Select all' will only select the conversations loaded on the current page. To bulk export all
> conversations in your account, scroll down and load all conversations on the page. Once loaded,
> click 'Select all'."

If he taps Select All without scrolling to the bottom first, he pays $30 and exports a fraction of his
life and never knows. **The scroll is the job.** This is handled in the click-by-click below.

**A possible $0 version, flagged honestly as unverified.** Otter offers a 7-day free Business trial.
The trial page states verbatim *"Business Trial. For teams and organizations. Free for 7 Days"* and
notes *"After your trial period is complete, your workspace will automatically be charged for Otter
Business Monthly."* A credit card is required. Sources: `https://otter.ai/start-for-free` and `https://help.otter.ai/hc/en-us/articles/1500007864861-About-your-Otter-Business-free-trial` (both checked 2026-08-17).

**[REASONED, NOT MEASURED]:** I could not verify whether an existing paid Pro subscriber is eligible to
start a Business trial, or whether trials are restricted to new signups. Trial eligibility for
existing paying customers is not documented on either page. **He should look for a "Start trial"
option on his plan screen, and if he sees one, take it. If he only sees "Buy now," pay the $30 and
move on.** The downside is bounded either way: if a trial auto-converts he is charged the same $30 he
was already willing to spend. Do not spend more than one minute hunting for the trial.

### PATH 2: A computer-use or browser-automation session

**Recommendation: do not do this. It is not permitted, and it is not needed.**

**Whether it is permitted.** Otter's Terms of Service, effective September 19, 2025, do not contain a
clause using the words robot, spider, scraper, or crawler. I checked the full text rather than relying
on a summary. But two clauses in Section 5.2, License Restrictions, land squarely on this path. Verbatim:

> "5.2 License Restrictions. Except and solely to the extent such a restriction is impermissible under
> applicable law, you may not: (a) reproduce, distribute, publicly display, or publicly perform the
> Service; (b) make modifications to the Service; (c) interfere with or circumvent any feature of the
> Service, including any security or access control mechanism; (d) access or use the Service in
> violation of any usage restrictions or other limitations associated with the level of Service you
> (or your Organization) have selected to access and purchased, if applicable."

Source: `https://otter.ai/terms-of-service` (effective 2025-09-19, checked 2026-08-17).

**Clause (d) is the one that decides it.** The entire purpose of automating the browser here would be
to obtain, on a Pro plan, the bulk extraction that Otter sells at the Business tier. That is by
definition using the Service in violation of a limitation associated with the level of Service he
purchased. It does not become permitted because the data is his own. The restriction is on the mode of
access, not the ownership of the content.

**Clause (c) is the second one.** Otter's help center sits behind bot protection that returns HTTP 403
to automated requests. I hit it directly while researching this document, on 2026-08-17, on
`help.otter.ai`. Any automation that had to get past a challenge like that on the app itself would be
circumventing an access control mechanism, named explicitly in (c).

**Third signal, independent of the terms.** Otter's `robots.txt` disallows exactly the paths that hold
conversation content:

```
User-agent: *
Allow: /
Disallow: /agent/
Disallow: /u/
Disallow: /s/
Disallow: /v/
Disallow: /note/
Disallow: /signin
Disallow: /signup
```

`/u/` is the conversation URL path. Otter's published machine-readable instruction to automated agents
is: do not read conversations, do not touch sign-in. Source: `https://otter.ai/robots.txt` (checked 2026-08-17).

**What it would cost.** Irrelevant. **What it would get him.** Irrelevant.

**The practical point that should end the discussion.** This path exists in his head as the clever way
around a paywall. The paywall is $30 and it is a one-time charge, and there is also a free sanctioned
connector. There is no scenario where the correct move is to take a terms-of-service risk on his own
primary account, holding his own most private material, to avoid a charge smaller than a tank of gas.
If the account is ever restricted, he does not lose $30, he loses the archive. **The cheap path being
real is exactly why this path is not worth considering.**

### PATH 3: A one-time manual export

**What it costs.** $0, plus his time.

**What it gets him.** Real files, legitimately, on whatever plan he is on today.
- On Pro: per-conversation export in TXT, DOCX, PDF, SRT, and MP3, with options for speaker names,
  timestamps, highlights, and combining paragraphs.
- On Basic: **TXT only.** Verbatim: *"Basic plan users can export conversations only as TXT files."*
  And only the 25 most recent are reachable at all.

Source: `https://help.otter.ai/hc/en-us/articles/360047733634-Export-conversations` (checked 2026-08-17).

**What it does not get him.** Scale. This is one conversation at a time: open it, three dots, Export,
pick format, pick options, save. He described *"hours of calls"* across what the docket records as
calls, journals, investor material, and the lost files. **[REASONED, NOT MEASURED]:** I could not
establish how many conversations are actually in his account, because that requires being signed in.
At roughly a minute per conversation of tapping, this is somewhere between an evening and a lost
weekend, and the failure mode is not that it is slow, it is that he stops halfway and the corpus is
silently partial. A partial corpus is worse than no corpus, because the doctrine reader cannot tell
the difference between "he never said it" and "we never pulled it."

**Is it permitted.** Yes, entirely. It is the documented flow.

**Where it is still the right tool.** If there are five specific conversations he needs in the system
tonight, this is faster than upgrading. It is the right path for a handful and the wrong path for an
archive.

---

## THE FOURTH PATH HE DID NOT ASK ABOUT

He asked *"How can we get her connected to that?"* There is a sanctioned answer to that exact
sentence, it is free, and it is on his current plan whatever his current plan is.

**Otter publishes an official MCP server and an official Claude connector.**

- Endpoint: `https://mcp.otter.ai/mcp`. I probed it on 2026-08-17 and it is live and returns
  `401 Authentication required`, which confirms it exists and is OAuth-gated rather than open.
- Auth: OAuth. Verbatim from Otter: *"All access is OAuth-authenticated with granular permissions.
  Your AI assistant can only access meetings you explicitly authorize."* No API key involved. No
  credential handed to anybody.
- It is read-only. The Anthropic connector listing describes it as read-only, retrieving and reviewing
  meeting data without modification permissions.
- Coverage, verbatim from Otter's FAQ: *"What meetings can I access through the MCP Server? You can
  access all meetings that you have captured in Otter, as well as any meetings shared with you from
  other users in your Workspace."*
- It exposes three tools: `get user info`, `search`, and `fetch`. `search` finds meetings, `fetch`
  *"Retrieves a full speech transcript of a meeting or conversation."*
- Otter's own claim: *"Search your meeting transcripts across all time periods."*
- It is available on **all four plans including free Basic**, verified against the pricing table markup.

Sources: `https://help.otter.ai/hc/en-us/articles/35287607569687-Otter-MCP-Server` (last updated 2026-08-12), `https://claude.com/connectors/otter-ai`, and `https://otter.ai/pricing`. All checked 2026-08-17.

**Now the part that keeps this from being oversold, because it matters more than the good news.**

**This is retrieval, not ingest, and it does not replace the export.** The documented toolset is
`search` and `fetch`. **There is no documented tool that enumerates every conversation in the
account.** That is the whole difference. `search` answers a question he thinks to ask. It cannot
guarantee it has surfaced everything, and it cannot be driven to walk the archive end to end the way
the API's cursor-paginated `GET /conversations` could. **[REASONED, NOT MEASURED]:** based on the
documented tool list, I judge that this connector cannot produce a complete, verifiable corpus. I did
not test it against a live account.

Three more honest limits:

1. **It is a live third-party call at query time.** Every question routes a slice of his private life
   out to Otter and back, at the moment of asking, forever. The export is one crossing and then it is
   his. The connector is a permanent open door. That is a privacy-fence decision, not a convenience
   decision, and it belongs to him.
2. **It is bounded by his plan's conversation history.** **[REASONED, NOT MEASURED]:** Otter documents
   that on Basic, conversations past the most recent 25 are archived and inaccessible until upgrade.
   Nothing states whether the MCP server sees archived conversations. I judge it does not, since the
   archive limit is described as account-level access. **Consequence: if he cancels all the way down
   to Basic after exporting, the connector likely goes blind past 25 conversations.**
3. **Nothing durable lands.** No files, no writer stamps, no provenance, nothing the doctrine reader
   can index. It is a window, not a corpus.

**So it is not the answer to the docket, but it is the answer to his literal question, it costs
nothing, and it works tonight.** Do both.

---

## RECOMMENDED PATH

**One month of Otter Business at $30, bulk export everything as TXT and SRT, then cancel to Pro.**
That is Path 1, reframed off the API and onto bulk export.

**Why this one.**
- It is the only path that produces a **complete** corpus. Path 3 produces a partial one and calls it
  complete. The connector cannot enumerate. Only bulk export takes everything in one motion.
- The crux question came back in his favour. **He is not renting a window into his history for a
  month, he is buying a copy of it forever.** The files are his after he cancels. Otter documents that
  the conversations stay in the account across the downgrade as well, so he keeps both the copy and
  the original.
- It is permitted, documented, and reversible.
- $30 is the whole cost. He said *"Even if I gotta pay something."* This is the something, and it is
  smaller than he was braced for.

**Do this alongside it, same day, free:** connect the Otter MCP connector. It costs nothing, it is on
his plan already, and it answers his literal question while the export is being processed.

**Then cancel to Pro and not to Basic.** Pro at $8.33 per month billed annually keeps unlimited
conversation history, keeps all export formats, and keeps the connector able to see the whole archive.
Falling to Basic re-archives everything past 25 conversations. Nothing is deleted, but it goes dark
until he pays again. **[REASONED, NOT MEASURED]** on the connector consequence specifically, as noted
above. The $8.33 is the cheap steady state, not the $0.

### The honest risk

**The real risk is not the money, it is the scroll.** Otter's `Select all` selects only the
conversations loaded on the current page. He pays $30, taps Select All, gets a ZIP with the most recent
handful, sees a ZIP arrive, believes he is done, and cancels. **The archive he was trying to save is
the part that did not load.** This is documented behaviour, not speculation, and Otter's own FAQ exists
because people hit it.

**The mitigation is one instruction: count before, count after.** Before exporting, scroll to the
bottom and get a rough count of conversations. After the ZIP arrives, count the files. If those two
numbers do not match, he has not exported his archive, and he still has the paid month to fix it. **Do
not cancel until the numbers match.**

Second risk, smaller. Otter labels its own downgrade article *"may not be up-to-date"* and reserves the
right to change limits at any time. Both of my sources agree today. Confirm the history is visible
after upgrading and before cancelling.

Third risk, smallest. The $30 is non-refundable. If the archive turns out to be twelve conversations,
he spent $30 to learn that. Checking the count first, on his current plan, costs nothing.

---

## CLICK BY CLICK FOR HIM

Written for a phone. Do the export part on a computer if one is anywhere near him, because Step 6 is
the one that matters and it is much easier with a mouse and a big screen. If it is phone only, the
phone browser works. Use the browser, not the app, for the export.

### Part A: Before he pays anything. Two minutes, $0.

1. Open the Otter app or go to `otter.ai` in his phone browser and sign in.
2. Tap his **profile picture or initials**, top of the screen.
3. Tap **Account Settings**, then tap **Plan**.
4. **He should see the name of his plan.** It will say Basic, Pro, Business, or Enterprise.
   - If it says **Pro**, good. Everything is visible to him already. Continue.
   - If it says **Basic**, that is fine too, it just means older conversations are hidden right now and
     the upgrade will bring them back. Continue.
5. Go back to **My Conversations**, the main list. **Scroll all the way down. Keep scrolling.** It will
   keep loading more as he goes. Get to the actual bottom where nothing new appears.
6. **Look at the oldest conversation at the bottom and note the date.** Then get a rough sense of how
   many there are. He does not need an exact number, he needs to know whether this is 40 or 400. Write
   it on something.

**This is the number that protects him later.** If the oldest thing he can see is recent and he knows
he has older calls, he is on Basic and the upgrade will unhide them.

### Part B: Connect her. Five minutes, $0. He can do this right now, before deciding anything.

7. In Claude, open **Settings**, then **Connectors**, then **Browse connectors**.
8. Find **Otter.ai**. It is published by Otter themselves, so it will say made by Otter.ai.
9. Tap **Connect**.
10. **He will be asked to sign in to Otter.** This is Otter's own sign-in screen, not ours. He signs in
    normally. Nobody on this side sees or holds his password.
11. He will see a screen listing what access is being granted. **He should read it.** Then tap
    **Authorize access**.
12. Back in Claude, in the chat box, tap the **search and tools** menu and **toggle Otter on**.
13. When she asks permission to use an Otter tool the first time, allow it. To stop being asked every
    time, go to **Connectors**, tap **Configure** next to Otter, and set the tools to **Always allow**.

**How he knows it worked.** Ask her something only Otter would know, like *"search my Otter meetings
for the last conversation about the pecking order."* If she comes back with a real transcript and a
link, it is connected. If she says she cannot find the tool, go back to step 12 and check the toggle.

**This is read-only.** She can read his transcripts. She cannot change or delete anything in Otter.

### Part C: The export. $30, one hour, once.

14. Go to **Account Settings**, then **Plan**.
15. **Look for a Business free trial option first.** If he sees anything offering a Business trial,
    take that instead of buying. If he only sees **Buy now**, do not go hunting. Move on.
16. Under **Business**, tap **Buy now**. Business must be purchased in a **web browser**, not in the
    app. If he is in the app, open `otter.ai` in Safari or Chrome and sign in there.
17. Fill in the company and payment info. The company name field becomes his workspace name and does
    not matter much. Pick something.
18. Finish the purchase. **He should now see a Workspace.** That is expected and correct.
19. Go back to **My Conversations**.
20. **If he was on Basic, his old conversations should now be visible.** Scroll down and check that he
    can now see further back than the date he wrote down in step 6. **If he cannot, stop and contact
    Otter support before doing anything else.** Do not export a partial archive.

### Part D: Step 6 again, and this is the whole job.

21. **On the My Conversations list, scroll all the way to the bottom.** Slowly. It loads more every
    time he reaches the end. **Keep going until scrolling stops producing new conversations.**

    **This is the step everything depends on.** Otter's Select All only selects what has been loaded
    onto the page. If he skips this, he will export the top of the list and lose the rest, and the
    export will look successful.

22. **Turn off any ad blocker.** Otter's own note: ad blockers prevent exports from working.
23. Now tap the **checkbox** on any one conversation. **A Select all checkbox will appear once at
    least one is selected.** It does not show up before that.
24. Tap **Select all**.
25. Tap the **Export icon** at the top of the list.
26. **Choose the format. Tick TXT.** Also tick **SRT** if it is offered, because SRT carries timestamps
    and that is worth having.
    - **Do not tick audio or MP3.** It makes the file enormous and he does not need it for this.
    - If there are options for **Show speaker names** and **Show timestamps**, **turn both on.** Those
      two make the transcripts usable and their absence cannot be fixed later.
27. Tap **Export**.
28. **On the web he will get an email with a link to download a ZIP file.** It is not instant. It can
    take a while with a large archive. **He should wait for the email and not re-run the export.**
29. Download the ZIP. On a phone it saves to Files or Downloads. **Do not open it in a preview app and
    assume that is saving it.** He needs the actual file.
30. **Count the files inside the ZIP against the number from step 6.**
    - **If the numbers roughly match: done. Move to Part E.**
    - **If the ZIP has far fewer: the scroll in step 21 did not go far enough.** He still has the paid
      month. Go back to step 21 and do it again, slower, all the way down. **Do not cancel yet.**
31. Get the ZIP to a safe place before cancelling anything. Send it to himself, put it in cloud
    storage, whatever he normally trusts. **Two copies.**

### Part E: Cancel, but only down to Pro.

**Only after the ZIP is downloaded, verified against his count, and backed up in two places.**

32. Go to **Account Settings**, then **Billing**.
33. **Look for Pause plan before Cancel plan.** Otter offers a pause. If he thinks he might want
    Business again soon, pause is better than cancel.
34. To change plans, tap **Cancel plan**, pick a reason, tap **Continue**, then read the popup and tap
    **Cancel subscription**.
35. **He keeps Business features until the end of the billing period he already paid for.** Nothing
    shuts off the moment he cancels.
36. **Then resubscribe to Pro, at $8.33 per month billed annually.** Do not let it fall to Basic. Basic
    re-hides everything past his 25 most recent conversations. Nothing is deleted, but it goes dark and
    the connector very likely goes blind with it.
37. **Cancel at least 24 hours before the next billing date** so he is not charged for a second month.
    Otter says this explicitly and subscriptions are non-refundable.

**Nothing he does in Part E deletes a single conversation.** Otter is explicit: conversations are only
deleted if he deletes them, or deletes the account. Cancelling is not deleting.

---

## WHAT I COULD NOT ESTABLISH

Listed rather than guessed. Each of these is genuinely open.

1. **How many conversations are actually in his account, and how many hours.** Requires being signed
   in. Step 6 of the click-by-click is how he finds out, and it is free. **Everything about whether
   Path 3 is merely tedious or actually impossible depends on this number, and I do not have it.**
2. **Which plan he is on today.** He said *"a personal plan,"* which maps to Pro, but I cannot confirm
   he is not lapsed to Basic. It does not change the recommendation or the price. It changes whether
   he can see his own history right now.
3. **Whether an existing paid Pro subscriber can start the 7-day Business trial.** Trial eligibility
   for current paying customers is documented on neither the trial page nor the help article. This is
   the only open question that could take the cost from $30 to $0. One look at his plan screen settles it.
4. **Whether the MCP connector can reach archived conversations on the Basic plan.** Otter documents
   the 25-conversation archive limit and separately documents that MCP reaches "all meetings that you
   have captured." The two statements are not reconciled anywhere. I reasoned it cannot, and marked
   that reasoning. I did not measure it.
5. **Whether the MCP connector can be driven to enumerate an entire archive.** The documented tools
   are `get user info`, `search`, and `fetch`. No listing tool is documented. Absence from the
   documentation is not proof of absence in the implementation. Untested against a live account.
6. **Any hard ceiling on bulk export volume.** Otter publishes no limit. A third-party guide states
   users have exported hundreds at once without issue, which is a claim I am reporting, not verifying.
   Source: `https://moat.works/export-otter` (checked 2026-08-17). **If his archive is unusually large,
   the export could fail or truncate in a way nobody documents. Step 30 is the check that catches it.**
7. **Exactly which fields survive into a bulk-exported TXT or SRT.** The per-conversation export
   article documents the option toggles. The bulk export article does not confirm the same options
   apply identically at bulk. **[REASONED, NOT MEASURED]:** likely the same, since it is the same
   export engine.
8. **Whether summaries and Takeaways come through in the same bulk run on the web.** Bulk export of
   Takeaways is documented as web-only and not available on mobile. Whether they arrive in the same ZIP
   as the transcripts, or a separate one, is not stated.
9. **Whether Enterprise could be bought for one month at any price.** No published price, no self-serve
   path, sales contact only. I did not contact sales. I judged it not worth the delay.
10. **What Otter retains on its own servers after a downgrade.** The privacy policy permits retention
    for legitimate business purposes. This is a normal SaaS posture and not specific to him, but it
    means the export gives him a copy, **not a deletion.** If he wants the material out of Otter, that
    is a separate decision and a separate document.

---

## AFTER THE EXPORT

**This is the largest single body of his own words the system has ever received, and it is his private
life at scale. It does not get to arrive casually.**

Three rules, and they are not negotiable by convenience.

**It is founder-world only.** Hard-isolated, behind the privacy fence, in his words: *"My transcript
should never even go anywhere near"* a partner's world or user 99's. **Not the blank world, not the
temp world, not a shared floor.** `PO1-23` governs. The ZIP does not get staged anywhere a
cross-world read could reach it, and it does not sit in a shared scratch space "just while we process
it." `R8` sub-phase `M5.2`.

**It goes through the doctrine reader, not around it.** Decoder pass, scrub pass bounded by the 4PM
rules, indexed by occurrence, presented through the read-back fence with writer stamps. `R8` sub-phase
`M5.3`.

**And the reason that rule exists, stated plainly, because the temptation to skip it will be enormous
once the ZIP is sitting there:** a bulk import that bypasses the fence is **a mass planted-memory
event.** Thousands of rows arriving in her memory with no writer and no provenance is not a corpus, it
is thousands of beliefs she holds as her own learning that nobody can trace, contest, or retract.
**The fence is not paperwork on the way to the payoff. The fence is what makes the payoff safe to
have.** One unstamped bulk load undoes the entire read-back guarantee, and it undoes it invisibly.

**One warning on the scrub, carried from `R8` M5.4 so it is not lost between documents:** the scrub
must not eat the reward. The personal, offhand, apparently unimportant material is exactly what makes
this corpus worth having. A scrub tuned to be safe by deleting everything human deletes the point. His
own words: *"this underrated little five minutes of my time is gonna come back."* Depends on `R4` F7.

**Sequence: the ZIP lands in founder-world, and it stays there until the doctrine reader has taken it.
Nothing goes into her memory directly. Not one row.**
