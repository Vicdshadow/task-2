# Mini Component Library — README

This repository contains a small, reusable component library built with pure CSS. The goal is to demonstrate consistent design tokens, CSS variables, and a small set of components you can copy into your projects.

Files

- `index.html` — component showcase and usage examples.
- `styles.css` — the library stylesheet with CSS variables and components.
- `PROMPTLOG.md` — original prompt and notes.
- `LEARNINGS.md` — reflection on what improved.

Principles

- CSS variables for colors and spacing
- Consistent naming with `c-` prefix (component-level classes)
- Pure CSS solutions where possible (modal uses checkbox toggle)

Quick preview
Open `index.html` directly in your browser, or serve it locally:

```powershell
# If you have Python installed (Windows PowerShell):
python -m http.server 8000; Start-Process "http://localhost:8000/index.html"
```

Component usage

- Buttons: use `class="c-btn"` with modifiers: `c-btn--primary`, `c-btn--secondary`.

  Example:

  ```html
  <button class="c-btn c-btn--primary">Primary</button>
  ```

- Inputs: `.c-input`, error state: `.c-input--error`. Wrap input in `.c-field` and include `.c-field__help--error` for error messages.

  Example:

  ```html
  <label class="c-field">
    <span class="c-field__label">Email</span>
    <input class="c-input" />
    <span class="c-field__help c-field__help--error">Required</span>
  </label>
  ```

- Cards: `.c-card`, elevated variant `.c-card--elevated`.

- Badges: `.c-badge`, modifiers `.c-badge--accent`, `.c-badge--pill`.

- Alerts: `.c-alert` and state modifiers `.c-alert--success`, `.c-alert--error`, `.c-alert--warning`.

- Navbar: `.c-navbar`, brand `.c-navbar__brand`, links `.c-navbar__link`.

- Modal (pure CSS): Use the checkbox pattern shown in `index.html`. The visible modal is controlled by `#modal-toggle`.

Deploying

- GitHub Pages: push this folder to a repo and enable Pages from the `main` branch (or `gh-pages` branch).
- Netlify: drag-and-drop the folder or connect the repo.

Next steps / suggestions

- Extract variables to a small `tokens.css` if you plan multiple themes.
- Add a tiny build step (PostCSS) for autoprefixing and minification if needed.
