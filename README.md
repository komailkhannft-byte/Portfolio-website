# Komail Ahmad — Portfolio (Vercel)

Static one-page site. No build step, no dependencies.

## Deploy — Option A: Vercel CLI (fastest)

```bash
npm i -g vercel
cd komail-portfolio-vercel
vercel
```

Follow the prompts (link/create a project), then for production:

```bash
vercel --prod
```

## Deploy — Option B: GitHub + Vercel dashboard

```bash
cd komail-portfolio-vercel
git init
git add .
git commit -m "Initial portfolio"
git branch -M main
git remote add origin <your-empty-github-repo-url>
git push -u origin main
```

Then on vercel.com: **Add New Project → Import** your GitHub repo → Framework preset: **Other** → Deploy. No build command or output directory needed — `index.html` is served as-is.

## Project structure

```
komail-portfolio-vercel/
├── index.html      # the entire site (HTML + CSS + JS inline)
└── vercel.json     # static site config
```

## Custom domain

In the Vercel dashboard: **Project → Settings → Domains** → add your domain and point its DNS as instructed.

## Updating content

Everything — copy, colors, reviews — lives inside `index.html`:
- Reviews data: the `names` / `texts` arrays near the bottom (`<script>` section)
- Colors: CSS variables at the top of `<style>` (`--red`, `--black`, etc.)
- Your photo: replace the `.photo-frame` placeholder (`<span class="avatar-initials">KA</span>`) with an `<img src="your-photo.jpg">` tag, and add the image file alongside `index.html`
