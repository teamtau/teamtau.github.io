# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

Single-page Jekyll site for TEAMTAU, deployed by GitHub Pages straight from `master` to https://teamtau.com/ (see `CNAME`). Pushing to `master` publishes — there is no CI, no staging, no tests and no linter.

## Commands

```bash
jekyll serve      # local preview at http://localhost:4000
jekyll build      # output to _site/ (gitignored)
```

There is no `Gemfile`; Jekyll and the plugins in `_config.yml` (`jekyll-minifier`, `jekyll-seo-tag`, `jekyll-feed`) must be installed as gems globally. GitHub Pages only runs its whitelisted plugins, so `jekyll-minifier` takes effect locally but not on the live site.

## Architecture

- `_layouts/default.html` is the whole page shell: `<head>`, fonts (Geist, Geist Mono), the GA4 tag, header, the shared Contact section (`#section-11`) and the footer include. Pages only supply the `<section>` blocks rendered into `{{ content }}`.
- `index.html` is the only real content page (hero + `#section-3` "What we do"). `404.html` reuses the same layout.
- `assets/css/custom.css` is the only stylesheet the layout loads, and the site loads no JavaScript apart from analytics. Colours, fonts and easing are CSS variables at the top of that file.
- The hero photo is set per page with an inline `--photo: url(...)` on `.hero-photo`; the CSS adds the dark overlay. The pipeline panel in the hero is illustrative markup, not live data.
- Asset and nav URLs are root-absolute (`/assets/...`, `/#section-3`) so `404.html` works at nested URLs. This relies on the site being served from the domain root.
- Includes are pulled in with `{% include_relative _includes/... %}`, not `{% include %}`.
- `assets/css/theme.css`, `helper.css`, `menu.css`, `assets/js/` and `assets/vendor/` are leftovers from the previous purchased theme and are no longer referenced by any page.

### Portfolio posts

`_posts/portfolio/*.html` are front-matter-only data records (`title`, `date`, `categories: portfolio`, `service`, `thumbnail`, `except`). Note the field is spelled `except`, not `excerpt`. They are currently rendered only by `debug.html` (using the bare `_layouts/debug.html`), which loops over `site.categories.portfolio`; the homepage does not show them.

## Known quirks

- `.jekyll-cache/` files are committed and not in `.gitignore`; `jekyll serve` will modify them, so avoid staging those changes with unrelated work.
- `.htaccess` is Apache config and has no effect on GitHub Pages.
