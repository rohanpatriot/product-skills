# Scope Hammer

I'll help you cut scope to ship within appetite. The scope hammer isn't a last resort — it's a required tool that you should be swinging throughout the cycle. If you're using it for the first time in Week 5, you waited too long.

## When to Use

- Work is clearly exceeding appetite (more left than time)
- A scope won't make it and you need to decide what stays
- The pitch needs to ship but not everything can ship
- You're in the final weeks and need to make hard calls
- New scope appeared mid-cycle and it needs to be evaluated

## Prerequisites

Read [core-concepts.md](../references/core-concepts.md) — specifically Fixed Time/Variable Scope — before proceeding. Read [anti-patterns.md](../references/anti-patterns.md) — the Scope section — to understand what you're preventing.

---

## Step 1: Establish the Scope Problem

Use `AskUserQuestion` to understand the situation:

**Question:** "Walk me through the scope problem. What's over budget — is it a specific scope, the whole pitch, or something new that appeared mid-cycle?"

Determine:
- How much time is left in the cycle?
- What's definitely done and shipped?
- What's still in progress and approximately where?
- What hasn't started yet?

Document the gap:

```
Cycle Status: [Week X of 6] — [N days remaining]

Done:
- [Scope A] ✓
- [Scope B] ✓

In progress:
- [Scope C] — [where on the hill / rough time remaining estimate]
- [Scope D] — [where on the hill / rough time remaining estimate]

Not started:
- [Scope E]
- [Scope F]

Rough remaining work vs. remaining time:
[Honest assessment: do these match, or is there significantly more work than time?]
```

---

## Step 2: Define "Must-Have" vs. "Nice-to-Have"

The scope hammer only works if you're honest about which work is load-bearing. Use `AskUserQuestion`:

**Question:** "For each scope still in progress or not started — is this load-bearing for the pitch, or is it a nice-to-have? What happens if it doesn't ship?"

The test for load-bearing:
- Without this, the pitch fails to deliver its core promise to users
- Without this, the released feature is unusable or broken
- Without this, the problem the pitch was solving goes unsolved

The test for nice-to-have:
- Without this, the core use case still works
- This makes the feature more polished or complete, but doesn't change whether it works
- Users could get real value without this

**Common nice-to-haves disguised as must-haves:**
- Empty states and edge case handling (often can be basic/ugly and shipped)
- Animation and transitions (rarely load-bearing)
- Advanced filtering or sorting (basic filter is usually enough for v1)
- Bulk operations (single-item operations ship first)
- Notification systems (email is enough; in-app notifications are nice-to-have)
- Historical data or retroactive application (new data only works for v1)
- Full error recovery flows (basic error messages are enough)
- Admin management UI (direct database edits work for low volume)

Document the classification:

```
Must-haves (load-bearing):
- [Scope C]: [Why it's load-bearing — what breaks without it]
- [Part of Scope D]: [The specific element that's load-bearing]

Nice-to-haves (cuttable):
- [Part of Scope D]: [What this part adds and why it's not essential]
- [Scope E]: [Why this doesn't affect core functionality]
- [Scope F]: [Why this is additive, not foundational]
```

---

## Step 3: Apply the Hammer

Work through cuttable scope systematically. Use `AskUserQuestion` for each cut:

**Question:** "For [nice-to-have scope/element] — can we ship the core without it? And if we cut it, is there any downstream effect on what we're keeping?"

For each cut, confirm:
- The cut doesn't break what's being kept
- The remaining feature is genuinely usable
- The cut is communicated to the team immediately (not discovered on ship day)

**Cutting tactics:**

### Cut the whole scope
The entire scope isn't load-bearing. Stop work, cut it cleanly.

```
Cut: [Scope F]
Rationale: Users can accomplish the core task without this. We'll evaluate for future shaping.
```

### Slice the scope
The scope has must-have and nice-to-have elements. Keep the must-have, cut the nice-to-have.

```
Slice: [Scope D]
Keep: [The specific element that's load-bearing]
Cut: [The element that's additive]
Rationale: The core functionality works without [cut element].
```

### Downgrade the quality
The scope must ship, but doesn't need to ship beautifully. A rough but functional version is better than a polished version that misses the deadline.

```
Downgrade: [Scope C]
Original: [What the team was building]
Shipped version: [The simplified version that works but isn't polished]
Rationale: Functional beats missing.
```

### Defer to follow-up
The scope is genuinely useful but not load-bearing for v1. Explicitly commit to a follow-up small batch pitch, if the problem is worth it.

```
Deferred: [Scope E]
To: [Future small batch pitch — "Follow-up: [name]"]
Rationale: Core ships without this. This is worth a dedicated 1-week effort next cycle.
```

---

