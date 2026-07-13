# Aruamz Associates — Offline Static Site

This repository contains the static site for Aruamz Associates (local XAMPP copy).

Quick setup

1. Serve locally:

   ```bash
   # from project root
   python -m http.server 8080
   # then open http://localhost:8080/
   ```

2. GitHub (create repo and push):

   Option A (GitHub CLI installed):

   ```bash
   gh repo create <owner>/<repo-name> --public --source=. --remote=origin --push
   ```

   Option B (manual):

   - Create a new empty repo on GitHub
   - Then run:

   ```bash
   git remote add origin https://github.com/<username>/<repo>.git
   git push -u origin main
   ```

3. Deploy to Netlify:

   - Easiest: Log in to Netlify, choose "New site from Git", connect your GitHub repo and pick the `main` branch. No build command required for a static HTML site; set publish directory to `/` or leave empty.

   - CLI option:

   ```bash
   npm i -g netlify-cli
   netlify login
   netlify init   # follow prompts to link the site to Netlify
   netlify deploy --prod
   ```

If you want, I can push the initial commit for you after you provide the GitHub repo URL or run the `gh` command yourself.
