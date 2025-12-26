# Default Settings Examples

This directory contains examples for using GitHub Copilot with its default configuration, as covered in [Article 1.1: Zero to Agent](https://m-tuyishime.dev/logs/vscode-agents-1-1-default-settings).

## Prerequisites

- Visual Studio Code (v1.107.0 or later recommended)
- GitHub Copilot Extension (v1.388.0 or later recommended)
- A GitHub Account with Copilot access

## The Three Modes

### 1. Autocomplete (Ghost Text)

**What it is**: Inline code suggestions that appear as you type.

**Examples**:
- See `autocomplete-examples/` for files demonstrating how docstrings influence autocomplete
- Function implementations that autocomplete from type signatures
- Pattern completion based on surrounding code

### 2. Chat Mode

**What it is**: Conversational interface with read-only tools (search, web fetch).

**Examples**:
- Research queries about the codebase
- Asking "how-to" questions
- Requesting code explanations

### 3. Agent Mode

**What it is**: Chat with write access—can create and modify files directly.

**Examples**:
- Multi-step task planning
- Self-verification and error fixing
- File creation and modification workflows

## Key Concepts

### Built-in Tools

- `search/codebase`: Find files or code snippets
- `read/readFile`: Read file contents
- `edit/editFiles`: Modify files
- `execute/runInTerminal`: Run commands
- `execute/getTerminalOutput`: Read terminal output
- `web/fetch`: Fetch documentation from the web

### Premium Requests

Different models have different costs:
- **1x models**: Claude Sonnet 4.5, Gemini 3 Pro
- **0.33x models**: Claude Haiku 4.5, Gemini 3 Flash
- **3x models**: Claude Opus 4.5

## Security Best Practices

1. Never enable auto-approve for web browsing
2. Review URLs before allowing the agent to visit them
3. Use the Approval System for terminal commands
4. Leverage Checkpointing to restore previous states
5. Keep `.env` files out of auto-approval lists

## Related Documentation

- [GitHub Copilot Quickstart Guide](https://docs.github.com/en/copilot/get-started/quickstart)
- [VS Code Chat Tools Documentation](https://code.visualstudio.com/docs/copilot/chat/chat-tools)
- [GitHub Copilot Trust Center](https://copilot.github.trust.page/)

---

**Last Updated**: December 26, 2025
