# Landing-page hero images — for the landing-page session

Made 2026-10-31 by the Sessionify app session, at the owner's request, to replace the two images in
the landing page's hero (`assets/screenshots/web/ipad-01-timeline.jpg` and `iphone-01-timeline.jpg`).

## What to fix, and why

The hero's two pictures were **App Store screenshots**, not pictures of the app. Each carried its own
baked-in headline ("Every photo knows what was said"), subtitle and purple gradient panel. On the page
that meant:

- **Three headlines at once** — the page's own, plus one inside each picture.
- **Two "posters" on the page** — the iPad's lighter purple panel sat as a rectangle on the dark
  background, and the iPhone, with its own panel, was laid over its corner.
- **Unreadable text** — the captions inside the pictures shrank to a few pixels.
- **On a phone, worse** — scrolling down reached a poster card with a headline in it, and the
  "Sessionify · Get" bar along the bottom covered it.
- The old iPad image's status bar also still said "SessionFlow", the app's former name. (Since fixed: the old name has been removed from the iPad screenshots in `screenshots/`; their status bars show only the time and date.)

**The fix:** show the app itself, in device frames, with **no caption and no panel, on a transparent
background**, so the page's own dark gradient shows around the devices and the page headline does all
the talking — as Apple's own product pages do. That is what these files are.

## Files

All PNG with transparency (that is the point — do not convert to JPEG, which would put a solid
background back). Same moment in every one: 25:15–25:20 of the demo session "PHYS 341 · Laser Rate
Equations" — the whiteboard with its yellow box, red circle and "Threshold!", the transcript on
"characteristic temperature", the timeline under it. Status bar 9:41, full signal and battery.

| | light | dark |
|---|---|---|
| `web/` (use these) | `ipad-hero-light-web.png` 1200 w · `iphone-hero-light-web.png` 600 w · `mac-hero-light-web.png` 1600 w | the same names with `-dark` |
| `full/` | full resolution of each (for retina srcset or later crops) | |
| `raw-screenshots/` | the unframed simulator / Mac window captures | |

`preview-on-page-*.png` show all three on the page's background colour (#0A0D1F) — a check, not an asset.

## Recommendations

- **Dark mode is the better match** for the page's dark design (owner: "show the beauty of dark mode").
  Use the dark set in the hero; consider swapping to the light set under `prefers-color-scheme: light`
  if the page ever gets a light theme.
- **iPad + iPhone** for the hero, the iPhone overlapping the iPad's lower right, as before — but now
  with nothing behind them. The **Mac** image is for a Mac section or a three-device row; it is the app
  window (rounded corners, soft shadow), which is how Apple shows Mac apps.
- **Dark Mac window on a dark page:** its edge barely separates from the background. Add a faint
  outline or glow on the page side (e.g. a 1px rgba(255,255,255,0.08) ring or a soft light shadow).
- **Mobile:** stack the devices below the text, and keep the bottom "Get" bar from covering them.
- Keep the `alt` text describing the app, not the marketing line.

## Regenerating

The whole pipeline is in the app repo: `Tools/demo/` (README there). `hero.py` makes these from fresh
screenshots: `python3 hero.py <ipad|iphone|mac> <screenshot.png> <out-stem> [web-width]`.
