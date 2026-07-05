# AGENTS.md — Programming Principles Skill

This repository contains an Agent Skills-format skill. To use it:

1. Clone or copy this repository into your agent's skills directory
2. Load the skill by name: `programming-principles`
3. The SKILL.md provides cross-cutting principles from 14 books
4. Load individual book rules from `references/{name}.mini.md` or `references/{name}.full.md`

## Quick Reference

`skill_view(name='programming-principles')` — load the core principles
`skill_view(name='programming-principles', file_path='references/clean-code.mini.md')` — load a specific book

## Structure

```
programming-principles/
├── SKILL.md                 # Core principles (load this first)
├── references/
│   ├── {book}.mini.md       # Per-book rule sets (14 files)
│   └── {book}.full.md       # Complete reference catalogs (14 files)
├── README.md
├── CONTRIBUTING.md
└── LICENSE
```
