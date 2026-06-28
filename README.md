# marc-challenge.github.io

Official homepage for the **MARC 2026 — MetaSejong AI Robot Challenge**, in conjunction with
IEEE MetaCom 2026. Jekyll static site, bilingual (English primary, Korean mirror).

## Local preview

```bash
bundle install
bundle exec jekyll serve        # http://localhost:4000   ( / -> /en/ )
```

Requires Ruby with `ruby-dev` / `build-essential` for native gems.

## Structure

- `_en/`, `_ko/` — pages (EN primary, KO mirror)
- `_layouts/`, `_includes/`, `_data/`, `assets/`
- `_config.yml` — site config incl. the season-state toggle
- `.github/workflows/jekyll.yml` — GitHub Pages build/deploy

## Multi-year operation

The site is reused at the same URL each edition. Operators switch tone by editing three keys
in `_config.yml` — `season_state` (`off-season` / `announced` / `active` / `archived`),
`edition`, and `competition_active` — with no content changes. Past editions are preserved
under the Editions section.

## Intro media

The intro slot (`_data/media.yml` -> `intro`) currently shows a concept image placeholder.
When the intro video is ready, change `type: image` to `video` and set `embed`/`src` in that
one file; the markup in `_includes/hero-media.html` handles the rest.

> Draft — schedule and external links are provisional / under internal review.
