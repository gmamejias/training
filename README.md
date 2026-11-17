# Gladya Training: install guide

Standalone version of your training app. It runs without a Claude login, works offline after the first load, and saves your log on your phone.

## What's in the folder

| File | Purpose |
|---|---|
| `index.html` | The app |
| `manifest.webmanifest` | App name, icon and full-screen setting for the Home Screen |
| `sw.js` | Offline support (caches the app on your phone) |
| `icon-180.png`, `icon-192.png`, `icon-512.png` | Home Screen icon |
| `README.md` | This guide (not needed online) |

## 1. Put the app online (once, about 15 minutes, easiest on a laptop)

1. Create a free account at github.com.
2. Tap **+ → New repository**. Name it `training`, set it to **Public**, tick **Add a README file**, and create it.
   - Public only means the app's code is visible. Your log is never uploaded; it stays on your phone.
3. In the repository, tap **Add file → Upload files**. Upload `index.html`, `manifest.webmanifest`, `sw.js` and the three icon files. Tap **Commit changes**.
4. Go to **Settings → Pages**. Under *Branch*, choose **main** and **/(root)**, then **Save**.
5. Wait 1–2 minutes and refresh the page. Your app's address appears at the top, like `https://your-username.github.io/training/`.

## 2. Install it on your iPhone

1. Open that address in **Safari**.
2. Tap **Share → Add to Home Screen → Add**.
3. Open it once from the new icon while online, so it saves itself for offline use.
4. Test it: log a weigh-in, close the app fully, reopen it. The entry should still be there, also in airplane mode.

## 3. Move your existing log over

1. Open the old Claude version of the app and go to **Progress → Backup → Copy backup**.
2. Open the new app, go to **Progress → Backup**, paste into the box, and tap **Restore from pasted text** twice.

## Keeping your data safe

- Your log lives only on this phone. Deleting the Home Screen icon deletes the log.
- Every week, tap **Progress → Save backup file** and save it to Files or iCloud Drive.
- To restore on a new phone, install the app, then use **Load backup file** and tap **Restore** twice.

## Updating the app later

When the app changes, upload the new `index.html` to the same repository (Add file → Upload files, replacing the old one). Open the app while online and it picks up the new version. Your log is not affected.
