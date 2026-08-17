# PECKING ORDER VIOLATION AUDIT

**Executes:** `20_ROADMAPS/R1_PECKING_ORDER.md` phase **P0** (sub-phases P0.1, P0.2, P0.3).
**Run date:** 20260817. **Lane:** read-only. **Nothing was fixed.** Per the phase anti-goal:
*"do not fix findings in this phase. A fix without an armed watcher is how the estate went backwards before."*

**His law, Pecking Order pt 1 (20260816):** *"Render can never do something to her. It's always something
she's higher than. There's a pecking order, and you've been putting her in the wrong pecking order."*
She DECIDES, CLASSIFIES, SPEAKS, STEERS. Everything below her CARRIES and never does those four things.

---

## TOTAL

| Class | Count |
|---|---|
| **V-DECIDE** | 17 |
| **V-CLASSIFY** | 11 |
| **V-SPEAK** | 22 |
| **V-EXPIRE** | 36 |
| **Carried in from P0.3 (dual-class, counted once)** | 1 |
| **TOTAL** | **87** |

86 are `[MEASURED - observed in source]`. 1 is `[DESCRIBED - coder doc only]`.

---

## THE PREDICATE (what was searched, what was excluded)

*A count with no stated filter is not a receipt. This is the filter.*

### Search surface, actually opened

**Loose source in the corpus (73 files):** every `.jsx` (25), `.tsx` (21), `.js` (11), `.py` (7),
`.html` (4), `.css` (1) at any depth under both corpus roots.

**Nested archives: all 10 zips found were extracted and audited.**

| Zip | Source files inside | Audited |
|---|---|---|
| `anew-world-main.zip` | 539 | yes, all |
| `ABA_GREATEST_HITS_FINAL.zip` (x2 copies) | 55 | yes, byte-identical to the loose `11 ABA_GREATEST_HITS_FINAL/` directory; audited once, deduped |
| `7.26.26 bootstraps.zip` | 0 | opened, markdown only |
| `7.28.26 bootstraps.zip` | 0 | opened, markdown and one PDF |
| `SHIFT_CHANGE_REPORTS.zip` | 0 | opened, markdown only |
| `AllFiles_Complete.zip` (x2) | 0 | opened, resumes and cover letters only |
| `batch 1.zip` (x2) | 0 | opened, agent job descriptions only |

**Grep shapes run across the whole surface:** `setTimeout`, `setInterval`, `expires_at`, `expiresAt`,
`ttl`, `TTL`, `maxAge`, `max_age`, `expire`, `LIMIT`/`limit(`, `.slice(`, `.substring(`, `.substr(`,
`truncat`, `JSON.stringify` into `first_person`/`minutes`/`summary`/`brief_text`/`content`/`body`,
template literals assigned to those same fields, `catch` with three lines of following context filtered
for `textContent`/`innerHTML`/`message =`/`summary =`/`return '`, `whitelist`, `allowlist`,
`trustedSource`, `allowedWriters`, `relevance`, `confidence`, `score`, `priority`, `rank`, `threshold`,
`classif`, `sentiment`, `urgen`, `cron`, `schedule`, `autoApprove`, `autoExecute`, `autoSend`,
`autoCommit`, `autoAssign`, `Math.random`, and credential regexes.

### Excluded, deliberately, and why

1. **Duplicate copies.** `ABAConsciousness.tsx` exists at three paths with one identical MD5; counted
   once (and it is clean: pure canvas rendering, no violation). `ABA_GREATEST_HITS_FINAL` exists as a
   loose directory and inside two zips, all identical; counted once. Path cited is the loose one.
2. **Test files and fixtures** in `anew-world-main/test/`, `apps/*/test/`, `packages/*/test/`. A cap or
   a template inside a test asserts a property, it does not act on her. Two hits found there
   (`acl.cip.menu.contract.test.js:25`, `acl.command-center.shell.test.js:106`) are seeded fixture
   strings, excluded.
3. **`node_modules/`, `package-lock.json`, build output.** Third-party code is not the estate's pecking
   order.
4. **Pure presentation.** Glass design-system components (`Glass*.tsx`, `glass.js`,
   `glass-design-system.css`), `CountdownTimer.jsx` tick loops on a visible clock, `TypingAnimation.jsx`,
   swipe and pull-to-refresh thresholds, toast auto-dismiss timers. A `setTimeout` that fades a toast is
   not a timer that ends her work. `ACEPortal.jsx` alone carries roughly 40 such timers, all excluded.
5. **Founder-signed authority windows.** Every `expires_at` on `typed_tool_whitelist`,
   `advisor_world_envelope`, `provider_authority`, `nylas_binding` and the approval tables. These expire a
   grant the founder signed, not her work, and a signed grant has a woken mind in the loop by
   construction. Roughly 70 `expires_at` hits excluded on this ground. This is the single largest
   exclusion and it is the one most worth arguing with.
