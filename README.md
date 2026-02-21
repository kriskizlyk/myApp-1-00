# My Lists - Firebase Edition

A checklist app with real user accounts and cloud sync powered by Firebase.

## Features
- Email/password sign up & sign in
- Lists sync across all your devices
- Works offline (syncs when back online)
- Create, rename, delete lists
- Copy/move items between lists
- Duplicate lists, uncheck all
- Custom icons and colors per list
- Installable as PWA on iPhone/Android

## Deploy to GitHub Pages

1. Create a new repository on GitHub (e.g., `my-lists`)
2. Upload all files from this folder: `index.html`, `manifest.json`, `icon-192.png`, `icon-512.png`
3. Go to repository Settings → Pages
4. Set Source to "Deploy from a branch" and select `main`
5. Your app will be live at `https://yourusername.github.io/my-lists/`

## Firebase Setup (already done)
- Authentication: Email/Password enabled
- Firestore: Database created in test mode

## Important: Firestore Security Rules
Go to Firebase Console → Firestore → Rules and set:

```
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /users/{userId} {
      allow read, write: if request.auth != null && request.auth.uid == userId;
    }
  }
}
```

This ensures each user can only read/write their own data.

## Add to iPhone Home Screen
1. Open your site URL in Safari
2. Tap the Share button (box with arrow)
3. Tap "Add to Home Screen"
4. Tap "Add"
