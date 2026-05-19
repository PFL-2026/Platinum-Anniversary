# The Platinum Anniversary 2028

A boys-trip cheat sheet comparing **Marbella** vs **Mykonos**. Built as a single HTML page that hosts cleanly on GitHub Pages.

---

## What's in this folder

```
platinum-anniversary-2028/
├── index.html          ← the whole page
├── README.md           ← this file
└── images/             ← 20 photos used by the page
```

**Don't rename `index.html`** — GitHub Pages serves whatever is called `index.html` by default. **Don't move the `images/` folder** — it must sit next to `index.html`. The HTML references images by relative path (`images/marbella-hero.jpg` etc.), so the folder structure must stay exactly as is.

---

## How to deploy on GitHub Pages (5 minutes)

### Option A — Web upload (easiest, no terminal needed)

1. **Go to** [github.com/new](https://github.com/new) and sign in.
2. **Create a new repository:**
   - Repository name: `platinum-anniversary-2028` (or anything you like)
   - Set it to **Public** (GitHub Pages free tier requires public repos)
   - ✅ Tick "**Add a README file**" — this lets GitHub initialise the repo so you can upload files into it.
   - Click **Create repository**.
3. **Upload the files:**
   - On the new repo's main page, click **Add file → Upload files**.
   - Drag the *contents* of this folder (the `index.html`, `README.md`, and the `images/` folder) into the upload zone. **Do not** drag the outer `platinum-anniversary-2028` folder itself — drag what's *inside* it. ⚠️ This is the most common mistake.
   - You should see `index.html`, `README.md`, and the `images/` folder listed.
   - Scroll down, type a commit message like "initial upload", click **Commit changes**.
4. **Enable GitHub Pages:**
   - Click the **Settings** tab (top right of the repo).
   - In the left sidebar, click **Pages**.
   - Under "Build and deployment", set **Source** to **Deploy from a branch**.
   - Under "Branch", choose **main** and **/ (root)**. Click **Save**.
5. **Wait ~1 minute**, then refresh the Pages settings screen. A green banner will appear at the top: **"Your site is live at https://<your-username>.github.io/platinum-anniversary-2028/"**. That's your shareable URL.

That's it. Send the link to the lads.

### Option B — Command line (if you prefer git)

```bash
# Unzip and cd into the folder
cd platinum-anniversary-2028

# Initialise git
git init
git add .
git commit -m "initial upload"

# Create an empty repo on github.com first, then:
git branch -M main
git remote add origin https://github.com/<your-username>/platinum-anniversary-2028.git
git push -u origin main
```

Then follow step 4 above to enable Pages.

---

## Testing it locally before uploading

Just **double-click `index.html`** — it'll open in your browser and everything should work (photos, navigation, voting). If photos don't show locally, check that the `images/` folder is in the same directory as `index.html`.

---

## Sharing the link

Once Pages is enabled, your URL will be:
**`https://<your-username>.github.io/platinum-anniversary-2028/`**

This works in WhatsApp, iMessage, email — anywhere. Mobile-friendly. No login required for viewers.

---

## Changing things later

**To swap a photo:** drop a new file with the same filename into the `images/` folder (via GitHub web UI: Add file → Upload files → drag new image with matching name → commit). Page updates within a minute.

**To edit text:** edit `index.html` directly on GitHub (click the file → pencil icon → make changes → Commit).

**Voting note:** votes are stored per-browser using `localStorage`. They are not synced between people. For a real shared poll, the lads would each see their own tally — fine for fun, but if you want a unified vote count you'd need a backend (out of scope for static hosting).

---

## Troubleshooting

- **"Site not found" after enabling Pages:** wait 2 more minutes, it can take a moment on first deploy.
- **Photos broken on the live site but work locally:** you uploaded the outer folder instead of its contents. Delete everything in the repo and re-upload the contents (not the folder itself).
- **Want a custom domain (e.g. `boystrip.com`):** GitHub Pages supports this — Settings → Pages → Custom domain. Beyond the scope of this README.
