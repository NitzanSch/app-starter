---
name: phase-2-live
description: Use after the app runs locally. Puts the app on the internet with Firebase, then adds data storage and login.
---

# Phase 2: on the internet

These steps assume Firebase. If the app uses something else, work toward the same goal for each step, using that platform's official docs.

## 2a. Connect Firebase

**Goal:** this folder is linked to a Firebase project the user owns.

1. Install the CLI: `npm.cmd install -g firebase-tools`. Run `add-dev-tools` again if the Firebase plugin isn't set up.
2. Ask if they have a Google account. If not, use `human-step/guides/google-account.md` first. Login needs a real terminal, so use `human-step/guides/firebase-login.md`.
3. Check it worked: `firebase.cmd projects:list`.
4. Create the project: `firebase.cmd projects:create <unique-id> --display-name "<App name>"`. If Firebase says terms must be accepted first, have them do it once at https://console.firebase.google.com with `human-step`.
5. Record the project ID in `memory/environment.md`, and create `.firebaserc` and `firebase.json`.

## 2b. First deploy

**Goal:** anyone can open the app at a public address.

1. Build it, then deploy with `firebase.cmd deploy --only hosting`. Use a manual deploy for now.
2. If auto mode blocks this, ask for approval as `AGENTS.md` describes, for example: "Yes, deploy this app to Firebase project my-app-123."
3. Give them the live address, and ask them to open it on their phone. A good moment to say: "This is now on the internet."
4. Record the address in `memory/environment.md`. Commit and push.

## 2c. Data and login

**Goal:** the app remembers things, and each person's data is safe. Do only what this app needs, in whatever order makes sense.

**Database (Firestore)**

1. Enable it with the CLI, or use `human-step` for the Firebase console if the CLI can't.
2. Write security rules from the start, so data is limited to who should see it. Never use open "test mode" rules.
3. Deploy the rules, and test that a stranger can't read private data.

**Login (Firebase Auth)**

1. Recommend Google sign-in, as it's the easiest for most users, and ask only if the audience suggests otherwise.
2. Turning on a sign-in method usually needs the console. Use `human-step`.
3. Have the user test logging in on the live site.

**Back end and paid services**

If the app must call a paid API, such as an AI model, never put the key in the browser code. That needs server code (Cloud Functions) and a billing account, so raise it as a **money** question first. Explain: what it might cost, that budget alerts warn but don't stop charges, and what the alternative is.

**File uploads**

Leave these until the app needs them. Check Google's current pricing page first, since storage may need a billing account.

## 2d. Check in

1. Deploy, then commit and push.
2. Show them what works now, in plain words.
3. Start `phase-3-grow`.
