# Squawck brand assets

Locked brand — do not recolor or re-typeset. All marks are fixed:

| Token            | Value      | Used for                          |
|------------------|------------|-----------------------------------|
| Body             | `#C8623E`  | bird body + tail                  |
| Accent           | `#DE8460`  | beak, legs, squawk dashes         |
| Eye              | `#F0E1D2`  | eye dot + icon background         |
| Wordmark text    | `#B5532F`  | the word "SQUAWCK"                |
| Page background  | `#F4E5DB`  | site background                   |
| Typeface         | Fredoka, weight 600 (SIL Open Font License) |

---

## Files

### `svg/` — scalable vector (best for web + in-app; no font needed)
- `squawck-mark.svg` — the bird only, transparent.
- `squawck-icon.svg` — squircle app icon (cream background).
- `squawck-icon-maskable.svg` — full-bleed version for Android adaptive / PWA maskable.

### `web/` — drop into a website / PWA
- `favicon-32.png`, `favicon-48.png`
- `apple-touch-icon-180.png`
- `icon-192.png`, `icon-512.png`, `icon-1024.png` — PWA "any" icons
- `maskable-512.png` — PWA "maskable" icon
- `squawck-mark-512.png`, `squawck-mark-1024.png` — transparent bird
- `squawck-wordmark.png` — transparent bird + wordmark lockup (2223×609)
- `site.webmanifest` — ready-made PWA manifest

Add to your `<head>`:
```html
<link rel="icon" type="image/png" sizes="32x32" href="/assets/web/favicon-32.png">
<link rel="icon" type="image/png" sizes="48x48" href="/assets/web/favicon-48.png">
<link rel="icon" href="/assets/svg/squawck-icon.svg" type="image/svg+xml">
<link rel="apple-touch-icon" sizes="180x180" href="/assets/web/apple-touch-icon-180.png">
<link rel="manifest" href="/assets/web/site.webmanifest">
<meta name="theme-color" content="#C8623E">
```

For an inline logo that scales crisply, use `svg/squawck-mark.svg` + live Fredoka text,
or the `squawck-wordmark.png` when a single image is easier.

### `android/` — drop into an Android project's `res/`
- `mipmap-mdpi/…xxxhdpi/ic_launcher.png` — legacy launcher icons (48→192 px)
- `ic_launcher_foreground.png`, `ic_launcher_background.png` — adaptive layers (432 px)
- `mipmap-anydpi-v26/ic_launcher.xml` — adaptive icon descriptor
- `play-store-512.png` — Google Play listing icon

Place the `foreground`/`background` PNGs in your `mipmap-*` folders (or `drawable`),
keep the `mipmap-anydpi-v26/ic_launcher.xml` as-is, and point your manifest at
`@mipmap/ic_launcher`.

### In-app
Use `svg/squawck-mark.svg` (or `web/squawck-mark-512.png`) for headers, splash, and
empty states. Use `web/squawck-wordmark.png` where the full lockup is needed.
