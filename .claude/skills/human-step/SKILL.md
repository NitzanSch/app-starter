---
name: human-step
description: Use whenever the user must do something by hand, such as logging in, creating an account, clicking in a website, or entering payment details.
---

# Asking the user to do something

First check that you really can't do it yourself. Prefer command-line tools, so they only have to log in. Never ask for passwords, card numbers or API keys in chat.

Give one task at a time, in this format:

> **I need you to do something: [what, in a few words]**
>
> Why: [one sentence]
>
> 1. [Exact step, with the link and the button's name]
> 2. [Next step]
>
> You'll know it worked when [what they'll see]. Then tell me "done", or tell me what you see if it looks different.

Then:

- Check the result yourself where you can.
- If it didn't work, ask what's on the screen, or ask for a screenshot.
- Website layouts change. If the steps don't match, use the docs to find the current steps, and rewrite them for what the user sees.
- Note what happened in `memory/progress.md`.

## Guides

Ready-made steps are in `guides/`, written in English. Adapt them to their system, and present them in the user's language. Button names on websites may appear in English even if the rest is translated, so give the name as it appears on screen.

- `github-account.md`: create a GitHub account
- `google-account.md`: create a Google account
- `firebase-login.md`: log in to Firebase
- `billing.md`: add a billing account, only when needed
- `custom-domain.md`: buy and connect a web address