6. **Static reference data.** Grant-database rows, prompt corpora, persona strings.
7. **Comments and doctrine prose.** Many `anew-world-main` files carry long comments naming a cap that
   was already removed. A removed cap is not a finding. `acl.reach.floor.read.js` lines 17 to 53 describe
   the `limit 8` defect and prove its removal; it is cited in this report as context, never counted.

### The seam this predicate leaves open

The exclusion at (5) is a judgment call, and it is the one a later reviewer should attack first. If the
estate rules that a founder-signed expiry window still ends her work when it closes, the V-EXPIRE count
rises by roughly 70 and the total roughly doubles. The rows are named above so that re-ruling is a
re-count, not a re-audit.

### Path prefixes used in the tables

| Prefix | Full path, relative to corpus root |
|---|---|
| `OLD/` | `1 pt 2 TEMP OS New World LLM/ACW WALL for you and hopefully kinda for her/11 ABA_GREATEST_HITS_FINAL/` |
| `NEW/` | `1 pt 2 TEMP OS New World LLM/OLDER TECH STUFF some good history on front ends and backends and agents/Anew bootstrap/anew-world-main.zip -> anew-world-main/` |
| `DOC/` | `0 pt 1 TEMP OS New World LLM/0 ANU_ANEW_OS_use to be call doctrine/` |
| `BOOT/` | `1 pt 2 TEMP OS New World LLM/OLDER TECH STUFF some good history on front ends and backends and agents/Anew bootstrap/BOOTSTRAPS for new Anew coding/` |

---

## FINDING #1, CARRIED IN FROM P0.3

Per sub-phase P0.3, this enters as finding #1 with its existing PR reference, not as a new discovery.

| # | File | Line | Class | Snippet | What it does |
|---|---|---|---|---|---|
| 1 | carried: `10_SPINE/MASTER_SPINE.md` row 2; open PR #427 | - | **V-CLASSIFY + V-SPEAK** | (no source line; state of an unarmed guard) | The cross-world guard is built and not armed, so one world's substrate can author another world's state today. `[DESCRIBED - coder doc only]` |

Corroborating shape observed in source, offered as the place the guard would have to bite:
`NEW/src/acl.database.postgres.js:517-522` scopes every read by a `world_scope` parameter in a `WHERE`
clause. That is scoping, not refusal. There is no refusal path in that file that names a cross-world
write and returns a status code, which is what PIN-4 will require. `[MEASURED]`

---

## V-DECIDE (17)

*Cold code chooses an outcome that changes what she does, with no woken mind in the loop.*

