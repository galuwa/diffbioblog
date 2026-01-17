# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static HTML blog for Diff Bio (blog.diff.bio) documenting robotics, software, and scientific work. Zero-build architecture - edit HTML/CSS/JS directly.

## Development

```bash
# Start local server at http://localhost:8080
bash host.sh
```

## Deployment

GitHub Pages deploys automatically on push to `master` branch.

## Architecture

- **Single-page site**: All content lives in `index.html`
- **No frameworks**: Vanilla HTML5, CSS3, JavaScript
- **Media assets**: Store in `/content/` directory

### Key Files

- `index.html` - Main page with all blog posts and JavaScript logic
- `style.css` - Terminal-style dark theme (VS Code inspired)
- `host.sh` - Development server script

### Design System

Terminal aesthetic with:
- JetBrains Mono / IBM Plex Mono fonts
- Colors: `--accent` (blue #569cd6), `--accent-2` (orange #ce9178), `--success` (teal #4ec9b0)
- Terminal window frame with title bar and traffic light buttons
- Cursor blink animation on main heading

### Post Structure

Each article is an `<article>` element containing:
- Metadata (date in brackets, tag pills)
- Title with `## ` prefix styling
- Expandable content sections (summary + "Read More")
- Images with alt text used as captions in lightbox

### JavaScript Features

- **Timeline scrubber**: Fixed position on right, draggable thumb, shows current date on hover
- **Lightbox**: Click images to open modal with prev/next navigation and captions from alt text
- **Post expand/collapse**: Summary view with thumbnails, full view on expand
- **Pinned posts**: Auto-populated from referenced posts in feed
