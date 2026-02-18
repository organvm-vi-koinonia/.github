# CLAUDE.md

## What This Is

Org-level infrastructure repo for [organvm-vi-koinonia](https://github.com/organvm-vi-koinonia). Contains the org profile README (what visitors see on the org page) and community health files. This is **not application code** — changes here affect the org-wide GitHub presence.

## Key Files

- `profile/README.md` — Renders on `github.com/organvm-vi-koinonia`. This is the public face of ORGAN-VI.
- `CODE_OF_CONDUCT.md`, `CONTRIBUTING.md`, `SECURITY.md` — Org-wide community health defaults (inherited by repos that lack their own)
- `organ-aesthetic.yaml` — Visual identity config for the organ
- `seed.yaml` — Orchestration metadata for the organvm system

## ORGAN-VI Context

ORGAN-VI (Koinonia / Community) has 5 sibling repos:

```
koinonia-db (shared DB layer — all others depend on this)
  ├── salon-archive (transcription, taxonomy, session archival)
  ├── reading-group-curriculum (multi-week reading programs)
  ├── adaptive-personal-syllabus (personalized learning paths — PROTOTYPE)
  └── community-hub (FastAPI web portal — FLAGSHIP, consumes all above)
```

Stack: Python 3.11+, SQLAlchemy 2.0+, PostgreSQL, FastAPI, Alembic.

## Editing Guidelines

- Profile README should stay in sync with actual repo count and implementation status
- Preserve the philosophical voice in Purpose and Philosophy sections — it's intentional
- System-wide stats (repo count, word count, essay count) come from `registry-v2.json` in the planning corpus
