# bokêh

A wardrobe app and the landing page that sells it. One product, two surfaces, one design system.

- `index.html` — the landing page (dark, floating pill nav, hero mosaic, partner strip, workflow bento, gallery, testimonial carousel, community CTA, footer monument wordmark).
- `app/index.html` — the app itself: feed, search, wardrobe, profile, post detail, piece detail, and the sheets.

Both files are self-contained. No build step, no dependencies, no network calls: fonts, icons and imagery are embedded. Open `index.html` in a browser and everything works, including the link through to the app.

## Run it

```
open index.html
```

Or serve the folder:

```
python3 -m http.server 8000
```

## Design system (app)

| Token | Value |
| --- | --- |
| Background | `#f4f4f1` |
| Surface | `#ffffff` |
| Sunken | `#ececea` |
| Hairline | `#e3e3de` |
| Ink | `#111110` / `#4a4a47` / `#6b6b68` |
| Accent | `#b4972c` |
| Type | DM Sans, steps 34 / 26 / 15 / 13 / 12 |
| Radii | 10 / 16 / 24 / 99 |

The landing page runs its own darker palette from the same language: flat ink surfaces, one yellow accent, no shadows and no gradients used decoratively.

## Motion

- Micro interactions 120–180ms, state changes 180–260ms, entrances 220ms.
- Easing: `cubic-bezier(.16,1,.3,1)` out, `cubic-bezier(.65,0,.35,1)` in-out.
- Nothing moves under `prefers-reduced-motion: reduce`; colour and state cues stay.
- Only `transform` and `opacity` are animated.

## Screens

Feed, Search, Wardrobe, Profile, Post detail, Piece detail, Settings, Create, Stylist and the claim-handle sheet. Checked at 1440, 1024, 768, 390 and 360 with zero horizontal overflow, zero console errors and no interactive target under 24×24.

## Notes

Worked out in place: a landing page and an app that share one set of rules rather than two designs bolted together. The wordmark is set in Grand Hotel and carries no full stop.
