# Product Skills

Claude Code skills for product management and discovery. Four structured frameworks — built from the source texts — that give Claude the vocabulary, workflows, and judgment to think through product problems the way the best practitioners do.

Install them once. Use them in any project.

## Installation

```bash
npx skills add rohanpatriot/product-skills
```

## Available Skills

| Skill | Author / Framework | What It Does |
|-------|--------------------|--------------|
| `continuous-discovery` | Teresa Torres | Runs the full continuous discovery loop: outcomes, customer interviews, opportunity mapping, ideation, and assumption testing |
| `jobs-to-be-done` | Bob Moesta | Conducts switch interviews, draws forces diagrams, writes job statements, and maps demand timelines to understand why customers switch |
| `shape-up` | Ryan Singer / Basecamp | Shapes raw ideas into pitches, sets appetite, runs betting tables, and tracks progress with hill charts |
| `story-mapping` | Jeff Patton | Builds user story maps, slices releases, facilitates discovery sessions, and escapes the flat-backlog trap |

## Skill Details

### Continuous Discovery

Applies Teresa Torres's continuous discovery habits to help product teams build the practice of weekly customer touchpoints, driven by outcomes rather than outputs.

**Workflows:**
- **Set Outcomes** — Define, negotiate, and commit to a product outcome tied to business results
- **Map Opportunities** — Interview customers, create interview snapshots, and build an Opportunity Solution Tree
- **Ideate Solutions** — Generate, compare, and select solutions using individual-first ideation
- **Test Assumptions** — Identify leap-of-faith assumptions and design small, fast experiments

**References included:**
- Core thesis and prerequisite mindsets
- 8 discovery frameworks with application guidance
- 12 guiding principles
- 11 step-by-step techniques
- 28 anti-patterns organized by phase
- Terminology precision guide

**Trigger phrases:** Opportunity Solution Trees, product trios, assumption testing, continuous interviewing, product outcomes, experience maps, interview snapshots.

---

### Jobs-to-be-Done

Applies Bob Moesta's demand-side thinking to uncover why customers switch, what forces drive or block the decision, and what job a product is actually hired to do.

**Workflows:**
- **Switch Interview** — Conduct a structured interview to reconstruct the full demand timeline and identify the struggling moment
- **Analyze Forces** — Map push, pull, anxiety, and habit forces acting on a customer's decision
- **Map Demand Timeline** — Reconstruct the customer's journey from first thought to purchase to outcome
- **Write Job Statement** — Craft a precise job statement that captures progress, circumstance, and motivation

**References included:**
- Core concepts and demand-side thinking principles
- Forces framework (push, pull, anxiety, habit)
- Interview techniques and question sequences
- Anti-patterns that lead to supply-side misdiagnosis

**Trigger phrases:** switch interviews, forces diagram, struggling moment, big hire, little hire, demand-side, push/pull/anxiety/habit, Bob Moesta.

---

### Shape Up

Applies Ryan Singer's Shape Up methodology so teams can move from raw idea to shaped pitch to shipped work — on a fixed cycle, with no backlog accumulating behind them.

**Workflows:**
- **Shape a Pitch** — Define the problem, sketch a solution at the right abstraction, identify rabbit holes, and set an appetite
- **Run the Betting Table** — Evaluate shaped pitches, make cycle bets, and decide what gets built next
- **Track Progress** — Use hill charts to surface unknowns and communicate progress without status meetings
- **Scope Hammer** — Cut scope to meet the appetite without losing the core value of the work

**References included:**
- Core concepts (appetite, shaping, betting, building)
- Guiding principles
- Anti-patterns that cause cycles to blow up

**Trigger phrases:** pitches, appetite, betting table, cool-down, hill charts, fat marker sketches, breadboards, scope hammering, fixed-time variable-scope, Ryan Singer.

---

### Story Mapping

Applies Jeff Patton's User Story Mapping to help teams build shared understanding, restore the narrative that flat backlogs destroy, and plan releases around walking skeletons rather than ranked lists.

**Workflows:**
- **Build a Map** — Construct a story map from user activities, tasks, and stories, with the backbone at the top
- **Slice Releases** — Cut horizontal slices through the map to define releases with minimum viable outcomes
- **Generate Stories** — Write user stories that preserve context and connect to a larger user journey
- **Facilitate Planning** — Run a story mapping session with stakeholders to build shared understanding

**References included:**
- Core concepts and narrative structure principles
- Mapping techniques (backbone, tasks, stories)
- Slicing principles for release planning
- Anti-patterns including the flat-backlog trap

**Trigger phrases:** story maps, backbone, walking skeleton, release slicing, flat backlog, shared understanding, Jeff Patton.

---

## Repository Structure

```
product-skills/
├── skills/
│   ├── continuous-discovery/
│   │   ├── SKILL.md
│   │   ├── references/
│   │   │   ├── anti-patterns.md
│   │   │   ├── core-thesis.md
│   │   │   ├── frameworks.md
│   │   │   ├── principles.md
│   │   │   ├── techniques.md
│   │   │   └── voice.md
│   │   └── workflows/
│   │       ├── set-outcomes.md
│   │       ├── map-opportunities.md
│   │       ├── ideate-solutions.md
│   │       └── test-assumptions.md
│   ├── jobs-to-be-done/
│   │   ├── SKILL.md
│   │   ├── references/
│   │   │   ├── anti-patterns.md
│   │   │   ├── core-concepts.md
│   │   │   ├── forces-framework.md
│   │   │   └── interview-techniques.md
│   │   └── workflows/
│   │       ├── switch-interview.md
│   │       ├── analyze-forces.md
│   │       ├── map-demand-timeline.md
│   │       └── write-job-statement.md
│   ├── shape-up/
│   │   ├── SKILL.md
│   │   ├── references/
│   │   │   ├── anti-patterns.md
│   │   │   ├── core-concepts.md
│   │   │   └── principles.md
│   │   └── workflows/
│   │       ├── shape-pitch.md
│   │       ├── run-betting-table.md
│   │       ├── track-progress.md
│   │       └── scope-hammer.md
│   └── story-mapping/
│       ├── SKILL.md
│       ├── references/
│       │   ├── anti-patterns.md
│       │   ├── core-concepts.md
│       │   ├── mapping-techniques.md
│       │   └── slicing-principles.md
│       └── workflows/
│           ├── build-map.md
│           ├── slice-releases.md
│           ├── generate-stories.md
│           └── facilitate-planning.md
├── CLAUDE.md
└── README.md
```

## License

MIT License — See [LICENSE](LICENSE) for details.
