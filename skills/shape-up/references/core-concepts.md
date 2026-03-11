# Core Concepts

The foundational ideas behind Shape Up. These aren't abstract principles — they are the practical mechanics that make the methodology work. Understanding them is prerequisite to shaping effective pitches and running clean cycles.

---

## Appetite

**The maximum time worth spending on a problem.** Not an estimate of how long it will take. A bet on how much it's worth.

Appetite comes in two sizes:
- **Small batch:** 1–2 weeks. Fits easily within a 6-week cycle alongside other small batches. Use for well-understood improvements, bug fixes with clear scope, or low-risk additions.
- **Big batch:** 6 weeks. Takes the whole cycle. Use for significant new capabilities, complex integrations, or problems requiring genuine exploration.

The critical distinction: **appetite is set before shaping begins, not after.** It's a constraint that drives shaping decisions. When you shape a 6-week pitch, you're committing to a solution that fits 6 weeks — not asking how long a given solution would take.

**Appetite vs. estimate:**
| Appetite | Estimate |
|----------|----------|
| Set before shaping | Given after scoping |
| Defines the constraint | Describes the work |
| Fixed (adjustable by reshaping) | Always drifts upward |
| Business decision | Technical prediction |

If you find yourself estimating, stop. Set an appetite instead. If the problem isn't worth 6 weeks, it's a small batch. If you can't solve it in 6 weeks, you need to narrow the problem.

---

## Fixed Time, Variable Scope

The principle that makes Shape Up work. Most product development gets this backwards: scope is fixed (we agreed to build X), time is variable (it'll be done when it's done). That's why everything is always late.

Shape Up fixes the time and lets scope vary. The 6-week cycle doesn't extend. At the end, the team ships what they built. If the work isn't done, it doesn't ship — and the team doesn't spend the next cycle finishing it. The unfinished work goes back to the betting table as a potential new pitch.

This creates the right pressure. Teams cut nice-to-haves. They find the simplest version that delivers the core value. They stop when the work is good enough, not when it's perfect.

**Scope adjusts, deadline doesn't:**
- The team discovers a feature is more complex than expected → they cut a nice-to-have to compensate
- The team finds a simpler implementation → they ship it without filling the remaining time
- The team runs out of time → they ship what works, not what was originally imagined

---

## Shaped vs. Unshaped Work

**Shaped work** has four properties:
1. **Roughness:** The solution is sketched at the right level — not pixel-perfect wireframes, not vague descriptions. Rough enough that the team has real creative latitude, specific enough that they know what they're building.
2. **Solved:** The major unknowns are resolved. The shaper has done enough thinking that the team won't encounter a dead end that makes the work impossible.
3. **Bounded:** It has a clear appetite. The team knows how much time it's worth.
4. **No rabbit holes:** The obvious rabbit holes — tangents that could consume the entire budget — are explicitly identified and cut.

**Unshaped work** is everything else: raw ideas, customer requests, feature lists, vague requirements. It goes in the raw ideas pool, not to the betting table.

Shipping unshaped work to teams is the most common Shape Up failure. The team takes on work they can't scope, hit unexpected complexity, and the cycle runs over.

---

## The Shaping Spectrum

Shaping isn't one activity — it spans a spectrum from fully abstract to fully concrete:

```
Abstract                                                  Concrete
|---------|---------|---------|---------|---------|---------|
  Words     Problem   Rough     Fat        Bread-    Wire-
  only      defined   elements  marker     board     frames
                               sketch
```

Good pitches land in the **fat marker sketch / breadboard zone** — concrete enough to show what's being built, abstract enough that the team owns the design decisions.

**Too abstract:** "Make the invoicing experience better" — team doesn't know what to build.
**Too concrete:** Full Figma mockups — team has no creative latitude, and the design will be wrong anyway.
**Goldilocks:** "Add a quick invoice resend option from the invoice detail page — a single button that generates a copy and triggers the send flow. Skip the edit flow for this version."

---

## Fat Marker Sketches

**Low-fidelity visual sketches that show the rough solution without pretending to be real design.** They communicate placement, relationships, and flow — not spacing, color, or typography.

Why fat marker? Because it forces the right level of abstraction. You literally can't draw details with a fat marker. The sketch shows what components exist and how they relate, not how they look.

What fat marker sketches show:
- Which elements appear on a screen
- How they relate to each other spatially
- Where the main interactions happen
- How the user moves from one state to another

What they don't show:
- Exact sizing and spacing
- Typography and color
- Edge cases and empty states
- Final visual design

Fat marker sketches belong in pitches. They communicate the solution without locking down design decisions that should belong to the team.

---

## Breadboards

**Text-based wireframes for interaction flows.** Where fat marker sketches show space, breadboards show flow. They use a simple notation:

```
Places (screens or pages):
  → Invoice Detail
  → Resend Confirmation Modal
  → Success Toast

Affordances (interactive elements):
  Invoice Detail
    [Resend Invoice] button
    → opens Resend Confirmation Modal

  Resend Confirmation Modal
    "Resend invoice to client@example.com?"
    [Cancel] → dismisses
    [Send] → triggers email, shows Success Toast
```

Use breadboards when the pitch involves a flow — navigation, multi-step interactions, or anything that involves moving between states. Use fat marker sketches when the pitch involves a new UI surface. Use both when the pitch has both.

