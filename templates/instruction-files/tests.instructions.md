---
applyTo: "__tests__/**/*.ts,__tests__/**/*.tsx,**/*.test.ts,**/*.test.tsx"
---

# Testing Conventions

[Customize this template for your testing practices]

## Test Structure

[Define your preferred test structure, e.g.:]
- Use descriptive test names that state the expected behavior
- Keep each test focused on single behavior
- Test both success and error cases
- Use meaningful assertion messages

## Test Organization

[Define how tests should be organized, e.g.:]
```typescript
describe("ComponentName", () => {
  describe("methodName", () => {
    it("should [expected behavior] when [condition]", () => {
      // Arrange
      // Act
      // Assert
    });
  });
});
```

## Common Patterns

[List patterns you want followed, e.g.:]
- Use `beforeEach` for shared setup
- Use `afterEach` for cleanup
- Group related tests with `describe`
- [Add your patterns]

## Coverage Expectations

[Define coverage requirements, e.g.:]
- Minimum coverage percentage
- Which code requires 100% coverage
- What can be excluded
