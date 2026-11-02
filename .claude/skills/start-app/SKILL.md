---
name: start-app
description: Use at the start of a new app, when memory/progress.md says "not started". Interviews the user about what they want and picks the tech.
---

# Start a new app

## 1. Check the setup

- Detect the operating system and record it in `memory/environment.md`.
- Confirm `origin` points to the user's own private repo, not the template. If it doesn't, follow "Connect to GitHub" in `phase-1-local`.

## 2. Interview

Have a friendly conversation, one question at a time. Stop as soon as you know enough, usually 3 to 5 questions.

- What should the app do, and for whom?
- Walk me through what someone does when they first open it.
- What's the one thing it must do well in the first version?
- How should it feel? Do you have an example you like?
- Will people need to log in? Do they need to see each other's data?
- What language should the app's screens be in? If it's right-to-left, like Hebrew or Arabic, build the layout for that from the start.

If the idea is vague, suggest a concrete version and let them correct you. Save the answers to `memory/project-brief.md` in English, quoting their exact words where the wording matters.

## 3. Choose the tech

This is your call. The default is:

| Part | Default | Why |
|---|---|---|
| App | React with TypeScript, built with Vite | Common, well documented, no server to run |
| Hosting, database, login | Firebase Hosting, Firestore, Firebase Auth | One account, with a free plan to start |

Change it if the app needs something else, and research what's current. Look up the newest stable versions first. Mobile apps, heavy back-end work and anything Firebase doesn't suit are fine if the user wants them: tell them the guided path is less tested for those, and explain what it means for them.

Tell the user the result in plain words, in one or two sentences. Only ask if it affects taste or money. Record the choices and reasons in `memory/decisions.md`.

## 4. Plan

Split the first version into small steps, and write them under "Next" in `memory/progress.md`. Tell the user what they'll see first and roughly what you'll need from them, then start `phase-1-local`.
