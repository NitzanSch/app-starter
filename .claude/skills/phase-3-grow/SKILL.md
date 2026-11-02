---
name: phase-3-grow
description: Use once the app is live. Makes it more useful, and adds automatic deploys, a test copy, basic tests, a custom domain and project-specific agent setup.
---

# Phase 3: growing

Run these side by side, in the order that helps most. Feature work comes first, and the rest fits around it.

## 3a. Make it more useful

Work from what the user asked for. Build in small pieces, show each, and adjust. Use subagents or parallel worktrees when work can be split.

## 3b. Automatic deploys and a test copy

**Goal:** saving work to GitHub updates the live app, and changes can be tried safely first.

1. Set up a GitHub Actions workflow that builds and deploys when `main` changes. Firebase's `firebase init hosting:github` can do this, and it needs a terminal, so use `human-step` if it asks questions you can't answer.
2. Add a test copy using Firebase Hosting preview channels, or a second Firebase project once the app has real users. Second project is the safer choice when real data is at stake.
3. Explain in plain words: "Now, when I save changes, the app updates itself."

## 3c. Basic tests

Add a small number of automated tests for what would hurt most if it broke, such as logging in and saving data. Run them in the automatic deploy, so a failure stops the deploy.

## 3d. Custom domain

Ask if they want their own web address now or later. If now, this is a **money** question: tell them the rough yearly cost, then use `human-step/guides/custom-domain.md`.

## 3e. Set up the agents

Look back at what this project keeps needing:

- Add project skills in `.claude/skills/` for repeated work.
- Add what you've learned about this app to `AGENTS.md`, keeping it short.
- Run `add-dev-tools` again if the stack changed.

Tell them in one line what you added.
