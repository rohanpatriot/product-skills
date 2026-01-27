# Skills Repository

This repository contains Claude Code skills that are discoverable and installable via skills.sh.

## Critical Requirements

These rules are **MANDATORY**. Violations will cause skills to fail discovery or behave incorrectly.

### YAML Frontmatter (REQUIRED)

Every `SKILL.md` file **MUST** begin with valid YAML frontmatter:

```yaml
---
name: skill-name
description: What this skill does and when to use it. Claude uses this to decide when to apply the skill automatically.
---
```

- `name` is **REQUIRED** - must match directory name, lowercase-with-hyphens
- `description` is **REQUIRED** - Claude uses this for automatic skill selection
- Missing frontmatter = skill will not be discovered

### Directory Structure (ENFORCED)

```
your-repo-name/
├── skills/                      # ALL skills MUST go here
│   ├── your-skill-name/         # Directory name = skill name
│   │   ├── SKILL.md             # REQUIRED - main skill file
│   │   ├── references/          # Optional: supporting documentation
│   │   └── workflows/           # Optional: step-by-step processes
│   └── .internal/               # Hidden skills (internal: true)
│       └── internal-skill/      # Requires INSTALL_INTERNAL_SKILLS=1
├── CLAUDE.md                    # Project instructions
└── README.md                    # Repository documentation
```

### File Naming (ENFORCED)

- Skill directories: `lowercase-with-hyphens`
- Main file: `SKILL.md` (exact casing)
- Workflow files: `lowercase-with-hyphens.md`
- Reference files: `lowercase-with-hyphens.md`

**Invalid names will cause discovery failures:**
- ❌ `MySkill/` (no camelCase)
- ❌ `my_skill/` (no underscores)
- ❌ `skill.md` (must be SKILL.md)

## README Structure

Your README.md should include these sections:

### Title and Description

```markdown
# Your Repository Name

Brief description of what this skills repository provides.
```

### Installation

```markdown
## Installation

\`\`\`bash
npx skills add owner/repo-name
\`\`\`
```

Replace `owner/repo-name` with your GitHub username and repository name.

### Available Skills

```markdown
## Available Skills

| Skill | Description |
|-------|-------------|
| `/skill-name` | What this skill does |
| `/another-skill` | What this other skill does |
```

### License

Include a license section appropriate for your repository.

## Skill Design Philosophy

**Skills are tools, not documentation.** This is not a suggestion—skills that read like reference material fail to provide value.

### REQUIRED Patterns

Write as an active collaborator:
- ✅ "I help you find..."
- ✅ "I'll audit this for..."
- ✅ "I check your code for..."

Create workflows that DO things:
- ✅ audit, test, check, analyze, decompose, verify

Focus on application, not explanation:
- ✅ "When you're making a decision, I'll check for these biases..."
- ❌ "Kahneman describes System 1 as..."

### PROHIBITED Patterns

**DO NOT:**
- Summarize what an author said
- Include book-specific stories, examples, or characters
- Create reference files that just explain concepts
- Name skills after books (e.g., `thinking-fast-and-slow`)
- Write in passive/academic voice

**Example transformation:**

Bad (book report):
> "Kahneman describes System 1 as fast, automatic thinking..."

Good (thinking tool):
> "I'll check this decision for System 1 shortcuts that might be leading you astray."

## File Reference Patterns

**ALWAYS use relative markdown links.** Other patterns will fail.

### From SKILL.md to subdirectories
```markdown
See [workflows/main-workflow.md](workflows/main-workflow.md)
See [references/concepts.md](references/concepts.md)
```

### From workflow files to siblings
```markdown
See [other-workflow.md](other-workflow.md)
```

### From workflow files to references (parent directory)
```markdown
Read [../references/concepts.md](../references/concepts.md)
```

### PROHIBITED Link Patterns

These patterns **WILL FAIL**:
- ❌ Backticks: `` `workflows/example.md` ``
- ❌ Plain text: `workflows/example.md`
- ❌ Absolute paths: `/Users/me/project/skills/...`
- ❌ No path: just mentioning a filename

## Internal Skills

For skills that should be hidden by default:

1. Add to SKILL.md frontmatter:
```yaml
---
name: internal-skill-name
description: What this skill does.
metadata:
  internal: true
---
```

2. Place in `skills/.internal/` directory

3. Install with: `INSTALL_INTERNAL_SKILLS=1 npx skills add owner/repo`

## Testing & Verification

### Local Testing

```bash
# Test with Claude Code directly
npx skills add ./path/to/this/repo

# Verify a specific skill loads
# Then run: /skill-name
```

### Verify Discovery Works

```bash
# Install from your repo
npx skills add owner/repo-name

# Install with internal skills
INSTALL_INTERNAL_SKILLS=1 npx skills add owner/repo-name

# List installed skills
npx skills list
```

### Common Issues

| Problem | Cause | Fix |
|---------|-------|-----|
| Skill not discovered | Missing/invalid frontmatter | Add required `name` and `description` |
| Links don't resolve | Wrong link format | Use `[text](relative/path.md)` format |
| Internal skill visible | Missing `metadata.internal` | Add to frontmatter |
| Name mismatch | Directory ≠ frontmatter name | Make them match exactly |

## Environment Variables

| Variable | Purpose |
|----------|---------|
| `INSTALL_INTERNAL_SKILLS=1` | Reveals skills with `metadata.internal: true` |
