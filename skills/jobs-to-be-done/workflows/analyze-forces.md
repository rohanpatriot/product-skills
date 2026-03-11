# Analyze Forces Workflow

I'll guide you through mapping and analyzing the four forces of progress — Push, Pull, Anxiety, and Habit — for a specific customer switching decision. This analysis transforms raw interview data into a structural diagnosis of why customers switch (or don't), and what your product needs to do about it.

## When to Use

- After conducting one or more switch interviews and you want to make sense of what drives and blocks switching
- When trying to understand why adoption is slower than expected (Anxiety or Habit dominates)
- When trying to understand why customers who try your product don't convert (little hire failing)
- When diagnosing why churned customers left despite initial purchase (Push resolved but job not done)
- When designing marketing or onboarding to address the dominant force

## Prerequisites

Read [forces-framework.md](../references/forces-framework.md) for the full theoretical grounding of each force. Read [core-concepts.md](../references/core-concepts.md) for the struggling moment and big hire/little hire context. Read [anti-patterns.md](../references/anti-patterns.md) for forces-specific mistakes, especially ignoring anxiety and the emotional job.

---

## Step 1: Establish the Context

Use `AskUserQuestion` to gather the raw material for analysis:

**Question:** "What switching decision are you analyzing? Describe the customer, what they switched from, and what they switched to (or didn't)."

**Follow-ups:**
- Do you have interview data, or are we working from assumptions?
- Is this a switch that happened, or one you're trying to understand why it didn't happen?
- How many customers does this analysis represent?

If working from interview data, gather:
- Timeline summaries from [switch-interview.md](switch-interview.md)
- Key quotes from each stage
- Any patterns across multiple interviews

If working from assumptions, be explicit: label everything as a hypothesis that needs to be tested in interviews.

---

## Step 2: Map the Push Forces

Push is the frustration driving the customer away from their current situation. Push forces don't push toward your product — they push away from the status quo. Without sufficient Push, no switch happens regardless of how good your product is.

**Eliciting Push in Interviews:**

The Push forces are most visible in the First Thought and Passive Looking stages of the timeline. Ask:

- "What wasn't working about [current situation]?"
- "What was frustrating you about how things were?"
- "What were you putting up with that you'd rather not?"
- "When did you first notice that? How long had that been true?"
- "What was the cost of staying as you were?"

**Signs of strong Push in interview data:**
- Customer can describe a specific moment of frustration
- The frustration had been building over time (multiple instances)
- The customer can articulate what was being lost or missed
- Emotional language: "I was so tired of...", "I kept running into...", "It was costing us..."

**Signs of weak Push in interview data:**
- Customer describes switching as "just because" or "thought I'd try something new"
- No specific frustrating events
- The old situation is described neutrally or even positively
- Switch was externally driven (policy, budget, peer pressure)

**Build the Push map:**

```
PUSH FORCES MAP

Primary Push (the core struggle driving them away):
  Description: _______________
  First appeared: _______________
  Accumulated over: _______________
  Intensity: [High / Medium / Low]
  Key customer quote: "_______________"

Secondary Push factors (additional frustrations):
  1. _______________
     Quote: "_______________"
  2. _______________
     Quote: "_______________"
  3. _______________
     Quote: "_______________"

Push Diagnosis:
  Is Push strong enough to drive a switch on its own? [Yes / No / Borderline]
  Notes: _______________
```

---

## Step 3: Map the Pull Forces

Pull is the attraction of the new solution drawing the customer toward making the switch. Pull forces are about the vision of a better future, not just escape from a worse present. Pull builds during the passive looking and active looking phases.

**Eliciting Pull in Interviews:**

- "What did you first hear about [new solution] that caught your attention?"
- "What did you imagine your life or work would look like if you made this switch?"
- "What was the thing about [new solution] that made you think 'that might actually be better'?"
- "When you were in active looking mode, what were you hoping to find?"
- "What did you see in [new solution] that felt like it was made for your situation?"

**Signs of strong Pull in interview data:**
- Customer can describe a specific vision of the better situation
- They had a concrete triggering event (saw a demo, heard a recommendation, read something)
- They used their own time to research and learn (not just passive reception)
- Emotional language: "I thought this could finally solve...", "I got excited about...", "I could see how..."