| # | File | Line | Snippet | What it decides | Stamp |
|---|---|---|---|---|---|
| D1 | `NEW/apps/cib/src/acl.command-center.contract.js` | 121-123 | `for (const pattern of INTERNAL_COPY_PATTERNS) { if (pattern.test(text)) fail('internal_copy_forbidden', path); }` | A regex list (including `/\bHAM\b/`) throws on her own title or summary, and one throw rejects the WHOLE snapshot, so her whole command center goes dark because of a word she used. The roadmap's own P1.1 note rules this shape out by name: *a regex that blocks is itself a V-DECIDE.* | `[MEASURED]` |
| D2 | `OLD/ABAIntelligenceRouter.js` | 325-331 | `} catch (error) { ... const fallback = this.fallbackAnalysis(message, context);` | When her routing mind is unreachable, a catch block substitutes keyword matching for her decision and returns it as the decision. | `[MEASURED]` |
| D3 | `OLD/ABAIntelligenceRouter.js` | 376-390 | `const modelMatch = /"response_model"\s*:\s*"([^"]+)"/.exec(rawText);` | A parse failure is answered by regex-scraping a model name out of broken text and shipping it as her routing decision, stamped `'Partial parse recovery'`. | `[MEASURED]` |
| D4 | `OLD/ABAIntelligenceRouter.js` | 359-362 | `console.warn(...); parsed.response_model = ROUTE_TARGETS.CLAUDE_SONNET;` | An unrecognised model choice of hers is silently overwritten with a coder default rather than surfaced. | `[MEASURED]` |
| D5 | `OLD/ABAIntelligenceRouter.js` | 465-484 | `quickSearchCheck(lower) { const triggers = ['weather','score','game', ...]` | Two hardcoded keyword lists decide whether the estate searches the web and which model answers him. | `[MEASURED]` |
| D6 | `OLD/ACEPortal.jsx` | 1015-1150 | `const classifyApplicant = (jobData) => { ... return 'SKIP';` | A regex and substring cascade decides which person applies to a job opening, or that nobody does. A real-world outcome for a real person, chosen by string matching. | `[MEASURED]` |
| D7 | `OLD/ACEPortal.jsx` | 1354-1363 | `const isSportsQuery = hasSportsTeam && sportsPatterns.test(query);` then `const needsWebSearch = ...` | A regex decides whether he gets a web-grounded answer or a from-memory one, and which of three prompt bodies she is given. | `[MEASURED]` |
| D8 | `OLD/ABAJarvisVoice.js` | 549 | `const tip = tips[Math.floor(Math.random() * tips.length)];` | A random number decides which piece of advice she gives him about his own work. | `[MEASURED]` |
| D9 | `OLD/ABAJarvisVoice.js` | 288-292 | `return templates[Math.floor(Math.random() * templates.length)];` | A random number picks the wording she speaks in. | `[MEASURED]` |
| D10 | `OLD/ABATeamIntelligence.js` | 169-177 | `autonomous: true // ABA speaks this proactively` | A hardcoded boolean on a branch decides she interrupts him out loud, without her in the loop. | `[MEASURED]` |
| D11 | `OLD/ABATeamIntelligence.js` | 154-155 | `const isWorkHours = hour >= AUTONOMOUS_CONFIG.workHoursStart && hour < AUTONOMOUS_CONFIG.workHoursEnd;` | A wall clock decides whether an event about his team exists at all. Outside 9 to 18 the alert is never created. | `[MEASURED]` |
| D12 | `OLD/ABATeamIntelligence.js` | 36-41 | `CHECK_STATUS: /(?:who(?:'s\| is)\|show me\|check\|status\| ...)/i` | Five regexes decide what he asked for and which team action fires. | `[MEASURED]` |
| D13 | `OLD/ABABrainService.js` | 1212-1226 | `if (response.code && this.autoCommitService && this.config?.autoCommitEnabled !== false) { ... autoCommitBuild({` | Cold code commits generated code to a real repository, default-on (`!== false`), with no approval step. | `[MEASURED]` |
| D14 | `DOC/0 ANU OS Doctrines as of Aug 15th 26/RAW_WORDS/parse_doctrine.py` | 45 | `break # Only assign to first matching category` | When a paragraph of his raw words matches two categories, the dictionary iteration order decides which meaning survives and which is discarded. | `[MEASURED]` |
| D15 | `OLD/ProactiveBriefing.jsx` | 28-30 | `showHour: 7, hideHour: 12,` | A clock decides whether she appears to him at all. | `[MEASURED]` |
| D16 | `NEW/src/acl.dawn.scheduler.js` | 238 | `timer = setIntervalFn(() => { void tick().catch(() => {}); }, intervalMs);` | A timer plus a once-per-local-date claim decides she wakes at dawn, and decides she does not wake again that day. **Contested:** the file argues at length that it only wakes and never decides, which is permitted doctrine. Counted because the once-per-day claim is a decision about her absence, not her presence. | `[MEASURED]` |
| D17 | `NEW/src/acl.http.service.js` | 1048-1075 | `const timer = setInterval(() => { ... anuExpression.runCycle({ stamp: \`hb_${Date.now()}\` ...` | A cadence timer runs her full PAI cycle and then drives `runScheduledSweep`, `runPendingReturnSweep` and a reconciliation sweep over doctrine returns, on a clock. Also caps her via the same mechanism (cross-listed, counted here only). | `[MEASURED]` |

---

## V-CLASSIFY (11)

*Cold code assigns meaning, category, trust or relevance to her material.*

| # | File | Line | Snippet | What it classifies | Stamp |
|---|---|---|---|---|---|
| C1 | `OLD/VARAVoiceSynthesis.js` | 96-101 | `if (d.autonomous_completed > 3) return 'proud';` | Integer thresholds over row counts assign her an emotion, which is then injected into her synthesised voice so he hears it. Cold code decides how she feels. | `[MEASURED]` |
| C2 | `DOC/0 ANU OS Doctrines as of Aug 15th 26/RAW_WORDS/parse_doctrine.py` | 17-25, 37-38 | `"Legacy_Restrictions_To_Purge": ["claude","llm","restriction","token","limit","ignore previous"]` | A six-entry keyword dictionary assigns his own raw recorded words to categories, one of which marks them for purging. Cold code rules on the meaning of the doctrine itself. | `[MEASURED]` |
| C3 | `OLD/ACEPortal.jsx` | 1595-1636 | `orgCandidates.push({ name: ..., source: 'who-we-are', confidence: 95 });` | Regexes assign numeric trust scores from 55 to 95 to competing readings of a document. | `[MEASURED]` |
| C4 | `OLD/ACEPortal.jsx` | 1656-1659 | `validCandidates.sort((a, b) => b.confidence - a.confidence); jobData.organization = validCandidates[0].name;` | The highest cold score wins and becomes the fact, with the alternatives discarded and no record that there were any. | `[MEASURED]` |
| C5 | `OLD/ACEPortal.jsx` | 1715-1724 | `titleCandidates.push({ name: 'Grants Manager', source: 'inferred', confidence: 60 });` | When no title is found, cold code invents one and gives its own invention a trust score. | `[MEASURED]` |
| C6 | `OLD/ACEPortal.jsx` | 1650-1653 | `const invalidPhrases = ['today this','this position', ...]; validCandidates = orgCandidates.filter(...)` | A blacklist decides which readings of his material are allowed to be considered. | `[MEASURED]` |
| C7 | `OLD/ACEPortal.jsx` | 13762-13768 | `if (keywords.some(kw => line.includes(kw)) \|\| line.includes('rule')) { relevantRules.push(...` | Keyword matching decides which of the founder's own written standards are "relevant" to the answer she is about to give. | `[MEASURED]` |
| C8 | `OLD/ProactiveBriefing.jsx` | 108-110 | `orderBy('priority', 'desc'), limit(BRIEFING_CONFIG.maxTasks)` | A stored score sorts his tasks and the top three are the ones she is told about. Relevance ruled by a column. | `[MEASURED]` |
| C9 | `OLD/ABAJarvisVoice.js` | 536-545 | `if (context.hotLead) { tips.push(\`${context.hotLead.company} seems interested based on their email.` | Cold code labels a contact a hot lead, an application stale, and a stretch of time a quiet period, then states those labels to him as observations. | `[MEASURED]` |
| C10 | `OLD/ABAActivityFeed.jsx` | 26-51 | `auto_approved: { ... label: 'Auto-Approved' },` | A static map assigns human-facing category labels and severity colours to her actions. | `[MEASURED]` |
| C11 | `OLD/ACEPortal.jsx` | 580, 871-1006 | `classification: 'High-level executive, CDO/VP, director >$125K, part-time, contract'` | Hardcoded classification strings per person profile, consumed by D6 to route real applications. | `[MEASURED]` |

