# Instructions for AI agents working on this repo

Read this before changing anything. It applies to any coding agent (Claude Code, Codex, Copilot, Cursor, Gemini CLI, others). Humans: see README.md.

## What this is

The website for Plan4Planet (plan4planet.org), a community at the intersection of AI planning and climate decisions. The 2026 AAAI Fall Symposium is its first event. The site is static Markdown and HTML built by Jekyll on GitHub Pages from the `main` branch. Every push to `main` goes live within a minute or two.

## Build facts

- GitHub Pages toolchain: Jekyll 3.10, kramdown, libsass. Sass uses `@import` only. No `@use`, no `math.div`, no Jekyll 4 features.
- No gem theme. The minima base styles are vendored in `_sass/vendor/` and must not be edited.
- Plugins: jekyll-seo-tag and jekyll-feed only. Do not add plugins; GitHub Pages ignores them.
- Local preview: `jekyll serve`, then http://127.0.0.1:4000. Do not commit `_site/`.

## Where things live

| Change | File |
|---|---|
| Home page copy, hero, announcement, call for participation | `index.md` |
| Section pages (speakers, papers, schedule) | `pages/*.md` |
| Top menu | `_data/navigation.yml` |
| Contact and social channels (Connect section and footer) | `_data/channels.yml` |
| Organizing committee | `_data/committee.yml` |
| Sponsors | `_data/supporters.yml` |
| Colours, fonts, radii, shadows | `_sass/_tokens.scss` |
| Styles for one part of the site | `_sass/components/_*.scss`, one partial per component |
| Site-wide element styles | `_sass/_base.scss` |
| Page shells | `_layouts/`, `_includes/head.html`, `header.html`, `footer.html` |
| Images | `assets/images/` |

## Rules

1. Content changes go in Markdown or the `_data/` files. Prefer editing data files over editing HTML.
2. No inline `style=""` attributes anywhere. Add a class and put the rule in the matching partial under `_sass/components/`.
3. Every colour, font, radius and shadow comes from a token in `_sass/_tokens.scss`. Never hard-code a colour in a partial. Do not change token values without the site owner's agreement; the visual identity is managed separately.
4. Asset paths in Markdown and includes go through `{{ '/assets/...' | relative_url }}`, never a bare `/assets/...` path.
5. The AAAI logo stays full colour, unrecoloured, with clear space, and linked to aaai.org. The event is called "AAAI Fall Symposium 2026" in that word order.
6. Do not edit `CNAME`, `_sass/vendor/`, `robots.txt`, or `sitemap.xml`.
7. Commented-out blocks in `index.md` (the announcement) are placeholders. Leave them in place unless asked to turn them on.
8. Keep the page working on phones. Anything new gets a `max-width: 640px` rule if it needs one.

## Commits

- One change per commit. Subject in conventional-commits form: `content:` for site copy, `feat:`, `fix:`, `refactor:`, `docs:`, `chore:`.
- No trailer lines (no Co-Authored-By or Generated-with).
- Build locally before committing. Check the changed page and the speakers page.
- Show the person you are working for the diff before pushing. If in doubt, commit to a branch and open a pull request instead of pushing to `main`.
