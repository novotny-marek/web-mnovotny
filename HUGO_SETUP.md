# Hugo Setup and Maintenance Guide

## Requirements

- **Hugo**: v0.131.0 or higher (Extended version)
- **Git**: For submodule management
- **Operating System**: Linux (Debian 13), macOS, or Windows

## Initial Setup

### 1. Install Hugo

#### Debian/Ubuntu Linux
```bash
# Download Hugo Extended v0.131.0
wget https://github.com/gohugoio/hugo/releases/download/v0.131.0/hugo_extended_0.131.0_linux-amd64.tar.gz
tar -xzf hugo_extended_0.131.0_linux-amd64.tar.gz
sudo mv hugo /usr/local/bin/
```

#### macOS
```bash
brew install hugo
```

#### Windows
```bash
choco install hugo-extended
```

### 2. Clone and Setup Repository

```bash
# Clone the repository
git clone https://github.com/novotny-marek/web-mnovotny.git
cd web-mnovotny

# IMPORTANT: Initialize submodules (Hugo Bear Blog theme)
git submodule init
git submodule update
```

## Development Workflow

### Local Development
```bash
# Start development server with live reload
hugo server --buildDrafts --bind 0.0.0.0

# The site will be available at http://localhost:1313
```

### Build for Production
```bash
# Clean build
hugo --cleanDestinationDir

# Output will be in ./public/ directory
```

## Content Management

### Adding New Content

#### New Publication
```bash
hugo new publications/my-new-paper.md
```

#### New Talk
```bash
hugo new talks/my-new-talk.md
```

#### New Page
```bash
hugo new my-new-page.md
```

### Content Structure

All content files use TOML front matter:
```toml
+++
title = 'Page Title'
date = '2025-01-01'
+++

# Your content here
```

## Theme Management

### Updating Hugo Bear Blog Theme
```bash
# Update theme to latest version
git submodule update --remote themes/hugo-bearblog
```

### Theme Customization

1. **Custom CSS**: Create `layouts/partials/custom_head.html`
2. **Template Overrides**: Copy from `themes/hugo-bearblog/layouts/` to `layouts/`

## Configuration Details

The `hugo.toml` configuration includes:

- **SEO optimizations**: robots.txt, meta descriptions
- **Clean URLs**: Disabled taxonomies for Bear Blog-style simplicity
- **Syntax highlighting**: Friendly style with line numbers
- **Social media**: Open Graph and Twitter Card support (when images added)

## Troubleshooting

### Common Issues

1. **Empty theme directory**: Run `git submodule init && git submodule update`
2. **Hugo not found**: Ensure Hugo is in your PATH
3. **Build errors**: Check Hugo version compatibility (v0.131.0+)

### Build Output Issues

The following directories are auto-generated and should not be committed:
- `public/` - Hugo build output
- `.hugo_build.lock` - Hugo build lock file
- `resources/_gen/` - Generated resources

These are excluded via `.gitignore`.

## Performance Tips

1. Use `hugo --minify` for production builds
2. Optimize images before adding to `static/images/`
3. Keep content files under 100KB for best performance
4. Use Hugo's built-in image processing for responsive images

## Security

- Never commit sensitive data to the repository
- Use environment variables for sensitive configuration
- Keep Hugo and theme updated for security patches