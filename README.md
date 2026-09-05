# Freehold by IAS (Income After Sports)

Design source for **Freehold** — the Phase 1 MVP iOS client app for IAS
(Income After Sport), the athlete-facing brand alongside AIL Properties.

This repository holds the Claude Design canvas and its supporting assets, not
application code. The canvas is the design of record; screens are laid out as
artboards on a single pan/zoom surface.

## Phase 1 scope

- Payment timeline notifications
- Portfolio transparency — properties, mortgages, rental income, net returns
- Projected returns dashboard

Target completion: end of 2026. Salesforce is the intended data source.
Stage 1 is to be tested with 5–10 trusted clients before wider rollout.

## Contents

| Path | What it is |
| --- | --- |
| `Freehold by IAS Client App.dc.html` | The design canvas — all artboards |
| `support.js` | Canvas runtime required to render the `.dc.html` |
| `ios-frame.jsx` | iOS device frame component used by the artboards |
| `.thumbnail` | Canvas preview image |
| `scraps/` | Exploration PNGs — onboarding, flows, fit studies, tab bar |
| `uploads/` | Brand assets: typefaces, app icon, brand guidelines, screenshots |

## Viewing the canvas

`Freehold by IAS Client App.dc.html` loads `./support.js` and the typefaces in
`uploads/` by relative path. Serve the folder over HTTP rather than opening the
file directly, so the font and asset requests resolve:

```
python3 -m http.server 8000
# then open http://localhost:8000/Freehold%20by%20IAS%20Client%20App.dc.html
```

## Brand

Dark forest ground (`#07100A`) with a mint accent (`#45FFAC`). Typefaces are
Bulevar (display) and Acumin Pro Wide (text). Full spec in
`uploads/IAS Brand Guidelines 2026.pdf`.

## A note on the typefaces

The canvas calls for Bulevar (display) and Acumin Pro Wide (text). Those font
files are **not committed** — this repository is public, and neither licence
permits redistributing the binaries. Drop them into `uploads/` from the team's
font source to render the canvas exactly; without them it falls back to Archivo.

`uploads/pasted-*.png` (Revolut Business screenshots from Mobbin) are likewise
not committed — third-party reference material, unused by the canvas.
