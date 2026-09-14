# Copilot instructions

## Project overview

This repository is a small static CV site published through GitHub Pages at
https://koukasen.github.io/rsschool-cv/.

- `cv.md` is the main CV content and includes the personal photo reference,
  contact details, skills, education, work history, and code example.
- `index.html` is the browser entry point and links to `style.css`. It currently
  contains an empty `.container` and references `js/scripts.js`; check whether
  those pieces are present or intentionally pending before changing the page
  structure.
- `style.css` contains the site styling.
- `photo-personal.jpg` is the image used by the CV content.

Keep links and asset paths compatible with a GitHub Pages deployment from the
repository subpath `/rsschool-cv/`. Preserve the existing public contact links
and image references unless the requested change explicitly updates CV data.

## Build, test, and lint

There is no package manifest, build system, test suite, or lint configuration in
the repository. Changes are served as static files directly by GitHub Pages.

For a local browser check, run:

```sh
python3 -m http.server 8000
```

Then open `http://localhost:8000/`. There is no single-test command; manually
check the affected HTML/CSS/Markdown behavior in the browser. For content-only
changes, inspect the rendered Markdown or the corresponding deployed page.

## Repository conventions

- Use plain HTML and CSS; do not introduce a framework, bundler, or dependency
  manager for a small site change without an explicit requirement.
- Keep the document language, metadata, stylesheet link, and relative asset
  paths consistent with `index.html`.
- Treat `cv.md` as structured resume content: preserve its section order and
  Markdown heading/list style when editing existing sections.
- Keep CSS changes in `style.css` and avoid inline styles unless the requested
  integration requires them.
- Verify that referenced files actually exist. In particular, do not assume the
  `js/scripts.js` reference in `index.html` is backed by a present JavaScript
  file.
