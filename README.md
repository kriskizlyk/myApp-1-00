# My Lists App - Setup Guide

## How to Host This for Free on Your iPhone

### Option 1: Netlify Drop (Easiest — 2 minutes)

1. Go to **https://app.netlify.com/drop** on any computer or phone browser
2. You don't need an account to start (but create one to keep it permanently)
3. **Drag and drop** the entire `my-lists-app` folder onto the page
4. Netlify will give you a URL like `https://random-name.netlify.app`
5. Open that URL in **Safari** on your iPhone
6. Tap the **Share button** → **"Add to Home Screen"**
7. Name it "My Lists" → Tap **Add**
8. Done! You now have an app icon that opens full-screen

### Option 2: GitHub Pages (Free, permanent)

1. Create a free account at **https://github.com**
2. Create a new repository called `my-lists`
3. Upload all the files from the `my-lists-app` folder
4. Go to **Settings → Pages** and set Source to "main" branch
5. Your app will be live at `https://yourusername.github.io/my-lists/`
6. Open in Safari → Share → Add to Home Screen

## Files Included

- `index.html` — The full app (everything is in this one file)
- `manifest.json` — Makes it work as a PWA (Progressive Web App)
- `icon-192.png` — App icon (small)
- `icon-512.png` — App icon (large)

## Notes

- All your data is saved in your phone's browser storage (localStorage)
- No internet connection needed after the first load
- Works on any device with a modern browser
