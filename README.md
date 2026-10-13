# modi_creations

Website for **Modi Creations**, Jaipur: handmade Kundan Jadau jewellery in 22kt gold, made since 1995.

It's a single-page, scroll-driven WebGL experience. The hero is the bird ring, built from two product photos and turned into a four-view turntable: as you scroll and the camera circles, the ring leans in perspective and turns to its next side under a flash of light. Behind it, a liquid-gold wave shader slowly shifts to emerald. Five chapters overlay the scene: Heritage, Story, Craft, Collection (a sideways-gliding gallery of background-free photos) and Visit.

## Files

| Path | What it is |
| --- | --- |
| `index.html` | The whole site: markup, styles and the Three.js scene (loaded from unpkg via an import map) |
| `assets/hero/ring-front.png`, `ring-side.png` | Bird ring cut-outs (from DSC_3955 and DSC_3958) used by the turntable |
| `assets/gallery/collection-01…10.webp` | Collection photos with the backdrop removed |
| `assets/og-image.jpg` | Preview image for links shared on WhatsApp, Facebook and similar |
| `assets/wordmark.png`, `monogram.png`, `favicon.png` | Logo pieces cut from the gold logo |
| `CNAME` | Custom domain for GitHub Pages (modicreations.com) |

The original camera files in `photos/` are kept out of the repo (about 27 MB each).

## Run locally

The ring photos load as WebGL textures, which browsers block from `file://`, so use a static server from this folder. For example:

```bash
npx serve .
```

## Hosting

GitHub Pages serves the `main` branch root at https://modicreations.com. DNS is managed in Wix: the apex has four A records pointing to 185.199.108–111.153, and `www` is a CNAME to `ashumodi72-cmd.github.io`.

## Editing content

- **Wording:** the chapters are the `.slide` blocks in `index.html`.
- **Contact details:** the `.contact-list` in the "Something Special" chapter.
- **Gallery:** the `.gallery-card` figures. Each photo is a 800×1200 WebP with a transparent background.
- **Chapter timing:** the `CHAPTERS` table in the script (where each chapter starts and ends in the scroll).
