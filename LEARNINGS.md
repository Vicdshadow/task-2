# Learnings

What I improved while building this mini library:

Potential improvements in follow-ups:

```markdown
# Learnings

What I improved while building this mini library:

- Design tokens clarify decisions: extracting colors and spacing into `:root` variables made it easy to enforce consistent rhythm and quickly iterate on color themes.
- Naming convention matters: choosing a single convention (`c-` prefix with BEM-like `__` and `--`) reduced ambiguity when composing classes and avoided global selector collisions.
- Prompt engineering is iterative: short, specific prompts produce useful scaffolds, but follow-up prompts must request accessibility checks, naming rules, and edge cases.
- Pure CSS techniques (checkbox toggle) are useful for demos, but I learned to always call out accessibility trade-offs and recommend small JS for production polish.
- Testing visually early: opening the page and inspecting color contrast/focus states early caught issues the AI didn't highlight.

Concrete next skills to practice:

- Add minimal JS for modal focus trap and `Esc` handling while keeping the CSS-first approach.
- Add automated contrast checks and a simple a11y checklist to the prompt when asking the AI for UI code.
- Expand the token system to support theming (`data-theme` or CSS media queries) and publish a small `tokens.md` to accompany the library.

Short checklist I used while auditing AI outputs:

1. Naming consistency across files (`--color-*`, `--space-*`, `c-` prefix).
2. Focus styles and keyboard affordances for interactive controls.
3. Color contrast for small text and alert borders.
4. Avoid global element selectors that could leak styles into consumer pages.
```
