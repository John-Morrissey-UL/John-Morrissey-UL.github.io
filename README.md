# John-Morrissey-UL.github.io

Source for my showcase site, live at **<https://john-morrissey-ul.github.io>**.

A single, self-contained static page listing my Brightspace (D2L) tooling —
zero-dependency, single-file widgets that run on the viewer's own session.

## What's here

- **`index.html`** — the entire site. One file: markup, styles, scripts and
  icons inline. No build step, no framework, no external fonts, scripts or
  stylesheets.

## How it works

- **Live project list.** Repositories, descriptions, stars, language and
  "last push" are fetched from the GitHub REST API on each load, so new repos
  appear automatically and everything stays current.
- **Curated extras.** Display titles, tags, badges and the "featured" flag live
  in a `CURATED` object near the top of the `<script>`, keyed by repo name.
  The curated blurb is shown first; GitHub's own description is the fallback for
  a repo without one. A repo not listed still renders automatically.
- **Offline fallback.** If the API is unreachable (or the 60 req/hr
  unauthenticated limit is hit), the page renders from a hardcoded snapshot
  instead of an empty grid.
- **Embedded avatar.** My GitHub photo is inlined as a base64 data URI — no
  external hotlink — to match the zero-dependency style of the tools it lists.

## Editing

Everything is in `index.html`:

- **Colours and spacing** — the `:root` block at the top of `<style>`.
- **Hero copy** — the `<div class="wrap hero">` block.
- **Project copy** — the `CURATED` object in the `<script>`.
- **"Approach" cards** — the `.principles` block.

## Deploying

It's a GitHub user site: pushes to `main` are served from the repo root by
GitHub Pages automatically. Open `index.html` directly in a browser to preview
locally — the GitHub API call is CORS-friendly from `file://`, so the cards
populate normally.

## Licence

Content © John Morrissey. The listed tools are open source under
CC BY-NC-SA 4.0 in their own repositories.
