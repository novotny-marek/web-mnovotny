# Personal website

This repository serves my [personal webpage](https://mnovotny.net).

## Hugo Setup

The website is built with Hugo static site generator using:
- **Theme**: [Hugo Bear Blog](https://github.com/janraasch/hugo-bearblog/) - Minimalist blogging theme
- **Configuration**: `hugo.toml` with optimized settings for performance and SEO
- **Content**: Publications, talks, and personal information
- **Deployment**: Automated via GitHub Actions to GitHub Pages

## Development

To run locally:
```bash
hugo server -D
```

To build for production:
```bash
hugo --gc --minify
```

## Content Management

- Use `hugo new publications/my-paper.md` to create new publications
- Use `hugo new talks/my-talk.md` to create new talks
- Content templates (archetypes) ensure consistent metadata structure

## Acknowledgements

This webpage is based on [Hugo Bear Blog](https://github.com/janraasch/hugo-bearblog/) template.