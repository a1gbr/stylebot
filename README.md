# stylebot — per-site dark mode CSS

A small collection of custom CSS themes I actually use every day, written for
[Stylebot](https://stylebot.dev/), the browser extension that injects user CSS into specific sites.

The idea is simple: most "dark mode" extensions invert colors and leave the result unreadable. These
files are hand-written per site — background, text, borders, links and the site's own accent color are
chosen so the page stays legible, not just dark.

## What is here

| Folder | Site | Notes |
|---|---|---|
| `canvas/` | Canvas (LMS) | Several variants: `canvasDarkMode.css`, `canvasDark.css`, `canvasAtual.css`, `darkRedDiabloIV.css` |
| `howtostudykorean/` | howtostudykorean.com | Reading-focused dark theme |
| `lostmerchants/` | Lost Merchants | Dark theme |
| `soundcloud/` | SoundCloud | Dark theme with the waveform/progress bar kept orange |

The `canvas/` variants are iterations: `canvasDarkMode.css` is the most complete one; the others are
earlier takes and one themed experiment (`darkRedDiabloIV.css`) kept for reference.

## How to run it

No build step — it is plain CSS.

1. Install the [Stylebot](https://chrome.google.com/webstore/detail/stylebot/oiaejidbmkiecgbjeifoejpgmdaleoha)
   extension (Chrome, Edge or Firefox).
2. Open the target site.
3. Open Stylebot → **Custom CSS** (or *Write CSS for this site*).
4. Paste the contents of the matching file and save.

To apply per-path variants, scope the CSS with the site's own selectors, or create separate Stylebot
styles per URL pattern.

## Notes

- Written against the sites' DOM as of 2024; if a site ships a redesign, class names will drift and the
  CSS will need a pass.
- `* { background-color: ... }` at the top of each file is the blunt instrument that makes these work in
  a few lines. For a production theme I would scope selectors instead — see `canvas/canvasDarkMode.css`
  for the more careful version.
- I no longer maintain this actively; it is published because it is useful and because it shows how I
  work: small, direct, ends with something that runs.

## License

MIT — take whatever is useful.
