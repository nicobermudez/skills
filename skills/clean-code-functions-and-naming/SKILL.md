---
name: clean-code-functions-and-naming
description: Write small, focused functions with clear names. Use when adding or refactoring function bodies, signatures, guard clauses, and naming.
---

# Clean Code Functions and Naming

Optimize function design for readability, clear intent, and safe change.

## Functions

- Keep functions small and focused on one thing at one level of abstraction.
- Choose names that explain what the function does without reading the body.
- Prefer few arguments. Group related arguments into a value object when a parameter list grows.
- Do not use flag arguments. Split behavior into separate well-named functions instead.
- Avoid hidden side effects. A function should do what its name says and nothing more.
- Prefer many small functions over one large function controlled by behavior flags or codes.
- Use guard clauses and early returns to handle edge cases up front and keep the happy path flat.

## Naming

- Choose descriptive, unambiguous, pronounceable, and searchable names.
- Make meaningful distinctions; avoid filler words that do not add meaning.
- Replace magic numbers and strings with named constants.
- Avoid encoded names unless the surrounding codebase already relies on them.

## Refactoring triggers

- Split functions that mix validation, orchestration, and domain logic.
- Rename functions, variables, and types whose meaning is unclear without extra explanation.
- Introduce a constant or value object when raw primitives are doing domain work.
