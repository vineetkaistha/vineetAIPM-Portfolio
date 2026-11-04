# AI Product Management Portfolio

This repository is being prepared as an AI Product Management portfolio. It is
currently a collection of small browser-game projects and product documents,
not a completed portfolio website. The games do not use AI.

## Start here

- [`context.md`](./context.md) — portfolio goals, repository context, case-study
  guidance, and evidence boundaries.
- [`read.me`](./read.me) — portfolio setup guide and readiness checklist.

## Current projects

| Project | Description | Product brief |
| --- | --- | --- |
| Memory Game | Responsive card-matching game with grid sizes, scores, keyboard support, and light/dark themes. | [`PRD_dark_theme.md`](./PRD_dark_theme.md) |
| Snake | Standalone Snake game with keyboard and touch controls, pause/resume, scoring, and responsive layout. | [`PRD_snake.md`](./PRD_snake.md) |

Open [`memory-game.html`](./memory-game.html) or
[`snake-game.html`](./snake-game.html) directly in a modern browser to play.
Both games are built with HTML, CSS, and JavaScript and require no dependencies.

## Portfolio readiness

Before presenting this repository as a finished portfolio:

- Confirm target roles and add an owner-approved professional introduction.
- Select projects you are authorized to discuss and document your own
  contribution.
- Support outcome claims with verified evidence; do not invent metrics,
  research, or AI experience.
- Clearly label self-directed, hypothetical, prototype, and production work.
- Review privacy, accessibility, mobile usability, and links before publishing.

## Git and publishing

Git is already initialized on the `main` branch. The current `origin` points to
the existing Memory Game repository, so do not push portfolio changes there
unless that is the repository you intend to use.

When the portfolio is ready, create or select its GitHub repository, then set
and verify the matching remote before pushing:

```powershell
git remote set-url origin https://github.com/<account>/<portfolio-repository>.git
git remote -v
git status
git push -u origin main
```

The `.gitignore` excludes common local editor/OS files, build output, logs, and
local environment or credential files. Never commit passwords, tokens, private
keys, or real `.env` files.

## Privacy note

Current project files were reviewed for personal contact details and
credentials. Git commit history has separate author metadata; changing or
removing that metadata requires rewriting history and can affect the existing
remote. Keep the existing history unless you intentionally choose a clean
portfolio repository or approve a history rewrite.
