# Lira & Dollar

A money tracker for USD and LBP that installs on an Android phone like a normal app. It works offline and keeps your data on the phone.

## What's in this folder

| File | What it does |
|---|---|
| `index.html` | The whole app (layout, styles and logic) |
| `manifest.webmanifest` | Tells Android the app's name, icon and colors, so it can be installed |
| `sw.js` | The service worker: saves the app on the phone so it opens without internet |
| `icons/` | App icons (normal and "maskable" for Android's round/squircle shapes) |

## Step 1: Put it online with GitHub Pages (free, about 10 minutes)

The app has to be served over HTTPS once so your phone can install it. GitHub Pages does that for free.

1. Go to **github.com** and sign in (create an account if you don't have one).
2. Click **+** (top right) → **New repository**.
   - Name: `lira-dollar`
   - Visibility: **Public** (GitHub Pages is free for public repositories)
   - Click **Create repository**.
3. On the new repository page, click **uploading an existing file**.
4. Unzip the folder on your laptop, open it, select **everything inside it** (`index.html`, `manifest.webmanifest`, `sw.js`, `README.md` and the `icons` folder) and drag it into the browser.
   - Upload the *contents*, not the outer folder. `index.html` must sit at the top level of the repository.
5. Click **Commit changes**.
6. Go to **Settings** → **Pages** (left menu).
   - Source: **Deploy from a branch**
   - Branch: **main**, folder **/ (root)** → **Save**.
7. Wait 1–2 minutes and refresh. GitHub shows your link:
   `https://YOUR-USERNAME.github.io/lira-dollar/`

Your entries never go to GitHub. GitHub only hosts the empty app; everything you type stays on your phone.

## Step 2: Install it on your Android phone

1. Open the link in **Chrome** on your phone.
2. Tap **Install app** at the bottom of the page, or Chrome's **⋮** menu → **Install app**.
3. Confirm. The app appears in your app drawer with its own icon.
4. Open it once while online. After that it works offline too.

## Step 3: Start using it

1. Tap the **Rate** button at the top and enter the rate you actually get (LBP for $1).
2. Log the cash you have now: **+ Add → Money in → Money I already have**, once in USD and once in LBP.
3. From then on, log every income, purchase and exchange.

## Protect your data

Your data lives only on this phone. If you clear Chrome's data, uninstall the app or lose the phone, it's gone unless you have a backup.

- Tap **Back up data** every week or two. A `.json` file goes to your Downloads.
- Send that file somewhere off the phone: Google Drive, or WhatsApp it to yourself.
- On a new phone: install the app, tap **Restore backup** and pick the file.
- The app reminds you if you haven't backed up in two weeks.

## Updating the app later

When you get a new version of `index.html` (or other files):

1. Open your repository on GitHub → **Add file** → **Upload files**, drop in the new files, and commit. Files with the same name are replaced.
2. Wait a minute, then open the app on your phone while online. It loads the new version automatically; close and reopen it once if you still see the old one.
3. Your entries are not touched by updates.

## Optional: run it on your laptop

From this folder, run `python -m http.server 8000` and open `http://localhost:8000`. Data saved there is separate from your phone.
