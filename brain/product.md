# Product

A self-contained, classic **Connect 4** game, built as the Chess.com Product Engineering Internship take-home.

## The spec (`ChessCom_Product_Engineering_Internship_Take_Home_Assignment.pdf`)

- **Task:** build a self-contained classic game of our choice. Connect 4 is one of the listed examples.
- **Stack:** Docker + Kubernetes; MySQL or PostgreSQL; PHP, Go or Java; Vue or React with HTML and CSS. This project uses Go, React, PostgreSQL.
- **What they value:** "your best product, design and engineering capabilities", and "a working, well-built core game over covering every feature". Prioritize what matters most for the player and the codebase.
- **Time:** not expected to exceed about 4 hours. They want a rough time split by part (`brain/time-log.md`).
- **AI:** allowed; agent transcripts must be shared with the result.

## Deliverables

1. A link to a Git repository (public, or shared with them).
2. A README explaining how to run the project locally, **ideally with a single command**.
3. A short note on main decisions and trade-offs, and what we'd do next with more time (source: `brain/decisions.md`, `brain/action-items.md`).
4. The time breakdown (`brain/time-log.md`) and agent transcripts.

## Connect 4 rules

- Two players, red and yellow, take turns; red moves first (convention, see `brain/decisions.md` once settled).
- The board is **7 columns × 6 rows**, standing vertically. A move is choosing a column; the disc falls to the lowest empty cell.
- A full column can't be played.
- The first player with **four in a row** horizontally, vertically or diagonally wins.
- If all 42 cells fill with no four in a row, the game is a draw.

## Core experience (priority order)

1. Play a complete game correctly: legal moves, turn order, win and draw detection, highlighting the winning four.
2. A clear, polished board: whose turn it is, hover/preview of the drop column, drop feedback, a result state and a "new game" action.
3. Games persist in Postgres, so a reload doesn't lose a game in progress.
4. Anything beyond that (opponent modes, history, accounts) only after the above is solid; see `brain/action-items.md`.

## Non-goals (for now)

- accounts, auth, ratings or matchmaking
- variant rules (other board sizes, Pop Out, etc.)
- production hosting; the target is running locally

## Source-of-truth order for product questions

1. the spec PDF
2. explicit decisions in `brain/decisions.md`
3. existing code behavior
