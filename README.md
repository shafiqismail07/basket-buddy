# Basket Buddy v4.0 — GitHub Pages PWA

## Upload to GitHub
Upload `index.html`, `manifest.webmanifest`, `sw.js` and the `icons` folder to the **root** of the repository. Preserve the folder names. Under Settings > Pages, deploy the `main` branch from `/(root)`.

## Firebase configuration
If your live `index.html` already contains a `BASKET_BUDDY_CONFIG` object, transfer that object into the new `index.html` before uploading, or use the app’s setup screen and re-upload the generated configured `index.html`. Do not replace the configured file blindly. The Firebase project and Firestore data are unchanged. Add your `YOUR-USERNAME.github.io` domain to Firebase Authentication > Settings > Authorized domains. Keep your secure Firestore rules.

## Install on iPhone
Open the GitHub Pages URL in Safari > Share > Add to Home Screen > Add. Repeat on the second iPhone.

## Functionality and limitations
The web app is installable with an icon, standalone appearance and basic cached app shell. The shell may load offline after an online visit; this does **not** promise complete offline shopping or cross-device sync without connection. Firebase Auth and hosted JS SDK require network in some cases. Existing Firebase catalogue/checklist functions remain. Reliable background push messages while the app is closed are **not** implemented. Browser notifications while the app is open are not background push.

For new releases, version the `CACHE_NAME` in `sw.js` (e.g. `basket-buddy-shell-v4-1`) to refresh cached assets. The service worker only caches first-party shell assets, not Firebase responses or user data.
