# Map Demand Timeline Workflow

I'll guide you through building a demand timeline — a visual representation of the customer's journey from first thought to post-purchase satisfaction or disappointment. The demand timeline is your map of when, why, and how customers move toward a switch. It reveals where demand builds, where it stalls, and what your product needs to do at each stage.

## When to Use

- After conducting multiple switch interviews and you want to find cross-customer patterns
- When trying to understand where customers get stuck in the decision process
- When win/loss patterns suggest a problem at a specific stage (e.g., customers consider but don't convert)
- When designing onboarding and want to understand what expectations customers bring at the moment of big hire
- When diagnosing why satisfied customers still leave (little hire failing despite strong big hire)

## Prerequisites

Read [interview-techniques.md](../references/interview-techniques.md) for energy mapping and the timeline structure. Read [core-concepts.md](../references/core-concepts.md) for the passive/active looking framework and big/little hire distinction. Have completed at least 3-5 switch interviews using [switch-interview.md](switch-interview.md).

---

## Step 1: Gather Interview Data

Use `AskUserQuestion` to understand what you're working with:

**Question:** "How many switch interviews do you have? Can you share the timeline summaries or key data from each?"

**Follow-ups:**
- Are these all the same type of switch (e.g., all new customers, all churned customers)?
- Are they from the same segment or different contexts?
- How recent are the switches?

Organize the raw data by timeline stage across all interviews:

```
INTERVIEW DATA INVENTORY

                  Int.1  Int.2  Int.3  Int.4  Int.5
First Thought:   [date] [date] [date] [date] [date]
Passive Phase:   [dur]  [dur]  [dur]  [dur]  [dur]
Active Start:    [date] [date] [date] [date] [date]
Deciding Moment: [date] [date] [date] [date] [date]
Big Hire:        [date] [date] [date] [date] [date]
Little Hire:     [qual] [qual] [qual] [qual] [qual]
```

---

## Step 2: Build the Timeline Structure

The demand timeline has seven stages. For each stage, you'll document:
- What is typically happening for customers
- What forces are active (and at what intensity)
- What the customer's energy level is (how actively they're engaged with the problem)
- Key events or moments that advance or stall the timeline

**Timeline structure:**

```
DEMAND TIMELINE

Stage 1: FIRST THOUGHT
↓
Stage 2: PASSIVE LOOKING
↓
Stage 3: ACTIVE LOOKING
↓
Stage 4: DECIDING MOMENT
↓
Stage 5: BIG HIRE (Purchase)
↓
Stage 6: LITTLE HIRE (First use)
↓
Stage 7: SATISFACTION / DISAPPOINTMENT
```

---

## Step 3: Map Energy Levels

Energy is how much attention and effort the customer is actively directing toward the problem and the potential solution. Energy is not enthusiasm — a customer can be frustrated (high energy) or resigned (low energy). Energy tells you how engaged with the problem they are at each stage.

**Energy scale:**
- **Dormant (1):** Not thinking about it. Status quo feels fine.
- **Background (2):** Occasional awareness that something isn't ideal, but no action.
- **Noticing (3):** Starting to pay attention to relevant information without seeking it.
- **Searching (4):** Actively researching, comparing, evaluating.
- **Deciding (5):** Committed to switching; focused on making the right choice.
- **Using (6):** Evaluating whether the switch was right; highly attentive.
- **Settled (7):** A new status quo has formed. Energy returns to baseline.

**Map energy by stage:**

```
ENERGY CURVE

Stage:      1st    Passive  Active  Deciding  Big    Little  Settled
            Thought Looking  Looking  Moment   Hire   Hire

Int. 1:     [1-7]  [1-7]   [1-7]   [1-7]    [1-7]  [1-7]   [1-7]
Int. 2:     [1-7]  [1-7]   [1-7]   [1-7]    [1-7]  [1-7]   [1-7]
Int. 3:     [1-7]  [1-7]   [1-7]   [1-7]    [1-7]  [1-7]   [1-7]
Int. 4:     [1-7]  [1-7]   [1-7]   [1-7]    [1-7]  [1-7]   [1-7]
Int. 5:     [1-7]  [1-7]   [1-7]   [1-7]    [1-7]  [1-7]   [1-7]

AVERAGE:    [1-7]  [1-7]   [1-7]   [1-7]    [1-7]  [1-7]   [1-7]

Energy narrative (describe the shape of the curve):
_______________
```

