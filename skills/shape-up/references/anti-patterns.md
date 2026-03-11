# Anti-Patterns

Twenty-two common Shape Up mistakes organized by phase. Each covers: what teams do wrong, why it fails, and how to fix it.

---

## Table of Contents

- [Shaping Anti-Patterns](#shaping-anti-patterns)
- [Appetite Anti-Patterns](#appetite-anti-patterns)
- [Betting Table Anti-Patterns](#betting-table-anti-patterns)
- [Building Period Anti-Patterns](#building-period-anti-patterns)
- [Progress Tracking Anti-Patterns](#progress-tracking-anti-patterns)
- [Scope Anti-Patterns](#scope-anti-patterns)

---

## Shaping Anti-Patterns

### 1. Shipping Unshaped Work

**The mistake:** Taking a raw idea — a customer request, an internal suggestion, a feature list — and betting it without shaping it first.

**Why it fails:** The team takes on work that hasn't had rabbit holes identified, appetite set, or solution sketched. They hit unexpected complexity, the cycle runs over, the circuit breaker trips, and nothing ships. The team is demoralized. The feature doesn't exist. The cycle was wasted.

**The fix:** No pitch goes to the betting table unless it's shaped. Shaped means: problem defined, solution sketched (fat marker or breadboard), appetite set, rabbit holes called out, no-gos listed. If the work isn't shaped, it doesn't get bet.

---

### 2. Over-Specifying the Solution

**The mistake:** Shapers produce detailed wireframes, full Figma mockups, pixel-perfect specifications, or technical implementation plans.

**Why it fails:** Over-specification removes the team's creative latitude. They execute someone else's design decisions without understanding the reasoning behind them. When the spec meets reality (and it will), nobody knows which decisions are load-bearing and which are arbitrary. The team can't adapt. Morale drops because good engineers hate being code monkeys.

**The fix:** Shape at the fat marker level. Show elements and flow, not layout and typography. Trust the team to make design decisions within the problem constraints.

---

### 3. Shaping in a Vacuum

**The mistake:** Shapers work alone, never talking to customers or the engineering team while developing a pitch.

**Why it fails:** The problem definition is based on assumption, not customer evidence. The solution approach ignores technical reality. The pitch lands in the betting table disconnected from both customer need and technical feasibility.

**The fix:** Shapers talk to customers to understand the problem before sketching solutions. Shapers do a quick technical spike or consult an engineer to validate feasibility before committing to an approach. Shaping is informed by both the business and engineering reality.

---

### 4. Defining Solutions Before Problems

**The mistake:** The pitch starts with a solution ("Add a bulk import feature") without first defining the problem that solution solves.

**Why it fails:** The team builds the feature without understanding why it exists. When it ships and doesn't solve the real problem, nobody knows why it failed. The pitch can't be evaluated for strategic fit at the betting table because the strategic fit isn't stated.

**The fix:** Every pitch begins with the problem: who is experiencing it, what they're doing wrong, what the consequence is, and how frequently it occurs. The solution comes after. The test: can you explain why this problem is worth 6 weeks of team time without mentioning the solution? If not, you haven't defined the problem.

---

### 5. Ignoring Rabbit Holes

**The mistake:** The pitch identifies an elegant solution but doesn't call out the obvious edge cases and technical tangents that could consume the entire budget.

**Why it fails:** The team hits a rabbit hole in week 2. They spend three weeks going down it because it seems technically necessary. The original scope never gets built. The cycle ends with an interesting technical exploration and no shipped feature.

**The fix:** When shaping, ask: "What could go wrong? What edge cases could turn into a 2-week detour? What technical assumptions is this solution making?" Call these out explicitly in the pitch as rabbit holes, and state how they should be handled (or explicitly excluded from scope).

---

### 6. Pitches That Require Presentation

**The mistake:** The written pitch doesn't stand on its own — it requires the shaper to present it, explain the context, or answer questions before the betting table can evaluate it.

**Why it fails:** If the shaper isn't in the room, the pitch can't be bet. If the shaper is in the room, they become advocates for their pitch rather than contributors to an honest betting decision. The betting table spends time in Q&A rather than making decisions.

**The fix:** Write pitches so they're self-contained. A person who wasn't involved in shaping should be able to read the pitch, understand the problem, see the proposed solution, know the appetite, and form a bet opinion — without the shaper explaining anything.

---

## Appetite Anti-Patterns

### 7. Treating Appetite as a Deadline

**The mistake:** Setting a 6-week appetite and then treating it as a commitment to deliver the full original scope in 6 weeks.

**Why it fails:** Appetite is a budget, not a deadline. The question "will we finish on time?" is the wrong question. The right question is "what's the most valuable thing we can ship within 6 weeks?" Treating appetite as deadline creates the same dysfunctions as traditional deadline-driven development.

**The fix:** State appetite explicitly as a budget: "We're willing to spend up to 6 weeks on this." The scope is variable within that budget. The team's job is to find the most valuable implementation that fits, not to complete an imagined scope.

---

### 8. Setting Appetite After Scoping

**The mistake:** Letting the team scope the work first, then setting an appetite based on how long the scope takes.

**Why it fails:** This is just estimation by another name. The appetite becomes a prediction rather than a constraint. The team has no incentive to find a simpler solution because the appetite will just match whatever they scope.

**The fix:** Set appetite before the team sees the work. The appetite constrains what gets shaped. If the problem seems worth 6 weeks, shape a 6-week pitch. If the shaped solution would take 10 weeks, narrow the scope or the problem before the pitch goes to the betting table.

---

### 9. Appetites That Never Vary

**The mistake:** Every pitch is a 6-week big batch. Small batches are never used.

**Why it fails:** The organization loses the ability to do small, targeted improvements. A fix that could ship in 2 weeks gets blown out to fill a 6-week slot. The team builds padding and unnecessary features to justify the time. Work expands to fill the available appetite.

**The fix:** Use small batches (1–2 weeks) for well-understood improvements, bug fixes with clear scope, and small new capabilities that don't require exploration. Save big batches for genuinely complex problems.

---

### 10. Extending Appetite Retroactively

**The mistake:** A team runs out of time at the end of a cycle, and management grants them another 2 weeks to finish.

**Why it fails:** This destroys the circuit breaker. Teams learn that appetite is soft. Urgency disappears. Scope expands without constraint. The betting table becomes meaningless because bets never really expire.

**The fix:** Enforce the circuit breaker. If a team runs out of time, they ship what they completed or they ship nothing. The unfinished work goes back to the betting table for honest re-evaluation. The shaper considers whether the problem needs to be reshaped with a tighter scope.

---

## Betting Table Anti-Patterns

### 11. Maintaining a Backlog

**The mistake:** Unbet pitches get placed in a backlog for consideration in future cycles.

**Why it fails:** Backlogs grow faster than teams ship. Pitches in a backlog age and go stale. The problem that inspired the pitch may no longer exist. The solution sketch may no longer be valid. Maintaining a backlog is work that produces no value and creates a false sense of commitment ("we'll get to it").

**The fix:** No backlog. Pitches that don't get bet expire. If the problem is still worth solving in the next cycle, the shaper reshapes it. The fresh shaping incorporates new information. The betting table sees current, relevant pitches — not a queue of inherited intentions.

---

### 12. Running the Betting Table as a Review Meeting

**The mistake:** The betting table becomes a presentation session where shapers defend their pitches to decision-makers.

**Why it fails:** Pitches should be evaluated on their written merits. If they require advocacy to get bet, the shaping wasn't good enough. Turning the betting table into a presentation creates political dynamics — the most persuasive shaper wins, not the best pitch.

**The fix:** Pitches are read before the betting table, not presented at it. The betting table discusses pitches with questions, but shapers don't present. If a pitch isn't compelling without explanation, it needs to be reshaped before the next betting table.

---

### 13. Betting Table with Too Many Participants

**The mistake:** Including the whole company in the betting table to ensure "alignment" and "buy-in."

**Why it fails:** The betting table is a decision meeting, not a consensus-building meeting. More participants means slower decisions, more political dynamics, and the diffusion of accountability. When everyone decides, nobody is accountable.

**The fix:** Keep the betting table small — the CEO, CTO, and at most one or two senior product leaders. These are the people with the authority to make bets and the judgment to evaluate them. Alignment happens through communication about decisions made, not through participation in making them.

---

### 14. Betting What's in Progress, Not What's Ready

**The mistake:** Betting pitches that aren't fully shaped because the alternative is an empty cycle.

**Why it fails:** Unshaped work going to a team creates the same problems as shipping unshaped work: rabbit holes hit mid-cycle, overruns, and demoralized teams. The instinct to "fill the cycle" leads to betting work that isn't ready.

**The fix:** If there aren't enough shaped pitches to fill a cycle, use the extra capacity for a longer cool-down. Let teams do more exploration work. Give shapers more time to develop pitches. Don't bet work that isn't ready.

---

## Building Period Anti-Patterns

### 15. Management Assigning Tasks

**The mistake:** During the building period, managers break down the work into tasks and assign them to individual team members.

**Why it fails:** The team loses autonomy and accountability. They're executing a manager's plan rather than solving a problem. Engineers stop thinking about the problem and start thinking about their task list. Unexpected complexity can't be handled dynamically because the plan is fixed.

**The fix:** Teams scope their own work. The pitch defines the problem. The team figures out what needs to be built, what order to build it in, and who builds what. Management reads the hill chart to monitor progress — they don't assign tasks.

---

### 16. Interrupting the Cycle

**The mistake:** Adding new work mid-cycle because something seems urgent — a customer complaint, an executive idea, a "quick" request.

**Why it fails:** Context switching is expensive. A team mid-implementation that gets pulled to handle something else loses days, not hours. The original work is harder to re-enter. The added work rarely fits in the remaining time. The cycle ends with two half-finished things.

**The fix:** New work waits for the next betting table. Genuine production emergencies go through a separate incident response process, not the Shape Up team. Customer requests go to the raw ideas pool for potential future shaping.

---

### 17. Building in Undefined Sequence

**The mistake:** The team builds features in the order they seem most interesting or technically convenient, rather than in an order that produces shippable work at any point.

**Why it fails:** If the team runs out of time, they have a half-built product that can't ship. The circuit breaker trips and nothing goes out. Users get nothing.

**The fix:** Build integrated slices that work end-to-end before building additional features. This way, at any point in the cycle, there's something real that could ship. The team can scope hammer what remains without sacrificing the core.

---

## Progress Tracking Anti-Patterns

### 18. Updating Hill Charts Dishonestly

**The mistake:** Teams update scope positions based on time elapsed or task completion rather than honest assessment of where they are in the problem/solution arc.

**Why it fails:** The hill chart becomes a performance metric rather than a diagnostic tool. Management reads false confidence. Real blockers stay hidden. Late-stage discovery of real blockers (where the team is actually still uphill) means no time to respond.

**The fix:** Hill chart positions should reflect the team's honest assessment of their understanding. A scope that's been worked on for two weeks might still be uphill if the team hasn't figured out the approach. That's the information leadership needs to see.

---

### 19. Using Hill Charts for Time Tracking

**The mistake:** Using scope positions to track "percent complete" or time spent rather than problem understanding.

**Why it fails:** "60% complete" means nothing if the team is still uphill — figuring out the approach — on the hardest parts. A scope that's 60% through time spent can be 90% of the way to done if most of the hard thinking is resolved. Using hill charts as time tracking defeats the diagnostic purpose.

**The fix:** Hill chart positions answer: "Do we know what we're doing?" Not: "How much time have we spent?" Uphill = still figuring it out. Top = approach is clear, executing is predictable. Downhill = executing a known plan.

---

### 20. Daily Status Meetings

**The mistake:** Running daily standups or status meetings during the building period to stay informed.

**Why it fails:** Daily status meetings are a sign that management doesn't trust the team or the hill chart. They interrupt flow, create reporting overhead, and produce status theater rather than useful information. Teams spend time preparing status rather than building.

**The fix:** The hill chart is the status mechanism. Managers read it. If something looks concerning (a scope stuck uphill for multiple updates), they can have a conversation. Otherwise, the team builds.

---

## Scope Anti-Patterns

### 21. Adding Scope Mid-Cycle

**The mistake:** As the cycle progresses, the team or stakeholders add new requirements that weren't in the original pitch.

**Why it fails:** The appetite was set for the original scope. New scope doesn't come with new time. Every addition is a zero-sum trade-off against what was already planned. Mid-cycle additions almost always push the cycle over.

**The fix:** Additions wait for the next betting table or get traded against existing scope. If something is truly must-have and wasn't in the pitch, the team identifies equivalent scope to cut and confirms with the shaper. More often, additions are nice-to-haves that should simply wait.

---

### 22. Defining Scopes Before the Building Period

**The mistake:** Shapers or managers define the implementation scopes in advance as part of the pitch or project planning.

**Why it fails:** Scopes are implementation artifacts — they reflect how the team has decided to decompose the problem. That decomposition can only happen once the team starts working and understands the technical reality. Pre-defined scopes are almost always wrong and constrain the team's ability to adapt.

**The fix:** The pitch defines the problem and solution approach. The team defines scopes during the first days of the building period. Scopes emerge from understanding; they aren't assigned.
