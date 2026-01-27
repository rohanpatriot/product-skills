---
name: example-internal
description: An internal skill demonstrating hidden skills. Only visible when INSTALL_INTERNAL_SKILLS=1 is set.
metadata:
  internal: true
---

# Example Internal Skill

This skill is hidden by default and only becomes visible when users install with:

```bash
INSTALL_INTERNAL_SKILLS=1 npx skills.sh install owner/repo-name
```

## When to Use Internal Skills

Internal skills are useful for:

1. **Work-in-progress skills** - Skills still being developed
2. **Team-specific tools** - Skills meant for internal team use
3. **Experimental features** - Testing new approaches before public release
4. **Sensitive workflows** - Processes that shouldn't be widely discoverable

## Structure

Internal skills follow the same structure as public skills:

```yaml
---
name: skill-name
description: What this skill does
metadata:
  internal: true    # This is the key flag
---
```

## Converting to Public

When ready to make a skill public:

1. Move from `skills/.internal/` to `skills/`
2. Remove `metadata.internal: true` from frontmatter
3. Update any documentation references

## Example Use Case

This template demonstrates the internal skill pattern. Replace this content with your actual internal skill logic.