**Common energy curve patterns:**

- **Gradual build:** Energy rises slowly from first thought through active looking. Patient, deliberate customers. Decision is considered, not reactive. Often habit-dominant.
- **Spike at event:** Energy jumps sharply at a specific triggering event (incident, recommendation, competitive threat). Push-dominant switches.
- **Plateau and drop:** Energy rises but stalls in active looking without reaching the deciding moment. Anxiety-dominant or pull is insufficient to tip the balance.
- **Crash after big hire:** High energy at purchase but drops sharply if early use disappoints. Little hire failing. Product-market fit problem.
- **Sustained high energy:** Customer remains highly engaged post-purchase, exploring features, expanding use. Strong pull and job alignment.

---

## Step 4: Plot Key Events and Moments

For each timeline stage, identify the recurring events and moments across interviews. These become the design targets — what your product, marketing, and sales motion should be creating or responding to.

**Stage 1: First Thought Events**

What triggers the first crack in the status quo?

```
FIRST THOUGHT EVENTS

Event type                 | Frequency | Energy spike? | Forces
---------------------------|-----------|---------------|-------
[Specific incident]        | x/5 intv  | [Yes/No]      | Push
[Product failure moment]   | x/5 intv  | [Yes/No]      | Push
[External trigger/event]   | x/5 intv  | [Yes/No]      | Push
[Comparison to competitor] | x/5 intv  | [Yes/No]      | Pull
[Conversation/referral]    | x/5 intv  | [Yes/No]      | Pull

Most common first thought trigger: _______________
Average time before first thought became action: _______________
```

**Stage 2: Passive Looking Events**

What information do customers notice and file away without seeking?

```
PASSIVE LOOKING EVENTS

Information type           | Frequency | Energy change | Forces
---------------------------|-----------|---------------|-------
[Word of mouth]            | x/5 intv  | [+/-/flat]    | Pull
[Marketing/advertising]    | x/5 intv  | [+/-/flat]    | Pull/Anxiety
[Peer/colleague use]       | x/5 intv  | [+/-/flat]    | Pull/Habit
[Industry content]         | x/5 intv  | [+/-/flat]    | Pull

Average duration of passive phase: _______________
What most commonly moves customers from passive to active: _______________
```

**Stage 3: Active Looking Events**

What triggers active research, and what do customers do?

```
ACTIVE LOOKING EVENTS

Trigger to active:
  [Event/circumstance]: x/5 intv

Research behavior:
  [Trial/demo]: x/5 intv
  [Reviews/comparison sites]: x/5 intv
  [Peer recommendations]: x/5 intv
  [Sales conversations]: x/5 intv
  [Content/documentation]: x/5 intv

Alternatives evaluated: _______________
Duration of active phase: _______________
Top questions customers are trying to answer: _______________
```

**Stage 4: Deciding Moment Events**

What resolves the dominant anxiety and tips the balance?

```
DECIDING MOMENT EVENTS

What resolved the switch:
  [Trial success]: x/5 intv
  [Specific conversation]: x/5 intv
  [Social proof / case study]: x/5 intv
  [Pricing/risk reduction]: x/5 intv
  [External deadline/event]: x/5 intv

What almost stopped the switch:
  [Fear type]: x/5 intv

Most powerful resolution mechanism: _______________
Average time from active looking to deciding: _______________
```

**Stage 5-7: Big Hire and Little Hire Events**

