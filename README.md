# John-Morrissey-UL.github.io

Source for my site, live at **<https://john-morrissey-ul.github.io>**: who I am,
and the free Brightspace (D2L) tools I've built and released.

## What's here

- **`index.html`**: the whole page. Markup, styles and the small gallery script
  are inline. No build step, no framework, no external fonts or scripts.
- **`media/`**: my photo, each tool's screenshots and demo videos, and the
  Summer Series overview video.
- **`screenshots/`**: the framed pictures used on the smaller "Also built" cards.
- **`og-image.jpg`**: the preview image LinkedIn shows when the link is shared.

## Editing

Everything is in `index.html`:

- **Colours and type**: the `:root` block at the top of `<style>` (with a dark
  version under `prefers-color-scheme: dark`).
- **Opening statement**: the `.intro` section.
- **Case studies**: one `<article class="case">` per featured tool, with the
  problem, what it does and its screenshot. The "Also built" cards follow.
- **Gallery pictures**: the `GALLERY` object in the script, keyed by the
  `data-gallery` names used on the buttons.

## Deploying

It's a GitHub user site: pushes to `main` are served from the repo root by
GitHub Pages. Open `index.html` directly in a browser to preview it locally.

## Licence

Content © John Morrissey. The listed tools are open source under
CC BY-NC-SA 4.0 in their own repositories.
