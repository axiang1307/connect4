# Action items

## Open questions

- [ ] **Opponent mode.** Local two-player on one screen (hot-seat), vs a computer opponent, or online two-player? Hot-seat is the smallest complete game; the others add a bot or real-time sync.
- [ ] **What Postgres stores.** At minimum the game in progress (so a reload resumes it); possibly the move list (enables replay/undo) and finished games (enables history). Decide before designing the schema.
- [ ] **Local Kubernetes cluster.** Docker Desktop's built-in Kubernetes, `kind`, or `minikube` (none set up yet, see `brain/dev-workflow.md`). Pick the one that makes the README's single command most reliable for a reviewer.
- [ ] **The single run command.** e.g. a `make up` / script that builds images and applies the manifests, possibly with a `docker compose` fallback. Decide once the cluster choice is made.
- [ ] **Frontend tooling.** e.g. Vite with TypeScript or JavaScript.

## Setup

- [ ] **`git init`** the repo, add a `.gitignore` (`node_modules/`, build output, `.DS_Store`), and create the remote (public or shared with Chess.com). `/update-brain`'s push-to-`main` flow needs both.

## Build (in priority order, see `brain/product.md`)

- [ ] Game rules in Go with unit tests (moves, turn order, win in all four directions, draw).
- [ ] HTTP API and Postgres persistence.
- [ ] React board UI.
- [ ] Dockerfiles and Kubernetes manifests; the single run command.

## Submission

- [ ] README: how to run locally (single command), decisions and trade-offs (`brain/decisions.md`), what's next, time breakdown (`brain/time-log.md`).
- [ ] Export the agent transcripts (location in `brain/dev-workflow.md`) and include them.
- [ ] Share the repository link.
