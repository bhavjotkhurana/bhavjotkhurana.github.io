# BK monogram - Bhavjot Khurana

Direction **L1 / C1**: Archivo 600, side by side, tracking -0.065em. Cream B, jade K,
on an ink tile. The SVGs embed a 908-byte subset of Archivo (glyphs B and K only),
so every file renders the true letterforms with no web-font dependency.

## Colors
| Role | Light background | Dark background |
| --- | --- | --- |
| Tile | Ink `#171310` | Cream `#F7F1E5` |
| B | Cream `#F7F1E5` | Ink `#171310` |
| K | Jade `#4FC08C` | Jade `#16804F` |
| Transparent mark | Ink + jade `#16804F` | Cream + jade `#4FC08C` |

## Files
| File | Use |
| --- | --- |
| `favicon.svg` | Primary scalable favicon - ink tile, full BK |
| `favicon.ico` | 16 (simplified B), 32, 48 |
| `favicon-96x96.png` | Legacy / Android |
| `apple-touch-icon.png` | 180 x 180 |
| `web-app-manifest-192x192.png` | PWA |
| `web-app-manifest-512x512.png` | PWA / splash |
| `logomark.svg` | Site header, transparent, light background |
| `logomark-dark.svg` | Site header, transparent, dark mode |
| `logomark-mono-ink.svg` / `-cream.svg` | Single colour: print, engraving, watermark |
| `icon-small-fallback.svg` | Simplified B for 16-24px contexts |
| `tile-jade.svg` / `tile-cream.svg` | Alternate tiles |
| `logomark-512.png` / `-dark-512.png` | Transparent raster for decks and signatures |
| `logo-source.svg` | Editable source - every variant, live text, construction notes |

## Legibility rule
Two colours inside 24px turns to mud, so the set breaks at 32px: below it, a single
cream **B** on ink; at and above it, the full two-colour **BK**. That break is already
baked into `favicon.ico`.

## Drop-in HTML
```html
<link rel="icon" href="/favicon.ico" sizes="32x32">
<link rel="icon" href="/favicon.svg" type="image/svg+xml">
<link rel="apple-touch-icon" href="/apple-touch-icon.png">
<link rel="manifest" href="/site.webmanifest">
```

```json
{
  "name": "Bhavjot Khurana",
  "short_name": "BK",
  "icons": [
    { "src": "/web-app-manifest-192x192.png", "sizes": "192x192", "type": "image/png", "purpose": "maskable" },
    { "src": "/web-app-manifest-512x512.png", "sizes": "512x512", "type": "image/png", "purpose": "maskable" }
  ],
  "theme_color": "#171310",
  "background_color": "#FDF7ED",
  "display": "standalone"
}
```

## Construction
Archivo 600 at font-size 100: B advance 70.60, K advance 69.50, left sidebearing 7.60,
cap height 68.60. Tracking -6.50 per 100em puts the K origin at 64.10, which leaves a
5.60 gap between the B's bowl and the K's stem - tight enough to read as one mark.

Mark crops to its ink: 123.90 x 68.60 at font-size 100, B at x=-7.60, K at x=56.50.
Tile: 120 box, radius 22, font-size 62, B at x=16.88, K at x=56.62, baseline 81.27,
side margin 21.59.

Clear space is one cap height on every side. Never re-track, outline, rotate, or add
a third colour.
