---
applyTo: "docs/**/*.md,*.md"
---

# Documentation Standards

When writing or updating documentation:

- Use clear, concise language
- Include code examples for technical concepts
- Keep paragraphs short (3-4 sentences max)
- Use headings to organize content hierarchically
- Link to related documentation when referencing other topics
- Include a "Last Updated" date at the bottom

## Markdown Style

- Use ATX-style headings (`#`, `##`, `###`) not underline style
- Use fenced code blocks with language identifiers
- Use relative links for internal documentation
- Use descriptive link text (not "click here")

## Code Examples

```markdown
\`\`\`typescript
// Good: Include context and explanation
function validateEmail(email: string): boolean {
  const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
  return emailRegex.test(email);
}
\`\`\`
```

- Always specify language for syntax highlighting
- Include comments to explain complex logic
- Keep examples focused and minimal
- Show both usage and output when relevant

## Structure

- Start with a brief introduction (1-2 paragraphs)
- Use table of contents for long documents
- Include prerequisites section when needed
- End with "Related Documentation" or "Next Steps" links
