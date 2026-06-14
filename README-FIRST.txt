Bags League 2026 — Shared Cloud Version

What this version does
- Runs from GitHub Pages on any phone browser.
- Saves scores and 4-baggers to Firebase Firestore.
- Everyone who opens the same GitHub Pages link sees the same shared standings.
- Also keeps a local browser backup on each phone.

Important
GitHub Pages hosts the app. Firebase Firestore stores the shared scores.
GitHub alone cannot sync scores between phones.

STEP 1 — Create Firebase project
1. Go to https://console.firebase.google.com/
2. Create a project named Bags League 2026.
3. Open Firestore Database.
4. Create database.
5. Start in test mode for easiest setup.
6. Choose a location and create it.

STEP 2 — Add a Firebase Web App
1. In Firebase Project Overview, click the Web icon: </>
2. App nickname: Bags League 2026
3. Register app.
4. Copy the firebaseConfig block.

STEP 3 — Paste Firebase config into index.html
1. Open index.html in GitHub or a text editor.
2. Find this section:
   const FIREBASE_CONFIG = {
      apiKey: "PASTE_YOUR_API_KEY_HERE",
      ...
   };
3. Replace the placeholder values with your real Firebase config.

STEP 4 — Firestore rules
For easiest setup, paste the contents of firestore-rules.txt into:
Firebase Console > Firestore Database > Rules > Publish

These rules are open for simplicity. That means anyone with your app link could change scores.
For league-only security, the next upgrade is adding a PIN or login.

STEP 5 — Publish on GitHub Pages
1. Create a GitHub repository, for example: bags-league-2026
2. Upload index.html, manifest.json, and firestore-rules.txt
3. Go to repository Settings > Pages
4. Under Build and deployment, set Source to Deploy from a branch
5. Choose main branch and /root folder
6. Save
7. Your app link will look like:
   https://YOUR-GITHUB-USERNAME.github.io/bags-league-2026/

STEP 6 — Add to iPhone Home Screen
1. Open the GitHub Pages link in Safari.
2. Tap Share.
3. Tap Add to Home Screen.
4. Name it Bags League.

STEP 7 — Add to Android Home Screen
1. Open the GitHub Pages link in Chrome.
2. Tap the three dots.
3. Tap Add to Home screen or Install app.

How to know it is working
- The app should show: Cloud sync connected / Cloud sync live.
- Enter a score on your phone.
- Open the same link on another phone.
- The score should appear there too.
