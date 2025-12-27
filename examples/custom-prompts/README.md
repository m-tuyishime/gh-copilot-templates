# Custom Prompts Examples

This directory contains example prompt files (`.prompt.md`) for reusable workflows, as covered in [Article 1.2: Custom Prompts](https://m-tuyishime.dev/logs/vscode-agents-1-2-custom-prompts).

## Setup

Prompt files can be stored in two locations:

1. **Repo-level**: `.github/prompts/` folder (shared with team)
2. **User-level**: Global profile via Command Palette → "Chat: Configure Prompt Files..." → "+ New prompt file..." → "user data"

## Available Examples

### `capture-conventions.prompt.md`
Scans chat history for user corrections that should become permanent conventions.

**Usage**: `#file:capture-conventions` or `/capture-conventions`

**When to use**:
- After a productive chat session
- Before clearing your chat history
- When you notice yourself correcting the agent repeatedly

### `commit-convention.prompt.md`
Enforces atomic commit practices and prevents accidental staging.

**Usage**: `#file:commit-convention` or `/commit-convention`

**When to use**:
- Before making git commits
- When working on multiple features simultaneously
- To prevent `git add -A` behavior

## Frontmatter Configuration

Available options in prompt file frontmatter:

| Field | Description |
|-------|-------------|
| `description` | Short description shown in autocomplete |
| `name` | Override file name for `/command` usage |
| `argument-hint` | Guidance text in chat input field |
| `agent` | Which agent runs the prompt: `copilot`, `edit`, or custom |
| `model` | Specific language model to use |
| `tools` | List of available tool/tool set names |

## When to Use Prompt Files vs Instruction Files

**Use Prompt Files when**:
- You need on-demand, specific workflows
- You want to control which model executes the task
- You need to restrict tool access for safety
- The task doesn't map to specific file patterns

**Use Instruction Files when**:
- Rules should apply automatically based on file patterns
- Context should always be available without manual reference
- You want zero-friction, auto-injected conventions

## Tips

1. Start simple—one sentence per convention
2. Be actionable ("Do X" not "Consider X")
3. Reference other prompt/instruction files if needed
4. Use descriptive names for easy autocomplete
5. Don't duplicate content between prompt and instruction files

## Related Documentation

- [VS Code Prompt Files Documentation](https://code.visualstudio.com/docs/copilot/customization/prompt-files)

---

**Last Updated**: December 26, 2025
