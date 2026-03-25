# Tadoo — Personal To-Do App

A single-file, mobile-first personal task manager that runs entirely in your browser. No server, no accounts, no dependencies — just open the file and go.

## Features

- **Work / Life sections** — every task belongs to one section
- **Recurrence** — daily, weekly (pick specific days), monthly (pick specific dates), or yearly
- **Smart views** — Today, This Week, This Month, This Year, No Deadline
- **Archive** — completed recurring instances are preserved with a timestamp
- **Browser push notifications** — opt-in reminders for overdue and due-soon tasks
- **Persistent** — tasks are saved to `localStorage` and survive page refreshes
- **Dark mode, mobile-first** — designed for one-thumb phone use

---

## Deploying to GitHub Pages (step-by-step)

### Step 1 — Create a GitHub repository

1. Go to [github.com](https://github.com) and sign in (or create a free account).
2. Click the **+** icon in the top-right corner → **New repository**.
3. Name it something like `todolist` or `tadoo`.
4. Leave it **Public** (required for free GitHub Pages).
5. Click **Create repository**.

### Step 2 — Upload the file

**Option A — via the GitHub website (easiest)**

1. Inside your new repository, click **Add file → Upload files**.
2. Drag `index.html` onto the page (or click "choose your files" and select it).
3. At the bottom, click **Commit changes**.

**Option B — via Git on your computer**

```bash
# From the todolist folder:
git init
git add index.html
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
git push -u origin main
```

Replace `YOUR_USERNAME` and `YOUR_REPO_NAME` with your actual GitHub username and repository name.

### Step 3 — Enable GitHub Pages

1. In your repository, click **Settings** (top tab).
2. In the left sidebar, click **Pages**.
3. Under **Source**, select **Deploy from a branch**.
4. Set the branch to **main** and the folder to **/ (root)**.
5. Click **Save**.

### Step 4 — Visit your app

After 1–2 minutes, GitHub Pages will publish your app. Your URL will be:

```
https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/
```

GitHub shows this URL in **Settings → Pages** once it's live.

### Step 5 — Add it to your phone's home screen (optional but recommended)

**iPhone (Safari):**
1. Open the app URL in Safari.
2. Tap the **Share** button (box with arrow).
3. Scroll down and tap **Add to Home Screen**.
4. Tap **Add**.

**Android (Chrome):**
1. Open the app URL in Chrome.
2. Tap the three-dot menu → **Add to Home screen**.
3. Tap **Add**.

The app will open full-screen like a native app.

---

## Updating the app

Whenever you want to change something, edit `index.html` locally and then upload the new version to GitHub (either via the website "Upload files" button, or `git add index.html && git commit -m "Update" && git push`). GitHub Pages will update automatically within a minute or two.

---

## Notes

- **Data lives in your browser.** `localStorage` is per-browser, per-device. If you use the app on your phone and your laptop, each device has its own task list.
- **Notifications require HTTPS.** GitHub Pages serves over HTTPS, so push notifications work. They won't work if you open the file directly from disk (`file://`).
- **No tracking, no analytics, no external requests.** The entire app is self-contained in one HTML file.
