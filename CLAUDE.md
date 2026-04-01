# Slideshow application

The task is to create a simple slideshow app that can be deployed to a server or run in a browser locally.

## Essential features:
- Simple JS / flatfile implementation that requires no libraries
- Can work locally without internet connection
- Displays images fullscreen in browser window
- User-defined slide intervals (default 4s)
- Reads images from folders & subfolders, traversing through these alphanumerically
- Loops on completion of displayed images (configurable, default on)

## Additional features
- Random mode (overrides default file traversal, but must have a way to store which images have been shown to avoid repeats)
- Music played if found in /music dir
- UI to upload images / music
- Ability to add captions to images


## Implementation notes
- Single `index.html` file — all HTML, CSS, and JS inline, no dependencies
- Requires a static file server (locally: `python3 -m http.server 8000`, on server: Apache)
- Auto-discovers images by parsing directory listings from `slides/` recursively
- Filters to browser-supported formats (jpg, jpeg, png, gif, webp, bmp, svg) — skips CR2, HEIC, etc.
- Controls appear on mouse move, auto-hide after 3s
- Keyboard shortcuts: Space (play/pause), Left/Right arrows (prev/next), S (settings), Esc (close settings)
- Settings panel for interval and loop toggle

## How to run locally
```
cd /path/to/slideshow
python3 -m http.server 8000
# open http://localhost:8000
```

