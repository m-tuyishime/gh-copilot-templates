---
applyTo: "__tests__/**/*.ts,__tests__/**/*.tsx"
---

# Testing Conventions

When writing tests for this repository:

- Use descriptive test names that clearly state what behavior is being tested: `it("should validate email with a valid address")`
- Keep each test focused on a single behavior—don't test multiple things in one test
- Always test both success and error cases
- Use meaningful assertion messages to explain what failed: `expect(result).toBe(true, "Email validation should accept valid addresses")`
- For async operations, use `async/await` rather than callbacks
- Mock external dependencies (API calls, file system, etc.)
- Keep test files colocated with source files when possible, or mirror the directory structure in `__tests__`

## Test Structure

```typescript
describe("ComponentName", () => {
  describe("methodName", () => {
    it("should do something when condition is met", () => {
      // Arrange
      const input = setupTestData();
      
      // Act
      const result = methodName(input);
      
      // Assert
      expect(result).toBe(expected);
    });
  });
});
```

## Common Patterns

- Use `beforeEach` for shared setup, not repeated code in each test
- Use `afterEach` for cleanup to prevent test pollution
- Group related tests with `describe` blocks
- Use `test.skip` or `it.skip` for temporarily disabled tests (never comment out tests)
- Use `test.only` or `it.only` for debugging specific tests (remove before committing)

## Coverage Expectations

- All new features must include tests
- Bug fixes should include regression tests
- Aim for >80% coverage on business logic
- 100% coverage is not required for UI components
