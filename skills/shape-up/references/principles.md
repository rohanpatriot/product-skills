# Principles

The governing beliefs behind Shape Up. These aren't rules to follow — they're the underlying logic that explains why the methodology is designed the way it is. When you understand the principles, you can make good decisions in situations the methodology doesn't explicitly cover.

---

## Bets, Not Backlogs

Backlogs are a lie. They imply that we'll eventually get to everything. We won't. The backlog grows faster than we ship. Items age past relevance. Teams spend time maintaining a list they'll never complete.

The betting table is honest. At the start of every cycle, you choose what to build from a pool of shaped pitches. What doesn't get bet on doesn't get scheduled. It might get shaped and bet next cycle. It might never get built. That's fine.

**The bet framing changes behavior:**
- Shapers do better work when they know a pitch that isn't compelling won't get chosen
- Leaders make deliberate decisions rather than working through a queue
- Teams get fresh starts rather than inherited technical debt of stale priorities

When someone asks "why didn't we build X?", the honest answer is: "We didn't think it was the best bet for that cycle." Not: "It's in the backlog." Not: "We'll get to it."

---

## Appetite, Not Estimates

Estimates are predictions about how long work will take. They're almost always wrong, and the wrongness compounds: complex work is systematically underestimated, estimates become commitments, commitments slip, and the team spends cycles in recovery.

Appetite is a declaration of how much a problem is worth solving. It comes from business judgment, not technical analysis. "This problem is worth two weeks of our team's time" is a business decision. "This will take two weeks to build" is a technical prediction.

**Setting appetite before shaping is the discipline:**
- Forces you to constrain the solution, not expand it
- Prevents scope creep from infecting the shaping process
- Creates clarity about trade-offs before the team sees the work
- Aligns business and engineering on what "done" means

When appetite and complexity don't align, you have three choices: narrow the problem, narrow the solution, or don't bet it this cycle. You don't extend the appetite retroactively.

---

## Senior People Shape, Teams Build

Shaping requires a particular combination of skills: business judgment, technical fluency, and product taste. It requires knowing what problems are worth solving, understanding what's technically feasible, and sensing what a good solution looks like.

This combination is rare. In most organizations, the people who have it are senior leaders who've built and shipped many things. The methodology channels them into shaping work during cool-down, not into managing the team during the building period.

**Why this works:**
- Senior people's time is best spent on the highest-leverage work: choosing the right problems and sketching the right solutions
- Teams who own implementation decisions make faster, better decisions than teams executing someone else's detailed spec
- Shaping is faster than managing: a shaped pitch takes 1-2 days to produce; managing a mis-specified project can consume the entire cycle

**What this doesn't mean:**
- Senior people don't disappear during the building period — they're available to help unblock serious problems
- Teams don't have unlimited latitude — the pitch defines the problem and appetite
- Only senior people can have product judgment — it means that judgment should be baked into pitches before the team sees them

---

## Building Periods and Cool-Down

The 6-week cycle isn't a sprint that repeats endlessly. It's separated from the next cycle by a mandatory 2-week cool-down. This isn't a luxury — it's structural.

**Cool-down is when:**
- Shapers do the shaping work for the next cycle without interruption
- Teams recover from the intensity of the building period
- Technical debt that accumulated during the cycle gets addressed
- Bugs and small maintenance items get handled
- Individual exploration happens

**Building period is when:**
- Teams execute with full autonomy and no interruptions
- No new work gets added mid-cycle
- The circuit breaker is active
- Management stays out of implementation decisions

**Why the separation matters:** If cool-down doesn't exist, shaping never happens. Shapers get pulled into helping teams finish cycle work. Pitches never get developed. The next betting table has nothing to bet on. The cycle collapses into an endless sprint.

---

## The Circuit Breaker Enforces Honesty

The 6-week cycle ends whether or not the work is done. This rule has teeth — when it's enforced. When it's not enforced, the entire methodology degrades.

Without the circuit breaker:
- Teams learn that deadlines are soft and urgency is performative
- Shapers get less rigorous about defining appetite because overruns get tolerated
- Cycles blur together into continuous semi-finished work
- The betting table becomes less meaningful because bets never really expire

With the circuit breaker:
- Teams apply the scope hammer naturally during the building period
- Unfinished work gets honest assessment at the next betting table
- Shapers feel real accountability for the quality of their pitches

**The circuit breaker doesn't mean perfection.** Teams can ship at the end of 6 weeks with rough edges, missing features, or next-cycle follow-up work defined. It means shipping something real, not extending the timeline because the original spec wasn't complete.

---

## Teams Have Full Autonomy During the Cycle

