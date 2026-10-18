# Dr. Tariq Nawaz Clinic – setup (about 15 minutes, once)

## Part 1 – Put the app on GitHub (free hosting)
1. Sign in at github.com → **New repository** → name it `clinic`, set it to **Public** and create it.
2. **Add file → Upload files**: upload `index.html`, `sw.js`, `manifest.webmanifest`, `icon-180.png`, `icon-512.png`. Commit.
3. **Settings → Pages** → Source: *Deploy from a branch* → Branch `main`, folder `/ (root)` → Save.
4. After a minute your app is live at `https://YOUR-USERNAME.github.io/clinic/`.
5. On the iPhone open that link in **Safari** → Share → **Add to Home Screen**.

Note: the repository is public, but it only contains the app code. Your clinic data is never uploaded to GitHub; it stays on the phone and in your Google Drive.

## Part 2 – Automatic Google Drive backup
1. Go to script.google.com (signed in to the Google account whose Drive should hold the backups) → **New project**.
2. Delete the sample code, paste in everything from `Code.gs`.
3. Change `CHANGE-THIS-TO-A-LONG-RANDOM-SECRET` to your own long secret (keep a copy).
4. **Deploy → New deployment → type: Web app** → Execute as: **Me** → Who has access: **Anyone** → Deploy → approve the Google permission prompts → copy the **Web app URL**.
5. In the app: Home tab → **Google Drive backup** → paste the URL and the same secret. Tap **Back up now**.
6. A folder "Dr Tariq Nawaz Clinic Backups" appears in your Drive with `clinic-backup-latest.json` plus one dated copy per day.

## Moving your current data
In the old (Claude) version use Export ledger and Export stock, then Import both files in the new app.

## Limits to know
- Backups run while the app is open (iOS does not let any web app run when closed). They send a few seconds after each change, when internet returns, and when you reopen the app.
- Anyone with the backup URL and secret could write to your backup, so keep them private.
- If you change the app files later, re-upload them to GitHub; `sw.js` updates the phone automatically.

## New in this version
Charts, printable monthly report (Home → Settings → Print / save PDF), receiver breakdown, Urdu toggle, undo after delete, editing entries (✎), medicine expiry dates, and an app lock (PIN, optional Face ID).
After uploading the new files, close and reopen the app twice so the phone picks up the update. Stock spreadsheets now have an optional `exp` column.
