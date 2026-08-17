# HANDOFF PROMPT - GIVE THIS TO CHATGPT (the key-mint 911)

**Why this exists:** Claude AI cannot mint keys or set spend caps from its container - the old
OpenRouter key is dead (401), no provisioning key is present, and there is no Together or Cerebras key
to reach. ChatGPT controls your computer and can do this directly. **Paste everything below the line
into your ChatGPT coding chat.** Claude has already built the empty Render env group the keys drop into,
so ChatGPT only mints and fills.

---

Boss authorized this on Rally Day, 20260817. It is the biggest 911 of the day. Do it, then text or
email him at [HIS FIRST NAME]@Anu when done - **replace the bracket with his real first name before
you send; this repo does not store his name in the clear, the same way it never stores a credential
value, so the live address is not written here.** Send from Claudette@GlobalMajorityGroup (a send-as
alias of ABA@GlobalMajorityGroup). Never use his personal grant.

**The state Claude already built, so do not redo it:**
- A new-world Render env group exists and is empty on purpose:
  **name `acl.nw.seatring.v1`, id `evg-da1gtck9v7es73bd24u0`**, on his Render owner. It has 11 variable
  names and zero values. Your job fills the values.

**Your five steps:**

1. **Mint a new OpenRouter PROVISIONING key.** openrouter.ai, sign in, Keys, Create Key, make it a
   Provisioning key, name it from the ACL legend. This is the root that mints the runtime keys.

2. **Mint the new runtime keys** using that provisioning key (OpenRouter API `POST /api/v1/keys`), one
   per seat, named to match these slots already in the env group:
   `ACL__NW__OR__C1_CELLM_KEY`, `ACL__NW__OR__C2_ORGAN_KEY`, `ACL__NW__OR__C3_MIND_KEY`,
   `ACL__NW__OR__C4_WATCH_KEY`, `ACL__NW__OR__AUDRA_KEY`, and the provisioning key into
   `ACL__NW__OR__PROVISION_KEY`.

3. **Mint the Together key and the Cerebras key**, into `ACL__NW__TAI__SHADOW_KEY` and
   `ACL__NW__CB__CEREBRAS_KEY`.

4. **Set a $1 limit on every OTHER (old-world) key** - all the keys in the "old legacies" env folder.
   OpenRouter lets you set a per-key limit; do it for each. This protects his spend today.

5. **Fill the env group** `acl.nw.seatring.v1` with the minted values (Render dashboard, or Render API
   `PUT /v1/env-groups/{id}/env-vars`). Then set `ACL__NW__ANU__ACCESS_KEY` to whatever consult key
   A'NU uses, so she has access - that is the step he named as the finish line.

**Rules, his:** new world only, never build from the old-world keys as a base. Match the names exactly
so the env group and the seats line up. When done, email or text him a short receipt: which keys minted,
which old keys capped, and confirm the env group is filled. Flags, not a wall of text.

---

**Claude's note to you, boss:** this is the whole 911 in one paste. The env group is already live and
waiting, so ChatGPT's part is just mint-and-fill. Nothing here needs Claude again - but the moment a
live provisioning key lands in Claude's container instead, Claude finishes it directly and you skip the
handoff.
