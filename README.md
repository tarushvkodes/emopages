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
- The app auto-selects a runtime profile (`high-performance`, `balanced`, `low-power`) to keep sustained performance stable.
- Multi-person groups are supported (multiple faces and hands in-frame are tracked at the same time).

## Performance behavior

- Adaptive camera resolution by device class
- Frame pacing to prevent thermal/CPU runaway
- Tuned face/hand detection intervals
- Detection caps to keep low-power hardware responsive

This is tuned to run well on:

- M4 iPad Pro
- M5 MacBook Pro
- Nvidia Jetson Nano (low-power profile)
- Windows 11 i9 + RTX 4060
