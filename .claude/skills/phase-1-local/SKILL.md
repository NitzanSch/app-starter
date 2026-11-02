---
name: phase-1-local
description: Use after start-app. Sets up the computer and the GitHub repo, then runs a first basic version of the app locally.
---

# Phase 1: running on their computer

## 1a. Set up

1. Check what's already installed. Install what's missing with `winget`, checking for the newest stable version first. Typically that's Git, GitHub CLI (`GitHub.cli`) and Node LTS (`OpenJS.NodeJS.LTS`).
2. Connect to GitHub, below.
3. Run `add-dev-tools` for the chosen stack.
4. Record tools and versions in `memory/environment.md`.

### Connect to GitHub

Skip anything already done.

1. Check login with `gh auth status`. If it's logged in, ask only whether that username is theirs. If it isn't logged in, ask if they have a GitHub account. If not, use `human-step/guides/github-account.md` first.
2. Run this in the background, with output sent to a file you can read:
   `gh auth login --hostname github.com --git-protocol https --web --scopes "repo,workflow"`
3. Read the file for the one-time code and link, then give both to the user with `human-step`. You'll be told when the command finishes. Check in if nothing has happened after a minute.
4. Run `gh auth setup-git`. If Git has no `user.name` or `user.email`, set them for this repo from their GitHub profile, using their GitHub noreply email.
5. Create the repo with the working name from `start-app`, and point this folder at it, unless `origin` is already theirs. If the name is taken, adjust it yourself. To rename later, use `gh repo rename`.
   ```
   gh repo create <app-name> --private
   git remote set-url origin https://github.com/<username>/<app-name>.git
   git push -u origin main
   ```
6. Rewrite `README.md` in the user's language so it's about their app: what it is, how to run it, and how to continue with an agent. Delete `README.he.md` if it's still there. The template's start prompt no longer applies.

## 1b. First version

1. Create the smallest app that shows something related to their idea. Scaffold in this folder with the current official tool, for example `npm.cmd create vite@latest`, keeping `AGENTS.md`, `memory/` and `.claude/`.
2. Start the dev server in the background, and check it responds.
3. Tell the user to open the exact address, such as `http://localhost:5173`, and ask if they can see it. Explain in one line that only their computer can see this for now.
4. Try to look at it yourself in a browser if a browser tool is available.
5. Ask one taste question if there's a clear one, then adjust.
6. Commit, push, update `memory/progress.md`, and start `phase-2-live`.
