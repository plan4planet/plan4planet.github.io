# Plan4Planet

Website for the 2026 AAAI Fall Symposium on _Planning for a Better Planet_ (Nov 5-7, 2026, Arlington, VA). Live at https://www.plan4planet.org.

The site is plain Markdown, built and hosted by GitHub Pages. To update the live site, edit the Markdown files on the `main` branch directly.
Note: You do *not* need to run `jekyll build` or install anything for this to work. See below if you want to preview your work locally before you push to the repo.

## What to edit

| You want to change | Edit this file |
|---|---|
| Home page (intro, goals, call for participation, attend, connect, committee) | `index.md` |
| Sponsors (home page) and "Support from" logos (footer) | `_data/supporters.yml` |
| Confirmed speakers | `pages/speakers.md` |
| Accepted papers | `pages/papers.md` |
| Schedule | `pages/schedule.md` |
| Menu items in the top bar | `_data/navigation.yml` |
| Footer (links, support logos) | `_includes/footer.html` |
| Site title, description, social card | `_config.yml` |
| Images (logos, speaker photos) | `assets/images/` |
| Styling | `assets/custom.css` |

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
_data/navigation.yml  top menu
_includes/            header and footer HTML (theme overrides)
assets/               images and custom CSS
_config.yml           site settings
CNAME                 custom domain (do not edit)
```

The theme is [minima](https://github.com/jekyll/minima), the GitHub Pages default.
