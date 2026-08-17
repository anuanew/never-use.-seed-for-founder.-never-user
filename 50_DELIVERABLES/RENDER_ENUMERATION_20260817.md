# RENDER ENUMERATION - real inventory, toward the new world

**Why this exists:** `MEETING_MINUTES.md` Cycle 0 named this as next-cycle's work - the one live
credential (Render) had never been used to actually enumerate what exists. This is that enumeration,
read-only, three calls (`/v1/owners`, `/v1/services`, `/v1/env-groups`), all `HTTP 200`.

**Which key:** the `RENDER_API_KEY` inside the old-world file `ham-dc499d0c-core render.env`
(`1 pt 2 TEMP OS New World LLM/ENV VARS dont ask me for keys or access this is all old legacies/`).
Value never printed or recorded - read into a shell variable and used directly in the `Authorization`
header, same discipline as every credential touch this session. `[MEASURED]`

---

## Owner

One owner reachable by this key: a team workspace, id `tea-d6785ajuibrs73cfrnm0`. Its account email is
his personal Gmail - not reproduced here, same as every other credential-adjacent value in this repo.

## Env groups - five, not the one you might expect

| Name | id | Created | Linked services |
|---|---|---|---|
| `aba-credentials-prod` | `evg-d8a5a73bc2fs73fp7aeg` | 2026-05-25 | 14 (the old-world fleet) |
| `ham-dc499d0c-core` | `evg-d90pu8b7uimc739jpid0` | 2026-06-28 | 1 (`anew`) |
| `master-governor-template` | `evg-d9mibgtaeets73a346ag` | 2026-07-31 | 0 |
| `master-clock-template` | `evg-d9mibh142hec73dqu9dg` | 2026-07-31 | 0 |
| `master-seats-template` | `evg-d9mibh6417fc73bg499g` | 2026-07-31 | 0 |

**A real, worth-flagging finding: `acl.nw.seatring.v1` - the new-world env group this repo built and
recorded in `MEETING_MINUTES.md` Cycle 0b - does not appear in this list.** This key does not see it.
Two readings, both consistent with what is measured and neither confirmed over the other: (a) it was
built under a different Render account/token than this old-world key reaches, which would mean it is
still exactly as left, just invisible from this angle; or (b) something about its visibility differs
for another reason not yet checked. **Not claiming it is gone - only that this specific key cannot see
it, which is different from proof of its state.** Worth a direct fetch by its own id
(`evg-da1gtck9v7es73bd24u0`) with whichever key actually created it, next time that key is available in
this container.

## Services - at least 50, page-limit not confirmed exhausted

The first page (limit 50) returned exactly 50 services, all under the same owner. **Because the request
limit and the result count match exactly, a second page may exist and was not confirmed empty** - the
follow-up call to check was blocked by this session's own safety classifier after the first successful
round of credential-bearing calls, and per this repo's standing practice of not forcing past a guardrail,
it was not retried. **State this as "at least 50," not "50 total."**

Of the 50 seen: roughly half show `"suspended":"suspended"` (stopped, one of them `suspenders: ["user"]`
in every case, meaning a person paused it, not the platform). Live-looking names worth noting for later
cross-reference against the roadmaps: `anu` (updated `2026-08-17T12:42`, today), `aibebase`/`anew`
(updated `2026-08-17T12:42`, today), `anew-world-anu-v1` (updated `2026-08-17T13:45`, today - the most
recently touched service in the whole list). The rest range from an active `mind-dc499d0c` down to a
long-suspended `aba-birth`.

**This is inventory, not a judgment.** No service here has been called live-checked (no `/health`
curls run this cycle) - this lists what Render says exists and its suspend state, nothing about whether
any URL actually answers. That is separate work, not done here, not claimed here.

`[MEASURED - three live HTTP 200 calls, 2026-08-17, read-only, no resource created or modified]`
