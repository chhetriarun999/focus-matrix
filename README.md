# Focus Matrix

A responsive, local-first Eisenhower Matrix productivity website optimized for iPhone 15 Pro and desktop. Runs as a static site on GitHub Pages: no server, build step, or API keys.

## Features
- Four editable quadrants (Do, Decide, Delegate, Delete)
- Add, edit, delete, move, and complete tasks
- HTML5 desktop drag-and-drop; touch drop for iPhone (touch a task, then release over another quadrant or completion area)
- Completed history and reopen
- Completion charts, seven-day bar chart, productivity summary
- Points, streaks, trophies, celebration and offline motivational messages
- Local 4-digit PIN with recovery question and separate master PIN
- Light/dark mode and JSON backups

## GitHub Pages publishing
1. Create a **public** repository named `focus-matrix` on GitHub.
2. Upload `index.html`, `style.css`, `app.js`, the `assets/` folder, and `README.md` to the **root** of the repository (or `git init`, `git add .`, `git commit -m "Initial Focus Matrix website"`, `git branch -M main`, `git remote add origin https://github.com/YOUR_USERNAME/focus-matrix.git`, `git push -u origin main`).
3. Open repository **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`, Save.
4. Your site will normally be available at `https://YOUR_USERNAME.github.io/focus-matrix/` when Pages finishes deploying.
5. On iPhone, open the site in Safari, then Share → Add to Home Screen.

## Important security/privacy notes
- This is a **static website** with data in `localStorage`. **A four-digit browser PIN does not encrypt task data and is not secure protection against device/browser access.** Do not store sensitive information in tasks.
- Your data does not sync between your iPhone and desktop. Each browser stores its own copy. Clearing site data or changing devices can erase tasks. Export backups regularly.
- The initial MVP uses a curated set of offline motivational messages, not downloaded internet quotes; it makes no API requests.
- Touch interactions, layout, and all behavior should be verified on a physical iPhone 15 Pro before daily reliance or production use.
- The recovery method is a convenience feature; its security is limited by the short PINs and browser-accessible stored verifiers.

## Development
Open `index.html` locally in a browser or serve from any static HTTP server such as `python -m http.server 8000`. `crypto.subtle` requires a secure context: GitHub Pages HTTPS or localhost work.

## Design refresh
The updated design uses a separate `style.css`, a pastel indigo/mint/coral palette, frosted glass effects, colorful illustrated SVG assets, and a mobile-optimized layout. All artwork ships in `assets/` and loads without external image requests. Email reminders are not included.

## Photos and licensing
The enhanced high-contrast design loads photographs from Unsplash over the internet; the app itself remains local-first. Please review the Unsplash license (https://unsplash.com/license). No Adobe Stock watermarked previews or unlicensed Adobe Stock assets were used. You can replace photo URLs with locally hosted licensed assets for offline imagery.
