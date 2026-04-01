# Slideshow

A simple, dependency-free slideshow app that runs in any browser. Just add images and serve.

## Quick start

```bash
# Add images to slides/ (subfolders supported)
python3 -m http.server 8000
# Open http://localhost:8000
```

## Features

- **Zero dependencies** — single HTML file, no build step
- **Auto-discovers images** from `slides/` folder and subfolders, sorted alphanumerically
- **Fullscreen display** with smooth fade transitions
- **Configurable interval** (default 4s) and loop toggle via settings panel
- **Keyboard shortcuts** — Space (play/pause), arrow keys (prev/next), S (settings)
- **Progress bar** — click to jump to any slide
- **Works anywhere** — locally with `python3 -m http.server`, or on any web server (Apache, Nginx, etc.)

## Supported formats

jpg, jpeg, png, gif, webp, bmp, svg

RAW formats (CR2) and HEIC are not supported by most browsers and will be skipped.

## Deployment

Copy `index.html` and your `slides/` folder to any static file server with directory listing enabled.

For Apache, directory listing (`mod_autoindex`) is typically enabled by default. For Nginx, add `autoindex on;` to your location block.
