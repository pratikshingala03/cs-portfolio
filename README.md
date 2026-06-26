# Pratik Shingala — Computer Science Portfolio

**🔗 Live site:** https://pratikshingala03.github.io/cs-portfolio
**📁 Repository:** https://github.com/pratikshingala03/cs-portfolio

<p align="center">
  <img src="https://github.com/pratikshingala03/cs-portfolio/blob/main/docs/screenshots/portfolio-hero.png" alt="Portfolio home page" width="100%">
</p>

## Overview

This portfolio is a single-page website designed as a concise technical showcase for a working-student application. Rather than describing skills in the abstract, the site *is* the evidence: the source code, the commit history, and the presentation are all part of what is on display. It is built to be readable by a hiring manager in a couple of minutes and inspectable by anyone who opens the repository.

## Features

- **Responsive, single-page layout** — fluid design that adapts from desktop down to mobile, with a fixed glass navigation bar and smoothly anchored sections.
- **About Me** — a short professional profile, core toolkit, strengths, and languages.
- **Technical exercises** — representative work across SQL database queries, Python data analysis, dashboards, and security/CTF write-ups (Advent of Cyber).
- **Embedded CV** — a one-page curriculum vitae compiled from LaTeX, viewable inline on the page and downloadable as a PDF.
- **Accessible & self-contained** — semantic HTML, visible keyboard focus, reduced-motion support, and no external dependencies or network calls.

### Technical exercises

<p align="center">
  <img src="https://github.com/pratikshingala03/Restaurant-Management-System" alt="Technical exercises section" width="100%">
</p>

### LaTeX CV

<p align="center">
  <img src="https://github.com/pratikshingala03/cs-portfolio/blob/main/cv/main.tex" alt="Embedded LaTeX CV" width="100%">
</p>

### Mobile view

<p align="center">
  <img src="https://github.com/pratikshingala03/cs-portfolio/blob/main/docs/screenshots/portfolio-mobile.png" alt="Responsive mobile layout" width="320">
</p>

## Tech stack

| Area | Technology |
|------|------------|
| Structure | HTML5 (semantic) |
| Styling | CSS3 (modular, responsive) |
| Behaviour | Vanilla JavaScript (progressive enhancement) |
| Documents | LaTeX (CV and project report) |
| Version control | Git |
| Hosting | GitHub Pages |

No frameworks or build tools are used: the site is intentionally lightweight, fast to load, and easy to maintain.

## Repository structure

```
cs-portfolio/
├── index.html                 # the portfolio (self-contained)
├── README.md                  # this file
├── docs/
│   └── screenshots/           # images used in this README
├── cv/
│   ├── cv.tex                 # LaTeX source of the CV
│   └── Pratik_Shingala_CV.pdf # compiled CV
├── exercises/
│   ├── python/                # data-processing scripts
│   ├── sql/                   # schema and example queries
│   └── network/               # network-scanning scripts
└── report/
    ├── report.tex             # B201 project report
    └── references.bib         # Harvard-style bibliography
```

## Run locally

The site is a single static file with no build step. Either open it directly:

```bash
# clone the repository
git clone https://github.com/pratikshingala03/cs-portfolio.git
cd cs-portfolio

# open index.html in your browser, or serve it locally:
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Build the documents (LaTeX)

The CV and the project report are compiled with a standard TeX distribution (TeX Live, MiKTeX, or Overleaf).

```bash
# Curriculum vitae
cd cv
pdflatex cv.tex
pdflatex cv.tex        # run twice so cross-references resolve

# Project report (uses natbib for Harvard-style references)
cd ../report
pdflatex report.tex
bibtex   report
pdflatex report.tex
pdflatex report.tex
```

## Deployment

The site is hosted on **GitHub Pages** directly from the `main` branch:

1. Push the repository to GitHub.
2. Go to **Settings → Pages**.
3. Under **Source**, choose the `main` branch and the `/ (root)` folder, then **Save**.
4. The site goes live at `https://pratikshingala03.github.io/cs-portfolio/` within a minute or two.

Because deployment is driven from version control, the live site always reflects the latest commit on `main`.

## Roadmap

- Add a GitHub Actions CI/CD workflow (HTML/CSS linting, link checking, Lighthouse audits) before each deploy.
- Add a dark/light theme toggle using CSS custom properties.
- Introduce a dynamic blog/writing section generated from Markdown.
- Expand the technical exercises into fuller, tested projects with documentation.

## License

Released under the MIT License — see `LICENSE` for details.

## Contact

**Pratik Shingala** — Berlin, Germany
✉️ Pratikshingala03@gmail.com
