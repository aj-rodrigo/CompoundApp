# Compound

A personal finance app for your iPhone Home Screen: investments, budget, take-home pay, net worth projections and debt planning. Everything runs on your phone. No account, no server, no tracking.

## Put it on your iPhone (about 5 minutes)

The app has to be hosted at a web address once so Safari can install it. GitHub Pages is free:

1. Create a free account at github.com, then create a new **public** repository (for example `compound`).
1. Click **Add file → Upload files** and upload all of these: `index.html`, `manifest.json`, `icon.png`, `icon-192.png`, `icon-512.png`.
1. Go to **Settings → Pages**, set Source to **Deploy from a branch**, pick `main` and `/ (root)`, and save.
1. After a minute your app is live at `https://YOUR-USERNAME.github.io/compound/`.
1. Open that address in **Safari** on your iPhone, tap **Share → Add to Home Screen**, then **Add**.

Netlify works too: drag the folder onto app.netlify.com/drop.

Your financial data is never uploaded. The hosted files are only the app itself; your numbers are saved inside Safari’s storage on your phone.

## Keep your data safe

- Data lives only on this phone. Use **Settings → Back up all data** regularly and keep the file in iCloud Drive or Files.
- To move to a new phone, install the app there and use **Restore from backup**.
- Deleting the Home Screen app, or clearing Safari website data, erases it.
- If you forget your passcode, you’ll need to erase the app’s data and restore a backup.

## Good to know

- **Passcode, not Face ID.** Home Screen web apps can’t use Face ID, so the app uses a 4-digit passcode (stored hashed) and locks after a minute in the background.
- **Alerts show inside the app.** Over-budget, stale balances, limit pace and upcoming bills appear on the Dashboard. iOS doesn’t allow true push notifications without a server.
- **Balances are manual.** Update them weekly (the app reminds you), or import a CSV from your bank’s website under Budget → Transactions.
- **Taxes are estimates.** Federal brackets, FICA and 2026 contribution limits (401(k) $24,500, IRA $7,500, HSA $4,400 / $8,750) are built in. State taxes use simplified brackets and exclude local taxes.
- Projections are simulations, not predictions. Nothing here is financial or tax advice.