# Product Skills

Claude Code skills for product management and discovery. Install them to give Claude structured frameworks for product strategy work.

## Installation

```bash
npx skills add rohanpatriot/product-skills
```

## Available Skills

| Skill | Description |
|-------|-------------|
| `continuous-discovery` | Applies Teresa Torres's continuous discovery habits — setting outcomes, interviewing customers, mapping opportunities, generating solutions, and testing assumptions |

## Skill Details

### Continuous Discovery

Guides product trios through the full continuous discovery loop:

**Workflows:**
- **Set Outcomes** — Define, negotiate, and commit to a product outcome tied to business results
- **Map Opportunities** — Interview customers, create snapshots, and build an Opportunity Solution Tree
- **Ideate Solutions** — Generate, compare, and select solutions using individual-first ideation
- **Test Assumptions** — Identify leap-of-faith assumptions and design small, fast tests

**References included:**
- Core thesis and prerequisite mindsets
- 8 discovery frameworks with application guidance
- 12 guiding principles
- 11 step-by-step techniques
- 28 anti-patterns organized by phase
- Terminology precision guide

**Trigger phrases:** Opportunity Solution Trees, product trios, assumption testing, continuous interviewing, product outcomes, experience maps, interview snapshots.

## Repository Structure

```
product-skills/
├── skills/
│   └── continuous-discovery/
│       ├── SKILL.md
│       ├── references/
│       │   ├── anti-patterns.md
│       │   ├── core-thesis.md
│       │   ├── frameworks.md
│       │   ├── principles.md
│       │   ├── techniques.md
│       │   └── voice.md
│       └── workflows/
│           ├── set-outcomes.md
│           ├── map-opportunities.md
│           ├── ideate-solutions.md
│           └── test-assumptions.md
├── CLAUDE.md
└── README.md
```

## License

MIT License - See [LICENSE](LICENSE) for details.
