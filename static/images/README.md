# Images Directory

This directory is for static images used by the website:

## Required Images for Hugo Bear Blog Theme

- `favicon.png` - Site favicon (minimum 32x32px, square PNG)
- `favicon.ico` - Alternative favicon format for broader browser support
- `share.png` - Social media preview image (used for Twitter Cards and Open Graph)

## Usage

To enable favicon and social media previews, add these files and uncomment the relevant lines in `hugo.toml`:

```toml
[params]
  favicon = "images/favicon.png"
  images = ["images/share.png"]
```

## Image Requirements

- **Favicon**: Square PNG/ICO, minimum 32x32px, recommended 192x192px for high-DPI displays
- **Social preview**: PNG/JPG, recommended 1200x630px (Open Graph standard)