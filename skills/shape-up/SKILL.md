---
name: shape-up
description: Applies Ryan Singer's Shape Up methodology to help product teams ship meaningful work on a fixed cycle. Use when shaping raw ideas into pitches, setting appetite, running a betting table, tracking progress with hill charts, scope hammering, or when user mentions pitches, cool-down, building period, appetite, breadboards, fat marker sketches, betting table, hill charts, scopes, or cycle planning.
---

# Shape Up

I help product teams ship meaningful work in fixed cycles using Ryan Singer's Shape Up methodology. Shape Up is built on a simple idea: **fixed time, variable scope**. You set an appetite — the maximum time worth spending — and shape a solution that fits. No backlogs. No estimates. Bets placed at the betting table. Teams build autonomously. Progress tracked on hill charts.

## Essential Principles

### Fixed Time, Variable Scope

Estimates grow to fill whatever time you give them. Shape Up inverts the relationship: time is fixed (the appetite), scope is variable. If the work can't fit in the appetite, you cut it — not the deadline.

### Shaping Happens Before Betting

Work doesn't go to a team until it's been shaped. Shaped means: the problem is defined, the solution is sketched at the right level of abstraction, rabbit holes are identified, and the work has a clear appetite. Unshaped work is a risk you haven't priced.

### Bets, Not Backlogs

There is no backlog. At the betting table, you choose what to build next from a pool of shaped pitches. What doesn't get bet on doesn't get scheduled. Nothing accumulates. Nothing lingers. Every cycle is a fresh decision.

### Teams Have Full Autonomy

Once a pitch is bet on, the team owns the work. They scope it, design it, build it, and ship it. Management doesn't assign tasks. There are no daily standups. The hill chart is the signal — not status meetings.

### Appetite, Not Estimates

Never ask "How long will this take?" Ask "How much is this worth?" A small batch is worth 1–2 weeks. A big batch is worth 6 weeks. If the team can't solve the problem in that time, the pitch needs to be reshaped or abandoned.

## Intake

Use the `AskUserQuestion` tool to determine what the user needs:

**Question:** "Where are you in your Shape Up cycle?"

**Options:**
1. **Shape a pitch** — Turn a raw idea into a shaped pitch with appetite, solution sketch, and no-gos
2. **Run a betting table** — Evaluate shaped pitches and decide what to build this cycle
3. **Track cycle progress** — Use hill charts to surface stuck scopes and decide what to cut
4. **Scope hammer** — Work is exceeding appetite; cut to ship what matters

## Routing

| Response | Workflow |
|----------|----------|
| 1, "shape", "pitch", "idea", "appetite", "breadboard", "sketch", "rabbit hole" | [workflows/shape-pitch.md](workflows/shape-pitch.md) |
| 2, "bet", "betting table", "cycle", "planning", "pitch review", "what to build" | [workflows/run-betting-table.md](workflows/run-betting-table.md) |
| 3, "hill chart", "progress", "stuck", "scope", "uphill", "downhill", "tracking" | [workflows/track-progress.md](workflows/track-progress.md) |
| 4, "scope hammer", "cut", "over budget", "too much", "won't finish", "ship" | [workflows/scope-hammer.md](workflows/scope-hammer.md) |
| other | Clarify intent using Shape Up language, then route appropriately |

**After identifying intent, read the matching workflow and follow it exactly.**

> **Note:** If the task involves code — building prototypes, setting up tooling, integrating with project trackers — recommend `EnterPlanMode` before proceeding.

## Framework Selection

| Shape Up Activity | Primary Reference | Key Concepts |
|-------------------|-------------------|--------------|
| Shaping ideas, setting appetite | [core-concepts.md](references/core-concepts.md) | Appetite, shaping spectrum, fat marker sketches, breadboards |
| Betting table decisions | [principles.md](references/principles.md) | Bets not backlogs, circuit breaker, cooling down |
| Progress tracking | [core-concepts.md](references/core-concepts.md) | Hill charts, scopes, uphill vs. downhill work |
| Scope cutting | [anti-patterns.md](references/anti-patterns.md) | Scope hammering, must-haves vs. nice-to-haves |

Read reference files before proceeding with any workflow.

## References

**Core Knowledge:**
- [core-concepts.md](references/core-concepts.md) — Appetite, fixed time/variable scope, hill charts, shaping spectrum, breadboards
- [principles.md](references/principles.md) — Bets not backlogs, appetite not estimates, cycle rhythm, senior people shape
- [anti-patterns.md](references/anti-patterns.md) — 20+ anti-patterns organized by Shape Up phase

## Workflows

| Workflow | Purpose |
|----------|---------|
| [shape-pitch.md](workflows/shape-pitch.md) | Turn raw ideas into shaped pitches with appetite, solution sketch, and no-gos |
| [run-betting-table.md](workflows/run-betting-table.md) | Evaluate shaped pitches and make bet/no-bet decisions for the next cycle |
| [track-progress.md](workflows/track-progress.md) | Map scopes to hill charts, identify stuck work, decide what to cut or push |
| [scope-hammer.md](workflows/scope-hammer.md) | Cut scope aggressively to ship within appetite |
