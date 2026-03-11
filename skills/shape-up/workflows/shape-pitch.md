# Shape a Pitch

I'll guide you from raw idea to a complete, betting-table-ready pitch. Shaping is a creative, iterative process — not a linear form to fill out. Expect to move back and forth between steps as the solution clarifies.

## When to Use

- You have a raw idea, customer request, or problem worth exploring
- Leadership wants to bet something next cycle but doesn't have a shaped pitch yet
- An existing pitch came back from the betting table for reshaping
- You're in cool-down and have time to shape for the next cycle

## Prerequisites

Read [core-concepts.md](../references/core-concepts.md) for appetite, fixed time/variable scope, fat marker sketches, and breadboards before proceeding. Read [principles.md](../references/principles.md) for the "Problems, Not Features" and "Shaping Is Not Design" principles.

---

## Step 1: Define the Problem

Use `AskUserQuestion` to understand what you're actually solving:

**Question:** "Tell me about the problem. Who is experiencing it? What are they trying to do? What goes wrong?"

Probe deeper:
- How do you know this is a real problem? Have you seen it or heard about it from customers?
- How often does this happen? To what percentage of your users?
- What's the consequence of this problem — what does the user lose, fail at, or have to do instead?
- Is this a new pain or something users have worked around for a long time?

**The test for a well-defined problem:** You can describe it entirely without mentioning a solution. If the problem description includes "we need to add a button that..." or "users want the ability to...", you're describing a solution, not a problem.

Document the problem:

```
Problem: [Who] trying to [what] runs into [what difficulty] which causes [consequence].

Evidence: [How do you know this is real — observed, interviewed, support tickets, etc.]

Frequency: [How often, how many users affected]
```

---

## Step 2: Set the Appetite

Use `AskUserQuestion` to establish the appetite before touching the solution:

**Question:** "Before we sketch anything — how much is this problem worth solving? Given your other priorities, is this a small batch (1–2 weeks) or a big batch (6 weeks)?"

Help them think through it:
- Small batch (1–2 weeks): The problem is clear, the solution approach is obvious, there aren't many unknowns. This fits alongside other small batch work in a cycle.
- Big batch (6 weeks): The problem is significant, the solution requires genuine design work, or there are enough unknowns that the team needs real time to explore.

**Appetite-setting questions:**
- If we shipped something that solved 80% of this problem in 2 weeks, would that be valuable?
- Would you be comfortable if this wasn't built this cycle at all?
- Is this problem worth giving up 6 weeks of a team's capacity?

Record the appetite clearly:

```
Appetite: [Small batch: 1–2 weeks] or [Big batch: 6 weeks]

Rationale: [Why this problem is worth this much time — not how long it will take]
```

If you can't justify the appetite based on problem severity, you may not have a real problem or may be overestimating the solution complexity.

---

## Step 3: Sketch the Solution

Now you can think about solutions — but at the right level of abstraction. The goal is to show what you're building without specifying how it's built.

Use `AskUserQuestion` to start sketching:

**Question:** "Walk me through your rough idea for the solution. What would the user see or do differently?"

As they describe it, guide toward the right level:

**If they're too abstract** ("make it easier to do X"):
- What element would the user interact with? A button? A new page? A modal?
- Where in the existing product does this appear?
- What's the first thing the user would do?

**If they're too concrete** (describing exact pixel layouts, color schemes, full Figma):
- We don't need that level yet — that's the team's job
- Let's describe what elements exist and how the user moves through them
- The team will make the design decisions; we just need to show the approach

**Tools for sketching:**

*Fat marker sketch* — use when the solution involves a new visual surface or layout:
```
[Describe what's on the screen and how elements relate spatially]
Example: "At the top of the invoice list, a new 'Bulk actions' bar appears when any invoice is selected. It contains a count and two buttons: Export selected and Mark as paid."
```

*Breadboard* — use when the solution involves flow across multiple states:
```
Places:
  → Invoice List
  → Bulk Export Modal

Affordances:
  Invoice List
    [Select All] checkbox in header
    Per-row checkbox
    When any selected: Bulk Action Bar appears
      [Export Selected] → opens Bulk Export Modal
      [Mark Paid] → updates status inline

  Bulk Export Modal
    Format options: PDF / CSV
    [Cancel] → dismisses
    [Export] → triggers download, shows success toast
```

Produce the sketch document:

```
Solution Sketch:

[Describe the key elements and flow at fat-marker / breadboard level]
[Include the sketch or breadboard notation]

Key elements:
- [Element 1 and what it does]
- [Element 2 and what it does]
- [Flow from state A to state B]
```

