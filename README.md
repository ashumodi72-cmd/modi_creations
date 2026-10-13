# modi_creations

Website for **Modi Creations**, Jaipur: handmade Kundan Jadau jewellery in 22kt gold, made since 1995.

It's a single-page, scroll-driven WebGL experience. As you scroll, the camera orbits a procedurally built 22kt gold Kundan ring: an engraved vine shank, a lotus collet, an emerald with a diamond halo, and twinkling glints. Behind it, a liquid-gold wave shader slowly shifts to emerald, and an editorial text overlay tells the story in four chapters: Heritage, Story, Craft, Visit.

## Files

| Path | What it is |
| --- | --- |
| `index.html` | The whole site: markup, styles and the Three.js scene (loaded from unpkg via an import map) |
| `assets/wordmark.png` | "MODI CREATIONS" wordmark (header), cut from the gold logo on a transparent background |
| `assets/monogram.png` | Feather "M" monogram (the Story chapter's image tile) |
| `assets/favicon.png` | Browser-tab icon |

## Run locally

Use any static file server from this folder. For example:

```bash
npx serve .
```

Then open the printed URL. Opening `index.html` straight from disk also works in most browsers.

## Hosting

The site is served by GitHub Pages from the `main` branch root:
https://ashumodi72-cmd.github.io/modi_creations/

## Editing content

- **Wording:** the four chapters are the `.slide` blocks in `index.html`.
- **Contact details:** the `.contact-list` in the "Something Special" chapter (address, WhatsApp, email, Instagram, Facebook).
- **Story image:** replace `assets/monogram.png` with a square product photo to show jewellery instead of the monogram.
