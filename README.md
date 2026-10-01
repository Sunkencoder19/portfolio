# Fattesing Rane | Portfolio

A single-file, scroll-driven 3D portfolio for a Mumbai-based cybersecurity student and full-stack developer. Everything (HTML, CSS, JS, fonts, map data) lives in one `index.html`, so it works offline and deploys anywhere static files do.

**Concept: "The Briefing."** The site reads like a declassified dossier. Redaction bars peel off the text as you read, a 3D globe follows the story from home base to simulated attacks to the countries where he has represented delegations, and Model UN conferences land as passport stamps. It covers three halves of the work: build (full-stack), break (red team, threat intel), govern (policy, MUN).

## Highlights

- **Marathi name, English on hover.** The hero shows फत्तेसिंग राणे. Hovering creates a wobbling liquid lens that reveals FATTESING RANE behind it (WebGL shader). It auto-sweeps once on load, loops on touch devices, and falls back to a hover/tap swap for reduced-motion users or browsers without WebGL.
- **Pinned 3D globe** (Three.js) with dotted land, attack arcs and DOM country labels.
- **Variable-width type** that stretches with scroll and cursor.
- **TryHackMe rank card** with a scroll-triggered counter and 100-tick strip.
- **Custom cursor** (ring and dot), Lenis smooth scroll, GSAP ScrollTrigger throughout.
- **Accessible fallbacks:** `prefers-reduced-motion`, touch, and no-WebGL paths.

## Stack

| Layer | Choice |
| --- | --- |
| Motion | GSAP 3.12.5 + ScrollTrigger |
| Smooth scroll | Lenis 1.1.13 |
| 3D | Three.js r128 |
| Fonts | Archivo (variable width), Instrument Sans, JetBrains Mono, Noto Sans Devanagari, all embedded as base64 woff2 (SIL OFL) |
| Map data | Natural Earth land via world-atlas (public domain), baked into a 19 KB bitmask |

All libraries are inlined, so there are no CDN calls.

## Design system

- **Palette:** fog `#E6EAEE`, ink `#0E1620`, muted `#586371`, line `#C5CCD4`, signal `#F2401E` (the only accent).
- **Shape:** sharp surfaces, full-pill interactive elements.
- **Theme:** light, locked.

## Repo layout

```
.
├── index.html                  # the whole site
├── Fattesing_Rane_Resume.pdf   # linked by the Resume buttons
└── README.md
```

The Resume buttons (hero and contact section) point to `Fattesing_Rane_Resume.pdf` in the same folder. Keep the filename, or update the two links in `index.html`.

## Run locally

No build step. Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy

Any static host works.

**GitHub Pages:** push to the repo, then Settings, Pages, deploy from the `main` branch root.

**Cloudflare Pages / Netlify:** connect the repo (or drag the folder in). No build command, publish directory is the repo root.

**Custom domain:** add the domain in the host's dashboard, then create the DNS records it shows at your registrar (A/ALIAS for the root, CNAME for `www`). HTTPS is issued automatically.

## Editing content

Content is plain HTML inside `index.html`. Common edits:

- **TryHackMe rank:** the `data-count="45"` value and the count-up target in the "TryHackMe rank strip" script.
- **Skills:** the `#skills` section.
- **Links:** contact section (`#contact`) and the TryHackMe card.
- **Favicon:** inline SVG `<link rel="icon">` in `<head>`.

The country list for the globe and the MUN stamps are also plain data in the markup and script.

## Honesty note

The NSMS attack arcs on the globe are drawn from the project's simulated dataset (RFC 5737 test ranges). Nothing on the page is invented data.

## Contact

- Email: cypher1906@gmail.com
- LinkedIn: [linkedin.com/in/fattesingrane](https://linkedin.com/in/fattesingrane)
- GitHub: [github.com/Sunkencoder19](https://github.com/Sunkencoder19)
- TryHackMe: [tryhackme.com/p/Sunkencoder19](https://tryhackme.com/p/Sunkencoder19)

&copy; 2026 Fattesing Rane. Fonts under SIL OFL; libraries under their own licenses.