---

## Step 4: Identify Rabbit Holes

Use `AskUserQuestion` to find the traps:

**Question:** "What are the obvious edge cases or technical tangents that could pull the team off course? What could turn into a 2-week detour?"

Common rabbit hole categories:
- **Edge cases:** What happens when there's no data? When the user has 10,000 items? When the operation fails halfway through?
- **Integrations:** What third-party systems does this touch? Are there API rate limits, sync delays, or consistency issues?
- **Permission/role complexity:** Does this behave differently for different user types?
- **Historical data:** Does this need to work retroactively on old data?
- **Error handling:** What are the failure modes, and how complex is graceful recovery?
- **Notifications:** Should any action trigger emails, webhooks, or other downstream events?

For each rabbit hole: decide whether to solve it or exclude it from scope.

```
Rabbit Holes:

1. [Rabbit hole]: [How it should be handled — solve it with X, or explicitly exclude it]
2. [Rabbit hole]: [How it should be handled]
3. [Rabbit hole]: [How it should be handled]
```

**The test:** Could any of these, if not addressed, consume the team's entire budget? If yes, either solve it in the pitch or explicitly mark it as out of scope.

---

## Step 5: Define No-Gos

Use `AskUserQuestion` to get explicit about scope boundaries:

**Question:** "What are you explicitly NOT building in this version? What would be reasonable for someone to expect, but you're deliberately excluding?"

No-gos prevent scope creep during the building period. They're a gift to the team: explicit permission not to build things that would seem obvious but aren't part of this bet.

Examples:
- "No CSV import, only export"
- "No bulk edit of invoice details — only status changes"
- "No mobile support in this version"
- "No API endpoint, only the UI"
- "No email notification when export completes"

```
No-Gos:
- [Thing that won't be built and why]
- [Thing that won't be built and why]
- [Thing that won't be built and why]
```

---

## Step 6: Assemble the Complete Pitch

Now pull everything together into a self-contained pitch document. Confirm with the user:

**Question:** "Let me assemble the pitch. Would you like to review it together before it goes to the betting table, or should I produce the final draft now?"

Produce the pitch:

```markdown
# [Pitch Title]

## Problem

[2–3 sentences describing who experiences this, what goes wrong, what the consequence is]

**Evidence:** [How you know this is real]
**Frequency:** [How often, how many users]

## Appetite

[Small batch: 1–2 weeks] / [Big batch: 6 weeks]

[One sentence explaining why this problem is worth that investment]

## Solution

[Describe the solution at fat marker / breadboard level]

[Include fat marker sketch or breadboard notation]

Key elements:
- [Element 1]
- [Element 2]
- [Flow description]

## Rabbit Holes

- **[Risk 1]:** [How it should be handled or explicitly excluded]
- **[Risk 2]:** [How it should be handled or explicitly excluded]

## No-Gos

- [Explicitly excluded capability 1]
- [Explicitly excluded capability 2]
- [Explicitly excluded capability 3]
```

---

## Step 7: Evaluate Pitch Readiness

Before calling the pitch ready, check it against these criteria:

| Criterion | Check | Red Flag |
|-----------|-------|----------|
| Self-contained | Can someone evaluate this without a presentation? | Requires explanation to make sense |
| Problem-first | Is the problem defined before the solution? | Solution mentioned before problem |
| Appetite set | Is the appetite stated as a business decision? | Missing or stated as an estimate |
| Right abstraction | Fat marker / breadboard level? | Too vague or too detailed |
| Rabbit holes named | Are the obvious traps addressed? | Unknown unknowns lurking |
| No-gos explicit | Is out-of-scope work named? | Ambiguous scope boundaries |
| Fits appetite | Could a team realistically build this in the appetite? | Scope doesn't fit the time |

Use `AskUserQuestion` for anything that fails the check:

**Question:** "The [failing criterion] needs more work before this goes to the betting table. [Specific question to address the gap]."

---

## Common Failures in Shaping

1. **Falling in love with the first solution** before adequately defining the problem
2. **Shaping in one sitting** without sleeping on the problem — best shapes come from iteration
3. **Skipping the no-gos** and leaving the team to guess what's in or out of scope
4. **Rabbit holes treated as the team's problem** — if you can see them, address them
5. **Pitch that can't stand alone** — if it needs you in the room to make sense, reshape it

## What Comes Next

A finished pitch goes to the betting table — [run-betting-table.md](run-betting-table.md). If the pitch gets bet, the team starts the building period. Track their progress with [track-progress.md](track-progress.md).
