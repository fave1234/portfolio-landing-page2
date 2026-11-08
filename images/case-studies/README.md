# Case study image slots

> **Status:** placeholder brand visuals are generated and wired in. Replace them
> with your own high-resolution exports whenever you're ready — keep the same
> filenames and nothing else needs to change.

## Janna's Bowls — `/work/jannas-bowls/`

The case study uses a **full-bleed asymmetrical gallery of exactly 10 slots**.
Slot order, span and ratio are set by the `.g-*` class on each `<figure>`.

| # | Slot | Current file | Class | Desktop span | Ratio |
|---|------|--------------|-------|--------------|-------|
| 01 | Hero / full-width opening | `jannas-hero.jpg` | `.g-hero` | 12 / 12 | 21:9 |
| 02 | Old vs new logo comparison | `jannas-logo-compare.jpg` | `.g-compare` | 7 / 12 | 16:10 |
| 03 | Logo sketches / process | `jannas-process.jpg` | `.g-process` | 5 / 12 | 16:10 |
| 04 | Final wordmark on dark | `jannas-wordmark-dark.jpg` | `.g-word-dark` | 4 / 12 | 4:5 |
| 05 | Final wordmark on light / colour variations | `jannas-wordmark-light.jpg` | `.g-word-light` | 4 / 12 | 4:5 |
| 06 | Brand colour palette application | `jannas-palette.jpg` | `.g-palette` | 4 / 12 | 4:5 |
| 07 | Packaging / bowl mockup (full width) | `jannas-packaging-02.jpg` | `.g-packaging` | 12 / 12 | 21:9 |
| 08 | Apparel & merch flat-lay | `jannas-merch.jpg` | `.g-apparel` | 6 / 12 | 4:3 |
| 09 | Bags + collateral | `jannas-bags.jpg` | `.g-bags` | 6 / 12 | 4:3 |
| 10 | Wide closing lifestyle / environmental | `jannas-closing.jpg` | `.g-closing` | 12 / 12 | 21:9 |

`jannas-lockup.jpg`, `jannas-packaging-01.jpg` and `jannas-monogram.jpg` are
still in the folder and free to swap into any slot.

### How to swap an image

Replace the file, or point the `src` at something else:

```html
<figure class="g-item g-apparel">
  <img src="../../images/case-studies/my-new-shot.jpg" alt="Describe the shot">
  <span class="g-num">08</span>
  <figcaption class="g-cap">Apparel &amp; merch</figcaption>
</figure>
```

- Keep the **`.g-*` class** — it controls grid span and aspect ratio.
- All images use `object-fit: cover`, so any source ratio will fill the frame
  without distortion. Export close to the slot ratio to avoid cropping.
- `loading="lazy"` is set on every gallery image.

### Layout behaviour

| Breakpoint | Grid | Behaviour |
|------------|------|-----------|
| Desktop | 12 columns | Full asymmetric rhythm (table above) |
| ≤ 1024px | 12 columns | Paired spans even out; tall tiles keep 4:5 |
| ≤ 820px | 6 columns | 2-up blocks — 6, 4+2, 3+3 |
| ≤ 600px | 1 column | Single column, still edge-to-edge |

The gallery sits **outside** the `.sec` max-width shell, so tiles run from the
left viewport edge to the right. `body { overflow-x: hidden }` guards against
horizontal scroll.

### Recommended export sizes

- Full-width (21:9): 2560 × 1097px
- 16:10 slots: 1800 × 1125px
- 4:3 slots: 1600 × 1200px
- 4:5 portrait slots: 1200 × 1500px

WebP at quality 80–85 keeps the page fast.


## Frootify Ramadan — `/work/frootify-ramadan/`

Same full-bleed asymmetrical system as Janna's Bowls, with Frootify brand accents
(green / orange / lantern gold).

| # | Slot | Current file | Class | Desktop span | Ratio |
|---|------|--------------|-------|--------------|-------|
| 01 | Hero desktop | `frootify-hero-desktop.jpg` | `.g-hero` | 12 / 12 | 21:9 |
| 02 | Devices mockup | `frootify-devices-mockup.jpg` | `.g-devices` | 7 / 12 | 16:10 |
| 03 | Packaging pouch | `frootify-packaging-pouch.jpg` | `.g-pouch` | 5 / 12 | 16:10 |
| 04 | Why you'll love it | `frootify-why-love-it.jpg` | `.g-why` | 4 / 12 | 4:5 |
| 05 | Papiano Kutoria | `frootify-papiano-kutoria.jpg` | `.g-papiano` | 4 / 12 | 4:5 |
| 06 | Tapioca Melodia | `frootify-tapioca-melodia.jpg` | `.g-tapioca` | 4 / 12 | 4:5 |
| 07 | Pre-order form (full width) | `frootify-preorder-form.jpg` | `.g-preorder` | 12 / 12 | 21:9 |
| 08 | Ramadan atmosphere | `frootify-ramadan-atmosphere.jpg` | `.g-atmosphere` | 6 / 12 | 4:3 |
| 09 | Social templates | `frootify-social-templates.jpg` | `.g-social` | 6 / 12 | 4:3 |
| 10 | Closing wide | `frootify-closing-wide.jpg` | `.g-closing` | 12 / 12 | 21:9 |

**Figma links:** the two prototype buttons in the hero (`.figma-row`) are live and
open in a new tab. To point them elsewhere, update the `href` on
`.figma-btn--primary` (desktop) / `.figma-btn--secondary` (mobile) in
`work/frootify-ramadan/index.html`. Keep `target="_blank"` and
`rel="noopener noreferrer"`.

## Homepage card

`index.html` → `.cs-grid`. Card 01 uses `jannas-hero.jpg`, card 02 uses
`frootify-hero-desktop.jpg`. Swap those `<img src>` values if you change either hero.
