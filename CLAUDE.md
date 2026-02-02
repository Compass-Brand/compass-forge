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

## Component Architecture

### forge-rag (Custom RAG System)
- **Architecture:** Ant Colony V2 - distributed retrieval with swarm intelligence
- **Features:** Document ingestion, semantic chunking, hybrid search (BM25 + vector)
- **Storage:** PostgreSQL with pgvector, Memgraph for knowledge graphs
- **API:** FastAPI endpoints for ingestion, query, and management

### forge-providers (Multi-Provider LLM Abstraction)
- **Purpose:** Unified interface for multiple LLM providers
- **Supported Providers:** OpenAI, Anthropic, Azure OpenAI, local models (Ollama)
- **Features:** Provider failover, cost tracking, rate limiting, response caching
- **Configuration:** Environment-based provider selection with fallback chains

---

## Standards & Guidelines

This project follows Compass Brand standards:
- **Tech Stack:** See [Universal Tech Stack](../docs/technical_information/tech_stack.md)
- **Brand Guidelines:** See [Brand Guidelines](../docs/brand/brand-guidelines.md)

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
