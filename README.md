# Compound

A personal finance app for your iPhone Home Screen: investments, budget, take-home pay, net worth projections and debt planning. Everything runs on your phone. No account, no server, no tracking.

## Put it on your iPhone (about 5 minutes)

The app has to be hosted at a web address once so Safari can install it. GitHub Pages is free:

1. Create a free account at github.com, then create a new **public** repository (for example `compound`).
1. Click **Add file → Upload files** and upload all of these: `index.html`, `sw.js`, `manifest.json`, `icon.png`, `icon-192.png`, `icon-512.png`.
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

## Importing Amex and bank transactions

1. On americanexpress.com (use **Request Desktop Website** in Safari), open your activity list, choose a date range, tap **Download**, and pick **CSV**. Statement PDFs can’t be imported.
1. In Compound, go to **Budget → Transactions → Import CSV** and choose the file.

- Card payments (like MOBILE PAYMENT - THANK YOU) are recorded as transfers. They never count as income or spending.
- Refunds and credits reduce what’s been charged, in their category.
- The Transactions list shows a running total: “Charged so far” for all spending, or a running “Balance” when you tap a card’s name.
- Re-importing a file repairs entries an older version counted as income.
- Charges are sorted using the card’s own category column (Amex, Chase) and known merchants. Anything unmatched goes to **Needs a category**. When you pick a category there, future imports from that merchant use it.
- Importing the same file twice is safe; duplicates are skipped.

## Live prices

1. Create a free account at finnhub.io/register and copy your API key from the Finnhub dashboard.
1. In Compound, open **Settings → Live prices** and paste the key.
1. Prices then update when you open the app, or when you tap **Refresh** on the Invest tab.

- Use exact tickers (VTI, AAPL). In a Crypto account, use the coin symbol (BTC, ETH).
- Mutual funds and many 401(k) funds aren’t covered on the free plan. They keep the price you enter. Turn on **Set the price myself** for those holdings to skip them.
- The free plan allows 60 lookups a minute. Large portfolios update in batches.

## Good to know

- **Passcode, not Face ID.** Home Screen web apps can’t use Face ID, so the app uses a 4-digit passcode (stored hashed) and locks after a minute in the background.
- **Alerts show inside the app.** Over-budget, stale balances, limit pace and upcoming bills appear on the Dashboard. iOS doesn’t allow true push notifications without a server.
- **Stock prices can update live** with a free Finnhub key (see above). Cash balances and share counts are still entered by you, or imported from your bank’s CSV under Budget → Transactions.
- **Taxes are estimates.** Federal brackets, FICA and 2026 contribution limits (401(k) $24,500, IRA $7,500, HSA $4,400 / $8,750) are built in. State taxes use simplified brackets and exclude local taxes.
- Projections are simulations, not predictions. Nothing here is financial or tax advice.

## Updating the app

Upload the new `index.html` (and `sw.js` if it changed) to GitHub. The next time you open Compound, a blue **A new version is ready** banner appears. Tap **Update**. The app also works offline once it’s been opened with a connection.