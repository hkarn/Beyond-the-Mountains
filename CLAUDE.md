# Working in this repository

This is a public repository. `main` is the easily visible history, so it holds only clean, finished, almost-releasable work.

## Workflow: branches, pull requests, squash-merge

- Never commit work in progress to `main`, and never push drafts to it.
- Work on a branch named by kind and topic: `draft/<topic>` for lore and world drafts, `fix/<topic>` and `feat/<topic>` otherwise. Commit as messily as needed there.
- When a piece is ready, open a pull request and merge it with **Squash and merge**, so `main` gets one clean commit per finished piece. Write that commit message as a release-quality summary of the piece, not of the steps.
- Do not rewrite or force-push `main`. Branches may be rebased or force-pushed freely.
- Branches are public once pushed. Push a branch only when the user says so.
- Commit and push only when the user asks.

## Local-only material: `scratchpad/`

`scratchpad/` is gitignored and exists only on the author's computer. Put there anything that should not be public or does not belong in the handbook:

- handoff documents and session notes
- anything about DreamGen mechanics, rules, tokens, builds, imports or the Studio workflow
- decision logs and source material for the work (for example the premise and the model draft it came from)

Never add it to git, never reference scratchpad or DreamGen-Studio from tracked files. Keep DreamGen references to a minimum. The final deliverable is a stand-alone player handbook for the universe.

## What this repository is

A readers' and players' lore handbook for *Beyond the Mountains*. The game build lives in the separate DreamGen Studio repository. Planned layout: `lore/`, `maps/`, `stories/`. Content is CC BY 4.0 with stated exceptions and code is MIT; see `LICENSING.md`.
