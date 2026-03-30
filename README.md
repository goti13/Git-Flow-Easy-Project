# Git Flow Lab

A minimal project for practising Git branching workflows.

## Project Structure

| File | Purpose |
|------|---------|
| `index.html` | Page markup and nav header |
| `styles.css` | Light and dark theme styles |
| `script.js` | Theme toggle behaviour |

## Features

### Dark Mode Toggle

A **🌙 Dark Mode** button sits in the top-right corner of the navigation bar.

**How it works**

1. Clicking the button reads the current `data-theme` attribute on `<body>`.
2. If the value is `"dark"`, it switches back to `"light"` (and vice-versa).
3. CSS attribute selectors (`[data-theme="dark"]`) apply the dark palette —
   no class juggling, no JavaScript style mutations.
4. A `transition` on `body` smooths the background and colour change over 250 ms.

**Extending themes**

To add more themes, define new `[data-theme="your-theme"]` blocks in
`styles.css` and update the toggle logic in `script.js` to cycle through them.

## Getting Started
```bash
# Serve locally (Python)
python3 -m http.server 8080

# or with Node
npx serve .
```

Open `http://localhost:8080` in your browser.
