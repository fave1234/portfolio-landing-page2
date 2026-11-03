# Case study image slots

> **Status:** placeholder brand visuals are already generated and wired in
> (`jannas-hero.jpg`, `jannas-lockup.jpg`, `jannas-packaging-01.jpg`,
> `jannas-packaging-02.jpg`, `jannas-merch.jpg`, `jannas-monogram.jpg`).
> Replace them with your own high-resolution exports whenever you're ready —
> keep the same filenames and nothing else needs to change.

Drop high-resolution assets in this folder and update the `src` in `work/jannas-bowls/index.html`.

## Janna's Bowls — `/work/jannas-bowls/`

| Slot                      | Current file                              | Ratio | Location in page |
|---------------------------|-------------------------------------------|-------|------------------|
| Hero image                | `jannas-hero.jpg`                        | 16:9  | `header.cs-hero` → `.cs-hero-media` |
| Master wordmark lockup    | `jannas-lockup.jpg`                      | 21:9  | `#gallery` → first `.g-slot.g-wide` |
| Packaging system          | `jannas-packaging-01.jpg`                | 4:3   | `#gallery` → `.g-slot` 2 |
| Bowl & delivery packaging | `jannas-packaging-02.jpg`                | 4:3   | `#gallery` → `.g-slot` 3 |
| Merch & uniform mockups   | `jannas-merch.jpg`                       | 4:3   | `#gallery` → `.g-slot` 4 |
| "J's" monogram applications | `jannas-monogram.jpg`                  | 4:3   | `#gallery` → `.g-slot` 5 |

### How to swap a slot

1. Save the asset here (e.g. `images/case-studies/jannas-hero.webp`).
2. In `work/jannas-bowls/index.html`, replace the whole placeholder block:

```html
<div class="slot-ph">
  <svg ...>...</svg>
  <span class="slot-ph-label">Hero Image — 16:9<b>images/case-studies/jannas-hero.webp</b></span>
</div>
```

with:

```html
<img src="../../images/case-studies/jannas-hero.webp" alt="Janna's Bowls identity hero">
```

The page already handles broken paths: if an `<img>` fails to load it is
removed and the striped placeholder becomes visible again, so the layout never
collapses.

## Homepage card

`index.html` → `.cs-card--wide` → `.cs-media` uses the same pattern. Swap the
`.cs-media-ph` block for:

```html
<img src="images/case-studies/jannas-hero.webp" alt="Janna's Bowls brand identity">
```

## Recommended sizing

- Hero: 2400 × 1350 px
- Wide gallery: 2400 × 1030 px
- Gallery slots: 1600 × 1200 px
- Export as WebP (quality 80–85) to keep the page fast.
