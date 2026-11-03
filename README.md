# portfolio-landing-page2

Personal portfolio site for **Favour Onasanya TL — Brand Designer | Brand Identity & Visual Systems**.

Static HTML/CSS/JS (no build step). Open `index.html` locally, or serve the folder
with any static host.

## Site structure

| Route | File | Purpose |
|-------|------|---------|
| `/` | `index.html` | Landing page — hero positioning, skills marquee, **Selected Case Studies** (4 cards), contact footer |
| `/work/jannas-bowls/` | `work/jannas-bowls/index.html` | Janna's Bowls case study — overview, challenge, strategy & naming, colour + typography, results, image slots |
| `/archive/` | `archive/index.html` | **Visual Archive** — standalone designs, social campaigns, presentations (2022 – 2026) with filters + lightbox |
| `/about.html` | `about.html` | Bio, experience timeline, skills, presentations, contact |
| `/work.html` | `work.html` | Legacy URL — redirects to `/archive/` |

## Local preview

```bash
python3 -m http.server 8080
# then open http://localhost:8080
```

Directory-style URLs (`/archive/`, `/work/jannas-bowls/`) resolve automatically
because each route is a folder containing an `index.html` — this works on GitHub
Pages, Netlify, Vercel and any static server without extra config.

## Editing content

- **Hero copy / capability pills** — `index.html`, `section.hero` and `.pillar-row`.
- **Marquee items** — `index.html`, `.ticker-track` (two identical `.ticker-group`
  blocks are required for the seamless 50% loop).
- **Case study cards** — `index.html`, `.cs-grid`. Card 1 links to
  `/work/jannas-bowls/`; cards 2–4 are reserved slots (`.is-pending`) ready for
  new studies.
- **Case study images** — see `images/case-studies/README.md` for the slot map and
  swap instructions.
- **Archive gallery** — `archive/index.html`, `allItems` / `presentations` data
  arrays near the bottom of the file.

## Notes

- Dark theme tokens live in `:root` in each page (`--bg`, `--ink`, `--line`, …).
- Motion respects `prefers-reduced-motion`.
- The contact CTA buttons use Calendly; the archive lightbox uses EmailJS for
  like notifications.
