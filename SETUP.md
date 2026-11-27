# Forest Study Room · Setup (one-time)

## A. Create a free Firebase project (~10 min)
1. Open https://console.firebase.google.com, sign in with a Google account → Add project (any name; Google Analytics can be off).
2. Build → **Firestore Database** → Create database → choose "Production mode" → pick a region near you.
3. Open the **Rules** tab of Firestore, paste the full contents of `firestore.rules`, and click Publish.
4. Build → **Authentication** → Get started → "Sign-in method" → enable both **Google** and **Email/Password** (Google needs a support email).
5. Project settings (gear icon, top left) → "Your apps" → click `</>` to add a web app → after registering, Firebase shows your `firebaseConfig`.
6. Open **`config.js`** in a text editor and replace the `const firebaseConfig=...` block with the one you copied. Save. (Don't touch config.js when you update index.html later.)

## B. Put the site online (~2 min)
1. Open https://app.netlify.com/drop and drag the whole `forest-study-room` folder in.
2. It gives you a URL — send it to your friends.

## How friends use it
Open the URL → sign in with Google (or register with email) → enter a nickname the first time → tap an empty seat to sit down. Signing in with the same account on any device brings your study records with you.

## Notes
- **Required:** Firebase → Authentication → Settings → Authorized domains: add the URL Netlify gave you (e.g. xxx.netlify.app), otherwise Google sign-in fails with "unauthorized domain".
- Google sign-in doesn't work in WeChat's built-in browser — use email, or open the page in a regular phone browser.
- Google and Firebase are usually blocked in mainland China without special network access, so friends there may not be able to open the site.
- "Only me" notes are only hidden in the page UI; task details are truly private (enforced by the rules).
- Firebase's free tier is plenty for a small study room.