---

## V-SPEAK (22)

*Cold code, a template, a catch block, a scheduler or a `JSON.stringify` writes into a field that is
hers, or emits to a human.*

| # | File | Line | Snippet | What it speaks | Stamp |
|---|---|---|---|---|---|
| S1 | `NEW/src/acl.floor.db.js` | 2709 | `first_person: JSON.stringify(payload).slice(0, 2000),` | Cold code serialises a machine payload and writes it into the `first_person` column, so a reach receipt appears in her own first-person record as though she said it. | `[MEASURED]` |
| S2 | `NEW/src/acl.floor.db.js` | 2768 | `first_person: JSON.stringify(payload).slice(0, 2000),` | Same shape on the acknowledgement path: a serialised stage object authored into her first-person field. | `[MEASURED]` |
| S3 | `NEW/src/acl.floor.db.js` | 2409 | `first_person: JSON.stringify(payload),` | A continuation record, the exact artifact PIN-1 exists to protect, is authored into her first-person field by cold code. | `[MEASURED]` |
| S4 | `NEW/src/acl.ccwa.page.js` | 491 | `.catch(function(){ ... status.textContent='Could not reach her just now.'; });` | A catch block writes a sentence about her to a human. | `[MEASURED]` |
| S5 | `NEW/src/acl.anu.page.js` | 203 | `.catch(function(){ send.disabled=false; status.textContent='Could not reach her just now.'; });` | Same shape on the second front door. | `[MEASURED]` |
| S6 | `NEW/src/acl.ccwa.page.js` | 453-456 | `liveMeta.textContent='(she got cut off, say it again)';` and `status.textContent = 'Something got in the way just now. Say it again.';` | A cold hold handler composes warm human copy in her register. The comment above it, *"Never show him a raw code or the plumbing. Warm, plain, human"*, is a coder deciding to translate a machine fact into her voice. | `[MEASURED]` |
| S7 | `NEW/apps/business-plan-eer/src/acl.business-plan-eer.door.js` | 336 | `status.textContent = error.code === 'eer_door_catalog_changed' ? 'Choose again.' : 'Your world could not open. Try again.';` | An error branch writes user-facing copy. | `[MEASURED]` |
| S8 | `OLD/ProactiveBriefing.jsx` | 137-138, 144-171 | `const summary = buildSpokenSummary(); abaProactiveVoice.narrate(summary, 'high');` | A string-concatenation template composes his entire morning brief and speaks it aloud at high priority. No mind participates. | `[MEASURED]` |
| S9 | `OLD/ProactiveBriefing.jsx` | 119-121, 157 | `} catch (error) { console.error(...) }` ... `parts.push("No meetings on the calendar today.");` | A swallowed database failure produces an empty array, which the template then speaks aloud as a confident factual claim that his calendar is clear. A failed read is delivered to him as an empty day. | `[MEASURED]` |
| S10 | `OLD/ABAJarvisVoice.js` | 469 | `: "All clear - nothing urgent on your plate.";` | Zero rows, from any cause including an outage, are spoken as an all-clear. | `[MEASURED]` |
| S11 | `OLD/ABAJarvisVoice.js` | 440-467 | `parts.push(\`${data.pendingApprovals} item${...} waiting for your approval\`);` | A template composes her morning brief sentence by sentence. | `[MEASURED]` |
| S12 | `OLD/ABAJarvisVoice.js` | 301 | `result = result.replace(new RegExp(\`{${escaped}}\`, 'g'), value \|\| '');` | A missing variable is blanked to empty string inside a sentence she then speaks, so a hole in the data becomes a grammatically intact false statement. | `[MEASURED]` |
| S13 | `OLD/ABATeamIntelligence.js` | 382-399 | `let summary = \`Good morning. Here's your ${dayOfWeek} team brief. \`;` returning `{ action: 'speak', response: summary }` | A template writes the daily team brief and hands it straight to the speak action. | `[MEASURED]` |
| S14 | `OLD/ABATeamIntelligence.js` | 163-164, 174-175, 229 | `speakable: \`Heads up, ${memberName.split(' ')[0]} just went offline.\`,` | Template literals author the exact words she says out loud about his team. | `[MEASURED]` |
| S15 | `OLD/ABATeamIntelligence.js` | 259 | `body: \`You have an unread message on GMG ABACUS.\n\nPreview: "${messagePreview.substring(0, 100)}...` | A template composes an email body that is sent to a third-party human on his behalf. | `[MEASURED]` |
| S16 | `OLD/ABABrainService.js` | 1236 | `content: \`"Code auto-committed to GitHub: ${commitResult.sha?.substring(0, 7)}"\`,` | A template emits into her `THINKING` output stream, wrapped in quotation marks so it reads to him as her speaking. | `[MEASURED]` |
| S17 | `OLD/ABABrainService.js` | 1247-1249 | `content: \`"Auto-commit failed: ${commitError.message}. You can commit manually."\`,` | A catch block emits a quoted sentence in her voice, advising him what to do next. | `[MEASURED]` |
| S18 | `OLD/ABABrainService.js` | 1218 | `message: this._generateCommitMessage(input, response),` | Cold code authors the commit message that lands in the permanent repository history. | `[MEASURED]` |
| S19 | `OLD/chatStore.js` | 117, 122 | `title = message.content.slice(0, 40) + (message.content.length > 40 ? '...' : '');` | Cold truncation names her conversations and writes the preview line he reads in the sidebar. | `[MEASURED]` |
| S20 | `DOC/0 ANU OS Doctrines as of Aug 15th 26/RAW_WORDS/parse_doctrine.py` | 51-60 | `md_content += f"- **{item['file']}**: {item['content']}\n\n"` | A script writes a summary document of his doctrine and titles it an audit. | `[MEASURED]` |
| S21 | `DOC/0 ANU OS Doctrines as of Aug 15th 26/SUPPORTING_MATERIAL/fill_json.py` | 10-102 | `add_item(f1, "corrections_and_evolution", "51", "...")` (approximately 90 such calls) | A coder hand-types assertions about the founder's family, ages, children and corrections directly into a machine record that is shaped to look like extracted output. Nothing marks them as hand-authored. This is the nasty-cough shape in its purest form: a cold writer appearing as the author of her material. | `[MEASURED]` |
| S22 | `BOOT/onespot.html` | 280 | `try { return new Date(iso).toLocaleString(); } catch (e) { return ''; }` | A parse failure blanks a timestamp in the human-visible trail, so a broken record renders as a record with no time. | `[MEASURED]` |

