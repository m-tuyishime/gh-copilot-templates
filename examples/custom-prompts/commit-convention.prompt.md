---
agent: "agent"
name: "commit-convention"
description: "Enforce atomic commit practices and prevent accidental staging"
---

# Git Commit Convention

Follow atomic commit practices to ensure clean git history.

## Process

1. **Review staged changes**: Use `git diff --staged` to see what will be committed
2. **Stage selectively**: Never use `git add -A` or `git add .`
   - Stage files individually: `git add path/to/file`
   - Stage parts of files if needed: `git add -p path/to/file`
3. **Verify staging**: Check `git status` before committing
4. **Write descriptive commits**: Use conventional commit format
   - `feat: add user authentication`
   - `fix: resolve memory leak in cache`
   - `docs: update API documentation`
   - `refactor: simplify error handling`
   - `test: add unit tests for validators`

## Anti-Patterns to Avoid

- ❌ `git add -A` (stages everything including unintended files)
- ❌ `git add .` (same issue as above)
- ❌ Generic commit messages like "updates" or "changes"
- ❌ Mixing multiple features in one commit
- ❌ Committing `.env` or sensitive files

## Safety Checks

Before committing:
1. Ensure `.env` files are NOT staged
2. Verify only related files are staged
3. Check for console.log or debugging code
4. Confirm tests pass for staged changes

## Example Workflow

```bash
# Stage specific files
git add src/components/Button.tsx
git add src/components/__tests__/Button.test.tsx

# Verify
git status

# Commit
git commit -m "feat: add Button component with variants"
```
