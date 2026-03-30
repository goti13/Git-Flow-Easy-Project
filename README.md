

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

<img width="1260" height="858" alt="image" src="https://github.com/user-attachments/assets/a3c458e9-1e73-436f-b279-52fecc498860" />

<img width="1258" height="920" alt="image" src="https://github.com/user-attachments/assets/73d6d368-af83-4c22-820f-020207948d92" />

<img width="1260" height="864" alt="image" src="https://github.com/user-attachments/assets/461630b1-0127-400d-883a-af7ae7fc8f5b" />

<img width="1268" height="914" alt="image" src="https://github.com/user-attachments/assets/e9790889-76f4-403d-a421-3bb24f28045b" />

<img width="1268" height="956" alt="image" src="https://github.com/user-attachments/assets/53d4bbbf-5fac-48db-8681-64049b03cc0c" />

<img width="1250" height="428" alt="image" src="https://github.com/user-attachments/assets/601ea992-6a78-4f09-acf7-b4a5ef2c4e93" />


<img width="1262" height="1076" alt="image" src="https://github.com/user-attachments/assets/a5e4fe01-cfea-4d42-8d01-df842c3fc6ae" />


<img width="1268" height="322" alt="image" src="https://github.com/user-attachments/assets/c04bbdab-da7f-4537-9cb5-3da53b6c2399" />

<img width="1290" height="234" alt="image" src="https://github.com/user-attachments/assets/d58150ef-d00a-442d-9e3c-264c2512c40c" />

<img width="1280" height="1302" alt="image" src="https://github.com/user-attachments/assets/287ee5e4-9f58-42cd-9b12-4920faa531b8" />


<img width="1268" height="1272" alt="image" src="https://github.com/user-attachments/assets/a118b160-8e75-4ad4-beab-92ff005bec39" />


<img width="1250" height="518" alt="image" src="https://github.com/user-attachments/assets/9eb77890-789f-42ba-aece-6be30968dbf3" />











