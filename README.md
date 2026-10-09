# Plan4Planet

Website for the 2026 AAAI Fall Symposium on _Planning for a Better Planet_ (Nov 5-7, 2026, Arlington, VA). Live at https://plan4planet.org.

The site is plain Markdown, built and hosted by GitHub Pages. To update the live site, edit the Markdown files on the `main` branch directly.
Note: You do *not* need to run `jekyll build` or install anything for this to work. See below if you want to preview your work locally before you push to the repo.

Using an AI coding agent (Claude Code, Codex, Copilot, Cursor, and the like) to make changes? Ask it to read [AGENTS.md](AGENTS.md) first. It holds the build facts, the file map, and the rules the site relies on. Most agents pick it up on their own; Claude Code reads it through `CLAUDE.md`.

## What to edit

| You want to change | Edit this file |
|---|---|
| Home page (hero, announcement, intro, goals, call for participation, attend) | `index.md` |
| Connect channels (home page and footer) | `_data/channels.yml` |
| Organizing committee | `_data/committee.yml` |
| Sponsors (home page) | `_data/supporters.yml` |
| Confirmed speakers | `pages/speakers.md` |
| Accepted papers | `pages/papers.md` |
| Schedule | `pages/schedule.md` |
| Menu items in the top bar | `_data/navigation.yml` |
| Footer | `_includes/footer.html` |
| Site title, description, social card | `_config.yml` |
| Images (logos, speaker and committee photos) | `assets/images/` |
| Colours and fonts | `_sass/_tokens.scss` |
| Styling of one part of the site | `_sass/components/` |

To edit on GitHub: open the file, click the pencil icon, make your change, and commit to `main`.

Each page in `pages/` starts with a short block between `---` lines (title and URL). Leave that block alone and edit the content below it.

## Preview locally (optional)

Requires Ruby. Install Jekyll once:

```
gem install jekyll webrick
```

Then from the repo folder:

```
jekyll serve
```

and open http://127.0.0.1:4000. The page reloads as you save.

## Layout

```
index.md              home page
pages/                one Markdown file per section page
_data/                menu, channels, committee, sponsors
_layouts/             page shells (default, home, page)
_includes/            head, header, footer, and the home page sections
_sass/                tokens, base styles, one partial per component, vendored minima base
assets/               images and the Sass entry point
_config.yml           site settings
CNAME                 custom domain (do not edit)
```

The site has no gem theme. The minima base styles are vendored under `_sass/vendor/` and everything visible is set by the tokens in `_sass/_tokens.scss` and the partials in `_sass/components/`.
