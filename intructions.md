# Git Flow Easy

## 1 ▸ Introduction

Welcome to the next level! In this lab you will practise **Git Flow** while building a *tiny* front‑end project consisting of three files:

```
web-lab/
├── index.html   # structure & content
├── styles.css   # presentation layer
├── script.js    # behaviour / interaction
└── readme.md      # project documentation
```

By the end you will have:

- A Git repository that follows the Git Flow branching model.
- A functioning web page that you can open locally in the browser.
- A clean history of commits pushed to GitHub.

> **Key idea:** Treat each small change to your site as a discrete, well‑named commit. This habit will save you (and your teammates) endless time when something breaks!
> 

---

## 2 ▸ Prerequisites

- **VS Code** or another code editor
- **Git CLI** (installed and added to PATH)
- **GitHub account** (or other remote service)
- A modern browser for previewing `index.html`

---

## 3 ▸ Scaffolding the Project & Initial Commit

### 3.1 Create the folder and files

```bash
mkdir web-lab && cd web-lab
code .               # or open the folder with your editor

touch index.html styles.css script.js
```

### 3.2 Add minimal content

`*index.html*`

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Git Flow Lab</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <h1>Hello, Git Flow 👋</h1>
    <script src="script.js"></script>
  </body>
</html>
```

`*styles.css*`

```css
body {
  font-family: system-ui, sans-serif;
  margin: 0;
  padding: 2rem;
  background: #f6f8fa;
}
```

`*script.js*`

```jsx
console.log("JS is connected! 🚀");
```

### 3.3 Initialize Git & first commit

```bash
git init
git add .
git commit -m "chore: project scaffold (HTML, CSS, JS)"
```

You have just placed the three files in your **Working Tree**, staged them, and recorded them in the **Local Repository**.

---

## 4 ▸ Connecting to GitHub

```bash
git remote add origin <your‑repo‑url>
git branch -M main      # rename default branch to main (if needed)
git push -u origin main
```

Check the repository page on GitHub – your first commit should be visible.

---

## 5 ▸ Introducing Git Flow (Basic)

Git Flow proposes *long‑lived* branches:

- **`main`** – production‑ready code only
- **`develop`** – integration branch for completed features

…and *short‑lived* supporting branches:

- **`feature/*`** – new developments
- **`release/*`** – pre‑production hardening
- **`hotfix/*`** – emergency fixes to `main`

In this lab we implement a *light* version.

### 5.1 Create & push the `develop` branch

```bash
git checkout -b develop
git push -u origin develop
```

---

## 6 ▸ Exercises

Each numbered exercise should be completed in its **own branch**, merged into **`develop`**, and finally merged into **`main`** once release‑ready. Keep commit messages concise and conventional (e.g. `feat:`, `fix:`, `docs:`).

### Exercise 1 — Add a Header Banner (`feature/header-banner`)

1. **Branch**
    
    ```bash
    git checkout -b feature/header-banner
    ```
    
2. **Code** – Insert a `<header>` element with a navigation bar in `*index.html*`, style it in `*styles.css*`.
3. **Commit & Push**
    
    ```bash
    git add .
    git commit -m "feat: add header banner with nav links"
    git push -u origin feature/header-banner
    ```
    
4. **Pull Request** – Open a PR on GitHub targeting `develop`, review, and merge.

### Exercise 2 — Responsive Button Interaction (`feature/cta-button`)

1. Create a button inside the header that toggles a dark theme.
2. Add JS in `*script.js*` to listen for clicks and flip a `data-theme` attribute on `<body>`.
3. Update `*styles.css*` to style `[data-theme="dark"]`.
4. Document the new behaviour in `*README.md*`.

    ```bash
    git add .
    git commit -m "message"
    git push
    make a pull request to develop branch
    ```

### Exercise 3 — Accessibility Fix (`fix/contrast-text`) *(Hot fix)*

Your teammate spots poor text contrast in dark mode.

1. Checkout from `main` (production) for a hotfix:
    
    ```bash
    git checkout main
    git checkout -b hotfix/contrast-text
    ```
    
2. Improve CSS colours.
3. Increment version number in `*index.html*` comment.
4. Commit, merge into `main`, then back‑merge into `develop`:
    
    ```bash
    git add styles.css
    git commit -m "fix: improve contrast in dark mode"
    git push -u origin hotfix/contrast-text
    
    # PR into main → merge
    git checkout develop
    git merge main
    git push
    ```
    

### Challenge — Release `v1.0.0`

- From `develop`, create `release/1.0.0`.
- Polish: lint HTML, minify CSS, update README.
- Merge into `main`, tag `v1.0.0`, push.

---

## 7 ▸ Using `.gitignore`

Create a file named `.gitignore` at the project root and add common front‑end exclusions:

```
# dependencies
node_modules/

# build output
/dist
*.log
.DS_Store
.env
```

Commit with `chore: add .gitignore`.

---

## 8 ▸ Helpful Commands Reference

| Action | Command |
| --- | --- |
| View commit graph | `git log --oneline --graph --decorate --all` |
| Amend last commit (message only) | `git commit --amend -m "new msg"` |
| List remote branches | `git branch -r` |
| Delete remote branch | `git push origin --delete <branch>` |
| Stash incomplete work | `git stash && git stash pop` |

---

## 9 ▸ Submission Checklist

1. **Repository link** (even if it's private).
2. Screenshots (or a Loom/GIF) demonstrating:
    - Running site in browser.
    - `git log --graph` illustrating branch merges.
3. A short write‑up (max ½ page) answering:
    - "What problem does Git Flow solve for teams?"
    - "Which Git command did you find most useful and why?"

> 🏁 **Celebrate** – you have implemented a mini web project *and* practised a professional branching strategy. Push onward to bigger things! 🚀
>
