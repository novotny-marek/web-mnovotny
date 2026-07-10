# Personal website (`web-mnovotny`)

This repository contains the source code for [mnovotny.net](https://mnovotny.net), a personal website built as a static site with [Hugo](https://gohugo.io/).

## What this repository is

- A Hugo-based personal site
- Content-focused project (Markdown content + Hugo configuration)
- Deployed to GitHub Pages via GitHub Actions

## Key technologies

- **Hugo** for static site generation
- **TOML** configuration (`/home/runner/work/web-mnovotny/web-mnovotny/hugo.toml`)
- **Markdown** content pages in `/home/runner/work/web-mnovotny/web-mnovotny/content`
- **Hugo Bear Blog** theme as a git submodule in `/home/runner/work/web-mnovotny/web-mnovotny/themes/hugo-bearblog`
- **GitHub Actions** workflow for build and deployment (`/home/runner/work/web-mnovotny/web-mnovotny/.github/workflows/hugo.yml`)

## Repository structure

- `/home/runner/work/web-mnovotny/web-mnovotny/hugo.toml` - main site configuration (base URL, theme, params, markup)
- `/home/runner/work/web-mnovotny/web-mnovotny/content` - site content
  - `_index.md` - homepage content
  - `publications/` - publication pages
  - `talks/` - talk/presentation pages
- `/home/runner/work/web-mnovotny/web-mnovotny/static` - static files served directly (for example `cv.pdf`)
- `/home/runner/work/web-mnovotny/web-mnovotny/images` - image assets used in content
- `/home/runner/work/web-mnovotny/web-mnovotny/themes/hugo-bearblog` - Bear Blog theme source (submodule)
- `/home/runner/work/web-mnovotny/web-mnovotny/.github/workflows/hugo.yml` - CI/CD workflow for Pages deployment
- `/home/runner/work/web-mnovotny/web-mnovotny/CNAME` - custom domain for GitHub Pages

## How content is organized

- Top-level pages are defined through folders in `content/`
- Each folder can have an `_index.md` list page
- Individual posts/pages are Markdown files with Hugo front matter (`+++ ... +++`)
- The homepage text and profile information live in `content/_index.md`

## Local development

1. Ensure Hugo Extended is installed.
2. Initialize submodules:

   ```bash
   git submodule update --init --recursive
   ```

3. Run local server from repository root:

   ```bash
   hugo server
   ```

4. Open the local URL shown by Hugo (typically `http://localhost:1313`).

## Deployment

- Pushes to `main` trigger `.github/workflows/hugo.yml`
- The workflow builds the site with Hugo and deploys it to GitHub Pages
- The site uses the custom domain from `CNAME`

## Acknowledgements

This website is based on [Hugo Bear Blog](https://github.com/janraasch/hugo-bearblog/).