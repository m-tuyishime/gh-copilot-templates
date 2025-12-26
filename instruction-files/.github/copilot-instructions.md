# GitHub Copilot Instructions

This file demonstrates GitHub Copilot-specific instructions that complement AGENTS.md with VS Code and Copilot-specific features.

## VS Code Copilot Chat Tools

When working with this codebase:

- Use `#tool:search/codebase` to search the codebase before making assumptions
- Use `#tool:read/readFile` to understand file contents before editing
- Use `#tool:web/fetch` to look up latest documentation when needed
- Check `#tool:read/problems` before claiming a fix is complete

See the full list of tools at: https://code.visualstudio.com/docs/copilot/chat/chat-tools

## Copilot Agent Workflows

### Multi-Step Tasks

When handling complex requests:
1. Search the codebase for relevant files first
2. Read files to understand current implementation
3. Plan changes before executing
4. Verify changes by running tests
5. Check for compilation errors before marking complete

### Self-Verification

After making changes:
- Run the test suite with `execute/runInTerminal`
- Check terminal output with `execute/getTerminalOutput`
- Fix any errors discovered before yielding back to user

## VS Code Settings

When configuring VS Code:
- TypeScript strict mode should be enabled
- ESLint should run on save
- Prettier should format on save
- File watcher should be enabled for tests

## GitHub-Specific Context

### GitHub Actions
- All PRs must pass CI checks before merging
- Tests run on push to main and PR branches
- Linting is enforced in CI

### Development Environment
- Use Node.js LTS version
- Dependencies managed with npm (not yarn or pnpm)
- Git hooks enforced with husky
