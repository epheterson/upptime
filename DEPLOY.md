# Deploying Upptime to Cloudflare Pages

Since this is a private repo, GitHub Pages won't work. Use Cloudflare Pages instead:

## Setup Steps

1. Go to Cloudflare Pages dashboard
2. Create new project → Connect to Git
3. Select the `epheterson/upptime` private repo
4. Build settings:
   - **Build command**: (leave empty - GitHub Actions builds it)
   - **Build output directory**: (leave empty - use root)
   - **Production branch**: `gh-pages`
5. Add custom domain: `health.zosia.io`
6. Done! GitHub Actions pushes to `gh-pages`, Cloudflare Pages deploys it

## How It Works

- GitHub Actions (workflows in `.github/workflows/`) monitor sites and build the status page
- Results pushed to `gh-pages` branch
- Cloudflare Pages deploys `gh-pages` branch to health.zosia.io
- Private repo stays private, status page is public