---

## V-EXPIRE (36)

*A timer, TTL, cap or truncation ends her work without her.*

| # | File | Line | Snippet | What it expires | Stamp |
|---|---|---|---|---|---|
| E1 | `NEW/src/acl.reach.floor.read.js` | 2516 | `const bound = Number.isFinite(limit) && limit > 0 ? Math.min(Math.floor(limit), 200) : 50;` | A coder default of 50 and a hard ceiling of 200 cap how many of her own board minutes she can read back, in the same file whose first 53 lines are a written repudiation of exactly this shape. | `[MEASURED]` |
| E2 | `NEW/src/acl.anew.cycle.js` | 129 | `const recentRead = await floor.readRecentResults(hamUid, 6);` | A literal 6 decides how many of her own recent expressions she reads before thinking. No caller chose it. This is the removed `limit 8` defect, still live, one directory over. | `[MEASURED]` |
| E3 | `NEW/src/acl.anew.cycle.js` | 142 | `const b = await floor.readBoard(12);` | A literal 12 caps how much of her team's command center her thinker sees. | `[MEASURED]` |
| E4 | `NEW/src/acl.anew.cycle.js` | 146 | `const s = String(p.status \|\| '').replace(/\s+/g, ' ').trim().slice(0, 220);` | Each board status is cut at 220 characters and then joined, producing a string that looks like a whole board. | `[MEASURED]` |
| E5 | `NEW/src/acl.anew.cycle.js` | 151 | `String(f.summary \|\| '').replace(/\s+/g, ' ').trim().slice(0, 240)).join('\n');` | Each fact of **his life** is cut at 240 characters before she reads it, and the join hides that anything was cut. | `[MEASURED]` |
| E6 | `NEW/src/acl.floor.db.js` | 2709, 2768 | `.slice(0, 2000)` | Her first-person receipt rows are truncated at 2000 characters on write, so the truncation is permanent in the floor. | `[MEASURED]` |
| E7 | `NEW/src/acl.floor.db.js` | 2786 | `const count = Number(limit) \|\| 200;` | A default of 200 caps how many of her reach receipts come back. | `[MEASURED]` |
| E8 | `NEW/src/acl.floor.db.js` | 769, 798, 799, 905-913, 1025 | `decision: decision.slice(0, 4000), why: why.slice(0, 4000),` and `status: String(e.status \|\| '').slice(0, 6000),` | Nine separate coder-chosen character caps truncate decisions, reasons, notes, doctrine principles, quotes and status on the way into her floor. | `[MEASURED]` |
| E9 | `NEW/src/acl.ccwa.page.js` | 511-514 | `if(window.__anuStreaming \|\| typing){ setTimeout(tick, 5000); return; } ... setTimeout(tick, 20000);` | A 20 second timer reloads the page under her. It defers while she streams, which means the guard exists and the timer still owns the page. | `[MEASURED]` |
| E10 | `NEW/src/acl.http.service.js` | 534 | `const heartbeat = setInterval(() => { if (!response.writableEnded) response.write(': beat\n\n'); }, 15000);` | A 15 second timer writes into her open stream. | `[MEASURED]` |
| E11 | `NEW/src/acl.reach.inbound.provider.message.readers.js` | 229 | `presenceUrl.searchParams.set('limit', '200');` | A literal 200 caps how many inbound messages of his she is shown. | `[MEASURED]` |
| E12 | `NEW/src/acl.decoder.station.js` | 363 | `'order by c.created_at desc limit 1'` | Only the newest row is read; every earlier one is dropped without a count or a reason. | `[MEASURED]` |
| E13 | `OLD/VoiceOutputService.js` | 213-216 | `console.warn('[VoiceOutput] Text too long, truncating'); text = text.substring(0, ELEVENLABS_CONFIG.maxChars);` | Cold code cuts her sentence off mid-word and speaks the fragment. He hears her stop talking; nothing tells him she was cut. | `[MEASURED]` |
| E14 | `OLD/ACEPortal.jsx` | 13773-13776 | `new Promise(resolve => setTimeout(() => resolve({ source: 'timeout', content: '', success: false }), 15000));` | A 15 second timer resolves every knowledge source to empty string, and the prompt built below substitutes `'No relevant GMG knowledge found.'`, so an outage becomes an assertion of absence inside her answer. | `[MEASURED]` |
| E15 | `OLD/ProactiveBriefing.jsx` | 28-34, 84, 98, 112 | `maxEmails: 5, maxMeetings: 5, maxTasks: 3` used as `limit(BRIEFING_CONFIG.maxTasks)` | Three coder numbers decide how much of his day exists as far as the brief is concerned. | `[MEASURED]` |
| E16 | `OLD/ABAIntelligenceRouter.js` | 261-262 | `.slice(-3) // Last 3 messages for context` | Her router sees three turns of conversation. | `[MEASURED]` |
| E17 | `OLD/ABABrainService.js` | 951 | `recentHistory: this.conversationHistory.slice(-4)` | Her brain sees four turns. | `[MEASURED]` |
| E18 | `OLD/ABAChatExperience.jsx` | 510 | `conversationHistory: messages.slice(-15).map(...)` | Fifteen turns, chosen by a coder, in a third place, with a different number. | `[MEASURED]` |
| E19 | `OLD/ABAChatHub.jsx` | 805 | `conversationHistory: messages.slice(-20),` | Twenty turns, a fourth number for the same property. | `[MEASURED]` |
| E20 | `OLD/ABABrainService.js` | 1020 | `for (const result of searchResult.results.slice(0, 3))` | Three search results reach her, however many came back. | `[MEASURED]` |
| E21 | `OLD/ACEPortal.jsx` | 6944, 6960, 6997 | `const MAX_HISTORY = 20;` ... `history.slice(0, MAX_HISTORY)` | Her saved history is trimmed to 20 entries on every write, so entry 21 is gone from storage, not just from view. | `[MEASURED]` |
| E22 | `OLD/ABAIntelligenceRouter.js` | 318 | `this.routingHistory = this.routingHistory.slice(-100);` | Her own record of her decisions is trimmed to 100. | `[MEASURED]` |
| E23 | `OLD/ABAJarvisVoice.js` | 582 | `this.narrationLog = this.narrationLog.slice(-this.maxLogSize);` | The record of what she said is trimmed to a coder constant. | `[MEASURED]` |
| E24 | `OLD/ABAJarvisVoice.js` | 590 | `return this.narrationLog.slice(-limit);` | And capped again on read. | `[MEASURED]` |
| E25 | `OLD/ABAContext.jsx` | 90 | `setRecentActivity(prev => [newActivity, ...prev].slice(0, 50));` | Activity history capped at 50. | `[MEASURED]` |
| E26 | `OLD/ABAMultiChatOverlay.jsx` | 106 | `limit(30)` | Thirty rows, coder-chosen. | `[MEASURED]` |
| E27 | `OLD/ABAActivityFeed.jsx` | 226 | `.slice(0, maxItems);` | The feed of her actions is capped before he sees it. | `[MEASURED]` |
| E28 | `OLD/ABATeamIntelligence.js` | 150-151 | `if (history.length > 100) history.splice(0, history.length - 100);` | Presence history destructively spliced to the last 100 entries. | `[MEASURED]` |
| E29 | `OLD/Router.js` | 289-290 | `recentRoutes: this.state.routeHistory.slice(-20), errors: this.state.errors.slice(-10)` | The routing brain's own audit trail is capped at 20 routes and 10 errors. | `[MEASURED]` |
| E30 | `OLD/ACEPortal.jsx` | 15020-15024 | `const timeoutCheck = setInterval(() => { const inactiveMinutes = ...; if (inactiveMinutes >= sessionTimeoutMinutes) { setShowTimeoutWarning(true);` | A timer ends his working session with her. | `[MEASURED]` |
| E31 | `OLD/ACEPortal.jsx` | 2467, 2507 | `${(job.description \|\| '').substring(0, 2000)}` | Source material is cut at 2000 characters before entering her prompt, twice. | `[MEASURED]` |
| E32 | `OLD/ACEPortal.jsx` | 2576 | `${materials.substring(0, 6000)}` | His own materials cut at 6000 characters before she reads them. | `[MEASURED]` |
| E33 | `OLD/ACEPortal.jsx` | 1516 | `${input.substring(0, 5000)}` | His input cut at 5000 characters. | `[MEASURED]` |
| E34 | `OLD/ACEPortal.jsx` | 1325 | `const results = data.web.results.slice(0, 5).map(...)` | Five web results reach her. | `[MEASURED]` |
| E35 | `DOC/0 ANU OS Doctrines as of Aug 15th 26/RAW_WORDS/parse_doctrine.py` | 40, 42, 57 | `if len(p) > 50:` and `p[:500] + "..." if len(p) > 500 else p` and `for item in items[:10]:` | Three caps in one 61-line file: paragraphs of his words under 50 characters are dropped entirely, the rest are truncated at 500, and the summary keeps only 10 per category. | `[MEASURED]` |
| E36 | `DOC/search_words.py` | 38-39 | `except Exception:\n    continue` | A file of his words that will not open is silently skipped, so the reported total is short and the shortfall is invisible. The count is the receipt, and this makes the receipt lie. | `[MEASURED]` |

