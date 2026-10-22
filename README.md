# Owen McGinty — Personal Website

A small, dependency-free static personal website. Plain HTML and CSS, no build
step, and no JavaScript. The design is intentionally easy to reuse as a
template: change the custom properties at the top of `styles/style.css` and edit
the content directly in the HTML files.

## Pages

| File | Contents |
| --- | --- |
| `index.html` | About and research/teaching experience |
| `research.html` | Research projects and interests |
| `teaching.html` | Teaching experience and curriculum |
| `courses.html` | Graduate and undergraduate coursework |
| `assets/owen-mcginty-resume.pdf` | Downloadable CV |

## Preview locally

From this directory:

```sh
python3 -m http.server 8000
```

Then open <http://localhost:8000>. Alternatively, run `npm start`, which uses the
same command. There is nothing to install or build.

## Editing

- **Colors, fonts, and width:** edit the custom properties in `:root` at the top
  of `styles/style.css`. Dark-mode overrides live in the
  `prefers-color-scheme: dark` block just below.
- **Navigation and footer:** these are repeated in each HTML file by design, so
  the site works without a templating engine. Update all pages when changing a
  nav link.
- **Content:** edit the HTML directly. Entries use a small, consistent structure:
  `.entry`, `.entry-head`, `.entry-meta`, `.entry-sub`, and `.bullets`.
- **CV:** replace `assets/owen-mcginty-resume.pdf` with an updated PDF, keeping
  the same filename (or update the links in the header and footer).
- **Year:** update the copyright year in each footer when needed.

## Deploying

This repository is set up for GitHub Pages at `omcginty.github.io`. Push the
files to the branch GitHub Pages serves (typically `main` or `master`); the site
is served from the repository root, with no build step.

## Design notes

- Single-column, responsive layout with a 46rem reading measure
- System serif and sans-serif stacks; no web-font downloads
- Automatic light and dark themes via `prefers-color-scheme`
- Print styles that hide navigation and expose link URLs
- Skip link, visible focus states, and semantic headings throughout
