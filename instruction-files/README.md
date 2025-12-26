# Instruction Files Examples

This directory contains example instruction files for automatic context injection, as covered in [Article 1.3: The Power of Instruction Files](https://m-tuyishime.dev/logs/vscode-agents-1-3-instruction-files).

## Setup

To enable instruction files in VS Code:

1. Set `github.copilot.chat.codeGeneration.useInstructionFiles` to `true`
2. For AGENTS.md support: Enable `chat.useAgentsMdFile` in settings

## File Types

### Repo-Wide Instructions

#### `AGENTS.md`
Cross-platform standard supported by 60k+ open-source projects (GitHub Copilot, Cursor, Codex, Zed, Windsurf, Gemini CLI).

**Use when**: You want portability across multiple AI coding tools.

**Contains**:
- General code quality standards
- Tech stack details
- Development workflow
- Important do-nots

#### `.github/copilot-instructions.md`
GitHub's repo-wide baseline for GitHub/VS Code ecosystem.

**Use when**: You're committed to GitHub Copilot and want zero friction.

**Contains** (if used standalone):
- Same as AGENTS.md

**Contains** (if used alongside AGENTS.md):
- VS Code Copilot Chat tool reminders
- Copilot-specific workflows
- VS Code-specific settings
- GitHub Actions setup

### Path-Specific Instructions

Files in `.github/instructions/*.instructions.md` with `applyTo` glob patterns.

**Auto-injected** when working on matching files.

**Examples**:
- `tests.instructions.md` → applies to `__tests__/**/*.ts`
- `dal.instructions.md` → applies to `lib/dal/**/*.ts`
- `docs.instructions.md` → applies to `docs/**/*.md`

## Bootstrap Path

**Level 1 (Start here)**: Create `.github/copilot-instructions.md` with 3-5 top conventions.

**Level 2 (Optional)**: Add `AGENTS.md` for portability or nested specialization.

**Level 3 (Advanced)**: Add path-specific `.instructions.md` files as friction points emerge.

## Writing Guidelines

- Be specific: "TypeScript strict mode, no implicit any" not "Use TypeScript"
- One bullet per convention, 1-2 sentences max
- Actionable: what to DO, not what to consider
- Plain markdown: no emojis, minimal formatting
- Don't duplicate across files

## Important Notes

1. **Not 100% reliable**: Models sometimes ignore instructions (it's stochastic)
2. **Use deterministic guardrails**: ESLint, Prettier, CI checks for hard rules
3. **Add incrementally**: Don't create all files at once, add as needs emerge
4. **Avoid token waste**: Don't duplicate same rules in multiple files

## Frontmatter for Path-Specific Files

```markdown
---
applyTo: "glob/pattern/**/*.ts"
---
```

## Related Documentation

- [VS Code Copilot Customization: Custom Instructions](https://code.visualstudio.com/docs/copilot/customization/custom-instructions)
- [GitHub Copilot: Configure Custom Instructions](https://docs.github.com/en/copilot/how-tos/configure-custom-instructions/add-repository-instructions)

---

**Last Updated**: December 26, 2025
