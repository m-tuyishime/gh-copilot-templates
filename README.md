# GitHub Copilot Templates

Practical templates and examples for customizing GitHub Copilot workflows. 

## 📂 Repository Structure

### `/templates` 
**Generalized files ready to copy and customize** for your own projects:
- Custom prompt templates (`.prompt.md`)
- Instruction file templates (`AGENTS.md`, `copilot-instructions.md`, path-specific `.instructions.md`)
- Agent file templates (`.agent.md`)
- Minimal placeholders and customization guidance

**Start here** if you want to set up your own repository from scratch.

### `/examples`
**Real-world implementations** showing the templates in action:
- Personalized versions with specific tech stacks
- Actual conventions and workflow patterns
- Complete examples for Next.js/React/TypeScript projects
- Specialized agent configurations for different workflows

**Start here** if you want to see how the templates work in practice.

## 🤖 What's Included

### Custom Prompts
Reusable prompt files for common tasks:
- Commit convention enforcement
- Convention capture from chat sessions

### Instruction Files
Auto-injected context for different file types:
- `AGENTS.md` - Cross-platform repo-wide conventions
- `copilot-instructions.md` - GitHub Copilot baseline
- Path-specific instructions for tests, docs, data access layers

### Agent Files
Specialized Copilot personas with tailored tools and instructions:
- **Researcher** - Read-only analysis and pattern discovery
- **Planner** - Implementation planning and task breakdown
- **Implementer** - Code writing and feature implementation
- **Tester** - Test writing and validation
- **Reviewer** - Code review and quality checks

## ⚡ Token Efficiency

LLM agents process your instruction files on every request. Avoid markdown formatting that wastes tokens:

| Avoid | Why |
|-------|-----|
| `**bold**`, `_italic_` | Visual sugar the LLM ignores |
| `- [ ]` checkboxes | Use `-` instead |
| Excessive blank lines | One is enough |
| Verbose explanations | Be direct |

Keep instruction files concise. Long files dilute context and make models less likely to follow all instructions.