```
BIG HIRE PATTERNS
  Purchase channel (how they bought): _______________
  Emotional state at purchase: _______________
  Level of commitment (all-in / hedging): _______________

LITTLE HIRE PATTERNS (First Use)
  What customers tried to do first: _______________
  Whether initial use delivered on expectations: _______________
  Common early friction: _______________
  Common early delight: _______________

SATISFACTION/DISAPPOINTMENT PATTERNS
  % highly satisfied at 30 days: _______________
  % mixed/neutral at 30 days: _______________
  % disappointed at 30 days: _______________
  Primary driver of disappointment: _______________
  Primary driver of satisfaction: _______________
```

---

## Step 5: Identify Win and Loss Moments

Win moments are points in the timeline where your product, marketing, or sales motion successfully advances the customer. Loss moments are where customers stall, drop out, or develop doubts.

Use `AskUserQuestion` to pressure-test your analysis:

**Question:** "Looking at this timeline, where do you see the most drop-off or hesitation across these customers? What seems to cause it?"

**Build the win/loss map:**

```
WIN/LOSS MOMENT MAP

Stage            | Win Condition               | Loss Condition
-----------------|-----------------------------|--------------------------
First Thought    | [What amplifies push]       | [What doesn't register]
Passive Looking  | [What we do to get noticed] | [What keeps us invisible]
Active Looking   | [What drives trial/demo]    | [What triggers exit]
Deciding Moment  | [What resolves anxiety]     | [What kills the deal]
Big Hire         | [Strong conviction]         | [Buyer's remorse trigger]
Little Hire      | [Job done on first use]     | [Expectation mismatch]
Settled          | [Habit formed, job done]    | [Silent churn building]

Critical win moment (most impactful positive):
  Stage: _______________
  What happens: _______________
  What we can do to create/reinforce it: _______________

Critical loss moment (most impactful negative):
  Stage: _______________
  What happens: _______________
  What we can do to prevent or recover from it: _______________
```

---

## Step 6: Identify Patterns Across Customers

With data from multiple interviews, look for structural patterns that indicate where to invest.

```
CROSS-CUSTOMER PATTERNS

Pattern: Where timeline stalls most often
  Stage: _______________
  Frequency: x/5 customers
  Root cause (force analysis): _______________
  Intervention opportunity: _______________

Pattern: Fastest-moving customers (first thought to big hire)
  What's different about them: _______________
  What we can learn from them: _______________
  Can we help slower customers move like this? _______________

Pattern: Highest-satisfaction customers at 30 days
  What's different about their little hire: _______________
  What job were they hired for vs. disappointed customers: _______________
  Onboarding implication: _______________

Pattern: Silent churners (leave without escalating)
  When does energy drop: _______________
  Was the job not done, or the wrong job: _______________
  Early warning signals: _______________
```

---

## Step 7: Build the Annotated Demand Timeline

Assemble everything into a single annotated timeline document:

