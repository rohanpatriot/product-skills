# Test Assumptions Workflow

I'll guide you through identifying, prioritizing, and testing the riskiest assumptions underlying your selected solution before committing to build.

## When to Use

- After selecting a solution (from [ideate-solutions.md](ideate-solutions.md))
- When a solution looks promising but the team hasn't validated its core assumptions
- When the team is about to commit engineering resources and wants to reduce risk first
- When a previously tested assumption needs re-evaluation

## Prerequisites

Read [frameworks.md](../references/frameworks.md) for Assumption Mapping. Read [techniques.md](../references/techniques.md) for Assumption Generation and One-Question Survey Testing. Read [anti-patterns.md](../references/anti-patterns.md) for Assumption and Testing anti-patterns.

## The Process

### Step 1: Generate Assumptions

I'll walk you through the story map of the selected solution step by step. At each step, ask: "What has to be true for this to work?"

Use the five assumption categories as prompts:

**1. Desirability Assumptions** — Will customers want this?
- Will the target customers care about this?
- Will they switch from their current approach?
- Is this a big enough improvement to change behavior?

**2. Viability Assumptions** — Does this work for the business?
- Can we afford to offer this?
- Does this align with our business model?
- Will this generate or protect revenue?

**3. Feasibility Assumptions** — Can we build this?
- Do we have the technical capability?
- Can we build this within a reasonable timeframe?
- Are there third-party dependencies we need?

**4. Usability Assumptions** — Can customers figure this out?
- Will customers understand how to use this?
- Can they complete the key tasks without assistance?
- Is the learning curve acceptable?

**5. Ethical Assumptions** — Should we build this?
- Are there unintended consequences?
- Does this respect customer privacy?
- Could this harm any customer segment?

Use `AskUserQuestion` to walk through each category:

**Question:** "Let's identify assumptions for your selected solution. Starting with desirability — what has to be true about customer demand for this to work?"

Repeat for each category. Write each assumption as a testable statement:
- "We assume that [specific claim about the world]."

### Step 2: Map Assumptions by Risk

Place each assumption on the assumption map:

```
                    More Evidence (we know this is likely true)
                         |
    SAFE             |   |   | KNOWN — NEEDS TESTING
    (skip these)     |   |   | (test when convenient)
                     |   |   |
    ─────────────────┼───┼───┼─────────────────
    Less Important   |   |   | More Important
    (to solution)    |   |   | (to solution)
                     |   |   |
    LOW PRIORITY     |   |   | LEAP-OF-FAITH
    (skip these)     |   |   | (TEST THESE FIRST)
                         |
                    Less Evidence (we don't know)
```

