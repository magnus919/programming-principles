# Programming Principles — Agent Skill

An [Agent Skills](https://agentskills.io)-format skill containing synthesized programming principles from 14 classic software engineering books. Use with any standards-compatible agent — Codex, Claude Code, Cursor, Hermes Agent, OpenCode, and others.

## What This Is

One skill, two layers of depth:

- **SKILL.md** — Cross-cutting principles synthesized from all 14 books, organized by coding concern (naming, functions, architecture, data, testing, error handling, refactoring). Plus a task-to-book mapping table, per-book compressed rule cards, and a compatibility guide for combining books.
- **`references/*.mini.md`** (14 files) — Each book's individual mini rule set with triggers, decision rules, and final checklists. Load on demand when a specific book's guidance is needed.
- **`references/*.full.md`** (14 files) — The complete rule catalog for each book (11–63 KB each). Load only for deep reference or audits.

The progressive disclosure pattern is built in: the SKILL.md contains enough to change decisions. Reference files provide depth when a task demands it.

## Books Covered

| Book | Author | Focus |
|------|--------|-------|
| A Philosophy of Software Design | John Ousterhout | Deep modules, complexity, information hiding |
| Clean Architecture | Robert C. Martin | Boundaries, dependency rule, replaceable details |
| Clean Code | Robert C. Martin | Readability, naming, small functions |
| Code Complete | Steve McConnell | Construction discipline, defect prevention |
| Designing Data-Intensive Applications | Martin Kleppmann | Consistency, replication, events, streams |
| Domain-Driven Design | Eric Evans | Ubiquitous language, bounded contexts |
| Domain-Driven Design Distilled | Vaughn Vernon | Lightweight DDD introduction |
| Implementing Domain-Driven Design | Vaughn Vernon | Tactical patterns, aggregates, events |
| Patterns of Enterprise Application Architecture | Martin Fowler | Layers, repositories, enterprise patterns |
| Refactoring | Martin Fowler | Behavior-preserving improvement, code smells |
| Refactoring.Guru | Refactoring.Guru community | Smell catalog, technique catalog |
| Release It! | Michael T. Nygard | Production reliability, stability patterns |
| The Pragmatic Programmer | Hunt & Thomas | Craftsmanship, automation, feedback loops |
| Working Effectively with Legacy Code | Michael Feathers | Seams, characterization tests, safe change |

## Usage

### Load the skill

Place this directory in your agent's skills path. For example:

**Hermes Agent / Codex / OpenCode:**
```
~/.hermes/skills/programming-principles/
~/.agents/skills/programming-principles/
```

**Claude Code:**
```
.claude/skills/programming-principles/
```

**Cursor:**
```
.cursor/rules/
```

### Invoke the skill

Tell your agent: "Load the programming-principles skill" or reference it by name. The agent reads SKILL.md for the core principles and loads reference files on demand.

### Load a specific book's rules

```
Load references/clean-code.mini.md from the programming-principles skill.
```

For deeper coverage:

```
Load references/clean-code.full.md from the programming-principles skill.
```

## Compatibility

Books marked ❌ should not be loaded as equal guidance:

- **Domain-Driven Design** ❌ **Patterns of Enterprise Application Architecture** — different data ownership paradigms
- **Implementing DDD** ❌ **PoEAA** — same conflict at implementation level

Books marked 🔁 overlap in coverage; choose one:

- **Clean Code** 🔁 **Pragmatic Programmer**, **Code Complete**, **A Philosophy of Software Design**
- **DDD** 🔁 **DDD Distilled**, **Implementing DDD**
- **Clean Architecture** 🔁 **Implementing DDD**, **PoEAA**
- **Refactoring** 🔁 **Refactoring.Guru**

All other pairs are complementary. Default to one primary always-on book and load others on demand per task.

## Upstream Source

This skill was inspired by and draws its first-wave reference files from [mattpocock/agent-rules-books](https://github.com/mattpocock/agent-rules-books) — a collection of pre-made AGENTS.md rule sets derived from classic programming books. That repo is the creative inspiration for this format and remains the upstream source for the 14 book rule sets bundled here as reference files.

The reference files are expected to grow: future additions may include rule sets from additional books, incident-derived patterns, and project-specific conventions.

The **SKILL.md synthesis** — the cross-cutting principles, per-book compressed cards, task-to-book mapping, and compatibility guide — is original to this repository.

## License

MIT — see [LICENSE](./LICENSE).
