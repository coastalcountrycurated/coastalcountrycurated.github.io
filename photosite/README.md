# Elena Marsh Photography — Site Template (v2: Scenery / Accommodation / Maternity)

## Structure

```
index.html              → homepage with 3 category tiles
scenery.html             → category page, links to galleries
accommodation.html       → category page, links to galleries
maternity.html           → category page, links to galleries
galleries/
  scenery-coastal-morning.html
  accommodation-driftwood-house.html
  maternity-golden-hour.html
styles.css                → all design tokens + styles live here
assets/                    → put your images in here, organized by category
```

## Adding your own photos

On any gallery page, replace slots like:

```html
<button class="photo-item" data-full="">
  <span class="placeholder-label">Photo 1</span>
</button>
```

with:

```html
<button class="photo-item" data-full="../assets/scenery/01-full.jpg">
  <img src="../assets/scenery/01.jpg" alt="Description of the photo">
</button>
```

- Use a smaller web-sized image (under ~500KB) as the visible `src`.
- `data-full` is optional — if set, that's the larger image shown when someone clicks (for the lightbox).
- Organize images into `/assets/scenery/`, `/assets/accommodation/`, `/assets/maternity/`.

## Adding a new album/gallery

1. Duplicate any file in `/galleries/`.
2. Rename it, e.g. `galleries/scenery-highland-light.html`.
3. Update the `<title>`, `<h1>`, subtitle line, and photo slots.
4. Add a matching card on the relevant category page (`scenery.html`, etc.) linking to it.

## Editing text, colors, fonts

- All copy lives directly in each `.html` file — edit in place.
- Colors, fonts, and spacing are controlled centrally in `styles.css` under `:root` at the top — change a value there and it updates everywhere.

## Deploying

Same GitHub Pages + custom domain process as before — upload all these files (keeping the folder structure) to your `yourusername.github.io` repo.
