# Money Tracker

A lightweight, mobile-first personal finance tracker that runs entirely in your browser. No server, no account, no dependencies — just one HTML file.

## Features

- **Multiple accounts** — Chase Checking, Savings, Capital One, Cash (or any accounts you create)
- **Add transactions** — log income or expenses with amount, description, account, and date
- **Edit anything** — tap any past transaction to change its amount, type, description, or delete it; balances update automatically
- **Correct balance** — override any account's total directly without logging a transaction
- **Persistent storage** — all data is saved in your browser's `localStorage`
- **Backup & restore** — export everything as a JSON file and re-import it any time
- **PWA** — open it on your phone and tap "Add to Home Screen" to use it like a native app
- **Dark mode** — clean, distraction-free UI built for mobile thumb reach

## Live App

> `https://YOUR_USERNAME.github.io/money-tracker/`

## How to Use

### Adding a transaction
1. Select an account from the pill row at the top
2. Tap the **+ Add** tab
3. Choose Income or Expense, enter an amount, pick a date, and add a description
4. Tap **Add Transaction** — the balance updates instantly

### Editing or deleting a transaction
1. Tap the **Transactions** tab
2. Tap any transaction in the list
3. Modify any field in the slide-up sheet, then tap **Save** — or tap **Delete** to remove it

### Correcting a balance manually
- Tap **Correct Balance** on the main balance card to set any account's total directly
- Useful when you just want to sync the app with your real bank balance without logging individual transactions

### Managing accounts
- Tap **+ New** in the account pill row to add an account
- Tap ✏️ on the balance card to rename the current account
- Tap 🗑️ to delete the current account (and all its transactions)

### Backup & Restore
1. Go to the **Settings** tab
2. Tap **Export** to download a `money-tracker-YYYY-MM-DD.json` file — keep this somewhere safe
3. Tap **Import** and select your JSON file to restore all data

## Deploy to GitHub Pages (3 steps)

**1. Push to GitHub**
```bash
cd money-tracker
git init
git add index.html README.md
git commit -m "init"
git remote add origin https://github.com/YOUR_USERNAME/money-tracker.git
git push -u origin main
```

**2. Enable Pages**

In your GitHub repo: **Settings → Pages → Source: Deploy from a branch → Branch: `main` / `/ (root)` → Save**

**3. Install on your phone**

Wait ~60 seconds, then visit `https://YOUR_USERNAME.github.io/money-tracker/`.

- **iOS Safari:** Share → Add to Home Screen
- **Android Chrome:** tap the banner or Menu → Add to Home Screen

## File Structure

```
money-tracker/
└── index.html    # Entire app — HTML, CSS, and JS in one file
```

## Data & Privacy

All data lives in your browser's `localStorage` under the key `mt_data`. Nothing is ever sent to a server. Clearing your browser data will wipe the app — use the **Export** button regularly to keep a backup.
