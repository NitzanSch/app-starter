# Log in to Firebase

Why: Firebase is what puts the app on the internet, and it needs to know it's you. Login requires a real terminal window, so this is the one step you run yourself.

1. Press the **Windows key**, type `cmd`, and press **Enter**. A black window opens.
2. Type or paste this, and press **Enter**: `firebase login`
3. If it asks about sending usage info, type `n` and press **Enter**.
4. A browser window opens. Choose your Google account and click **Allow**.
5. Close the black window.

You'll know it worked when the browser says you're logged in.

## Notes for the agent

- If `firebase` isn't recognized, the window was opened before the install. Have them open a new one, or use `npx firebase-tools login`.
- Check with `firebase.cmd projects:list`.
- If the Firebase MCP server is connected, its login tool is an alternative that needs no terminal.
- On Mac, use the Terminal app instead of `cmd`.
