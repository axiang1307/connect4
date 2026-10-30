# Architecture

## Repo layout

Not a git repository yet (see `brain/action-items.md`).

| Path | What it is |
|---|---|
| `frontend/` | React app, HTML and CSS (`brain/frontend.md`). Empty so far |
| `server/` | Go backend: game rules, HTTP API, Postgres access (`brain/server.md`). Empty so far |
| `ChessCom_..._Assignment.pdf` | the take-home spec (`brain/product.md`) |
| `brain/` | persistent project knowledge |

Planned, not yet created: Docker images for `frontend/` and `server/`, Kubernetes manifests, a Postgres schema/migrations, and the single command that runs it all (`brain/dev-workflow.md`).

## How the pieces connect (target)

```
browser ──HTTP──▶ frontend (React, static build)
browser ──HTTP /api──▶ server (Go) ──SQL──▶ Postgres   game state
```

- The server is the authority on game rules: it validates every move and decides win/draw, so the client can't put a game in an illegal state.
- All three pieces run as containers, orchestrated by Kubernetes for local runs.

## Build status

| Part | Status |
|---|---|
| Game rules (Go) | not started |
| HTTP API | not started |
| Postgres schema | not started |
| React board UI | not started |
| Docker / Kubernetes | not started |
| README + decisions note | not started |
