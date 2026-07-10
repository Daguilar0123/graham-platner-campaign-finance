# Social image metadata — graham-platner-campaign-finance

Sidecar metadata for every image in `social/`. Each image has a JSON file named
`<image filename>.json` sitting next to it (e.g. `og-1200x630.png` → `og-1200x630.png.json`).

All images: © 2026 Daniel Ismael Aguilar · https://grownfromconcrete.org
Source page: https://daguilar0123.github.io/graham-platner-campaign-finance/

Fields in every sidecar: title, description, alt_text, creator, creator_url, copyright,
credit, copyright_year, date_created, dimensions, format, keywords, source_page, usage_note
(+ accessibility_note on animated GIFs, whose first frame is near-empty by design).

| Image | Sidecar | Title |
|---|---|---|
| `og-1200x630.png` | `og-1200x630.png.json` | What Can $11 Million Buy? — $34 : $1 |
| `x-1600x900.png` | `x-1600x900.png.json` | What Can $11 Million Buy? — dramatized dollar figures |
| `ig-1080x1080.png` | `ig-1080x1080.png.json` | What Can $11 Million Buy? — 34-vs-1 unit grid |
| `ig-1080x1350.png` | `ig-1080x1350.png.json` | What Can $11 Million Buy? — dramatized figures, portrait |
| `story-1080x1920.png` | `story-1080x1920.png.json` | What Can $11 Million Buy? — proportional vertical bars |
| `spending-animated.gif` | `spending-animated.gif.json` | Spending race — animated counters |
| `infographic-money-pipeline-1200x2260.png` | `infographic-money-pipeline-1200x2260.png.json` | Who paid for the $11 million spent against Graham Platner? |
| `waffle-squares-animated.gif` | `waffle-squares-animated.gif.json` | Every outside dollar in this race, as squares — animated |
| `donut-97-animated.gif` | `donut-97-animated.gif.json` | 97¢ of every opposition dollar — animated donut |
| `trail-goes-dark-animated.gif` | `trail-goes-dark-animated.gif.json` | The spending is public. The source isn’t. — animated money trail |
| `section-money-flow-1600x900.png` | `section-money-flow-1600x900.png.json` | One PAC · six checks · one vendor |
| `section-pine-tree-dossier-1600x900.png` | `section-pine-tree-dossier-1600x900.png.json` | Committee file: Pine Tree Results PAC |
| `section-hidden-money-1600x900.png` | `section-hidden-money-1600x900.png.json` | The spending is public. The source isn’t. |
| `og-1200x630-donut.png` | `og-1200x630-donut.png.json` | What Can $11 Million Buy? — 97¢ donut OG card |

## Notes

- `og-1200x630.png` here describes the **$34 : $1 ratio hero** currently live in the repo.
  The newer 97¢-donut version generated July 10 has its metadata in `og-1200x630-donut.png.json` —
  if you replace the OG image with the donut version, rename that sidecar to `og-1200x630.png.json`.
- Animated GIFs loop forever; their first frame is intentionally near-empty (the animation builds
  from zero), so pair them with a static PNG on platforms that use frame 1 as the preview.
- Embedding this metadata INTO the files (EXIF/XMP for PNG, GIF comment blocks) requires a tool
  like exiftool, e.g.:
  `exiftool -Artist="Daniel Ismael Aguilar" -Copyright="© 2026 Daniel Ismael Aguilar" -XMP-dc:Rights="© 2026 Daniel Ismael Aguilar · grownfromconcrete.org" -XMP-dc:Title≤"..." -XMP-dc:Description≤"..." <file>`
  — the JSON sidecars carry every value an agent needs to do that per file.
