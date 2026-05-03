# Trademark assets

The files in this directory are © 2024–2026 AIskaron Inc. and may be
used to refer to the DuckysMusic product in articles, listings, and
posts that are accurate and not derogatory. Do not modify the
artwork, do not use it as the icon of a competing product, and do
not use the DuckysMusic name in a way that implies AIskaron Inc.
endorsement when none has been given.

## Inventory

### Brand

- `logo.png` — official raster logo, used in the README hero.
- `logo.webp` — same logo, smaller binary, suitable for embeds.
- `og-image.png` — Open Graph preview used by GitHub, Twitter/X,
  Discord and Slack when the showcase URL is shared.
- `icon.svg` — vectorised square icon, AIskaron brand palette
  (`#02E093` green, `#0EA6BC` cyan, `#0D3DA6` deep blue, `#000` bg,
  `#DCE6E8` fg).

### Section icons

`icons/` holds nine 40×40 SVG glyphs referenced by the README feature
grid: `playback`, `queue`, `voice`, `search`, `dj`, `uptime`,
`sources`, `filters`, `languages`. Stroke style, AIskaron palette,
24×24 viewBox so they upscale cleanly.

### Screenshots

`screenshots/` holds product screenshots referenced from the README
"In action" section. Filenames are stable; the README does not
break if a file is missing (GitHub renders the alt text).

| File | What to capture |
|---|---|
| `01-play.png` | `/play <url>` with full embed: title, artist, progress bar, requester. |
| `02-queue.png` | `/queue` paginated, 5+ tracks, current position highlighted. |
| `03-search.png` | `/search <term>` showing the interactive picker with thumbnails and source badges. |
| `04-nowplaying.png` | `/nowplaying` with live progress bar, duration, source. |
| `05-help.png` | `/help` showing the categorised command list. |
| `06-language.png` | `/language` flow showing the bot in two locales (e.g. en → es). |

Recommended specs: 1200×800 PNG, ~150 KB each. Blur or crop guild
identifying details (server icons, member tags, channel names with
business context) before commit.