## Step 4: Validate What Remains

After applying the hammer, validate that what remains is actually shippable. Use `AskUserQuestion`:

**Question:** "After these cuts — walk me through what a user actually experiences when they use this feature. Is it complete? Is it broken anywhere? Are there obvious gaps that would confuse or frustrate them?"

Walk through the core user journey:
1. What does the user see when they first encounter this feature?
2. What do they do next?
3. What happens at each step?
4. How does it end?

Check for broken experiences:
- Steps in the flow that reference removed functionality
- Empty states that aren't handled
- Error conditions that would confuse users
- Paths that lead nowhere

If the remaining scope has obvious broken experiences, you have two choices:
- Spend a small amount of time fixing the broken experience (if it's truly small)
- Cut more scope so the remaining feature doesn't have that path

Document the validated scope:

```
Remaining scope (post-hammer):

Core user journey:
1. [User lands on X]
2. [User does Y]
3. [User achieves Z]

What ships:
- [Scope A — complete]
- [Scope B — complete]
- [Scope C — must-have elements only]

What doesn't ship this cycle:
- [Scope D — cut, follow-up pitch recommended]
- [Scope E — cut, evaluate future value]
- [Scope F — cut, not worth reshaping]
```

---

## Step 5: Communicate the Cuts

Bad: Team discovers cuts on ship day.
Good: Team knows cuts as soon as decisions are made.

Use `AskUserQuestion`:

**Question:** "Who needs to hear about these cuts? What's the right way to tell the team — a quick meeting, a written update, or directly in the tracking tool?"

**For the team:**
- Be direct: "We're cutting [scope]. Stop work on it now and focus on [remaining]."
- Explain why: "This lets us ship the core. [Cut scope] is a nice-to-have."
- Acknowledge the tradeoff: "We know this means the feature won't have [thing]. That's the right call."
- Don't apologize: scope hammering is the system working correctly.

**For leadership/stakeholders:**
- What's shipping this cycle and what isn't
- Why the cuts were made (not load-bearing for the core promise)
- What will happen to cut scope (future pitch, not backlog)

**For users (if applicable):**
- Sometimes cuts affect what was communicated externally
- If so, update messaging before ship day, not after

---

## Step 6: Prevent Future Overruns

After the cycle, do a brief retrospective on why scope hammering was needed. Use `AskUserQuestion`:

**Question:** "Now that the cycle is over — where did the scope problem originate? Was it the pitch, the estimation, unexpected technical complexity, or mid-cycle scope creep?"

Common root causes:

**Pitch-level problems:**
- Appetite was set too small for the actual complexity
- Rabbit holes weren't identified
- No-gos weren't explicit enough, leading to scope creep

**Execution-level problems:**
- Team didn't scope hammer early enough, waiting until Week 5
- Team added scope mid-cycle (nice-to-haves crept in)
- Team built the polished version before validating the core worked

**Unknowns:**
- Genuine technical surprise that couldn't have been anticipated
- Third-party API limitation discovered mid-cycle
- Data structure didn't support the intended solution

Document the lesson:

```
Root cause: [Brief description]
Shaping lesson: [What should be done differently in future pitches]
Building lesson: [What the team should do differently in future cycles]
```

---

## Scope Hammer Rules

**Rule 1: Swing early, swing often.** The scope hammer is most effective in Week 2–3. In Week 5–6, you're cutting in panic, not in control.

**Rule 2: Functional beats polished.** A rough but working feature ships. A beautifully designed feature that isn't done doesn't.

**Rule 3: Core before completeness.** Build the core user journey end-to-end before building any feature completely. That way, you always have something that could ship.

**Rule 4: Must-have is a high bar.** Something is only a must-have if the feature is genuinely broken or unusable without it. Polish, edge cases, and nice-to-haves don't meet the bar.

**Rule 5: Cuts are real.** When you cut a scope, it doesn't automatically come back next cycle. It goes to the pool of raw ideas. If it's worth building, someone shapes it again.

**Rule 6: No guilt.** Scope hammering is not failure. It's evidence that the system is working. Fixed time, variable scope. This is what "variable scope" means.

---

## Scope Hammer Decision Tree

```
Is this scope load-bearing?
├── No → Cut it
└── Yes → Is there time to complete it?
    ├── No → Can it be sliced to a smaller version?
    │   ├── Yes → Slice and ship the smaller version
    │   └── No → Does the pitch work without it?
    │       ├── Yes → Cut it and ship the rest
    │       └── No → The whole pitch may not ship — escalate to leadership
    └── Yes → Continue on current track
```

## What Comes Next

After applying the scope hammer, track progress on the remaining scope in [track-progress.md](track-progress.md). At end of cycle, the team ships what's done, then enters cool-down.
