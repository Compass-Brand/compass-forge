# Planning

This folder is the live BMAD planning surface for `compass-forge`.

The old backlog, sprint, epic, and spike layout is being retired. The active planning model now uses:

- `planning/roadmap/`
- `planning/current/`
- `planning/previous/`
- `planning/lessons/`

Because `compass-forge` orchestrates child repos, it also maintains:

- `planning/repositories.yaml`
- `planning/current/initiative-index.yaml`
- `planning/current/initiatives/`

## Structure

```text
planning/
├── README.md
├── repositories.yaml
├── roadmap/
├── current/
│   ├── phase.md
│   ├── phase-state.yaml
│   ├── initiative-index.yaml
│   └── initiatives/
├── previous/
├── lessons/
└── decisions/
```

## Operating Model

- `compass-forge` owns domain-level roadmap and initiative routing for its child repos.
- Repo-local delivery work still happens in the authoritative child repo root, such as `compass-engine`, `forge-rag`, or `forge-providers`.
- `roadmap.yaml` is authoritative over `roadmap.md`.
- `phase-state.yaml` is authoritative over `phase.md`.
- `initiative-index.yaml` is authoritative for concurrent initiative routing and overlap gates.

## Legacy Content

Older `planning/backlog/`, `planning/sprints/`, `planning/epics/`, and `planning/spikes/` lanes may remain temporarily during migration, but they are no longer the active standard.

## Related

- [Workspace Planning](../../planning/README.md)
- [ADR-0002: BMAD Polyrepo Planning And Repo-Root Authority](../../planning/decisions/adr-0002-bmad-polyrepo-planning.md)
