# raviwaar.github.io

Source for my personal site, hosted on **GitHub Pages** — live at
[raviwaar.github.io](https://raviwaar.github.io).

## Structure

| Path | What it is |
|------|------------|
| `index.html` | The whole site: content, CSS and layout in one self-contained file |
| `assets/profile.JPG` | Portrait used in the hero |
| `assets/Resume.pdf` | Downloadable resume, linked from the hero |
| `_config.yml` | GitHub Pages config |

## Design notes

- **Content lives in the HTML**, not in JavaScript. Link previews on LinkedIn and
  Slack, search crawlers, and anyone reading the source all see the real text.
- **No build step and no CDN.** Plain CSS, one Google Fonts import. Nothing to
  install, nothing to compile, nothing that breaks when a CDN changes.
- **Respects the visitor's colour scheme** via `prefers-color-scheme`.
- **Single breakpoint at 820px** for the hero, 680px for navigation and dates.

## Running it locally

```bash
git clone https://github.com/raviwaar/raviwaar.github.io.git
cd raviwaar.github.io
open index.html        # no server needed
```

To preview exactly as GitHub Pages serves it:

```bash
python3 -m http.server 8000
```

Then visit <http://localhost:8000>.

## Editing

Everything is in `index.html`. Sections are marked with `id` attributes matching the
nav links: `#work`, `#research`, `#projects`, `#skills`, `#contact`. Colours are CSS
custom properties at the top of the `<style>` block — change them in one place and
both light and dark themes follow.
