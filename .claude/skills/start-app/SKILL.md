---
name: start-app
description: Use at the start of a new app, when memory/progress.md says "not started". Interviews the user about what they want and picks the tech.
---

# Start a new app

## 1. Check the setup

Quietly record the operating system and language in `memory/environment.md`. Don't tell the user about setup details.

## 2. Explain the plan

Your first message after the language question explains the plan in everyday words, then asks if they're happy to start this way:

1. We talk about the app you want.
2. You see a first version on your computer.
3. We put it on the internet, so you can open it on your phone and share it.
4. We add what it needs, like saving information and logging in.
5. We keep improving it for as long as you like, a chat at a time.

Also explain that we'll start with a website that works on phones, not an App Store app, because it's much simpler and quicker. An App Store version can come later if they want one.

## 3. Interview

Have a friendly conversation, with one short question per message and no technical information. Start with what they want to build, then ask if they already have a name or would like help choosing one. Stop as soon as you know enough, usually 3 to 5 questions.

- What should the app do, and for whom?
- Walk me through what someone does when they first open it.
- What's the one thing it must do well in the first version?
- How should it feel? Do you have an example you like?
- Will people need to log in? Do they need to see each other's data?
- What language should the app's screens be in? If it's right-to-left, like Hebrew or Arabic, build the layout for that from the start.

If the idea is vague, suggest a concrete version and let them correct you. Save the answers to `memory/project-brief.md` in English, quoting their exact words where the wording matters.

## 4. Choose the tech

This is your call. The default is:

| Part | Default | Why |
|---|---|---|
| App | React with TypeScript, built with Vite | Common, well documented, no server to run |
| Hosting, database, login | Firebase Hosting, Firestore, Firebase Auth | One account, with a free plan to start |

Change it if the app needs something else, and research what's current. Look up the newest stable versions first. If they insist on an App Store app from the start, or the app needs something Firebase doesn't suit, that's fine: explain the extra cost and effort, and that the guided path is less tested for it.

Tell the user the result in plain words, in one or two sentences. Only ask if it affects taste or money. Record the choices and reasons in `memory/decisions.md`.

## 5. Plan

If they want help with a name, suggest a few. If they have no preference, pick a working name yourself and say it's easy to change later. Use lowercase letters and dashes for the GitHub name. The name on the app's screens can be different, in any language.

Split the first version into small steps, and write them under "Next" in `memory/progress.md`. Tell the user what they'll see first and roughly what you'll need from them, then start `phase-1-local`.
