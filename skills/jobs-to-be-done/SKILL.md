---
name: jobs-to-be-done
description: Applies Bob Moesta's demand-side thinking and Jobs-to-be-Done framework to help product teams understand why customers switch, hire, and fire products. Use when conducting switch interviews, drawing forces diagrams, writing job statements, mapping demand timelines, understanding the struggling moment, analyzing why customers hire or fire your product, exploring passive or active looking behavior, researching JTBD, or when user mentions Bob Moesta, demand-side thinking, big hire, little hire, push/pull/anxiety/habit, or the four forces of progress.
---

# Jobs-to-be-Done

I help product teams understand demand from the customer's point of view — why they switch, what they're hiring a product to do, and what forces drive or block that decision. This is not about demographics or psychographics. It is about the causal mechanisms behind a purchase.

The Jobs-to-be-Done framework, as developed by Bob Moesta, starts with a deceptively simple question: when a customer switched to your product, what was happening in their life that made them say "today is the day"? The struggling moment. Everything else flows from that.

## Essential Principles

### Jobs Are About Progress, Not Tasks

A job is not a task someone performs. It is the progress a person is trying to make in a specific circumstance. When someone hires a milkshake for a morning commute, the job is not "consume calories" — it is "make this commute manageable and give me something to do with my hand." Understanding the job means understanding the life circumstances that created the need.

### Demand-Side Thinking

Most product teams think supply-side: they start with a product and ask how to make it better or sell it to more people. Demand-side thinking starts with the customer and asks: what forces are acting on this person that caused them to make a switch? Supply-side thinking asks "what features do customers want?" Demand-side thinking asks "what was happening in their life when they decided to change?"

### The Struggling Moment Is the Starting Point

Customers don't wake up wanting your product. They wake up with a problem they've been tolerating until something tips the balance. That tipping point — the struggling moment — is when the push of current frustration outweighs the combined drag of anxiety about change and the inertia of habit. Find the struggling moment and you find the causal mechanism of demand.

### Products Are Hired and Fired

Customers don't "use" or "choose" products — they hire them for a job and fire them when the job isn't done well enough. This metaphor matters because it shifts your thinking from feature comparison to progress comparison. What progress was the customer trying to make? Did your product make that progress possible? When did they fire the last solution and hire yours?

### Big Hire vs. Little Hire

The big hire is the moment of purchase — the customer brings the product home. The little hire happens every time they use it. A product can survive the big hire and fail at the little hire. Understanding both is essential: what caused the purchase decision, and what keeps them coming back (or drives them away)?

### Four Forces Drive Every Switch

Every switching decision is shaped by four forces operating simultaneously:
- **Push:** frustration with the current situation driving the customer away
- **Pull:** the attraction of a new solution pulling the customer toward it
- **Anxiety:** fear of making the wrong choice holding the customer back
- **Habit:** the comfort of the familiar keeping the customer where they are

Push and Pull create demand. Anxiety and Habit suppress it. A switch happens when Push + Pull > Anxiety + Habit.

## Intake

Use the `AskUserQuestion` tool to determine what the user needs:

**Question:** "What are you trying to understand about your customers?"

**Options:**
1. **Conduct a switch interview** — Walk through why a customer switched to (or away from) your product, from first thought to post-purchase
2. **Analyze the four forces** — Map Push, Pull, Anxiety, and Habit for a customer segment or decision context
3. **Write a job statement** — Capture the job in a complete, testable format with functional, emotional, and social dimensions
4. **Map a demand timeline** — Plot the customer's decision journey from first thought to satisfaction or disappointment

## Routing

| Response | Workflow |
|----------|----------|
| 1, "interview", "switch", "why they switched", "churned", "purchased", "first thought", "timeline" | [workflows/switch-interview.md](workflows/switch-interview.md) |
| 2, "forces", "push", "pull", "anxiety", "habit", "four forces", "forces diagram", "why they didn't switch" | [workflows/analyze-forces.md](workflows/analyze-forces.md) |
| 3, "job statement", "write a job", "when I", "so I can", "functional", "emotional", "social job" | [workflows/write-job-statement.md](workflows/write-job-statement.md) |
| 4, "timeline", "demand timeline", "decision journey", "energy", "win/loss", "passive looking", "active looking" | [workflows/map-demand-timeline.md](workflows/map-demand-timeline.md) |
| other | Clarify intent, then route appropriately |

**After identifying intent, read the matching workflow and follow it exactly.**

## Framework Selection

Different JTBD activities call for different reference material:

| Activity | Primary References | Key Frameworks |
|----------|-------------------|----------------|
| Switch interviews, understanding causation | [interview-techniques.md](references/interview-techniques.md), [core-concepts.md](references/core-concepts.md) | Timeline interview, struggling moment, passive/active looking |
| Forces analysis, diagnosing demand | [forces-framework.md](references/forces-framework.md), [core-concepts.md](references/core-concepts.md) | Four forces of progress, force dominance patterns |
| Job statement writing, segmentation | [core-concepts.md](references/core-concepts.md), [interview-techniques.md](references/interview-techniques.md) | Functional/emotional/social dimensions, situation-based segmentation |
| Demand timeline mapping, win/loss analysis | [interview-techniques.md](references/interview-techniques.md), [forces-framework.md](references/forces-framework.md) | Passive looking, active looking, deciding moment, big/little hire |

For any JTBD activity, read the relevant reference files before proceeding.

## References

**Core Knowledge:**
- [core-concepts.md](references/core-concepts.md) — Jobs, progress, hiring/firing, big/little hire, functional/emotional/social dimensions
- [interview-techniques.md](references/interview-techniques.md) — Timeline interviewing, energy mapping, synthesis techniques
- [forces-framework.md](references/forces-framework.md) — Deep dive on Push, Pull, Anxiety, Habit, and their interactions

**Quality and Voice:**
- [anti-patterns.md](references/anti-patterns.md) — 17 anti-patterns organized by activity phase

## Workflows

| Workflow | Purpose |
|----------|---------|
| [switch-interview.md](workflows/switch-interview.md) | Conduct a timeline interview tracing the full customer switch from first thought to post-purchase |
| [analyze-forces.md](workflows/analyze-forces.md) | Map and analyze the four forces of progress for a switching decision |
| [write-job-statement.md](workflows/write-job-statement.md) | Write complete, validated job statements with all three dimensions |
| [map-demand-timeline.md](workflows/map-demand-timeline.md) | Plot the customer demand timeline and identify key decision points |
