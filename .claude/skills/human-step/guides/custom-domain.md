# Buy and connect a web address

Why: this gives the app its own name, like `myapp.com`, instead of the free Firebase address.

1. Pick a name and buy it from a domain seller, such as Cloudflare, GoDaddy or Namecheap. Check the renewal price as well as the first-year price. Enter your card only on their site.
2. In https://console.firebase.google.com, open your project, then **Hosting**, then **Add custom domain**.
3. Enter your domain. Firebase shows some records to add.
4. Log in to where you bought the domain, find its **DNS** settings, and add those records exactly. If you'd like the agent's help, send a screenshot.
5. Wait. It can take from minutes to a day.

You'll know it worked when your address opens the app with a padlock in the browser.

## Notes for the agent

If the user wants DNS managed by Cloudflare, or the seller has an API or CLI login they're willing to use, do as much as you can yourself. Check the current Firebase docs, since these steps change.
