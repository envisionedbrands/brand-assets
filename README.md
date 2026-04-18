# Envisioned Brands — Brand Assets

Single source of truth for Envisioned Brand visual assets. Consumed by:
- **kie.ai** — image generation (identity pack as MAINTAIN reference)
- **Envisioned Wiki** — documentation/embedded images
- **Website** — hero images, portraits, CDN
- **Claude skills** — auto-loaded reference library
- **Distribution tools (GHL, etc.)** — social/email imagery

## Structure

```
brand-assets/
├── identity-pack/            6-image reference pack for face-consistent AI generation
├── approved-images/          Production-ready brand imagery organized by scene type
│   ├── portraits/            Hero close-ups, featured portraits
│   ├── environmental/        Scene-in-context (café, kitchen, workspace)
│   ├── travel/              Destination / aspirational
│   └── (more folders as library grows)
└── README.md
```

## Identity Pack — 6 Anchor Photos

Every face-consistent AI image generation passes all 6 of these as reference. Pack composition (per spec in main repo `01-BRAND/identity-pack.md`):

1. `identity-pack/01-front.png` — front-facing
2. `identity-pack/02-three-quarter-left-A.jpg` — three-quarter left (A)
3. `identity-pack/03-three-quarter-left-B.png` — three-quarter left (B, different expression)
4. `identity-pack/04-three-quarter-right-A.jpg` — three-quarter right (A)
5. `identity-pack/05-three-quarter-right-B.png` — three-quarter right (B, different expression)
6. `identity-pack/06-profile.png` — profile (substitute — library lacks true 90° profile)

**Raw URL pattern (for API consumption):**
```
https://raw.githubusercontent.com/envisionedbrands/brand-assets/main/identity-pack/[filename]
```

## Approved Images

Each file paired with a metadata `.md` in the main repo (`01-BRAND/generated-images/approved/[category]/`).

## Usage in kie.ai (Nano Banana 2)

```python
image_input = [
  "https://raw.githubusercontent.com/envisionedbrands/brand-assets/main/identity-pack/01-front.png",
  "https://raw.githubusercontent.com/envisionedbrands/brand-assets/main/identity-pack/02-three-quarter-left-A.jpg",
  # ... all 6
]
```

## Related Repositories
- [envisionedbrands/envisioned-wiki](https://github.com/envisionedbrands/envisioned-wiki) — internal documentation, voice/strategy
- Main workspace: `envisioned-os-april-2026/01-BRAND/` — DNA, identity-pack.md, theme library, generated-images

## License
All rights reserved. This repo contains private brand assets for Envisioned Brands.
