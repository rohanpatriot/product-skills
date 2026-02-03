# Set Outcomes Workflow

I'll guide you through defining, negotiating, and committing to a product outcome that connects team work to business results.

## When to Use

- Starting a new discovery cycle or quarter
- Leadership has assigned a business goal and the team needs to translate it into a product outcome
- The team lacks clarity on what success looks like
- The team's current outcome is too broad, too narrow, or misaligned

## Prerequisites

Read [core-thesis.md](../references/core-thesis.md) for the outcomes-over-outputs argument and [frameworks.md](../references/frameworks.md) for the Outcome Types Hierarchy before proceeding.

## The Process

### Step 1: Identify the Business Outcome

Use `AskUserQuestion` to understand the starting context:

**Question:** "What is the business result your team is being asked to support?"

**Follow-ups:**
- What metric does leadership care about most right now?
- Is this a growth goal (acquire more), retention goal (keep more), or monetization goal (earn more)?
- Is there an explicit target, or is the direction "improve"?

Document the business outcome clearly: "[Business metric] from [current state] to [target state] by [timeframe]."

### Step 2: Map the Causal Chain

I'll walk you through decomposing the business outcome into product-level and team-level outcomes:

1. **Business outcome** → What product behaviors drive this business result?
   - Example: Revenue → depends on conversion rate, average order value, purchase frequency, retention
2. **Product outcome** → Which of these can your product directly influence?
   - Example: Your team's product directly affects conversion rate through the onboarding experience
3. **Team outcome** → What specific metric can your trio move?
   - Example: Activation rate (users who complete key action within first 7 days)

Draw the causal chain:

```
Business Outcome: [Revenue growth]
    ↑ driven by
Product Outcome: [Conversion rate improvement]
    ↑ driven by
Team Outcome: [Activation rate — % of new users completing key action in 7 days]
```

Verify: Is the causal chain plausible? Can the team articulate how their work moves up the chain?

### Step 3: Evaluate the Team Outcome

Check the candidate team outcome against these criteria:

| Criterion | Question | Red Flag |
|-----------|----------|----------|
| Influenceable | Can this trio directly move this metric through their work? | Metric depends on other teams or external factors |
| Measurable | Can you measure this today, or can you set up measurement? | No existing data, no way to instrument |
| Connected | Does improving this plausibly improve the product outcome? | Causal chain requires too many assumptions |
| Scoped | Is this narrow enough for one trio to own? | Multiple teams would need to coordinate |
| Stable | Can you commit to this for a quarter? | Likely to be deprioritized next month |

If any criterion fails, iterate on the team outcome. Use `AskUserQuestion` to explore alternatives with the user.

### Step 4: Set Learning Goals Alongside Performance Goals

For the team outcome, define both:

**Performance goal:** "Improve [metric] from [baseline] to [target] by [date]."

**Learning goals:**
- "Understand the top reasons customers don't [desired behavior]"
- "Identify the three biggest opportunities in the [relevant experience]"
- "Discover what distinguishes customers who [succeed] from those who don't"

Learning goals ensure the team builds understanding, not just hits numbers. They are especially important when the team is entering unfamiliar territory.

### Step 5: Prepare to Negotiate With Leadership

If the team needs to negotiate the outcome with leadership, prepare:

1. **What leadership proposed** — the original request (often a feature or business metric)
2. **What you're proposing** — the team outcome with causal chain
3. **Why it's better** — autonomy for the team, accountability for results, faster learning
4. **What you need** — clarity on the business outcome, time commitment, measurement support
5. **What you're committing to** — regular check-ins showing progress on both learning and performance goals

**Negotiation frame:** "We'd like to own [team outcome] because it directly drives [business outcome]. This gives us the autonomy to discover the best way to move the metric, while giving you clear accountability for results."

### Step 6: Document and Commit

Produce a clear outcome statement:

```
## Our Discovery Outcome

**Business context:** [What the company is trying to achieve]

**Team outcome:** [Specific metric we own]
- Baseline: [Current value]
- Target: [Target value]
- Timeframe: [Duration]

**Learning goals:**
1. [Learning goal 1]
2. [Learning goal 2]
3. [Learning goal 3]

**Causal chain:**
Team outcome → Product outcome → Business outcome
[Specific metric] → [Product behavior] → [Business result]

**Check-in cadence:** [How often we'll share progress with leadership]
```

## What Comes Next

With a clear outcome defined, the team moves to [map-opportunities.md](map-opportunities.md) — interviewing customers, building the experience map, and populating the Opportunity Solution Tree.

## Common Failure Modes

1. **Accepting the first outcome suggested** without evaluating alternatives or checking the causal chain
2. **Skipping learning goals** and only setting performance targets — leads to metric gaming
3. **Not negotiating** — accepting whatever leadership hands down, even if it's an output goal
4. **Outcome too broad** — "increase engagement" is not actionable for one trio
5. **No baseline** — can't measure progress without knowing where you start
