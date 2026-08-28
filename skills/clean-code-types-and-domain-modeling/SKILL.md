---
name: clean-code-types-and-domain-modeling
description: Model domains with precise types and explicit concepts. Use when designing TypeScript types, value objects, entities, or domain-layer code.
---

# Clean Code Types and Domain Modeling

Use types to make the domain clearer and invalid states harder to represent.

## TypeScript types

- Prefer inferred types for locals when the inferred type is obvious.
- Add explicit types at public or module boundaries and where inference is ambiguous.
- Never use `any`. Prefer precise types, generics, or `unknown` with narrowing.
- Avoid primitive obsession. Use dedicated domain types or value objects for important concepts.
- Favor immutability: default to `const`, `readonly`, and returning new values instead of mutating inputs.

## Domain-driven design

- Model the domain explicitly with entities, aggregate roots, and value objects.
- Keep the ubiquitous language consistent between the code and domain conversations.
- Keep domain logic in the domain layer, free of framework and persistence details.

## Objects and data structures

- Hide internal structure and expose behavior instead of leaking internals.
- Avoid hybrids that are half object and half exposed data structure.
- Keep classes small, with few instance variables and one reason to change.
- Base classes should not depend on details of their derivatives.
- Prefer instance methods over static methods when behavior depends on state.
