# emopages

A GitHub Pages-compatible webcam demo that:

- Draws **tracked face bounding boxes**
- Shows face **age estimate** and **emotion**
- Draws **tracked hand bounding boxes**
- Shows **fingers held up** for each hand

## Run locally

Because webcam access requires a secure context, use either:

- GitHub Pages (`https://...github.io/...`), or
- localhost with a static server

Example:

```bash
python3 -m http.server 8080
```

Open `http://localhost:8080`.

## GitHub Pages

This repository uses a static `index.html`, so it can be served directly by GitHub Pages.

## Notes

- Camera permission is required.
- Performance depends on device/browser capabilities.
- On iPad/iOS Safari, tap **Start Camera** to begin.
