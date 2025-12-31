# AGENTS.md Template

This file provides a starting point for creating your own `AGENTS.md` file. This is a cross-platform standard that works with GitHub Copilot, Cursor, Windsurf, Gemini CLI, and other AI coding tools.

**Location**: Place this file in your repository root.

**Activation**: Enable in VS Code with `chat.useAgentsMdFile` setting.

## What to Include

### 1. Project Overview
Brief description of what the project does and its tech stack.

### 2. Code Quality Standards
Your general coding conventions:
- Naming conventions
- Formatting preferences
- Comment style
- Language-specific patterns

### 3. Tech Stack Details
Specific technologies and their usage:
- Frameworks and versions
- Preferred libraries
- Configuration patterns

### 4. Development Workflow
Commands and processes:
- Build commands
- Test commands
- Lint/format commands
- Git conventions

### 5. Important Constraints
Hard rules that must be followed:
- Security requirements
- Performance constraints
- Accessibility requirements
- Browser/platform support

---

## Example Template

```markdown
# Project Name

Brief description of what this project does.

## Tech Stack

- Next.js 15 with App Router
- React 19 with Server Components
- TypeScript strict mode
- Tailwind CSS 4
- Vitest for testing

## Code Quality

### TypeScript
- Use TypeScript strict mode
- Prefer `?.` over `!` assertions
- Use explicit return types for public functions
- No `any` types (use `unknown` if necessary)

### React
- Prefer Server Components over Client Components
- Use functional components with hooks
- Extract custom hooks for reusable logic
- Keep components focused and composable

### Naming
- Use PascalCase for components: `UserProfile.tsx`
- Use camelCase for utilities: `formatDate.ts`
- Use kebab-case for routes: `/user-profile`
- Prefix test files with component name: `UserProfile.test.tsx`

## Development Workflow

### Commands
- Build: `npm run build`
- Dev server: `npm run dev`
- Tests: `npm run test`
- Lint: `npm run lint`

### Testing
- Write tests for business logic
- Use React Testing Library for components
- Keep tests colocated: `__tests__/` folders

### Git
- Use conventional commits: `feat:`, `fix:`, `docs:`, `refactor:`
- Keep commits atomic and focused
- Write descriptive commit messages

## Important Rules

- Never use `console.log` - use logger from `lib/logger`
- Always validate user input with Zod schemas
- Use `next/image` for all images (never `<img>`)
- Use Server Components by default, only use Client Components when needed
- Fetch data in Server Components, not in Client Components
```

---

## Customization Tips

1. **Start minimal**: Include only your most important 3-5 conventions
2. **Be specific**: "Use TypeScript strict mode" not "use TypeScript well"
3. **Update as you go**: Add conventions when you notice repetition in prompts
4. **Reference examples**: Point to actual files that show good patterns
5. **Keep it under 100 lines**: Token efficiency matters

## Related Files

- For GitHub Copilot-specific instructions: `.github/copilot-instructions.md`
- For path-specific instructions: `.github/instructions/*.instructions.md`
- For reusable prompts: `.github/prompts/*.prompt.md`
- For specialized agents: `.github/agents/*.agent.md`

## Further Reading

- [Article: Instruction Files](https://github.com/m-tuyishime/gh-copilot-templates#vscode-agents-workflow-series)
- [AGENTS.md Official Site](https://aaif.io/)
