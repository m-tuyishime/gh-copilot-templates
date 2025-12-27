# Project Guidelines

This file demonstrates a cross-platform instruction file that works across GitHub Copilot, Cursor, Codex, Zed, Windsurf, Gemini CLI, and other AI coding tools.

## Code Quality Standards

- Use TypeScript strict mode with no implicit `any`
- Prefer `?.` optional chaining over `!` non-null assertions
- Enable exhaustive switch case checking
- Use meaningful variable names that describe intent
- Keep functions focused on a single responsibility
- Document complex logic with JSDoc comments

### JSDoc Format

```typescript
/**
 * Brief description of what the function does.
 * 
 * @param paramName - Description of the parameter
 * @returns Description of what is returned
 * @throws {ErrorType} Description of when this error is thrown
 */
```

## Tech Stack

- **Frontend**: React 19 with Server Components for data fetching
- **Styling**: Tailwind CSS with custom design tokens
- **Type Safety**: TypeScript in strict mode
- **Testing**: Vitest with React Testing Library
- **Linting**: ESLint with recommended rules

## Development Workflow

### Build Commands
```bash
npm run build      # Production build
npm run dev        # Development server
npm run test       # Run tests
npm run lint       # Run linter
```

### Code Organization
- Components in `components/`
- Server actions in `app/actions/`
- Utilities in `lib/`
- Tests colocated in `__tests__/` directories

## Important Do-Nots

- ❌ Never use `console.log` for production code
  - ✅ Use the logger from `lib/logger` instead
- ❌ Never commit `.env` files
- ❌ Never use `git add -A` or `git add .`
  - ✅ Stage files individually for atomic commits
- ❌ Never disable TypeScript strict mode
- ❌ Never use `any` type without explicit justification

## Error Handling

- Use custom error classes for domain-specific errors
- Always handle async errors with try-catch
- Provide meaningful error messages to users
- Log errors with appropriate context for debugging

## Performance Considerations

- Use React Server Components for data fetching when possible
- Implement proper loading states with Suspense
- Lazy load heavy components with dynamic imports
- Optimize images with Next.js Image component

## Accessibility

- All interactive elements must be keyboard accessible
- Use semantic HTML elements
- Include proper ARIA labels where needed
- Maintain minimum contrast ratios for text
