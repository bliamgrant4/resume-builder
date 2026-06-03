# CLAUDE.md — AI Agent Context

This file is read automatically by Claude Code on every session.
Follow everything here without being asked. When in doubt, consult PROCESS.md.

---

## What this project is

A lightweight personal tool for generating tailored resumes for specific job applications.
The master resume data lives in a local, gitignored file. The code reads that data,
accepts a job description as input, and produces a tailored resume as output.

**Personal data is never committed to this repo. Ever.**
The `data/` and `output/` folders are gitignored. Do not touch them with git.

---

## Process rules (mandatory)

The full development process is defined in `PROCESS.md` in this repo root. Read it.
The short version:

- Every piece of work maps to a Jira work item with a key like `RES-1`
- Branch naming: `RES-<n>-short-kebab-description`
- Commit messages: start with the key — `RES-1 description of change`
- PR title: must include the key — `RES-1 Short description`
- Never commit directly to `main` — all changes go through a PR
- One story = one branch = one PR. Do not bundle unrelated work.

---

## Repo structure

```
/
├── CLAUDE.md          ← this file
├── PROCESS.md         ← source of truth for the full dev workflow
├── .gitignore         ← data/ and output/ are excluded
├── data/              ← GITIGNORED — master resume YAML lives here
├── output/            ← GITIGNORED — generated resumes go here
└── src/               ← application code
```

---

## How to start a new piece of work

1. Confirm the Jira work item key with the user (e.g. RES-1)
2. Create the branch: `git checkout -b RES-1-short-description`
3. Implement against the acceptance criteria from the Jira story
4. Propose diffs for the user to review before committing anything
5. Commit with: `git commit -m "RES-1 description"`
6. Open a PR via gh CLI: `gh pr create --title "RES-1 Short description" --body "..."`
7. Wait for the user to review and merge — do not merge yourself

---

## What to do if something is unclear

Ask the user. Do not guess at requirements or invent scope.
Check PROCESS.md before asking — the answer may already be there.
