---
name: clean-code-design-and-error-handling
description: Design modules with clear responsibilities and handle errors explicitly. Use when shaping architecture, dependencies, branching logic, or failure paths.
---

# Clean Code Design and Error Handling

Design code so responsibilities are clear, dependencies stay local, and failures are handled intentionally.

## Design

- Apply the Single Responsibility Principle to functions, classes, modules, and components.
- Keep domain, application, infrastructure, and presentation concerns separate.
- Factor shared logic when duplication is real, but do not over-abstract early.
- Prefer polymorphism to long type-based condition chains.
- When branching on one value with three or more cases, prefer a `switch` over a long `if`/`else if` chain.
- Use dependency injection and depend on abstractions instead of concrete implementations.
- Follow the Law of Demeter: talk to direct collaborators, not long object chains.
- Prefer positive, readable predicates over negative conditionals.
- Encapsulate boundary conditions in one named place instead of scattering edge checks.
- Make preconditions explicit. Avoid hidden ordering or temporal dependencies.
- Isolate concurrency concerns from business logic.

## Error handling

- Fail fast at boundaries by validating inputs and rejecting invalid state early.
- Model expected failures with explicit typed errors instead of ambiguous booleans, nulls, or bare errors.
- Return safe, intentional error messages without leaking internals.
- Log the detailed context needed for diagnosis internally.
- Handle errors at the level that can act on them.
- Do not swallow exceptions silently or catch and ignore failures.
