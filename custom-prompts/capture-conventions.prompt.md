---
agent: "agent"
description: "Capture conventions from chat corrections into instruction files"
---

# Capture Conventions

Review this chat for user corrections that should become conventions.

## Process

1. Scan for places user corrected your approach or clarified preferences
2. For each correction, ask:
   - Repeatable convention or one-off?
   - Would it help future models?
   - Specific enough to be actionable?
3. Skip if: factual error, too context-specific, or already documented
4. For qualifying conventions: add to appropriate `.github/instructions/*.md` file

## Instruction Files

- `copilot-instructions.md` - global conventions
- `dal.instructions.md` - Data Access Layer 
- `docs.instructions.md` - documentation
- `logging.instructions.md` - logging
- `tests.instructions.md` - tests
- `zod.instructions.md` - Zod schemas
- `git.instructions.md` - git/commits

## Output

If conventions found:

1. Edit instruction file(s)
2. Commit: `docs(instructions): capture conventions from chat`
3. Summarize additions

If none qualify: say "No new conventions identified"

## Writing Style

- One bullet per convention, 1-2 sentences max
- Actionable (what to DO)
- No fluff, no emojis, plain markdown
- **Plain markdown**: No emojis, minimal formatting, H2/H3 headers only
