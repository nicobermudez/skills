---
name: clean-code-testing
description: Write focused, behavior-oriented tests. Use when adding or updating tests for acceptance criteria, outcomes, and edge cases.
---

# Clean Code Testing

Write tests that protect real behavior and stay easy to understand.

## Testing principles

- Test the acceptance criteria, not coverage for its own sake.
- Verify behavior and outcomes instead of implementation details.
- Prefer builders or factories for test data so tests stay readable and reuse real validation rules.
- Keep one logical assertion per test.
- Make tests fast, independent, repeatable, self-validating, and readable.
- Name tests to describe the behavior under test.

## What to avoid

- Tests that only prove trivial getters, setters, or internal helper calls.
- Assertions about logging or other incidental implementation details.
- Brittle setup that couples tests tightly to private structure.

## When updating tests

- Follow the existing test style and helpers in the repository.
- Add edge-case coverage when the change affects branching, validation, or error handling.
- Prefer the smallest test changes that still prove the user-visible behavior.
