# Trip Site — Setup & Hosting Guide

This folder is a ready-to-publish website. `index.html` is the itinerary.
Follow the steps below once; after that you edit by talking to Claude Code.

---

## STEP 1 — Install Claude Code (one time)
You need a Claude Pro/Max plan (the same login you use for the Claude app).

**Mac (Terminal app):**
```
curl -fsSL https://claude.ai/install.sh | bash
```
**Windows (PowerShell):**
```
irm https://claude.ai/install.ps1 | iex
```
Then confirm:
```
claude --version
```
First run will prompt you to log in through your browser.

> Windows only: install Git for Windows first from https://git-scm.com if you
> don't have it.

---

## STEP 2 — Create the GitHub repo (one time)
1. Go to https://github.com/new
2. Repository name: `trip` (or anything)
3. Set it to **Public** (required for free GitHub Pages)
4. Do NOT add a README/gitignore (this folder already has them)
5. Click **Create repository**
6. Leave that page open — you'll need the URL it shows, like
   `https://github.com/YOURNAME/trip.git`

---

## STEP 3 — Let Claude Code do the rest
Open your terminal, move into this folder, and start Claude Code:
```
cd path/to/trip-site
claude
```
Then paste this to Claude Code:

> Initialize this folder as a git repo, commit everything, connect it to my GitHub
> repo at https://github.com/YOURNAME/trip.git, push to main, then tell me how to
> turn on GitHub Pages.

(Replace YOURNAME with your GitHub username.)

If you'd rather run it yourself, the commands are:
```
git init -b main
git add -A
git commit -m "Initial itinerary"
git remote add origin https://github.com/YOURNAME/trip.git
git push -u origin main
```

---

## STEP 4 — Turn on GitHub Pages (one time, in the browser)
1. On your repo page: **Settings** → **Pages**
2. Under "Build and deployment", Source = **Deploy from a branch**
3. Branch = **main**, folder = **/ (root)** → **Save**
4. Wait ~1 minute. Your live URL appears at the top of that Pages screen:
   `https://YOURNAME.github.io/trip/`
5. Text that link to Keren and bookmark it on both phones.

---

## FROM NOW ON — editing by talking to Claude
Any time you want a change, open the terminal:
```
cd path/to/trip-site
claude
```
Then just say what you want, e.g.:
- "Change Tuesday's hotel to Cable Mountain Lodge and add the confirmation number."
- "Push the latest changes live."

Claude Code edits `index.html` and pushes to GitHub; the live site updates in under a
minute. (You may need to hard-refresh your phone browser to see it.)

---

## OFFLINE BACKUP (recommended for the no-signal stretches)
Open the live link once on each phone, then use the browser's **Add to Home Screen**.
Because everything is in one file, it works with no signal — handy around Goldfield,
Tonopah, and the open Nevada highways.
