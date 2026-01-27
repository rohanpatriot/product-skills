# Skills Template

A template repository for creating Claude Code skills compatible with [skills.sh](https://skills.sh).

## Quick Start

1. Click "Use this template" on GitHub to create your repository
2. Rename the example skill in `skills/example-skill/`
3. Edit `SKILL.md` with your skill's logic and frontmatter
4. Install and test locally

## Installation

Install skills from this repository:

```bash
# Install from GitHub
npx skills.sh install owner/repo-name

# Or install with internal skills visible
INSTALL_INTERNAL_SKILLS=1 npx skills.sh install owner/repo-name
```

## Testing Locally

```bash
# Test with Claude Code
claude --plugin-dir /path/to/this/repo
```

## Repository Structure

```
skills-template/
├── skills/
│   ├── example-skill/           # Your public skills go here
│   │   ├── SKILL.md             # Main skill file (required)
│   │   ├── references/          # Supporting documentation
│   │   └── workflows/           # Step-by-step processes
│   └── .internal/               # Hidden skills (require INSTALL_INTERNAL_SKILLS=1)
├── CLAUDE.md                    # Project instructions
└── README.md                    # This file
```

## Creating Skills

### Required: SKILL.md

Every skill needs a `SKILL.md` file with YAML frontmatter:

```yaml
---
name: your-skill-name
description: What this skill does and when Claude should use it.
---

# Your skill content here
```

### Optional Directories

- **references/** - Background knowledge, concept explanations, quick-reference tables
- **workflows/** - Step-by-step processes the skill can invoke

### File Linking

Always use relative markdown links:

```markdown
See [workflows/main-workflow.md](workflows/main-workflow.md)
See [references/concepts.md](references/concepts.md)
```

### Internal Skills

Skills that should be hidden by default:

1. Place them in `skills/.internal/`
2. Add `metadata.internal: true` to frontmatter:

```yaml
---
name: internal-skill
description: Only visible with INSTALL_INTERNAL_SKILLS=1
metadata:
  internal: true
---
```

## Skill Naming

- Use lowercase with hyphens: `my-skill-name`
- Be descriptive but concise
- Name after what it does, not where it came from

## Environment Variables

| Variable | Purpose |
|----------|---------|
| `INSTALL_INTERNAL_SKILLS=1` | Reveals skills with `metadata.internal: true` |

## Resources

- [skills.sh](https://skills.sh) - Skills marketplace and installer
- [vercel-labs/skills](https://github.com/vercel-labs/skills) - Official skills repository
- [Claude Code Skills Docs](https://code.claude.com/docs/en/skills) - Skill development guide

## License

MIT License - See [LICENSE](LICENSE) for details.
