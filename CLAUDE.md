# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

A self-contained **Connect 4** game built for the Chess.com Product Engineering Internship take-home (`ChessCom_Product_Engineering_Internship_Take_Home_Assignment.pdf`, the source of truth for requirements).

Stack, fixed by the spec and the developer's choice:
- `frontend/`: React, with HTML and CSS
- `server/`: Go backend
- PostgreSQL database
- Docker and Kubernetes for infrastructure

## Goals

- **A working, well-built core game beats feature coverage.** The spec says so explicitly. Finish and polish the core loop before adding anything else.
- **Showcase product, design and engineering judgment.** The reviewers read the code, the README and the decisions note, so clarity matters as much as features.
- **The time budget is about 4 hours.** Prefer the simplest thing that works well; record cut scope in `brain/decisions.md` so it can go in the trade-offs note.

## Working norms

- **Build only when delegated.** The developer wants to take part in every building step. Propose and explain the next step, then wait. Write code, schema or infra changes only for a step the developer explicitly hands off, and stop when that step is done. Answering design questions is not a go-ahead to implement.
- Explain the reasoning behind a change (why this layer, the trade-offs, the standard convention), especially in `server/`.
- After changes, run the checks listed in `brain/dev-workflow.md`.
- Agent transcripts are a deliverable (see `brain/product.md`), so keep sessions focused and readable.

## The brain

`brain/` holds the project knowledge that persists across sessions. Read the relevant files before working in an area.

| File | Contents |
|---|---|
| `brain/product.md` | the take-home spec, Connect 4 rules, scope, non-goals, deliverables |
| `brain/architecture.md` | repo layout, how the pieces connect, build status |
| `brain/server.md` | Go server: layering, game logic, routes, error contract, database, env |
| `brain/frontend.md` | React app: screens, state and data flow, styling, env |
| `brain/dev-workflow.md` | toolchain, run (single command), checks, Docker / Kubernetes, gotchas |
| `brain/decisions.md` | settled decisions and their rationale (feeds the README's trade-offs note) |
| `brain/time-log.md` | time spent per part of the project (feeds the README's time breakdown) |
| `brain/action-items.md` | **the only place** for to-dos and open questions |

Rules:
- Info files state how things are; to-dos go only in `action-items.md`. Delete finished items, moving lasting knowledge to an info file.
- Update the describing file in the same change; record decisions in `decisions.md`.
- Each fact lives in one file. Edit in place; never append a contradiction.
- **Brain edits go only to `main`, never into a feature-branch commit.** Leave `brain/` and `CLAUDE.md` out of feature commits (e.g. `git add -A -- . ':!brain' ':!CLAUDE.md'`). `/update-brain` records the session's lasting knowledge and moves those edits to `main` from a worktree. A branch picks up newer brain content by merging `main`.

@brain/architecture.md
@brain/action-items.md
