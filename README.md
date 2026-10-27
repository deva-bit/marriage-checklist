# Marriage checklist

A shared wedding budget checklist. You and your partner sign in and see the same list.
When one person ticks an item, the other person sees it straight away.

## Setup (about 15 minutes, one time only)

### 1. Create a Firebase project (free)
1. Go to https://console.firebase.google.com and sign in with Google.
2. Click **Create a project**. Name it `marriage-checklist`. You can turn off Google Analytics.

### 2. Turn on Google sign-in
1. In the left menu: **Security > Authentication > Get started**.
2. Choose **Google**, switch it on, pick your email as the support email, click **Save**.

### 3. Create the database
1. Left menu: **Build > Firestore Database > Create database**.
2. Pick a location close to you (for example `asia-southeast1` Singapore).
3. Choose **Start in production mode**.
4. Open the **Rules** tab. Paste everything from `firestore.rules` in this repo.
   Change the two emails to your real emails. Click **Publish**.

### 4. Get your settings
1. Click the gear icon > **Project settings**.
2. Under **Your apps**, click the **</>** (web) icon. Name it `checklist`. Do not tick Hosting.
3. Firebase shows a `firebaseConfig` block. Copy the values.
4. Open `index.html`, find `PASTE_HERE` near the top, and replace each one.
   (These settings are not secret. The rules in step 3 keep your list private.)

### 5. Put it online with GitHub Pages
1. Push the code to GitHub.
2. In your repo: **Settings > Pages**. Under **Branch**, pick `main` and `/ (root)`. Click **Save**.
3. After 1 to 2 minutes your site is at `https://deva-bit.github.io/marriage-checklist/`
4. Back in Firebase: **Authentication > Settings > Authorized domains > Add domain**,
   and add `deva-bit.github.io`.

### 6. First use
Open the site and sign in. Tap **Load the list from my diary** once. This adds all the items.
Your girlfriend signs in with her account and sees the same list.

Note: if your repo is private, GitHub Pages may need a paid plan. Making the repo public is fine:
your list data is in Firebase, not in the code.