For each assumption, assess:
- **Importance:** If this assumption is false, does the solution fail? (High = solution depends on it)
- **Evidence:** How confident are we that this is true? (Low = we're guessing)

**Leap-of-faith assumptions** are high importance + low evidence. These are the assumptions that would kill the solution if wrong and that you don't yet have evidence for.

### Step 3: Prioritize Leap-of-Faith Assumptions

List the leap-of-faith assumptions in order of risk (most dangerous first):

```
## Leap-of-Faith Assumptions (Test First)

1. [Assumption] — Importance: Critical / Evidence: None
2. [Assumption] — Importance: Critical / Evidence: Weak
3. [Assumption] — Importance: High / Evidence: None

## Known — Needs Testing (Test When Convenient)

4. [Assumption] — Importance: High / Evidence: Moderate
5. [Assumption] — Importance: Moderate / Evidence: Weak
```

Use `AskUserQuestion`:

**Question:** "Here are the riskiest assumptions. Which one, if false, would most completely kill this solution?"

Start testing from the top. If assumption #1 is false, there's no point testing assumptions #2-5.

### Step 4: Design Assumption Tests

For each leap-of-faith assumption, design the smallest possible test:

**Test Design Template:**

```
Assumption: [Statement]

Test Type: [Prototype test / Fake door / One-question survey /
           Concierge test / Wizard of Oz / Data analysis /
           Technical spike / Customer interview]

Method:
- [What specifically will you do?]
- [Who will you test with? How many?]
- [How long will this take?]

Success Criteria (set BEFORE running):
- We'll consider this VALIDATED if: [specific measurable result]
- We'll consider this INVALIDATED if: [specific measurable result]

Evaluation Method:
- [How will you measure the result?]
```

**Test Type Selection Guide:**

| Assumption Type | Preferred Test Methods |
|-----------------|----------------------|
| Desirability | Fake door test, one-question survey, prototype test |
| Viability | Financial modeling, pricing page test, concierge test |
| Feasibility | Technical spike, proof of concept |
| Usability | Prototype test, five-second test, task completion test |
| Ethical | Customer interview, expert review |

**Key principle:** Favor simulated environments over built environments. Ask "Can I test this without writing code?" before designing a test that requires engineering.

### Step 5: Run Tests

Execute the tests, following these rules:

1. **One assumption per test** — don't combine. Ambiguous results are useless.
2. **Set criteria before seeing results** — prevents confirmation bias.
3. **Use real customers** — internal feedback doesn't count for desirability or usability assumptions.
4. **Time-box** — tests should take days, not weeks. If a test takes longer than a week, simplify it.
5. **Document everything** — record the test, results, and interpretation.

### Step 6: Interpret Results and Decide

For each completed test:

```
## Test Results: [Assumption]

**Result:** [What happened]

**Criteria check:**
- Success criteria: [Met / Not met]
- Failure criteria: [Met / Not met]

**Interpretation:**
- [ ] VALIDATED — Evidence supports the assumption. Move to next assumption.
- [ ] INVALIDATED — Evidence contradicts the assumption. Pivot needed.
- [ ] INCONCLUSIVE — Test didn't produce clear signal. Redesign and retest.

**Next action:** [What the team will do based on this result]
```

**Decision rules:**
- **Validated:** Move to the next leap-of-faith assumption. Continue testing down the priority list.
- **Invalidated:** Stop testing this solution. Return to your runner-up solutions from ideation, or revisit the opportunity. Don't rationalize — the fix is to learn, not to defend.
- **Inconclusive:** Redesign the test. Check: Was the sample too small? Was the question unclear? Was the success criterion too vague?

Use `AskUserQuestion` to discuss results with the user and determine next steps.

### Step 7: Iterate or Advance

After testing the top 2-3 leap-of-faith assumptions:

**If key assumptions are validated:**
- Update the Opportunity Solution Tree (move the solution forward)
- Move remaining assumptions to the delivery backlog (test during build)
- Begin delivery planning with the story map as the foundation

**If a key assumption is invalidated:**
- Return to the runner-up solutions from ideation
- Check if the invalidated assumption applies to runner-ups too
- If all solutions are invalidated, revisit the target opportunity or return to the Opportunity Solution Tree

**If results are mixed:**
- Test from a different angle (triangulate)
- Consider whether a modified version of the solution could work
- Discuss with the trio — is there enough signal to proceed with caution?

## Output

By the end of this workflow, the team should have:

- A complete assumption inventory organized by category
- An assumption map showing risk distribution
- Test designs for leap-of-faith assumptions
- Test results with clear interpretations
- A decision: advance to delivery, pivot to another solution, or revisit the opportunity

## What Comes Next

- If assumptions are validated: Move to delivery. Use the story map to plan sprints.
- If assumptions are invalidated: Return to [ideate-solutions.md](ideate-solutions.md) with runner-up solutions or revisit [map-opportunities.md](map-opportunities.md).
- Regardless: Continue [map-opportunities.md](map-opportunities.md) interviews to keep the Opportunity Solution Tree fresh for the next cycle.

## Common Failure Modes

1. **Skipping assumption identification** and jumping to "let's just build it"
2. **Testing easy assumptions first** instead of the riskiest ones
3. **No success criteria before testing** — leads to confirmation bias
4. **Building to test** when simulated tests would work
5. **Ignoring negative results** and rationalizing away failed tests
6. **Testing the whole idea** instead of individual assumptions
7. **One-and-done testing** — important assumptions deserve converging evidence