---

## Hill Charts

**A visual metaphor for how work progresses through a cycle.** Every scope of work follows the same arc: you start not knowing how to solve it (uphill), you figure it out (top of the hill), and then you execute the known solution (downhill).

```
                    ●
                  /   \
                /       \
              /           \
            /               \
          /                   \
─────────────────────────────────────
  Figuring out                 Executing
  (problem space)              (solution space)
```

**Uphill:** Problem space. The team is figuring out the approach. Work is uncertain. Movement is slow and non-linear. Risk is highest here.

**Top of the hill:** The team knows what they're doing. The approach is clear. The remaining work is execution.

**Downhill:** Solution space. The team is executing a known plan. Work is predictable. Progress is steady and linear.

**How to use it:**
- Every scope (not the entire project) gets its own position on the hill chart
- The team updates scope positions periodically — not daily, but often enough to spot problems
- Scopes stuck on the uphill side need attention — either help, or a cutting decision
- Multiple scopes clustered at the top or downhill means the work will ship

**Red flags:**
- A scope stuck in the same uphill position for multiple updates → problem, intervene
- New scopes appearing late in the cycle → scope creep, apply the scope hammer
- Scopes jumping from uphill to shipped → the team probably isn't tracking honestly

---

## Scopes

**The meaningful chunks of work that a team tracks on a hill chart.** Scopes are not tasks. They're not user stories. They're the integrated pieces of the problem that have to work together to deliver value.

Good scopes have names that reflect what they accomplish from the user's perspective:
- "Resend flow" not "Add button and modal"
- "Invoice history" not "Database query and UI component"
- "Notification delivery" not "Email integration"

Scopes emerge from the team's understanding of the work during the building period. They're not assigned by management or defined in the pitch in advance. The pitch defines the problem. The team figures out how to scope the solution.

**Scope signals:**
- Too many scopes (>10 for a 6-week project): work is over-granularized, team is task-managing
- Too few scopes (1-2): work isn't decomposed enough, hard to track real progress
- Scopes that don't move: either stuck or not being tracked honestly

---

## The Cycle

Shape Up runs on a **6-week building period followed by a 2-week cool-down.** This is the fundamental rhythm.

**Building period (6 weeks):**
- Teams work on bet pitches with full autonomy
- No interruptions from management
- Circuit breaker is active: if work isn't done at 6 weeks, it doesn't ship

**Cool-down (2 weeks):**
- No scheduled work — teams fix bugs, explore ideas, do tech debt
- Shapers work on next cycle's pitches
- Betting table happens at the end of cool-down, before the next cycle begins
- Teams rest and recharge before the next 6-week push

**Why 6 weeks?**
- Long enough to build something meaningful
- Short enough to feel urgent
- Short enough that a bad bet doesn't sink the whole year

**Why cool-down?**
- Prevents technical debt accumulation
- Gives shapers uninterrupted time to do the next round of shaping
- Prevents the team from burning out on 52 consecutive weeks of sprints

---

## The Betting Table

**The moment where leaders decide what to build next.** It happens during cool-down, before the next building period begins. The participants are senior leaders — not product managers presenting a roadmap, not teams advocating for their work.

At the betting table:
- Every shaped pitch gets a bet or no-bet decision
- No-bet pitches don't go to a backlog — they expire
- Bet pitches get assigned to a team
- The entire cycle is decided in a single session

**The betting metaphor is intentional.** You're placing real bets with real consequences. If the bet doesn't pay off, the team doesn't get more time to finish — the work stops. This creates accountability for the quality of shaping.

**Who attends:** CEO, CTO, senior product and engineering leaders. Small group. Fast decisions.

---

## The Circuit Breaker

**The rule that makes fixed time real.** At the end of a 6-week cycle, if the work isn't done, it doesn't automatically continue. The team doesn't get more time. The pitch goes back to the shaping pool.

This sounds harsh. It's actually liberating. The circuit breaker creates real urgency. It prevents the pathological pattern where every project takes "a little more time" until the budget bloats. It forces teams to scope hammer as the cycle progresses, shipping what matters instead of building what was imagined.

**When the circuit breaker trips:**
- The team ships what they completed — or ships nothing
- The unfinished work is evaluated fresh at the next betting table
- The pitch is reshaped if there's still appetite for the problem
- The bet may not happen again — the problem may no longer be worth the investment

The circuit breaker only works if leaders enforce it. If leaders always extend cycles, teams learn that deadlines are soft, and the urgency disappears.

---

## Raw Ideas

**Everything that isn't a shaped pitch.** Customer requests, internal ideas, bugs, product intuitions — they all go in the raw ideas pool. Not a backlog. Not a prioritized list. Not a Jira board.

The raw ideas pool is intentionally unstructured. Most ideas don't get shaped. Most don't get bet on. The right ideas find their moment when the appetite, problem, and solution align.

What happens to raw ideas:
- They might get shaped by a senior person during cool-down
- They might inspire a pitch that looks quite different
- They might wait years for the right moment
- Most of them simply fade

This is not a bug. It's the system working correctly. A backlog of 500 items is a maintenance burden and a false promise. An unstructured pool of raw ideas is honest about what they are.
