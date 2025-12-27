# GitHub Copilot Instructions

This template provides GitHub Copilot-specific instructions. Customize for your workflow.

## VS Code Copilot Chat Tools

[Define how you want the agent to use built-in tools, e.g.:]

- Use `#tool:search/codebase` to search before making assumptions
- Use `#tool:read/readFile` to understand files before editing
- Use `#tool:web/fetch` for up-to-date documentation
- Check `#tool:read/problems` before claiming completion

Full tool list: https://code.visualstudio.com/docs/copilot/chat/chat-tools

## Copilot Agent Workflows

### Multi-Step Tasks

[Define your preferred workflow for complex tasks, e.g.:]
1. Search for relevant files
2. Read and understand current implementation
3. Plan changes
4. Execute and verify
5. Run tests before completion

### Self-Verification

[Define verification expectations, e.g.:]
- Run test suite after changes
- Check for errors before yielding
- Verify build passes

## Project-Specific Context

### Development Environment
[Document your dev environment specifics]

### CI/CD
[Document your continuous integration expectations]

### Tooling
[List project-specific tools and their usage]
