# Dev workflow

## Toolchain (on the developer's Mac, checked 2026-10-29)

| Tool | Version |
|---|---|
| Go | 1.26.3 (darwin/arm64) |
| Node | 22.20.0 (nvm) |
| Docker | 29.8.1 (Docker Desktop) |
| kubectl | 1.36.1 |

- **No local Kubernetes cluster is configured:** `kubectl config get-contexts` is empty, and neither `kind` nor `minikube` is installed. Choosing one is an open item in `brain/action-items.md`.
- Docker Desktop's built-in Kubernetes would add a `docker-desktop` context once enabled in its settings.

## Run

_(the single command from the README, and how to run each piece on its own for development)_

## Checks

_(what to run after changes: e.g. `go test ./...` and `go vet ./...` in `server/`, the frontend typecheck/lint/build)_

## Agent transcripts

Claude Code stores this project's session transcripts as `.jsonl` files in `~/.claude/projects/-Users-alexxiang-personal-projects-chesscom-take-home/`. They're a submission deliverable (`brain/product.md`).

## Gotchas

_(things that cost time; add as they come up)_