Once a bet is placed and a team is assigned, management steps back. The team:
- Scopes the work themselves (management doesn't assign tasks)
- Makes design decisions within the pitch parameters
- Decides what to cut when facing time pressure
- Reports status through the hill chart, not status meetings

This is not abdication — it's trust combined with accountability. The team is accountable for shipping within appetite. The autonomy is what makes that accountability meaningful. If management micro-manages the execution, the team can't be held responsible for the outcome.

**What this looks like in practice:**
- No daily standups with a manager
- No sprint planning meetings where tasks get assigned
- Hill charts visible to leadership — but read, not micromanaged
- Leadership available to help unblock genuine blockers, not to make implementation decisions

**What this doesn't look like:**
- Teams going silent for 6 weeks with no visibility
- Teams building whatever they want within a general problem area
- Teams ignoring the appetite and building whatever takes as long as it takes

---

## Problems, Not Features

Features are solutions. Problems are opportunities. Shape Up starts with problems.

"Add a bulk export feature" is a feature request. "Finance teams have to download invoices one at a time to reconcile accounts — it takes hours and users tell us they'd switch if we solved it" is a problem. The feature is one possible solution. The problem tells you what success looks like.

**Starting with problems:**
- Opens up more solution space than starting with features
- Enables the team to find better solutions than the one specified
- Aligns the bet with business value rather than feature count
- Helps the betting table assess risk and strategic fit

**The pitch defines the problem clearly before proposing a solution.** The solution sketch answers the problem — it doesn't exist independently of it.

---

## Shaping Is Not Design

Shaping happens before the building period. Design happens during it. The distinction matters.

**Shaping:**
- Done by senior product/engineering leaders
- Produces rough sketches (fat markers, breadboards)
- Identifies the problem and solution approach
- Defines appetite and no-gos
- Removes rabbit holes

**Design:**
- Done by the team during the building period
- Produces real UI, real components, real decisions
- Builds on the approach sketched in the pitch
- Makes the hundreds of small decisions the pitch doesn't cover

When shapers produce finished Figma mockups, they've overstepped into design. The team inherits those decisions without having done the thinking behind them. When requirements change (and they will), nobody knows which decisions are load-bearing and which are arbitrary. The team can't adapt.

Leave design decisions to the team. Give them the problem, the solution concept, and the appetite. Let them figure out the rest.

---

## Scope Hammering Is Required, Not Optional

Every 6-week cycle hits a moment where the team realizes there's more work than time. This moment is inevitable. How the team responds determines whether the cycle succeeds.

**Scope hammering is the active process of cutting:** distinguishing must-haves from nice-to-haves and cutting the nice-to-haves. The scope hammer is not a last resort. It's a tool that gets used throughout the cycle, starting from the first week.

**The alternative to scope hammering is:**
- Asking for a timeline extension (circuit breaker prevents this)
- Shipping a broken or unfinished product (unacceptable)
- Burning the team out to hit an impossible scope (unsustainable)

Teams that don't scope hammer either overrun the cycle or ship low-quality work. Teams that scope hammer naturally ship real, working software that delivers the core value of the pitch.

---

## No Interruptions During the Cycle

Once a building period begins, nothing interrupts it. Not customer complaints. Not executive requests. Not urgent-seeming bugs. The team works the pitch for 6 weeks without scope changes.

**Why this matters:** Context-switching is expensive. A team in the middle of a complex implementation that gets pulled to handle a different problem loses days of productive work, not hours. Repeated interruptions make 6-week cycles effectively impossible.

**How to handle interruptions:**
- Bugs → classify severity; only production outages or data-loss issues interrupt the cycle
- Customer requests → log as raw ideas for potential future shaping
- Executive ideas → log as raw ideas; bring to the next betting table
- Technical blockers → legitimate reason to engage management, not a scope change

**The 6 weeks is inviolable.** If something is truly urgent enough to interrupt a cycle, it probably shouldn't be handled by the team mid-cycle — it should be handled by other means (a dedicated response team, a hotfix process, a separate small-batch bet).

---

## Pitches Must Be Self-Contained

A shaped pitch should be readable by the betting table without a presentation from the shaper. If a pitch requires explanation to make sense, it hasn't been shaped well enough.

**A self-contained pitch includes:**
- The problem: who is struggling with what, and when
- The appetite: how much time this is worth
- The solution sketch: fat marker or breadboard showing the key elements
- Rabbit holes: what the team should not get pulled into
- No-gos: what's explicitly out of scope

**A self-contained pitch does not include:**
- Technical implementation details (that's the team's job)
- Full design specs (that's the team's job)
- Timeline breakdowns (that's what the appetite is for)
- User stories (that's task-management, not shaping)

---

## Cool-Down Is Non-Negotiable

Teams need the 2-week cool-down. It's not a vacation. It's not time for the next cycle's planning. It's structural recovery and maintenance time.

When organizations skip cool-down:
- Technical debt compounds uncontrollably
- Teams burn out
- Shaping never happens — the next betting table has no shaped pitches
- The methodology degrades into sprint planning by another name

Cool-down is what makes 6-week cycles sustainable across multiple years, not just one quarter.

---

## The Unbeatable Pitch vs. The Surviving Pitch

Not all pitches are created equal. A great pitch:
- Describes a real, painful problem that the team has evidence for
- Proposes a solution that's elegant and clearly fits the appetite
- Anticipates rabbit holes and explicitly cuts them
- Makes the bet decision obvious: "of course we should build this"

A mediocre pitch:
- Describes a vague problem ("users want better X")
- Proposes a solution that's ambitious for the appetite
- Leaves obvious unknowns unaddressed
- Requires explanation to seem compelling

The betting table sorts pitches honestly. Strong pitches get bet. Weak pitches wait for reshaping or fade. Shapers who get pitches bet consistently have learned what makes a pitch compelling. Shapers whose pitches consistently don't get bet should examine whether they're solving real problems, setting appropriate appetites, and doing enough customer research to ground the problem definition.
