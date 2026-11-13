# Working in this repository

This is a public repository. `main` is the easily visible history, so it holds only clean, finished, almost-releasable work.

## Workflow: branches, pull requests, squash-merge

- Never commit work in progress to `main`, and never push drafts to it.
- Work on a branch named by kind and topic: `draft/<topic>` for lore and world drafts, `fix/<topic>` and `feat/<topic>` otherwise. Commit as messily as needed there.
- When a piece is ready, open a pull request as a draft. The owner marks it ready, reviews it and merges it with **Squash and merge**, so `main` gets one clean commit per finished piece. The repository uses the pull request's title and description as that commit, so write them as a release-quality summary of the piece, not of the steps, and update them when the piece changes.
- Assign every pull request you open to `hkarn`, so it shows up in the owner's GitHub views: `gh pr create --assignee hkarn`, or `gh pr edit <N> --add-assignee hkarn` for a pull request opened another way (a GitHub MCP tool, or a draft the environment opened).
- Review comments, from Copilot or a person: check each claim against the text first, fix what is real in a new commit, and reply on the thread with what you found and what changed (or why nothing did). Never resolve a conversation; the owner does.
- Never merge, approve or enable auto-merge on a pull request; the owner's merge is the approval.
- Sign everything you post on GitHub (pull request descriptions, issues, comments and review replies) with a last line `🤖 Generated with [Claude Code](https://claude.com/claude-code)`.
- Do not rewrite or force-push `main`. Branches may be rebased or force-pushed freely.
- Branches are public once pushed. Push a branch only when the user says so.
- Commit and push only when the user asks.
- Unpublished and draft work lives on its own branch, not on `main`, so before starting work, check the other branches (`git branch -a`, after a fetch) for anything related: a draft may exist only locally, never on the remote. Look at what a relevant branch holds (`git log main..<branch>`, `git show <branch>:<path>`) instead of assuming `main` is the whole picture. The author keeps the number of simultaneous branches small, so this stays cheap; if the branch list gets long, ask which ones matter rather than scanning them all.

## What belongs here

- This repository holds player handbooks for the universe and pure stories. A more specific adaptation, such as a role-play scenario, belongs in its own repository.
- Never reference private repositories, in tracked files, issues or pull requests. The README may name the adaptation planned as the first milestone, but not where it is built.
- Be mindful of which parts of a prose creative process suit a fully tracked git workflow, even when transparency is desired. Rough drafting, brainstorming and the back-and-forth of decisions are often better kept out of the public history; what lands in git is the finished piece.

## Local-only material: `scratchpad/`

`scratchpad/` is gitignored and exists only on the author's computer. Put there anything that should not be public or does not belong in the handbook:

- handoff documents and session notes
- material for an adaptation: its mechanics, rules, builds and tooling
- decision logs and source material for the work (for example the premise and the model draft it came from)

Never add it to git, and never reference it from tracked files. The final deliverable is a stand-alone player handbook for the universe.

## What this repository is

A readers' and players' lore handbook for *Beyond the Mountains*, and in time its stories. Planned layout: `lore/`, `maps/`, `stories/`. Content is CC BY 4.0 with stated exceptions and code is MIT; see `LICENSING.md`.

## The @claude workflow on GitHub

- A `@claude` mention in an issue runs `.github/workflows/claude.yml`, which is read-only. Only when running in that workflow (the prompt says you are helping with a GitHub issue, and Bash/Edit/Write are denied): review the issue against the content on `main`; if it's already done or no longer applies, say so and suggest closing it; otherwise reply with a concrete plan (files, steps, open questions). Don't try to change files or push there. Every other session, wherever it runs, works on issues as usual.
- Copilot reads `.github/copilot-instructions.md`, which points to this file; keep the rules here, not there.
