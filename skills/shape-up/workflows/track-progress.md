# Track Cycle Progress

I'll help you read your hill charts, identify stuck scopes, and decide what to do about them. The hill chart is the primary signal during the building period — not status meetings, not daily standups.

## When to Use

- During the building period (you're in an active cycle)
- You see a scope that hasn't moved in multiple updates
- You're approaching the end of the cycle and want an honest progress assessment
- A scope seems to be taking longer than expected
- You need to decide whether to cut, continue, or escalate

## Prerequisites

Read [core-concepts.md](../references/core-concepts.md) — specifically the Hill Charts and Scopes sections — before proceeding.

---

## Step 1: Get the Current State

Use `AskUserQuestion` to understand where you are:

**Question:** "Where are you in the cycle, and what does your hill chart look like right now? Walk me through each scope and its current position."

Ask for:
- Week of the cycle (e.g., "Week 3 of 6")
- Number of scopes
- Position of each scope: far uphill, mid-uphill, top of hill, mid-downhill, near done, done
- How long each scope has been in its current position

Document the state:

```
Cycle Status: Week [X] of [6]

Scope: [Name]
  Position: [uphill / top / downhill / done]
  Last moved: [X days / X weeks ago]
  Team assessment: [what the team says about this scope]

Scope: [Name]
  Position: [uphill / top / downhill / done]
  Last moved: [X days / X weeks ago]
  Team assessment: [what the team says about this scope]
```

---

## Step 2: Identify Scope Health

For each scope, evaluate its health. Use `AskUserQuestion` for any scope that looks concerning:

**Question:** "Tell me more about [scope name]. What does 'uphill' mean for them right now — what are they figuring out?"

### Uphill Scopes — Signal Reading

Uphill is expected early in the cycle. It becomes a red flag when:

**Early cycle (Week 1–2):** Uphill is normal. Team is figuring out the approach.

**Mid-cycle (Week 3–4):** A scope still in the early uphill position is concerning. They should be converging on an approach by now.

**Late cycle (Week 5–6):** Any scope still uphill is a crisis. There isn't enough time to figure out the approach AND execute. This scope almost certainly won't ship.

**Stuck uphill signals:**
- "We're still deciding between two approaches"
- "We discovered the database schema doesn't support this"
- "We found a third-party API limitation we didn't anticipate"
- "The team keeps going back and forth on the design"
- Scope has been in the same uphill position for 2+ check-ins

Use `AskUserQuestion` for any stuck uphill scope:

**Question:** "What specifically is blocking [scope]'s progress uphill? Is this a technical unknown, a design decision, or something else? What would it take to get over the hill?"

---

## Step 3: Triage Stuck Scopes

For each stuck or concerning scope, you have four options. Work through them in order:

### Option A: Help the Team Get Over the Hill

Sometimes an uphill scope needs senior input — a technical decision, a design call, or access to information the team doesn't have.

Use `AskUserQuestion`:

**Question:** "Is this scope stuck because the team needs a decision made for them, or because the problem is genuinely unsolved? What would a senior technical or product perspective add here?"

**Appropriate interventions:**
- A 30-minute conversation where a senior person has seen this problem before
- A clear decision on a design question the team is debating
- Access to a data source or subject-matter expert
- Removal of an organizational blocker

**Not appropriate:**
- Assigning a manager to the scope
- Adding more engineers mid-cycle
- Changing the scope to something easier

### Option B: Cut the Scope

If a scope can't be gotten over the hill in time, cut it. The question is whether the pitch delivers value without this scope.

Use `AskUserQuestion`:

**Question:** "If [scope] doesn't ship this cycle, does the pitch still deliver the core value it promised? Is there a version of this that ships without [scope] and is still meaningful?"

**Cut criteria:**
- The scope is nice-to-have, not load-bearing
- The pitch's core promise holds without this scope
- There isn't time to solve the technical problem and execute
- The team has other scopes that are more important to ship

If cutting, be explicit:

```
Decision: Cut [scope name] from this cycle

Rationale: [Why this scope isn't load-bearing for the pitch]

What ships instead: [What the pitch delivers without this scope]

Follow-up: [Note this as a potential future pitch / small batch if the problem is worth solving]
```

### Option C: Slice the Scope

Sometimes a scope is too big. Instead of building all of it, identify the essential slice that delivers the core value.

Use `AskUserQuestion`:

**Question:** "Is there a simpler version of [scope] that still solves the core problem? What's the minimum that has to exist for this scope to be useful?"

**Slicing examples:**
- "Bulk export" → scope to "export up to 50 items, no progress indicator"
- "Advanced filter" → scope to "filter by date range only, no saved filters"
- "Notification system" → scope to "email-only, no push or in-app"

### Option D: Accept the Scope Won't Ship

Sometimes the honest answer is that a scope won't make it, and that's okay if the rest of the pitch ships.

Use `AskUserQuestion`:

**Question:** "If we accept that [scope] won't ship this cycle, is the rest of the pitch still worth shipping? Or does that create a product that's too incomplete to release?"

If the pitch can ship without the scope, accept the cut, note it for future shaping, and let the team focus on what will ship.

If the pitch can't ship without the scope, see [scope-hammer.md](scope-hammer.md) for aggressive scope reduction across the entire pitch.

---

## Step 4: Check Downhill Scopes

Downhill work is executing a known plan. It should be predictable. If downhill scopes aren't progressing steadily, something is wrong.

Use `AskUserQuestion`:

**Question:** "For the scopes that are downhill — what's the blocker? Downhill work should be moving steadily toward done. What's slowing it?"

**Downhill blockers:**
- Unexpected technical complexity (scope is actually still uphill)
- External dependencies (waiting on another team, API, deployment)
- Team capacity (someone out sick, a genuine emergency)
- Scope creep (the team added work during execution)

For each downhill blocker, identify the cause and remove it:

```
Downhill scope: [Name]
Blocker: [What's slowing execution]
Action: [How to remove the blocker]
Expected: [When should this scope be done?]
```

---

## Step 5: Project End-of-Cycle State

At any point in the cycle, you can project what will ship. Use `AskUserQuestion`:

**Question:** "Based on current scope positions and velocity, what's your honest assessment — what ships at end of cycle?"

Build a simple projection:

```
End-of-Cycle Projection (Week [X] of 6):

Will ship:
- [Scope A] — downhill, on track
- [Scope B] — downhill, on track

Likely to ship (needs intervention):
- [Scope C] — uphill, but team knows the approach

Unlikely to ship:
- [Scope D] — stuck uphill, cut or slice recommended

Already done:
- [Scope E] — completed Week 2
```

---

## Step 6: Update Based on Triage

After working through stuck scopes, document the decisions and communicate them:

**Question (use `AskUserQuestion`):** "Who needs to know about these scope decisions — the team, leadership, or both? How do you typically communicate mid-cycle adjustments?"

For the team:
- Clear decisions on cut scopes (stop working on X, confirmed)
- Clear decisions on sliced scopes (build the simplified version, confirmed)
- Any intervention coming (we're sending [person] to help unblock [scope])

For leadership:
- Honest progress summary: what's on track, what's been cut, what the cycle will ship
- No surprises at end of cycle — leaders who've been tracking the hill chart shouldn't be surprised by the outcome

---

## Hill Chart Hygiene

Good hill chart practices that keep the signal accurate:

**Update frequency:** Every 2–3 days during active building, not daily (avoids micro-tracking) and not weekly (too slow to catch problems).

**Update honesty:** Scope positions should reflect the team's honest understanding, not what they think management wants to see. A scope stuck uphill for two weeks is information — don't hide it.

**Scope granularity:** 5–10 scopes for a 6-week project is healthy. Fewer than 4 means the work isn't decomposed enough to track meaningfully. More than 15 means the team is task-managing, not hill-charting.

**New scopes appearing late:** If new scopes appear in Week 4 or 5, that's scope creep. Unless they're replacing cut scopes, they shouldn't be there. See [scope-hammer.md](scope-hammer.md).

**Scope consolidation:** If the team finds that multiple scopes always move together, consolidate them. They're not really separate scopes.

---

## Reading Patterns

### Healthy Cycle
```
Week 1: Most scopes uphill (normal)
Week 2-3: Scopes reaching top of hill
Week 4-5: Most scopes downhill
Week 6: Scopes completing, at or near done
```

### Struggling Cycle
```
Week 4: Multiple scopes still early uphill
Diagnosis: Shaping underestimated complexity, or team hit rabbit holes
Action: Scope hammer — aggressive cutting to ensure something ships
```

### False Progress
```
Week 5: All scopes suddenly move from uphill to "almost done"
Diagnosis: Team was tracking dishonestly, now panicking
Action: Honest conversation about what's actually done vs. what's still working
```

### Creeping Scope
```
Week 3: New scopes appearing that weren't in the original pitch
Diagnosis: Team is adding nice-to-haves or solving adjacent problems
Action: Cut the new scopes, refocus on the pitch
```

## What Comes Next

If scopes won't fit the appetite, apply [scope-hammer.md](scope-hammer.md). If the cycle is on track, the team ships at the end of the building period and enters cool-down.
