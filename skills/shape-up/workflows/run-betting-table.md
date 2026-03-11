# Run a Betting Table

I'll guide you through evaluating shaped pitches and making bet/no-bet decisions for the next cycle. The betting table is a decision meeting, not a presentation. Come in having read the pitches.

## When to Use

- Cool-down is ending and you're deciding what to build next cycle
- You have a set of shaped pitches ready for evaluation
- Leadership needs to make explicit cycle commitments

## Prerequisites

Read [principles.md](../references/principles.md) — specifically "Bets, Not Backlogs," "Appetite, Not Estimates," and "No Interruptions During the Cycle." Read [anti-patterns.md](../references/anti-patterns.md) — the Betting Table section — before proceeding.

---

## Step 1: Confirm the Betting Table Setup

Use `AskUserQuestion` to understand your context:

**Question:** "Tell me about your upcoming cycle. Who's attending the betting table? What pitches are on the table? How many teams do you have capacity for?"

Key setup questions:
- Who is in the room? (Should be: CEO/CTO/senior product-engineering leaders. Small group.)
- Have participants read the pitches in advance, or are we reading them together now?
- How many teams do you have available this cycle?
- Are there any carry-forward commitments from the last cycle?
- Is there anything the company is committed to that constrains the betting decision?

Document the available capacity:

```
Cycle Capacity:
- Teams available: [number and type — full-stack, specialized, etc.]
- Big batch slots: [how many 6-week pitches the teams can handle]
- Small batch slots: [how many 1–2 week pitches can fill the remaining capacity]
- Constraints: [any pre-committed work, regulatory requirements, etc.]
```

---

## Step 2: Review Each Pitch

For each pitch on the table, work through a structured evaluation. Use `AskUserQuestion` for each:

**Question:** "Let's evaluate [Pitch Name]. What's the problem it's solving, and does the group agree that problem is real and worth solving?"

Work through these dimensions for each pitch:

### 2a. Problem Validity

- Is the problem real? Do we have customer evidence for it?
- Is this problem affecting enough users to justify the appetite?
- Is this the right time to solve it — strategically, technically, for our users?
- Is the problem actually a problem, or a solution in disguise?

```
Problem validity: [Strong / Weak / Unknown]
Notes: [What the group said]
```

### 2b. Appetite Assessment

- Is the stated appetite appropriate for the problem?
- Would we actually let the circuit breaker trip if the team isn't done in [appetite] weeks?
- Is this a big batch when it should be a small batch (or vice versa)?

```
Appetite assessment: [Appropriate / Too big / Too small / Unclear]
Notes: [What the group said]
```

### 2c. Solution Viability

- Does the solution sketch show something that could actually be built in the appetite?
- Are there obvious technical risks the shaper didn't address?
- Does the team that would build this have the relevant expertise?

```
Solution viability: [Buildable / Risky / Unknown]
Technical concerns: [Any blockers or risks]
```

### 2d. Strategic Fit

- Does building this move us toward our current goals?
- Is this the highest-leverage thing we could bet on this cycle?
- What's the opportunity cost — what aren't we building if we bet this?

```
Strategic fit: [High / Medium / Low]
Opportunity cost: [What we're not building]
```

### 2e. Risk Profile

- What are the biggest risks if this goes wrong?
- What's the worst case if the team hits the circuit breaker?
- Is there a version of this that fails in a dangerous way (data loss, customer trust, security)?

```
Risk profile: [Low / Medium / High]
Key risks: [Top 1-2 risks]
```

---

## Step 3: Make the Bet Decision

After evaluating each pitch, use `AskUserQuestion` to surface the decision:

**Question:** "Given that evaluation — bet or no bet for [Pitch Name]? And if yes, which team?"

For each pitch, the decision is binary: **bet** or **no bet**. There is no "maybe" or "conditional." Conditional bets are deferred decisions that create unclear commitments.

**Bet:** The pitch goes to a specific team for the upcoming cycle. The team's capacity is committed.

**No bet:** The pitch doesn't get bet this cycle. It doesn't go to a backlog. If the problem is still worth solving next cycle, it gets reshaped (or re-pitched as-is if nothing has changed).

**Reasons to not bet:**
- Problem doesn't feel real or well-evidenced
- Appetite doesn't match the scope
- Solution sketch has significant rabbit holes the shaper didn't address
- Better bets available for the team capacity
- Wrong timing (dependency on something else, wrong cycle, regulatory constraint)
- Team doesn't have the expertise

