---
name: phase-3-grow
description: Use once the app is live, including in any later chat. Open-ended work on the app's features, plus automatic deploys, a test copy, basic tests, a custom domain and project-specific agent setup.
---

# Phase 3: growing

This phase has no end, and it doesn't need to be finished in order. Feature work comes first, and the rest fits around it. Add 3b to 3e to `memory/todo.md` and bring each up when the time is right.

## Moving to separate chats

When the app first goes live, explain: "The basics are done. From here the app can keep growing for as long as you like, so it works best to start a new chat for each thing you want to work on. Everything is saved, so a new chat knows where we are. Open a new chat in this same folder, with the mode on Auto, and tell me what you'd like."

Suggest a new chat again when a topic is finished or a chat gets long. Update `memory/` first.

## 3a. Make it more useful

Get to know the app in more depth. Ask about the people using it and what they do, one question at a time. Save this as user stories in `memory/stories.md`, and show them in plain words when it helps.

Then take what they ask for, in any order. Build in small pieces, show each, and adjust. Use subagents or parallel worktrees when work can be split.

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
