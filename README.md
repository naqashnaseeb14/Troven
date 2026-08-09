# TROVEN — one page site

Static site, no build step. Two files that matter:

```
index.html
assets/troven-mark-transparent.png
```

## Go live on GitHub Pages

**1. Create the repository**
- Go to github.com, click **New repository**.
- Name it anything, for example `troven-site`.
- Keep it **Public** (Pages needs a public repo unless you're on a paid plan).
- Do not add a README, .gitignore, or license from GitHub's side, you already have the files.

**2. Push these files to it**

From inside this folder, run:

```bash
git init
git add .
git commit -m "TROVEN site"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/troven-site.git
git push -u origin main
```

Replace `YOUR-USERNAME` and the repo name with your own.

**3. Turn on Pages**
- In the repo, go to **Settings → Pages**.
- Under **Build and deployment**, set **Source** to `Deploy from a branch`.
- Set **Branch** to `main` and folder to `/ (root)`.
- Click **Save**.

**4. Wait about a minute, then visit**

```
https://YOUR-USERNAME.github.io/troven-site/
```

GitHub shows the exact URL at the top of the Pages settings page once it's live.

## Updating the site later

Edit `index.html` (and `assets/` if you swap the logo), then:

```bash
git add .
git commit -m "update copy"
git push
```

Pages redeploys automatically within a minute or two of every push.

## Custom domain (optional, once you're off GitHub Pages as "temporary")

If you point a real domain at this later:
1. Add a file named `CNAME` (no extension) at the root, containing just your domain, e.g. `troven.co`.
2. In your domain's DNS, add a CNAME record pointing to `YOUR-USERNAME.github.io`.
3. Re-check **Settings → Pages**, GitHub will confirm the custom domain and offer to enforce HTTPS. Turn that on.

## Notes
- All copy avoids em dashes and filler/agency jargon on purpose, keep new copy in that voice.
- Colors, type (Bebas Neue + Inter + JetBrains Mono), and the teal signal accent follow TROVEN's brand kit, don't introduce new colors.
- Fonts load from Google Fonts CDN, requires internet access to render correctly, which GitHub Pages visitors will have.
