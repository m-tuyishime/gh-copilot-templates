---
applyTo: "lib/dal/**/*.ts"
---

# Data Access Layer Conventions

When working with data access code:

- All database queries must be wrapped in try-catch blocks
- Use prepared statements to prevent SQL injection
- Return typed results using TypeScript interfaces
- Validate input data before database operations
- Use transactions for operations that modify multiple tables
- Log database errors with appropriate context

## Error Handling

```typescript
try {
  const result = await db.query(/* ... */);
  return result;
} catch (error) {
  logger.error('Database operation failed', { 
    operation: 'fetchUser',
    error: error.message,
    context: { userId }
  });
  throw new DatabaseError('Failed to fetch user', { cause: error });
}
```

## Query Patterns

- Prefer parameterized queries over string concatenation
- Use connection pooling for better performance
- Close connections in finally blocks
- Implement proper pagination for list queries
- Use indexes for frequently queried columns

## Validation

- Validate all inputs before queries
- Use Zod schemas for input validation
- Sanitize user input to prevent injection
- Check for required fields before database operations
