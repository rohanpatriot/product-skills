# Ideate Solutions Workflow

I'll guide you through generating, comparing, and selecting solutions for a target opportunity using individual-first ideation and compare-and-contrast evaluation.

## When to Use

- After selecting a target opportunity (from [map-opportunities.md](map-opportunities.md))
- When the team needs to generate solution ideas for a specific customer opportunity
- When the team is stuck on a single solution and needs to explore alternatives

## Prerequisites

Read [frameworks.md](../references/frameworks.md) for Story Mapping and Compare-and-Contrast Decision Making. Read [techniques.md](../references/techniques.md) for Individual-First Ideation, Dot Voting, and Story Mapping a Solution. Read [anti-patterns.md](../references/anti-patterns.md) for Ideation anti-patterns.

## The Process

### Step 1: Restate the Target Opportunity

Before ideating, make sure everyone is aligned on what they're solving:

Use `AskUserQuestion`:

**Question:** "What is the target opportunity you're generating solutions for?"

Restate it in the standard format: "[Customer segment] needs/struggles with/desires [specific thing]."

**Verify:**
- Is this framed as a customer opportunity, not a solution?
- Is it specific enough to generate solutions for?
- Does it connect to the team's desired outcome?

If the opportunity is too broad, decompose it into child opportunities and pick one.

### Step 2: Individual Ideation — Round 1

I'll walk you through individual ideation:

1. Set a timer for 5-10 minutes
2. Each trio member silently generates as many solutions as possible
3. Write each idea on a separate sticky note, card, or document entry
4. Ideas should be brief descriptions or sketches — not polished proposals
5. No discussion, no sharing, no peeking at others' ideas

**Prompt for ideation:** "How might we address [target opportunity] in a way that moves [desired outcome]?"

**If the team is stuck, offer constraints:**
- "What if you had to solve this without writing any code?"
- "What if you had unlimited engineering resources?"
- "What if you could only change one thing about the current experience?"
- "How would a competitor solve this?"
- "What's the simplest possible solution?"

### Step 3: Share — Round Robin

1. Each person shares one idea at a time, rotating around the trio
2. Brief explanation only — 30 seconds per idea
3. No evaluation yet — "Yes, and" not "Yes, but"
4. Continue rotating until all ideas are shared
5. Group obviously similar ideas together

### Step 4: Build and Extend

Now that all ideas are visible:

1. Identify ideas that could be combined or enhanced
2. Ask: "Does anyone see connections between ideas?"
3. Create hybrid ideas that merge the best elements
4. Add any new ideas sparked by the group discussion

### Step 5: Individual Ideation — Round 2

The first round primes new thinking. Run a second round:

1. Set a timer for 5 minutes
2. Each person generates new ideas silently — the first round should have sparked fresh thinking
3. Share round-robin again
4. Add to the collection

The team should now have 10-20+ distinct solution ideas.

### Step 6: Select Top Three — Dot Voting

1. Display all solution ideas visibly
2. Each trio member gets 3 votes
3. Vote silently — place dots on your top choices
4. Count votes
5. Select the top three

**If there are ties:** Discuss briefly and break ties as a group. Favor diversity — if two tied solutions are very similar, keep one and include the next most different option.

**If one idea dominates:** That's fine, but ensure the other two are genuinely different approaches, not minor variations.

### Step 7: Story Map Each Solution

For each of the three selected solutions:

1. **Identify the backbone:** What are the 3-5 major activities?
2. **List steps under each activity:** What does the user do?
3. **Order by necessity:** Most essential at top
4. **Draw the walking skeleton:** Minimum viable version

```
Solution [A/B/C]: [Name]

[Activity 1]     [Activity 2]     [Activity 3]
     |                |                |
  Step 1.1         Step 2.1         Step 3.1    ← Walking skeleton
  Step 1.2         Step 2.2         Step 3.2    ← Next slice
  Step 1.3         Step 2.3                     ← Future scope
```

Story mapping all three makes the compare-and-contrast evaluation concrete and rigorous.

### Step 8: Compare and Select

Compare the three solutions side by side:

| Criteria | Solution A | Solution B | Solution C |
|----------|-----------|-----------|-----------|
| How well does it address the opportunity? | | | |
| Desirability — will customers want this? | | | |
| Feasibility — can we build this? | | | |
| Usability — can customers use this? | | | |
| Viability — does this work for the business? | | | |
| Assumption risk — how many unknowns? | | | |
| Speed to test — how fast can we learn? | | | |

Use `AskUserQuestion` to walk through the comparison with the user:

**Question:** "Looking at the three solutions side by side, which best addresses the opportunity with acceptable risk?"

**Follow-ups:**
- Which solution has the fewest critical unknowns?
- Which could you test fastest?
- Which excites the trio most? (Enthusiasm matters for execution)

### Step 9: Decide and Document

Document the selection:

```
## Solution Selection

**Target Opportunity:** [Statement]

### Selected Solution: [Name]
[Brief description]

**Why selected:** [Key reasons from comparison]

### Runner-Up Solutions:
- [Solution B name] — [Why not selected / when to revisit]
- [Solution C name] — [Why not selected / when to revisit]

### Story Map of Selected Solution:
[Include the story map from Step 7]

### Next Step: Assumption Testing
[Move to test-assumptions.md]
```

Keep runner-up solutions documented. If the selected solution fails assumption testing, you already have alternatives ready.

## Output

By the end of this workflow, the team should have:

- 10-20+ solution ideas generated through individual-first ideation
- Three solutions story-mapped in detail
- A compare-and-contrast evaluation of all three
- One selected solution with documented rationale
- Runner-up solutions preserved for potential pivot

## What Comes Next

With a selected solution, move to [test-assumptions.md](test-assumptions.md) to identify, prioritize, and test the riskiest assumptions before building.

## Common Failure Modes

1. **Skipping individual ideation** and jumping to group brainstorming — produces anchored, narrow ideas
2. **Evaluating just one solution** — no comparison, no trade-off analysis
3. **Falling in love** with the first idea and going through the motions on the others
4. **Solutions that don't address the opportunity** — always check: does this solve the customer's need?
5. **Skipping story mapping** — solutions remain vague, making assumption identification impossible
6. **Choosing the easiest solution** instead of the one that best addresses the opportunity
