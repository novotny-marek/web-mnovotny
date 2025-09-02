# Personal Website

This repository serves my [personal webpage](https://mnovotny.net/).

## Tech Stack

- **Static Site Generator**: [Hugo](https://gohugo.io/) v0.131.0+
- **Theme**: [Hugo Bear Blog](https://github.com/janraasch/hugo-bearblog/) 
- **Hosting**: GitHub Pages

## Development Setup

### Prerequisites

- Hugo v0.131.0 or higher (Extended version recommended)
- Git

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/novotny-marek/web-mnovotny.git
   cd web-mnovotny
   ```

2. Initialize and update git submodules (for the theme):
   ```bash
   git submodule init
   git submodule update
   ```

3. Install Hugo (if not already installed):
   - **Debian/Ubuntu**: Download from [Hugo releases](https://github.com/gohugoio/hugo/releases)
   - **macOS**: `brew install hugo`
   - **Windows**: `choco install hugo-extended`

### Development Commands

- **Start development server**: `hugo server --buildDrafts`
- **Build for production**: `hugo --cleanDestinationDir`
- **Check Hugo version**: `hugo version`

### Project Structure

```
├── hugo.toml          # Hugo configuration
├── content/           # Markdown content files
│   ├── _index.md     # Homepage content
│   ├── publications/ # Academic publications
│   └── talks/        # Conference talks and presentations
├── static/           # Static assets (images, files)
├── themes/           # Hugo themes (git submodule)
└── public/           # Generated site (ignored in git)
```

### Adding Content

- **New page**: `hugo new my-page.md`
- **New publication**: `hugo new publications/my-publication.md`
- **New talk**: `hugo new talks/my-talk.md`

### Configuration

The site configuration is in `hugo.toml`. Key settings:
- SEO optimizations enabled (robots.txt, meta descriptions)
- Clean URLs with disabled taxonomies (following Bear Blog philosophy)
- Syntax highlighting configured for code blocks

### Theme Customization

The Hugo Bear Blog theme maintains the minimal, fast philosophy of the original Bear Blog. For customizations:
- Add custom CSS in `layouts/partials/custom_head.html`
- Override templates by copying from `themes/hugo-bearblog/layouts/` to `layouts/`

### Deployment

The site is automatically deployed to GitHub Pages via GitHub Actions when changes are pushed to the main branch.

## Acknowledgements

This webpage is based on [Hugo Bear Blog](https://github.com/janraasch/hugo-bearblog/) template by [Jan Raasch](https://www.janraasch.com), which is inspired by [Herman's Bear Blog](https://bearblog.dev/).