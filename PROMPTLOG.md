# Prompt Log

Original brief:

"Build a “Mini Component Library” in Pure CSS — single page showcasing components: Buttons (primary, secondary, disabled), Inputs + error states, Cards, Badges, Alerts, Navbar, Modal style. Use CSS variables for colors + spacing. Use a consistent naming convention. Deliver README, PROMPTLOG.md, LEARNINGS.md and deployed showcase."

---

## AI Output 1 — HTML scaffold for the showcase (suggested by AI)

Summary of AI output:

- A full `index.html` scaffold containing sections for Buttons, Inputs, Cards, Badges, Alerts, Navbar, and a checkbox-powered Modal.

What I accepted from the AI:

- The overall page structure and component sections.
- The idea to keep the modal purely CSS-driven using a checkbox toggle for minimal JS.
- Use of a simple, readable markup with component examples in place.

What I modified:

- Renamed and standardized classes with a `c-` prefix for consistent component scoping.
- Tightened markup semantics (ensured `article` was used for cards, `nav` for navigation, and labels/inputs grouped correctly).
- Added links and anchor targets in the navbar for the demo sections.

AI mistakes (>=3):

1. Accessibility omissions: the modal output lacked `aria-*` attributes, focus management, and a keyboard trap — checkbox toggle alone doesn't provide good a11y.
2. Interactive semantics: the AI used a `<label>` as a button trigger without explaining keyboard behavior or alternate activation methods for assistive tech.
3. Missing progressive enhancement notes: the scaffold didn't note JS fallback options for improved accessibility or focus handling.

---

## AI Output 2 — CSS variables and tokens (suggested by AI)

Summary of AI output:

- A `:root` token set with colors, spacing variables, radii, and shadows plus component styles for buttons, inputs, cards, badges, alerts, navbar, and modal.

What I accepted from the AI:

- The overall token approach: separate variables for colors and spacing and using them throughout components.
- Component names and many baseline styles (padding, border-radius, subtle shadows).

What I modified:

- Consolidated variable names to be consistent (e.g., `--space-*` and `--color-*`) and tuned some color opacity values for better contrast.
- Increased border-radius consistency and standardized small/medium radius tokens.
- Adjusted button focus/hover states for clearer affordance and added disabled styling.

AI mistakes (>=3):

1. Contrast and color accessibility: some suggested rgba overlays from the AI produced insufficient contrast for small text in a few states.
2. Inconsistent naming examples: the AI mixed naming styles in examples (BEM-like `__`/`--` plus other ad-hoc modifiers), requiring manual normalization.
3. Overly broad selectors: a few AI-proposed rules used element selectors that risk global side effects (I replaced these with component-scoped selectors).

---

## AI Output 3 — Modal pattern (pure-CSS recommendation)

Summary of AI output:

- A checkbox-toggle modal pattern that shows a modal when `#modal-toggle:checked` and hides otherwise — no JS.

What I accepted from the AI:

- The checkbox technique as a minimal, no-JS demonstration is valid for a showcase.
- Simple backdrop and centered panel layout were fine to illustrate styling only.

What I modified:

- Documented the accessibility trade-offs inline in this log and in `LEARNINGS.md`.
- Ensured the modal close control is clearly visible and added a visible focus outline for keyboard users (still recommends small JS for focus trap in production).
- Scoped modal styles to avoid accidental global overrides and used `id` selectors cautiously for the toggle.

AI mistakes (>=3):

1. Accessibility assumption: presenting the checkbox technique as a full solution without caveats (focus trap, screenreader announcements) is misleading.
2. Missing ARIA roles: AI output omitted `role="dialog"`/`aria-modal="true"` and labeling recommendations for the modal panel.
3. Keyboard interaction details were absent: the AI didn't propose an approach for closing the modal with `Esc` (requires JS) or verbal guidance for assistive users.

---

## Notes and next steps

- I kept the AI’s helpful structural suggestions and token ideas, but audited and fixed accessibility, naming, and contrast issues manually.
- For production usage, I recommend adding a small JS module for modal focus management and to improve keyboard behavior.
- To deploy: push the repo to GitHub and enable Pages, or use Netlify/Vercel.

# Prompt Log

Original brief:

"Build a “Mini Component Library” in Pure CSS — single page showcasing components: Buttons (primary, secondary, disabled), Inputs + error states, Cards, Badges, Alerts, Navbar, Modal style. Use CSS variables for colors + spacing. Use a consistent naming convention. Deliver README, PROMPTLOG.md, LEARNINGS.md and deployed showcase."

Notes about work performed:

- Implemented components in `index.html` and `styles.css`.
- Used `c-` prefix for component classes for consistency.
- Modal implemented using pure-CSS checkbox toggle to avoid JavaScript.
- Provided `README.md` with usage and simple deployment instructions.

Next actions (manual):

- Push repository to GitHub and enable Pages, or deploy to Netlify for a live demo.