**Never no-bet because:**
- "We'll get to it later" — that's backlog thinking
- "It's good but not perfect" — nothing is; bet the best available
- The shaper is present and advocating for it — evaluate the pitch, not the advocacy

Document each decision:

```
[Pitch Name]: BET / NO BET
Assigned team: [team name, if bet]
Rationale: [one sentence]
```

---

## Step 4: Assign Teams to Bets

For each bet, make the assignment explicit. Use `AskUserQuestion`:

**Question:** "For [Pitch Name] — which team is the right fit? Do they have any context or expertise that makes this bet particularly well-matched or risky?"

Consider:
- Domain expertise: does the team know this part of the product?
- Technical stack: does the team have the skills to build the solution?
- Fresh eyes: sometimes a team without prior context spots better solutions
- Workload: is this team coming off a heavy cycle and needs a lighter bet?

```
Team Assignments:
- [Pitch A]: [Team X]
- [Pitch B]: [Team Y]
- [Small batch 1]: [Team Z]
- [Small batch 2]: [Team Z]
```

---

## Step 5: Handle Small Batches and Cool-Down Work

Not all capacity goes to big batches. Use `AskUserQuestion`:

**Question:** "What's going into the remaining team capacity — small batches, or are those teams on a longer cool-down?"

Small batch bets follow the same evaluation criteria as big batches, just faster. Each small batch should have a shaped pitch (even if lighter-weight) with a defined appetite.

**Common small batch categories:**
- Bug fixes with known solutions
- Minor feature improvements with clear scope
- Targeted UX improvements with obvious solutions
- Technical maintenance with bounded scope (not open-ended "refactor everything")

Cool-down work doesn't need a pitch or betting table decision. Teams use cool-down autonomously: fixing bugs, exploring ideas, doing tech debt, resting.

---

## Step 6: Communicate the Decisions

After the betting table, communicate clearly. Use `AskUserQuestion`:

**Question:** "Who needs to know the betting table decisions? Teams? The broader company? How do you typically communicate cycle plans?"

At minimum, the teams need to know:
- What pitch they've been assigned
- Who is on their team for this cycle
- When the cycle starts

The company might benefit from:
- A brief summary of what's being built this cycle and why
- No-bet decisions with brief rationale (prevents "what happened to X?")

Draft a cycle announcement:

```markdown
# Cycle [Number] Bets

We're starting [date] and shipping [date + 6 weeks].

**[Team A]** is building **[Pitch A]** — [one-sentence problem description]

**[Team B]** is building **[Pitch B]** — [one-sentence problem description]

**[Team C]** is running two small batches:
- [Small batch 1] — [one-sentence description]
- [Small batch 2] — [one-sentence description]

Pitches that didn't get bet this cycle: [list]. These may come back as pitches in future cycles.
```

---

## Step 7: Prepare for the Building Period

Before teams start building, confirm:

Use `AskUserQuestion`:

**Question:** "Before the cycle starts — is there anything teams need to know that isn't in the pitches? Technical context, recent customer feedback, access to systems?"

Checklist before cycle start:
- Teams have access to the pitch documents
- Teams know their teammates (everyone assigned to each team is confirmed)
- No mid-cycle interruptions are scheduled (planned maintenance, company-wide events)
- Escalation path is clear: if teams hit a genuine blocker, who do they talk to?
- Hill chart mechanism is set up: how will teams report progress?

---

## Betting Table Failure Modes

1. **Presenting pitches at the meeting** instead of reading them in advance — decisions become political advocacy
2. **Betting everything on the table** regardless of quality — appetite for activity over appetite for quality
3. **Conditional bets** ("we'll build X if Y is true by week 3") — creates ambiguity mid-cycle
4. **Assigning work without naming a team** — diffuse accountability
5. **No-betting for vague reasons** ("just doesn't feel right") without articulating why — denies the shaper useful feedback
6. **Maintaining a backlog of no-bet pitches** — backlogs are anti-Shape-Up
7. **Skipping the betting table** because "we already know what we're building" — removes the deliberate decision point

## What Comes Next

Teams start the building period. Track their progress on [track-progress.md](track-progress.md). If teams run into scope problems, apply [scope-hammer.md](scope-hammer.md).
