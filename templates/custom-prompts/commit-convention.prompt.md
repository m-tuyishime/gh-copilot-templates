---
agent: "agent"
name: "commit-convention"
description: "Enforce commit best practices for your workflow"
---

# Git Commit Convention

[Customize this prompt file to match your git workflow preferences]

## Process

1. **Review staged changes**: Use `git diff --staged` to see what will be committed
2. **Stage selectively**: [Define your staging preferences]
   - Example: Stage files individually with `git add path/to/file`
   - Example: Use `git add -p` for partial staging
3. **Verify staging**: Check `git status` before committing
4. **Write descriptive commits**: [Define your commit message format]

## Commit Message Format

[Choose your format, e.g.:]
- Conventional Commits: `type(scope): description`
- Simple format: `[Type] Description`
- Custom format: Define your own

## Common Types

- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `refactor`: Code restructuring
- `test`: Adding or updating tests
- `chore`: Maintenance tasks

## Anti-Patterns to Avoid

[List behaviors you want to prevent, e.g.:]
- ❌ Generic messages like "updates" or "changes"
- ❌ Mixing unrelated changes in one commit
- ❌ Committing sensitive files

## Safety Checks

Before committing:
- [List your safety requirements]