```
DEMAND TIMELINE — [Product/Segment Name]
Based on [N] switch interviews | Compiled [date]

═══════════════════════════════════════════════════════════
STAGE 1: FIRST THOUGHT
═══════════════════════════════════════════════════════════
What's happening: _______________
Typical trigger: _______________
Average energy level: [1-7]
Dominant force: Push [H/M/L], Pull [H/M/L], Anxiety [H/M/L], Habit [H/M/L]
Duration before next stage: _______________
Representative quote: "_______________"
Win condition for us: _______________
Design/marketing opportunity: _______________

═══════════════════════════════════════════════════════════
STAGE 2: PASSIVE LOOKING
═══════════════════════════════════════════════════════════
What's happening: _______________
What customers notice: _______________
Average energy level: [1-7]
Dominant force: Push [H/M/L], Pull [H/M/L], Anxiety [H/M/L], Habit [H/M/L]
Duration: _______________
Representative quote: "_______________"
Win condition for us: _______________
Design/marketing opportunity: _______________

═══════════════════════════════════════════════════════════
STAGE 3: ACTIVE LOOKING
═══════════════════════════════════════════════════════════
What's happening: _______________
What triggers active search: _______________
What customers evaluate: _______________
Top anxieties being resolved: _______________
Average energy level: [1-7]
Duration: _______________
Representative quote: "_______________"
Win condition for us: _______________
Design/sales opportunity: _______________

═══════════════════════════════════════════════════════════
STAGE 4: DECIDING MOMENT
═══════════════════════════════════════════════════════════
What's happening: _______________
What resolves the dominant anxiety: _______________
What almost stops the switch: _______________
Average energy level: [1-7]
Representative quote: "_______________"
Win condition for us: _______________
Product/sales opportunity: _______________

═══════════════════════════════════════════════════════════
STAGE 5: BIG HIRE
═══════════════════════════════════════════════════════════
What's happening: _______________
Emotional state: _______________
Level of commitment: _______________
Average energy level: [1-7]
Representative quote: "_______________"
Onboarding entry condition: _______________

═══════════════════════════════════════════════════════════
STAGE 6: LITTLE HIRE (First Use)
═══════════════════════════════════════════════════════════
What customers try to do first: _______________
Whether the job gets done: _______________
Common friction: _______________
Common delight: _______________
Average energy level: [1-7]
Representative quote: "_______________"
Product/onboarding opportunity: _______________

═══════════════════════════════════════════════════════════
STAGE 7: SATISFACTION / DISAPPOINTMENT
═══════════════════════════════════════════════════════════
30-day satisfaction breakdown: _______________
Primary satisfaction driver: _______________
Primary disappointment driver: _______________
Whether job is being done: _______________
New jobs that emerged: _______________
Representative quote: "_______________"
Retention/expansion opportunity: _______________
```

---

## Step 8: Identify Priority Interventions

Use `AskUserQuestion` to discuss the implications with the user:

**Question:** "Looking at the timeline, what's the highest-leverage place to intervene? Where are you losing customers you should be keeping, or failing to advance customers who are ready to switch?"

**Priority intervention framework:**

```
PRIORITY INTERVENTIONS

Intervention 1:
  Stage: _______________
  Problem: _______________
  Proposed change: _______________
  Expected impact: _______________
  Who owns it: [Product / Marketing / Sales / Onboarding]

Intervention 2:
  Stage: _______________
  Problem: _______________
  Proposed change: _______________
  Expected impact: _______________
  Who owns it: _______________

Intervention 3:
  Stage: _______________
  Problem: _______________
  Proposed change: _______________
  Expected impact: _______________
  Who owns it: _______________
```

---

## Output

By the end of this workflow, you will have:

1. A complete seven-stage demand timeline with energy curve
2. Win/loss moment map across the full timeline
3. Cross-customer pattern analysis
4. An annotated timeline document with stage-by-stage design opportunities
5. Priority intervention list

## What Comes Next

- Use the timeline to inform onboarding design: customers arrive at the big hire with specific expectations; design first use to deliver on those
- Use the timeline to inform marketing: meet customers at the stage they're in, not the stage you wish they were
- Use the active looking stage data to refine positioning and trial experience
- Share the timeline with sales to align messaging with where buyers actually are
- Update the timeline quarterly as you conduct new interviews — demand dynamics shift

## Common Failure Modes

1. **Treating the timeline as linear when it isn't** — Customers loop back, pause, and skip stages. The timeline is a framework, not a conveyor belt.
2. **Building the timeline from one customer** — One story is a hypothesis. You need at least 5 to see patterns.
3. **Ignoring the little hire** — Products fail at the little hire more often than the big hire. Don't stop at purchase.
4. **Conflating satisfaction with job completion** — Customers can be satisfied with a product that doesn't do the job (because they've lowered expectations) and dissatisfied with a product that does the job (because they expected more). Ask about job completion, not just satisfaction.
5. **Building the timeline and not acting on it** — The timeline is an analytical tool. Its value comes from the interventions it reveals.
