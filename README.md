# Flow Trace launcher

Gives the Flow Trace Google Apps Script web app a proper **Home Screen icon and name** on iPhone (and Android).

Why this is needed: iOS takes the Home Screen icon from an `apple-touch-icon` tag on the **top-level** page. For an Apps Script web app that page is Google's `script.google.com` wrapper, which you can't edit, so iOS falls back to a screenshot. This small page carries your logo and forwards to the app.

## Files
| File | Purpose |
|---|---|
| `index.html` | Launcher page. Opened from the Home Screen it jumps straight to the app. |
| `apple-touch-icon.png` | 180×180 iPhone icon, made from the Flow Trace logo |
| `icon-192.png` | Android / manifest icon |
| `favicon-32.png` | Browser tab icon |
| `manifest.webmanifest` | Android "Install app" name and icons |

## Publish free with GitHub Pages (about 5 minutes)
1. Sign in at github.com → **New repository** → name it `flow-trace-app` → **Public** → Create.
2. **Add file → Upload files** → drag in all files from this folder → **Commit changes**.
3. **Settings → Pages** → Source: **Deploy from a branch** → Branch: `main`, folder `/ (root)` → **Save**.
4. After about a minute your launcher is live at `https://shadykhalil02-dev.github.io/flow-trace-app/`.

## Add to your iPhone
1. Open `https://shadykhalil02-dev.github.io/flow-trace-app/` in **Safari**. It must be Safari; iOS uses Safari's Add to Home Screen.
2. Tap **Share → Add to Home Screen → Add**. The Flow Trace logo appears as the icon.
3. Delete any old screenshot-icon shortcut you added before.

If you change your Apps Script deployment URL, edit `APP_URL` in `index.html`.
