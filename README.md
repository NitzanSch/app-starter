# App Starter

[עברית](README.he.md)

Build a real web app by describing what you want. You don't need to know how to code: Claude acts as your software engineer, and you make the decisions about what the app should be.

## Start here

**You need:** a paid Claude plan and the [Claude desktop app](https://claude.ai/download). This guide assumes Windows, and it works on a Mac too.

1. Open the Claude app, sign in, and click the **Code** tab.
2. Under the message box, make sure it's set to run on your computer (local).
3. Next to that, click the **folder** button and create a new, empty folder for your app, such as `C:\Users\YourName\Apps\my-app`. Each app gets its own folder. Avoid folders synced by OneDrive if you can.
4. Under the message box, click the mode button and choose **Auto**, so Claude doesn't stop to ask about every small step.
5. Under the message box, click the model button and choose **Opus**, in the newest version shown. It's a strong choice for building a whole app. If you reach your plan's usage limit, switch to **Sonnet**, which uses less.
6. Click the copy button on the box below, paste it into Claude, and press **Enter**.

```text
Set up a new app project in this folder from the template at https://github.com/NitzanSch/app-starter

Before anything else, ask me only this: English or עברית? From then on, talk to me in that language.

I'm not a developer, so use plain, non-technical words, keep messages short and ask one thing at a time. Don't report what you've done unless it matters to me. Assume I have no accounts and nothing installed. Never wait silently: if a step may show a Windows approval prompt, tell me first, because it can open behind this window.

After I answer, do these in order:

1. Check my operating system. If Git or GitHub CLI are missing, I approve installing them with winget. Run the installs in the background.
2. Clone the template directly into this folder, not into a subfolder.
3. Read AGENTS.md and follow it from now on. This session started before the files existed, so read skills directly from .claude/skills/<name>/SKILL.md.
4. Follow the start-app skill and interview me about my app.
5. Follow the phase-1-local skill. For GitHub, I approve creating a new private GitHub repository under my own account for this app, using a working name you choose, changing this folder's origin remote to that repository, and pushing this project to it. Never push to the template.
```

That's it. Claude takes it from here.

## What happens next

1. Claude asks which language you prefer, then gets the project ready. Windows may ask you to click **Yes** once or twice.
2. Claude asks about your app, and what you want it to do.
3. Claude sets up a safe online copy, then you see a first version on your own computer.
4. Claude puts it on the internet, and you open it on your phone.
5. Claude adds saved data and login if your app needs them, then asks what you'd like next.

## When Claude asks you something

Claude handles the technical decisions. It should only stop you for one of these, and say which:

- **Your taste:** how something should look or work
- **Money:** anything that could cost you
- **Something only you can do:** like logging in or creating an account
- **Risk to your computer:** it explains why, and asks first

You can always say "I'd rather do it differently", or ask "what does that mean?".

If Claude asks you to approve something and gives you an exact sentence to reply with, use that sentence. Claude's safety check needs to see you name the specific action.

## Coming back later

Open the **Code** tab, choose the same folder, make sure the mode is **Auto**, and say "let's continue". Everything Claude needs to remember is saved in the project itself.

## Good to know

- **Accounts:** you'll need free GitHub and Google accounts. Claude walks you through creating them or logging in.
- **Language:** write to Claude in your own language and it replies in that language. Its working files stay in English, and you never need to read them.
- **Cost:** Firebase, the hosting service, has a free plan that suits a small app. Claude asks before anything that could cost money.
- **Your code:** it's saved in your own private GitHub repository, and only you can see it.
- **Safety:** Auto mode has a safety check, but it isn't a guarantee. Claude can run commands on your computer without asking each time, so use this on a computer you're comfortable with and keep an eye on it.
- **Passwords:** never paste passwords, card numbers or secret keys into the chat. Claude will send you to the right website instead.

## What's in this project

| Part | Purpose |
|---|---|
| `README.md` | This guide, for people |
| `AGENTS.md` | The working rules, for the agent |
| `.claude/skills/` | Step-by-step instructions for each phase, for the agent |
| `memory/` | What the agent remembers about your app, saved with the project |

Once your app is set up, Claude replaces this README with one about your app.
