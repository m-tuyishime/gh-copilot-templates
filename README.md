# GitHub Copilot Examples

This repository contains practical examples and reference implementations for the VSCode Agents Workflow series from [m-tuyishime.dev](https://m-tuyishime.dev).

## 📚 Related Articles

- [Article 1.1: Zero to Agent - Mastering GitHub Copilot with Default Settings](https://m-tuyishime.dev/logs/vscode-agents-1-1-default-settings)
- [Article 1.2: Custom Prompts](https://m-tuyishime.dev/logs/vscode-agents-1-2-custom-prompts)
- [Article 1.3: The Power of Instruction Files](https://m-tuyishime.dev/logs/vscode-agents-1-3-instruction-files)

## 📂 Repository Structure

### `/default-settings`
Examples demonstrating standard GitHub Copilot features without customization:
- Autocomplete (Ghost Text) examples
- Chat mode interactions
- Agent mode workflows

### `/custom-prompts`
Example prompt files (`.prompt.md`) for reusable workflows:
- Git commit workflows
- Convention capture automation
- Code review templates

### `/instruction-files`
Example instruction files for automatic context injection:
- `AGENTS.md` - Cross-platform agent instructions
- `.github/copilot-instructions.md` - GitHub Copilot repo-wide instructions
- `.github/instructions/*.instructions.md` - Path-specific instructions
  - Testing conventions
  - Data Access Layer patterns
  - Documentation standards
  - Logging patterns

## 🚀 Getting Started

Each directory contains its own README with specific setup instructions and usage examples.

## 📖 What Are These Files For?

These examples complement the VSCode Agents Workflow series, providing real-world implementations you can adapt for your own projects.

### Quick Reference

- **Default Settings**: No configuration needed—works out of the box
- **Custom Prompts**: Reusable prompt templates you reference with `#file:name` or `/name`
- **Instruction Files**: Auto-injected context based on file patterns you're editing

## 🤝 Contributing

Found a better pattern? Open an issue or PR! These examples evolve as the ecosystem does.

## 📄 License

MIT

---

**Last Updated**: December 26, 2025
