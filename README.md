https://img.shields.io/badge/version-1.0.0-blue

# Git Flow Lab

[![version](https://img.shields.io/badge/version-1.0.0-blue)](https://github.com/goti13/Git-Flow-Easy-Project/releases/tag/v1.0.0)

A minimal project for practising Git branching workflows, featuring a
fixed navigation bar and an accessible dark mode toggle.

---

## Project Structure

| File            | Purpose                              |
|-----------------|--------------------------------------|
| `index.html`    | Page markup, nav header, landmarks   |
| `styles.css`    | Authored styles (light + dark theme) |
| `styles.min.css`| Minified production stylesheet       |
| `script.js`     | Dark mode toggle behaviour           |
| `README.md`     | Project documentation                |

---

## Features

### Navigation Bar
A fixed header with a brand name and four nav links.
Stays visible while scrolling; content is offset with `padding-top`.

### Dark Mode Toggle
A **🌙 Dark Mode** button in the top-right corner of the nav bar.

| Detail | Implementation |
|--------|---------------|
| Trigger | Click `#theme-toggle` button |
| Mechanism | Flips `data-theme="dark"` on `<body>` |
| Styling | CSS `[data-theme="dark"]` attribute selectors |
| Transition | 250 ms ease on `background` and `color` |
| Contrast | WCAG AA compliant (min 4.5 : 1 ratio) |
| Accessibility | `aria-label="Toggle dark mode"` on button |

---

## Git Flow Branch History

| Branch                  | Purpose                                     |
|-------------------------|---------------------------------------------|
| `main`                  | Production-ready code, tagged releases      |
| `develop`               | Integration branch for features             |
| `feature/nav`           | Added header and navigation bar             |
| `feature/dark-mode`     | Added JS dark mode toggle                   |
| `hotfix/contrast-text`  | Fixed WCAG AA contrast in dark mode (1.0.1) |
| `release/1.0.0`         | Release polish — lint, minify, docs         |

---

## Getting Started
```bash
# Clone
git clone https://github.com/youruser/web-lab.git
cd web-lab

# Serve locally (Python)
python3 -m http.server 8080

# or with Node
npx serve .
```

Open `http://localhost:8080` in your browser.

---

## Release Notes

### v1.0.0 — Initial Release
- Fixed navigation bar with brand and links
- Dark mode toggle with WCAG AA contrast
- Accessible landmarks (`<main>`, `aria-label`)
- Minified production stylesheet

### v1.0.1 — Hotfix
- Improved dark mode text contrast for WCAG AA compliance
