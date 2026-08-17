# Cuir Plus — Website

A single-page, static website for Cuir Plus (buying & selling agents for Pakistan's leather
tannery industry). No build step, no framework, no dependencies — just HTML, CSS and a
little vanilla JS, so it will run forever on any static host.

## Files

```
index.html      the whole page (About, Services, Mission/Vision, Contact)
styles.css      all styling
script.js       mobile menu, scroll reveal, footer year
assets/logo.png    Cuir Plus logo
assets/favicon.svg favicon
```

## Run it locally

Just open `index.html` in a browser — or, for a local server:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy on GitHub

1. Create a new repository on GitHub (e.g. `cuirplus-website`).
2. Push these files to the `main` branch:
   ```bash
   git init
   git add .
   git commit -m "Cuir Plus website"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-repo>.git
   git push -u origin main
   ```

### Option A — GitHub Pages (free, on github.io)
1. In the repo, go to **Settings → Pages**.
2. Under "Build and deployment", set **Source** to `Deploy from a branch`.
3. Pick **Branch: main**, folder **/ (root)**, then **Save**.
4. Your site will be live at `https://<your-username>.github.io/<your-repo>/` within a minute
   or two.

### Option B — Cloudflare Pages (free, faster global CDN, custom domain support)
1. Go to the [Cloudflare dashboard](https://dash.cloudflare.com/) → **Workers & Pages → Create → Pages → Connect to Git**.
2. Select the `cuirplus-website` repository.
3. Build settings: leave **Build command** empty and **Build output directory** as `/`
   (this is a static site — nothing to build).
4. Click **Save and Deploy**. Cloudflare will give you a `*.pages.dev` URL immediately.
5. To use your own domain (e.g. `cuirplus.com.pk`), go to the project's **Custom domains**
   tab and follow the prompts — Cloudflare will handle the DNS and free SSL certificate.

That's it — no ongoing maintenance, no server costs, and both platforms auto-redeploy the
site whenever you push a change to `main`.

## Editing content

All copy lives directly in `index.html`, in the section marked with an HTML comment
(`<!-- ============ SECTION NAME ============ -->`). Colors, fonts and spacing are all
defined as CSS variables at the top of `styles.css` under `:root`, so a rebrand only
touches a handful of lines.
