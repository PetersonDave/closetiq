# ClosetIQ PWA

AI-powered outfit suggestions based on your wardrobe photos and real-time weather.

## What you get
- Upload clothes from your iPhone photo library
- Wardrobe persists across sessions via localStorage
- Real weather via Open-Meteo (free, no API key)
- AI outfit suggestions via Claude (your Anthropic API key)
- Installable as a home screen app on iPhone via Safari

---

## Deploy to GitHub Pages (free, ~5 minutes)

### 1. Create a GitHub account
If you don't have one: https://github.com/signup

### 2. Create a new repository
- Go to https://github.com/new
- Name it `closetiq` (or anything you like)
- Set to **Public**
- Click **Create repository**

### 3. Upload the files
- Click **uploading an existing file** on the repo page
- Drag and drop `index.html` and `manifest.json`
- Click **Commit changes**

### 4. Enable GitHub Pages
- Go to your repo → **Settings** → **Pages**
- Under Source, select **Deploy from a branch**
- Branch: `main`, folder: `/ (root)`
- Click **Save**

### 5. Your app is live
After ~60 seconds, your app will be at:
`https://YOUR-USERNAME.github.io/closetiq/`

---

## Install on iPhone

1. Open the URL in **Safari** (must be Safari, not Chrome)
2. Tap the **Share** icon (box with arrow)
3. Tap **Add to Home Screen**
4. Tap **Add**

The app icon appears on your home screen and opens full-screen with no browser chrome.

---

## API Key setup

On first launch, the app will prompt you for an Anthropic API key:

1. Go to https://console.anthropic.com/settings/keys
2. Click **Create Key**
3. Copy the key (starts with `sk-ant-`)
4. Paste it into the app and tap **Save**

The key is stored in localStorage on your device only — it's never sent anywhere except directly to `api.anthropic.com`.

---

## Storage notes

- All wardrobe photos are compressed to 480px / 72% JPEG quality before saving
- Typical storage: ~50–80 items before approaching browser limits (~5–10MB)
- If storage fills up, use **Clear all** and re-add your core pieces
- Data lives in your browser's localStorage — clearing Safari site data will erase it

---

## Files

| File | Purpose |
|------|---------|
| `index.html` | The entire app — HTML, CSS, JS in one file |
| `manifest.json` | PWA manifest for home screen install |
| `icon-192.png` | App icon (192×192) — add your own |
| `icon-512.png` | App icon (512×512) — add your own |

The app works without the icons — Safari will generate a screenshot-based icon automatically.
