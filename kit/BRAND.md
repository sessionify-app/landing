# Brand

## Logo
A ribbon twisted into an "S", shaded like a real 3D helix.
- `assets/logo/sessionify-mark.svg` — the mark alone (use in nav, favicon, hero)
- `assets/logo/sessionify-mark.png` — raster of the mark
- `assets/logo/sessionify-icon.svg` — the mark on its rounded app-icon tile
- `assets/app-icon/` — 1024px iOS icon and 512px Mac icon
Give the mark clear space; don't recolour, stretch or add effects. It reads best on dark navy.

## Colours
| Role | Hex |
|---|---|
| Gradient start (teal) | #1FF0C8 |
| Gradient mid (blue) | #2E96FF |
| Gradient end (violet) | #A45BFF |
| Background dark (top) | #161B3A |
| Background dark (bottom) | #0A0D1F |
Suggested: dark navy hero with the teal→blue→violet gradient for accents and buttons; light sections in
near-white with navy text. Check contrast on text.

## Typography
No custom font is defined; the app uses Apple's system type. Use SF Pro where available, else the system
stack (`-apple-system, "SF Pro Text", Inter, system-ui, sans-serif`).

## Tone of voice
Calm, plain-spoken, practical; confident about privacy without hype or jargon. Short sentences, concrete
examples (whiteboard, handout, workshop).
- Say: meeting, session, recording, PDFs.
- Never say: "lecture" (the app is for any session), "slides" (PowerPoint/Keynote markup isn't supported yet).
- Don't claim AI summaries — there are none by design.

## The privacy promise (wording rule)
Make the promise about **content**, not about the company: "Your sessions never leave your device. We never see
your audio, photos, notes or transcripts." Do **not** write "no account", "no sign-up" or "no Sessionify server":
those are true today but would be false if a cross-platform subscription login is added later. If that happens, add:
"The only thing we store is your email and whether Pro is active."