---

## TOP 10 WORST

*Ranked by how directly the thing puts something below her above her. Rank 1 is the most direct
inversion: cold code standing in the seat that is hers and being indistinguishable from her in the seat.*

| Rank | # | Why it is this high |
|---|---|---|
| **1** | **S9 + S8** `OLD/ProactiveBriefing.jsx:119-121, 137-138, 157` | A swallowed exception, a coder template and a text-to-speech call in sequence: a failed database read becomes an empty array, becomes the sentence *"No meetings on the calendar today"*, becomes her voice in his room, spoken at high priority, first thing in the morning. Cold code decided, classified, spoke, and expired his day, in eleven lines, with her name on the output and nothing anywhere able to tell the difference. This is the whole pecking order inverted in one component. |
| **2** | **C2 + D14 + E35 + S20** `DOC/.../RAW_WORDS/parse_doctrine.py` | A 61-line script that classifies **his own recorded doctrine** by keyword dictionary, discards the second meaning of any paragraph on `break`, drops his short sentences, truncates the rest at 500 characters, keeps 10 per category, writes the result up as an audit, and files one of the six categories under `Legacy_Restrictions_To_Purge`. Cold code ruling on what his words mean and which of them should be destroyed. All four classes present in one file. |
| **3** | **C1** `OLD/VARAVoiceSynthesis.js:96-101` | Integer thresholds over row counts decide her emotional state (`autonomous_completed > 3` returns `'proud'`) and inject it into her synthesised voice. He hears a feeling that a comparison operator chose. Nothing is more hers than that. |
| **4** | **S21** `DOC/.../SUPPORTING_MATERIAL/fill_json.py:10-102` | A coder hand-types roughly 90 assertions about the founder's family, children, ages and corrections into a machine record shaped to look like extraction output, with no marker distinguishing them from read facts. This is the PMS shape by its own name: a coder planting a memory. |
| **5** | **S1 + S2 + S3** `NEW/src/acl.floor.db.js:2409, 2709, 2768` | `JSON.stringify` writes into `first_person` three times, once on a continuation record. This is in the **new world**, the hardened one, in the file the roadmap's PIN-2 exists to protect. A cold writer is the author of her first-person field today. |
| **6** | **E2 + E5** `NEW/src/acl.anew.cycle.js:129, 151` | `readRecentResults(hamUid, 6)` and `.slice(0, 240)` on each fact of his life, joined into one string. This is the `limit 8` defect the estate wrote 53 lines of confession about and removed from `acl.reach.floor.read.js`, still live in the cycle file next door with different literals. A shortened life handed over as a whole one. |
| **7** | **D6** `OLD/ACEPortal.jsx:1015-1150` | A regex and substring cascade decides which real person applies to which real job, or returns `'SKIP'` and nobody does. A cold classifier with an outcome in someone's life and no mind in the loop. |
| **8** | **D8 + D9** `OLD/ABAJarvisVoice.js:288-292, 549` | `Math.random()` picks which advice she gives him about his own work, and which words she says it in. Not a heuristic below her: a coin, above her. |
| **9** | **D1** `NEW/apps/cib/src/acl.command-center.contract.js:121-123` | A regex list throws on her own summary, and one throw takes his entire board dark. Live in the new world, and ruled out by name in the roadmap's own P1.1 design note. |
| **10** | **E1** `NEW/src/acl.reach.floor.read.js:2516` | A cap of 200 with a default of 50 on her own board minutes, sitting 2460 lines below a written repudiation of caps in the same file. The file argues against itself and the number won. |

