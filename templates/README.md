# Templates

This folder contains generalized template files that you can copy to your own repository and customize.

## How to Use

1. **Copy** the files you need to your project
2. **Customize** them to match your workflow and conventions
3. **Place** them in the appropriate locations:
   - `AGENTS.md` → root of your repository
   - `copilot-instructions.md` → in your `.github/` folder (or project root)
   - `*.instructions.md` → in your `.github/instructions/` folder (or appropriate directory)
   - Custom prompts → `.github/prompts/` folder or user profile

## Available Templates

### Custom Prompts (`/custom-prompts`)
- `capture-conventions.prompt.md` - Template for capturing conventions from chat
- `commit-convention.prompt.md` - Template for git commit workflows

### Instruction Files (`/instruction-files`)
- `AGENTS.md` - Cross-platform repo-wide instructions
- `copilot-instructions.md` - GitHub Copilot-specific instructions
- `tests.instructions.md` - Testing conventions
- `docs.instructions.md` - Documentation standards

## Customization Tips

1. **Start small**: Don't customize everything at once. Begin with 3-5 key conventions.
2. **Be specific**: "Use TypeScript strict mode" is better than "Use TypeScript"
3. **Stay actionable**: Focus on what to DO, not what to avoid
4. **Iterate**: Add conventions as friction points emerge
5. **Keep it DRY**: Don't duplicate the same rules across multiple files

## Need Examples?

Check the `/examples` folder to see these templates in action with real customizations.