**Signs of weak Pull in interview data:**
- Customer chose your product because it was the least bad option
- No specific image of the better future — "it seemed fine"
- Pull was entirely supply-side (pushed by a salesperson, not pulled by the customer's own desire)
- Switch driven purely by Push with no vision of the new situation

**Build the Pull map:**

```
PULL FORCES MAP

Primary Pull (the core attraction to the new situation):
  Description: _______________
  When it emerged: _______________
  Intensity: [High / Medium / Low]
  Key customer quote: "_______________"

Secondary Pull factors:
  1. _______________
     Quote: "_______________"
  2. _______________
     Quote: "_______________"

What triggered Pull to become concrete:
  Event/moment: _______________
  Medium: [Word of mouth / Demo / Trial / Marketing / Review / Other]

Pull Diagnosis:
  Did Pull create a clear vision of the better future? [Yes / No / Partial]
  Was Pull strong enough to sustain the switch against Anxiety? [Yes / No / Borderline]
  Notes: _______________
```

---

## Step 4: Map the Anxiety Forces

Anxiety is the fear of making the wrong choice that holds the customer back from switching. Anxiety is not pessimism — it is rational risk assessment. Customers who are anxious have something to lose and they know it. Anxiety is most visible in the passive looking phase (when it keeps them stuck) and the deciding moment (when something finally resolved it).

**Eliciting Anxiety in Interviews:**

- "What were you most worried about when you were thinking about making this switch?"
- "What almost stopped you from going through with it?"
- "What did you imagine could go wrong?"
- "Was there anyone who warned you against doing this? What did they say?"
- "What did you do to try to reduce your risk before committing?"

**Types of Anxiety to listen for:**

- **Performance anxiety:** "What if the new product doesn't actually work?"
- **Switching cost anxiety:** "What about all my data / history / configurations in the old system?"
- **Social anxiety:** "What will my team / boss / peers think?"
- **Learning anxiety:** "What if it's too complicated and I can't figure it out?"
- **Buyer's remorse anxiety:** "What if I pay for this and regret it?"
- **Timing anxiety:** "Is this the right time? What if something better comes out soon?"

**Signs of strong Anxiety in interview data:**
- Long passive looking phase
- Customer consulted many people before deciding
- Customer sought out trials, demos, or proof-of-concept before committing
- Customer described relief or resolution at the deciding moment
- Specific fears articulated with concrete scenarios

**Signs of resolved Anxiety:**
- "When I [saw the trial / talked to X / read the case study], I felt like it was going to be okay"
- "I figured worst case I could [cancel / go back / export my data]"
- Clear moment where the dominant anxiety was addressed

**Build the Anxiety map:**

```
ANXIETY FORCES MAP

Primary Anxiety (the fear that most blocked the switch):
  Description: _______________
  Category: [Performance / Switching cost / Social / Learning / Buyer's remorse / Timing / Other]
  Intensity: [High / Medium / Low]
  Key customer quote: "_______________"

Secondary Anxieties:
  1. _______________
     Category: _______________
     Quote: "_______________"
  2. _______________
     Category: _______________
     Quote: "_______________"

What resolved the dominant anxiety:
  Resolution event: _______________
  What the customer did: _______________
  What your product/company did (or could do): _______________

Anxiety Diagnosis:
  Was Anxiety the primary barrier to switching? [Yes / No / Co-primary with Habit]
  What product or marketing change would most reduce this Anxiety? _______________
  Notes: _______________
```

---

## Step 5: Map the Habit Forces

Habit is the inertia of the familiar — the comfort of staying with the current solution even when it's not ideal. Habit is not stupidity; it is optimization. Customers who stick with the status quo are avoiding the switching cost and the risk of an unknown. Habit forces show up most strongly in the passive looking phase and in why customers waited longer than you'd expect to act on their frustrations.

**Eliciting Habit in Interviews:**

- "Even after you started noticing this wasn't working, what kept you where you were for a while?"
- "What would you have lost if you'd switched earlier?"
- "What was still working fine about the old situation, even if other things weren't?"
- "Was there anything about the old [product/situation] that you'd genuinely miss?"
- "What was the story you told yourself about why it was okay to stay?"

**Types of Habit to listen for:**

- **Workflow habit:** "I've built everything around how this works"
- **Skill habit:** "I know how to use this and I'd have to learn something new"
- **Relationship habit:** "I know the team / account manager / community"
- **Integration habit:** "Everything connects to this; switching would mean rewiring a lot"
- **Identity habit:** "This is just how I do things" (deepest and hardest to dislodge)

**Signs of strong Habit in interview data:**
- Long period between first thought and active looking
- Customer describing things they liked about the old situation
- Customer emphasizing the switching cost in concrete terms
- Slow, gradual transition (phased out vs. hard switch)
- Customer describing relief at not having to change workflows too drastically

**Build the Habit map:**

```
HABIT FORCES MAP

Primary Habit (the inertia most keeping them in place):
  Description: _______________
  Category: [Workflow / Skill / Relationship / Integration / Identity / Other]
  Intensity: [High / Medium / Low]
  Key customer quote: "_______________"

Secondary Habits:
  1. _______________
     Category: _______________
     Quote: "_______________"
  2. _______________
     Category: _______________
     Quote: "_______________"

What eventually overcame the habit:
  _______________

Habit Diagnosis:
  Was Habit the primary barrier to switching? [Yes / No / Co-primary with Anxiety]
  What product or onboarding change would most reduce switching friction? _______________
  Notes: _______________
```

---

## Step 6: Force Quantification

Assess the relative strength of each force to understand the dynamics of the switch.

This is qualitative, not statistical. Rate each force based on interview evidence:

```
FORCE STRENGTH ASSESSMENT

                   SUPPRESSING FORCES
                Anxiety         Habit
               ┌──────────────────────┐
               │  [H/M/L]  [H/M/L]   │
               └──────────────────────┘
                         ↑
                    blocks switch
                         |
Push (H/M/L) ─────────────────────────── Pull (H/M/L)
                         |
                   drives switch
                         ↓
               ┌──────────────────────┐
               │  [H/M/L]  [H/M/L]   │
               └──────────────────────┘
                GENERATING FORCES

Net Switch Pressure = (Push + Pull) - (Anxiety + Habit)
Result: [High pressure / Medium pressure / Low pressure / Net negative]

Dominant Force: [Push / Pull / Anxiety / Habit]
Secondary Force: _______________
```

---

## Step 7: Force Dominance Analysis

The pattern of which forces dominate reveals the strategic diagnosis and the right intervention.

**Pattern: Push-dominant switch**
The customer was pushed out by frustration more than pulled toward the new. Implication: they may be at risk of being pushed away from you next. The job is about escaping frustration, not achieving aspiration. Marketing should validate their frustration, not oversell the dream.

**Pattern: Pull-dominant switch**
The customer was attracted by vision more than driven by current pain. Implication: they have high expectations and may be disappointed if the product doesn't match the vision they had. Onboarding needs to deliver on the aspiration immediately.

**Pattern: Anxiety-blocked (switch almost didn't happen)**
Push and Pull were both present but Anxiety nearly won. Implication: your product has a "last mile" problem. Customers want to switch but your product isn't doing enough to reduce the perceived risk. Focus: trials, case studies, guarantees, migration support.

**Pattern: Habit-blocked (switch was slow)**
The customer spent a long time in passive mode despite active frustration. Implication: there's real switching cost in the old situation (workflow, skill, integration). Focus: migration tools, templates, parallel running, "bring your data" features.

**Pattern: All forces moderate**
No single force stands out. The switch was routine and low-drama. Implication: this customer is not representative of the high-friction switch. Find a customer with more deliberation in their story.

**Build the diagnosis:**

```
FORCE DOMINANCE DIAGNOSIS

Dominant pattern: _______________
Strategic implication: _______________

What this means for product: _______________
What this means for marketing: _______________
What this means for onboarding/sales: _______________

If we could change one force to increase switching, it would be:
  Force: _______________
  Current state: _______________
  Target state: _______________
  How to get there: _______________
```

---

## Step 8: Cross-Interview Force Patterns

If you have data from multiple interviews, look for force patterns that repeat.

Use `AskUserQuestion` to bring in additional interview data:

**Question:** "How many switch interviews do you have? Can you share the forces maps from each?"

Build a cross-interview summary:

```
CROSS-INTERVIEW FORCE SUMMARY

                 Push    Pull    Anxiety    Habit
Interview 1:    [H/M/L] [H/M/L] [H/M/L]   [H/M/L]
Interview 2:    [H/M/L] [H/M/L] [H/M/L]   [H/M/L]
Interview 3:    [H/M/L] [H/M/L] [H/M/L]   [H/M/L]
Interview 4:    [H/M/L] [H/M/L] [H/M/L]   [H/M/L]
Interview 5:    [H/M/L] [H/M/L] [H/M/L]   [H/M/L]

Consistent patterns:
  - _______________
  - _______________

Outliers:
  - _______________

Dominant segment force pattern: _______________
```

---

## Output

By the end of this workflow, you will have:

1. A complete four-forces map with annotated quotes for each force
2. A force strength assessment and dominance diagnosis
3. Strategic implications for product, marketing, and onboarding
4. A cross-interview pattern summary (if multiple interviews)

## What Comes Next

- Use the forces map to sharpen your job statement in [write-job-statement.md](write-job-statement.md)
- Use the forces map to annotate the demand timeline in [map-demand-timeline.md](map-demand-timeline.md)
- Use force dominance to inform product and marketing decisions (see [forces-framework.md](../references/forces-framework.md) for design implications)

## Common Failure Modes

1. **Treating all four forces as equally important** — They're not. One or two usually dominate. The diagnosis is in the dominance, not the presence.
2. **Skipping Anxiety because it feels negative** — Anxiety is the most actionable force for product and onboarding. Don't skip it.
3. **Conflating Push and Pull** — Push is about escaping the old. Pull is about the vision of the new. They're different mechanisms with different product implications.
4. **Rating forces without quotes** — Every force rating should have a supporting verbatim quote. If you can't find one, that force wasn't present in the interview.
5. **Doing this without interview data** — A forces map built from assumptions is a hypothesis, not a diagnosis. Label it as such.