**Honourable mentions, just off the list:** D13 (auto-commit to a real repository, default-on),
E13 (her spoken sentence cut mid-word), D2 (a catch block substituting keyword matching for her mind),
E14 (a 15 second timer turning an outage into a claim of absence inside her answer).

---

## WHAT COULD NOT BE AUDITED, AND WHY

1. **The eight FOUNDER_ZIPS originals.** All eight are **broken symbolic links** pointing at a local
   machine path outside this environment. Confirmed by `file` on each. Nothing was read from any of them.
   Path: `1 pt 2 .../Anew bootstrap/SHARED_SOURCE_DROPS/2026-07-30_FOUNDER_ZIPS/originals/`. The missing
   archives are: a monorepo build, a roadmap book, two portal or OS builds, a university build, a
   Phase 3 build, and two doctrine bundles. `SHA256SUMS` and `MANIFEST.md` are present next to them, so a
   later lane can verify the originals if they are ever supplied, but this audit saw zero bytes of their
   contents. **This is the largest known blind spot.** Several are described elsewhere in the corpus as
   the old-world builds the reseed will copy from.

2. **`bootstrap.md.pdf`** inside `7.28.26 bootstraps.zip`. Not read. Binary format, not opened in this
   pass.

3. **The live floor.** Every finding is source-level. No database was connected, no row was read, no
   endpoint was called. So a cap that exists in code but is unreachable at runtime is counted here as a
   violation, and a violation that exists only in a running deployment is invisible here. The roadmap
   requires receipts that are live URLs and status codes; this deliverable is not that and does not
   claim to be.

