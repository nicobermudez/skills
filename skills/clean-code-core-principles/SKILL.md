---
name: clean-code-core-principles
description: Keep code simple, consistent, readable, and maintainable. Use when implementing or refactoring code and you need general clean-code guidance.
---

# Clean Code Core Principles

Write code that teammates can read, understand, and safely change. When there is tension between options, choose the one that is simplest to understand.

## Default approach

- Follow the surrounding codebase conventions before introducing new ones.
- Do similar things the same way throughout the codebase.
- Reduce complexity relentlessly. Prefer the simplest design that solves the real problem.
- Leave touched code cleaner than you found it, but keep cleanups scoped.
- Fix root causes instead of layering workarounds on top of symptoms.
- Do not add speculative flexibility or configuration that is not needed yet.

## Comments

- Explain yourself in code first.
- Add comments only when they clarify intent, non-obvious behavior, or important consequences.
- Do not add comments that restate the code.
- Delete commented-out code instead of leaving it behind.
- Avoid changelog-style comments about previous implementations.

## Source code structure

- Keep related code close together and separate unrelated concepts clearly.
- Declare variables near where they are used.
- Prefer a top-down reading flow: higher-level callers above lower-level helpers.
- Use whitespace to group related ideas.
- Keep formatting natural; do not hand-align code horizontally.

## Smells to avoid

- Rigidity: small changes causing widespread edits.
- Fragility: one change breaking unrelated behavior.
- Immobility: useful code being hard to reuse.
- Needless complexity, repetition, or opacity.

When a change introduces one of these smells, stop and refactor toward a simpler design.
