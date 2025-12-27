---
agent: "agent"
description: "Capture conventions from chat corrections into instruction files"
---

# Capture Conventions

Review this chat for user corrections that should become conventions.

## Process

1. Scan for instances where the user corrected your approach or clarified preferences during the current chat session.
2. For each correction, ask:
   - Repeatable convention or one-off?
   - Would it help future models?
   - Specific enough to be actionable?
3. Skip if: factual error, too context-specific, or already documented
4. For qualifying conventions: add to appropriate instruction file

## Instruction Files

[List your instruction files here, e.g.:]
- `copilot-instructions.md` - global conventions
- `tests.instructions.md` - testing conventions
- `docs.instructions.md` - documentation standards

## Output

If conventions found:

1. Edit instruction file(s)
2. Commit with descriptive message
3. Summarize additions

If none qualify: say "No new conventions identified"

## Writing Style

- One bullet per convention, 1-2 sentences max
- Actionable (what to DO)
- Plain markdown: no emojis, minimal formatting
