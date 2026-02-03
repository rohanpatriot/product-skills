# Frameworks

Eight frameworks for structured discovery thinking. Each framework is a visual or conceptual tool that makes a specific aspect of discovery rigorous and shared.

---

## Table of Contents

- [Opportunity Solution Tree](#opportunity-solution-tree)
- [Product Trio](#product-trio)
- [Experience Map](#experience-map)
- [Interview Snapshot](#interview-snapshot)
- [Assumption Mapping](#assumption-mapping)
- [Story Mapping](#story-mapping)
- [Outcome Types Hierarchy](#outcome-types-hierarchy)
- [Compare-and-Contrast Decision Making](#compare-and-contrast-decision-making)

---

## Opportunity Solution Tree

**Insight:** Teams need a shared visual that connects outcomes to the opportunity space to the solutions being considered. Without this map, decisions fragment and teams lose sight of why they're building what they're building.

**Structure:**

```
          [Desired Outcome]
               |
    -------------------------
    |           |           |
[Opportunity] [Opportunity] [Opportunity]
    |                         |
  -----                    -----
  |   |                    |   |
[Sol] [Sol]              [Sol] [Sol]
  |                        |
[Assumption Tests]       [Assumption Tests]
```

- **Top:** A single desired outcome (the metric the team is trying to move)
- **Second level:** Opportunities — customer needs, pain points, and desires discovered through research
- **Third level:** Solutions — ideas the team generates to address each opportunity
- **Bottom:** Assumption tests — experiments to validate the riskiest assumptions in each solution

**Application Steps:**
1. Start with your desired outcome at the top
2. Through continuous interviewing, populate the opportunity space (second level)
3. Structure opportunities as a tree — parent opportunities break into child opportunities
4. For your target opportunity, generate multiple solutions
5. For your top solutions, map and test assumptions

**When to Use:** Throughout the entire discovery process. The Opportunity Solution Tree is the central artifact — start it early and evolve it weekly.

**Common Misapplication:** Treating the tree as a static deliverable instead of a living artifact. The tree should change every week as you learn. If your tree looks the same as last month, you're not doing discovery.

---

## Product Trio

**Insight:** Product decisions require three perspectives — business viability (product manager), usability (designer), and feasibility (engineer). When any perspective is missing, the team makes incomplete decisions.

**Structure:**

| Role | Brings | Without Them |
|------|--------|-------------|
| Product Manager | Business viability, customer context, outcome focus | Solutions lack business case, don't connect to strategy |
| Designer | Usability, customer empathy, experience thinking | Solutions are functional but unusable, miss emotional needs |
| Software Engineer | Feasibility, technical constraints, implementation insight | Solutions are desirable but unbuildable, miss technical opportunities |

**Application Steps:**
1. Identify your product trio — one PM, one designer, one engineer (minimum)
2. All three participate in customer interviews together
3. All three synthesize interview insights together
4. All three ideate solutions together
5. All three evaluate and select solutions together

**When to Use:** Every discovery activity. The trio is not an occasional collaboration — it's the default operating mode.

**Common Misapplication:** Having the PM do interviews alone and "share findings" with the team. Secondhand insights lose nuance. The trio must have direct customer contact.

---

## Experience Map

**Insight:** Before you can identify opportunities, you need to understand the customer's current experience. An experience map captures the end-to-end journey a customer takes to accomplish their goal, revealing where needs, pain points, and desires live.

**Structure:**

```
[Step 1] → [Step 2] → [Step 3] → [Step 4] → [Step 5]
   |           |           |           |           |
 Needs      Pain pts    Needs      Pain pts    Desires
```

A visual map of the steps a customer takes, annotated with what they need, where they struggle, and what they wish for at each step.

**Application Steps:**
1. Define the scope — what is the customer trying to accomplish?
2. Map the major steps in their current experience (not your product flow — their actual journey)
3. For each step, capture needs (what they're trying to do), pain points (what's hard or broken), and desires (what they wish were better)
4. Populate from interview data, not assumptions
5. Use the map to identify where the biggest opportunities live

**When to Use:** Early in discovery to frame the opportunity space. Update as you learn more through interviews.

**Common Misapplication:** Mapping your product's user flow instead of the customer's actual experience. The experience map should capture the full context of how the customer accomplishes their goal — including steps that happen outside your product.

---

## Interview Snapshot

**Insight:** Teams conduct interviews but fail to synthesize and share insights in a usable way. Interview snapshots are one-page visual summaries that capture the essential insights from each interview in a consistent, shareable format.

**Structure:**

```
Interview Snapshot: [Customer Name/ID]    Date: [Date]

Quick Facts: [context about this customer]

Opportunities Identified:
- [Opportunity 1: need, pain point, or desire]
- [Opportunity 2]
- [Opportunity 3]

Key Quotes:
- "[Direct quote illustrating an opportunity]"
- "[Direct quote]"

Experience Insights:
[What we learned about their experience]

Surprises:
[What we didn't expect]
```

**Application Steps:**
1. Complete the interview
2. Immediately after, the trio fills out the snapshot together (within 1 hour)
3. Focus on opportunities — what needs, pain points, and desires did this customer reveal?
4. Capture direct quotes that illustrate opportunities
5. Note surprises — things that challenged your assumptions
6. Add new opportunities to the Opportunity Solution Tree

**When to Use:** After every customer interview. The snapshot is the bridge between interview and Opportunity Solution Tree.

**Common Misapplication:** Writing long narrative summaries instead of structured snapshots. Length doesn't equal insight. The snapshot format forces you to extract what matters.

---

## Assumption Mapping

**Insight:** Every solution rests on assumptions. Before building, identify those assumptions, assess their risk, and test the riskiest ones first. Assumption mapping makes hidden assumptions visible and prioritizable.

**Structure:**

```
                    More Evidence
                         |
    Known True     |     |     | Known to Need Testing
    (skip)         |     |     | (test these)
                   |     |     |
    ───────────────┼─────┼─────┼───────────────
    Less Important |     |     | More Important
                   |     |     |
    Unknown but    |     |     | Leap-of-Faith
    Unimportant    |     |     | Assumptions
    (skip)         |     |     | (TEST FIRST)
                         |
                    Less Evidence
```

A 2x2 matrix: importance (how critical is this assumption to the solution working?) vs. evidence (how much do we know about whether it's true?).

**Application Steps:**
1. List all assumptions underlying your solution (use the five assumption categories: desirability, viability, feasibility, usability, ethical)
2. Place each assumption on the map based on importance and current evidence
3. Identify leap-of-faith assumptions — high importance, low evidence (bottom-right quadrant)
4. Test leap-of-faith assumptions first
5. Update the map as you gather evidence

**When to Use:** After selecting solutions to pursue, before building. Also useful for evaluating competing solutions — the one with fewer or less risky leap-of-faith assumptions may be safer.

**Common Misapplication:** Skipping the mapping and testing the easiest assumptions instead of the riskiest ones. The goal is to retire risk, not to generate evidence for the assumptions you're already confident about.

---

## Story Mapping

**Insight:** A solution needs structure before you can identify its assumptions and plan delivery. Story mapping breaks a solution into a backbone of activities, the steps within each activity, and variations that represent scope choices.

**Structure:**

```
[Activity 1]     [Activity 2]     [Activity 3]
     |                |                |
  Step 1.1         Step 2.1         Step 3.1    ← Walking skeleton
  Step 1.2         Step 2.2         Step 3.2    ← Next slice
  Step 1.3         Step 2.3                     ← Future scope
```

- **Top row (backbone):** High-level activities the user performs
- **Below each activity:** Steps in order of necessity — the top step is the minimum, lower steps add richness
- **Horizontal slices:** The walking skeleton (top row of steps) is the minimum viable version

**Application Steps:**
1. Identify the backbone — what are the major activities in this solution?
2. Under each activity, list the steps the user would take
3. Order steps vertically by necessity — most essential at top
4. Draw a horizontal line across the minimum viable set of steps (the walking skeleton)
5. Use the story map to identify assumptions at each step

**When to Use:** After selecting a solution, before assumption testing and before building. Story mapping is the bridge between "we picked this solution" and "here's what we need to test and build."

**Common Misapplication:** Story mapping the entire product instead of a single solution to a specific opportunity. Keep the scope tight — one solution at a time.

---

## Outcome Types Hierarchy

**Insight:** Not all outcomes are equal. There's a hierarchy from company mission down to individual team outcomes, and each level serves a different purpose. Teams need to understand where their outcome fits so they can negotiate effectively with leadership.

**Structure:**

```
Mission / Vision
    |
Company-Level Outcomes (business outcomes)
    |
Product-Level Outcomes (product outcomes)
    |
Team-Level Outcomes (traction metrics)
```

- **Mission/Vision:** Why the company exists. Doesn't change frequently.
- **Company-Level Outcomes:** Business metrics the company is trying to move (revenue, market share, profitability). Owned by leadership.
- **Product-Level Outcomes:** Product behaviors that drive business outcomes (activation rate, retention, engagement). Owned by product leadership.
- **Team-Level Outcomes:** Specific metrics a single team can influence. Owned by the product trio.

**Application Steps:**
1. Understand the company-level outcome your product supports
2. Identify product-level outcomes that drive the company outcome
3. Negotiate a team-level outcome that you can directly influence
4. Ensure the causal chain is plausible — your team outcome should plausibly drive the product outcome, which should plausibly drive the business outcome

**When to Use:** At the start of a discovery cycle, when negotiating outcomes with leadership, and when connecting daily work to business strategy.

**Common Misapplication:** Accepting a business outcome (like revenue) as your team outcome. Business outcomes are too broad for a single team to influence directly. You need a product or traction metric that you can actually move.

---

## Compare-and-Contrast Decision Making

**Insight:** Humans make better decisions when comparing options side by side than when evaluating a single option in isolation. This is well-established in cognitive science — comparison activates more critical thinking and reveals trade-offs that single-option evaluation misses.

**Structure:**

| Criteria | Solution A | Solution B | Solution C |
|----------|-----------|-----------|-----------|
| Addresses opportunity? | | | |
| Feasibility | | | |
| Usability risk | | | |
| Business viability | | | |
| Assumption risk | | | |
| Time to test | | | |

**Application Steps:**
1. Generate at least three solutions for your target opportunity (never evaluate just one)
2. Define the criteria that matter — always include how well each addresses the target opportunity
3. Evaluate all solutions against the same criteria simultaneously
4. Discuss trade-offs as a trio
5. Select based on the comparison — which solution best addresses the opportunity with acceptable risk?

**When to Use:** Whenever choosing between solutions, prioritizing opportunities, or selecting assumption tests. The compare-and-contrast pattern applies to any decision with multiple options.

**Common Misapplication:** Generating three solutions but then immediately gravitating to the first one. The comparison must be genuine — give each option fair consideration. If you've already decided before comparing, you're performing the ritual without the benefit.
