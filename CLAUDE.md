# CLAUDE.md

This file provides guidance to Claude Code when working in this repository.

## Project: Compass Forge

**Description:** AI development platform - the core engine powering Compass Brand's intelligent tools.

**Project Type:** platform

---

## Components

| Component | Purpose |
|-----------|---------|
| `forge-rag/` | Custom RAG system with Ant Colony V2 architecture |
| `forge-providers/` | Multi-provider LLM abstraction (OpenAI, Anthropic, local) |
| `bmad-engine/` | BMAD methodology automation engine |

---

## Tech Stack

| Layer | Technology |
|-------|------------|
| Language | Python 3.11+ |
| Framework | FastAPI |
| Database | PostgreSQL + Memgraph |
| Embeddings | OpenAI / Local models |
| Observability | Langfuse |

---

## Development Methodology: TDD

All functional code MUST follow Test-Driven Development.

```
RED -> GREEN -> REFACTOR
```

---

## Git Discipline (MANDATORY)

**Commit early, commit often.**

- Commit after completing any file creation or modification
- Maximum 15-20 minutes between commits
- Use conventional commit format: `type: description`

Types: `feat`, `fix`, `refactor`, `docs`, `chore`, `test`
