# TODO

This file tracks examples and content that need more information or context to implement properly.

## Missing Examples

### Default Settings (`/default-settings`)

- [ ] **Autocomplete examples**: Need specific code files showing how docstrings influence autocomplete behavior
  - Example: A well-documented function where autocomplete generates the full implementation
  - Example: Pattern-based completion from surrounding code
  - Example: Type signature-driven autocomplete

- [ ] **Chat mode examples**: Need screenshots or transcripts of actual chat interactions
  - Research query examples
  - How-to question examples
  - Code explanation examples

- [ ] **Agent mode examples**: Need step-by-step workflow demonstrations
  - Multi-step task planning example
  - Self-verification workflow example
  - Error fixing loop example

### Custom Prompts (`/custom-prompts`)

- [ ] **Additional prompt templates**: Could add more specialized prompts based on common workflows
  - Code review prompt template
  - Refactoring workflow prompt
  - Documentation generation prompt
  - Test generation prompt

### Instruction Files (`/instruction-files`)

- [ ] **Logging conventions**: Need `logging.instructions.md` example
  - What logging library to use
  - Log level conventions
  - Structured logging format
  - What should/shouldn't be logged

- [ ] **Zod schema conventions**: Need `zod.instructions.md` example
  - Schema organization patterns
  - Validation error messages
  - Schema composition patterns
  - Integration with TypeScript types

- [ ] **Git conventions**: Need `git.instructions.md` example (mentioned in capture-conventions prompt)
  - Commit message format
  - Branch naming conventions
  - When to commit vs when to continue working
  - Post-commit workflows

## Future Enhancements

- [ ] Add working example project that uses all these files together
- [ ] Include before/after comparisons showing impact of instruction files
- [ ] Create video demonstrations or animated GIFs for complex workflows
- [ ] Add troubleshooting section for common issues
- [ ] Include metrics on token usage with/without instruction files

## Questions to Resolve

1. Should we include actual VS Code screenshots or keep it text-based?
2. Do we need separate examples for each model (Claude, Gemini, GPT)?
3. Should we show anti-patterns alongside best practices?
4. How much detail on the MCP tools mentioned in the articles?

---

**Last Updated**: December 26, 2025

**Contributing**: If you have specific examples or can fill in any of these gaps, please open an issue or submit a PR!