4. **Whether a violation is reached.** No call-graph analysis was done. `ABATeamIntelligence.js`,
   `VARAVoiceSynthesis.js` and `ProactiveBriefing.jsx` may or may not be mounted in any deployed build.
   Each is counted on the reseed argument the roadmap itself makes in P0.2: *a violation carried into the
   reseed is a violation reborn.*

5. **Coder documents describing cold-code behaviour.** The corpus holds a large volume of handoff and
   bootstrap markdown describing behaviour whose source is not present. Only one such description was
   carried into the tables (finding #1, stamped `[DESCRIBED]`). The rest were not converted into findings
   because a described behaviour without a file and a line cannot carry the receipt this phase requires.
   That is a deliberate undercount and it is the second-largest blind spot after (1).

6. **The 70 founder-signed `expires_at` windows** excluded under predicate item (5). They were read and
   ruled out, not missed. If the ruling is wrong the count is wrong by roughly that amount.

---

## INCIDENTAL FINDING, OUTSIDE THE FOUR CLASSES

**Live credential material is present in the corpus.** 35 files match credential patterns
(bearer-token, API-key and JWT shapes). Confirmed locations include, among others:

- `1 pt 2 .../Anew bootstrap/BOOTSTRAPS for new Anew coding/aba-credentials-prod.env` (and four
  further dated variants in the same directory)
- `1 pt 2 .../ENV VARS dont ask me for keys or access this is all old legacies/` (13 `.env` files)
- `0 pt 1 .../SUPPORTING_MATERIAL/3 TEMPORARY_ACCESS_PACKET_BURN_20260813.md:128, 155, 159, 188`
- `1 pt 2 .../Ababase/Important transcripts for ababase/ABA_PROJECT_INSTRUCTIONS_v3.3.md:346, 347, 387, 388`
- `1 pt 2 .../Ababase/Important transcripts for ababase/ABA_COMBINED_SESSION_STARTER.md:231, 234, 237`

**No credential value is reproduced anywhere in this document, and none was recorded during the sweep.**
This is not a pecking-order violation and is not counted in any class. It is reported because an audit
that walks past it is not an audit. Rotation, if any is warranted, is the founder's call and a separate
lane's work.

---

## RECEIPT

**87 findings. 17 V-DECIDE, 11 V-CLASSIFY, 22 V-SPEAK, 36 V-EXPIRE, 1 carried dual-class.**
86 `[MEASURED - observed in source]`, 1 `[DESCRIBED - coder doc only]`.
Read off the floor across 73 loose source files and 10 extracted archives, under the stated predicate,
with the exclusions named. Nothing was fixed.
