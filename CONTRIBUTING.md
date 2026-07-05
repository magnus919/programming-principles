# Contributing to Programming Principles

## Scope

This repository contains an [Agent Skills](https://agentskills.io)-format skill. Contributions should improve the skill's guidance for coding agents.

## What to Add

- **New reference files** from additional software engineering books or authoritative sources
- **Improvements to cross-cutting principles** — principles that span multiple sources
- **New compatibility entries** — documented conflicts or overlaps between books
- **Bug fixes** — factual errors, unclear phrasing, broken links

## What Not to Add

- Book-specific content that duplicates an existing reference file without adding new coverage
- Marketing language or framework-specific advocacy
- Agent-specific tool instructions (keep it portable)

## Process

1. Open an issue describing what you want to change and why
2. Fork, make your changes, and open a pull request
3. Reference files from new books should follow the `mini`/`full` variant pattern
4. Update the compatibility table in SKILL.md if adding a new book

## Format

The skill follows the [Agent Skills specification](https://agentskills.io/specification.html). Reference files should be self-contained Markdown with clear section headers (When to use, Primary bias, Decision rules, Trigger rules, Final checklist).
