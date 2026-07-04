# github-profile

# Personal Profile Site

A custom, full-HTML/CSS personal profile page — dark, techy, satellite/telemetry-inspired — meant to be hosted for free on GitHub Pages and linked from your GitHub profile README.

## Set it up

1. **Create a new repo** on GitHub, e.g. `profile-site` (any name works — it does NOT need to match your username).
2. Upload `index.html` to the root of that repo (drag-and-drop on github.com works fine, or via git):
   ```bash
   git init
   git add index.html
   git commit -m "Add profile site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/profile-site.git
   git push -u origin main
   ```
3. In the repo, go to **Settings → Pages**.
4. Under "Build and deployment", set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`. Save.
5. Wait ~1 minute. Your site goes live at:
   ```
   https://<your-username>.github.io/profile-site/
   ```
6. (Optional) Link it from your actual GitHub profile: create/edit the special `<your-username>/<your-username>` repo's `README.md` and add something like:
   ```
   🔗 [My profile site](https://<your-username>.github.io/profile-site/)
   ```

## Customize

Everything lives in one file, `index.html`, with all CSS inline in the `<style>` block at the top:

- **Colors** — edit the `:root` variables at the top of the `<style>` block (`--teal`, `--amber`, `--bg`, etc.)
- **Text** — name, role, base, focus tags, and mission cards are plain HTML further down — just edit the text directly.
- **Links** — update the `href` values in the "Ground Control" section at the bottom (GitHub, email, LinkedIn).
- **Missions** — duplicate a `.mission` block to add more projects.

No build step, no dependencies — it's a static file, so any edit just needs a `git push` to go live.
