# Contributing to cssapi.dev

Thank you for helping improve cssapi.dev.

## 1. Core Principles

- **Standards-first**: Native HTML, CSS, and JS only.
- **Separation of concerns**  
  - HTML = structure and semantics  
  - CSS = presentation and UI/data state logic  
  - JS = data retrieval, normalization, and delivery only (no DOM manipulation for UI)
- **Agnostic by design**: Data-, framework-, platform-, and browser-agnostic.
- **Declarative UI**: Prefer native states and selectors (`:has()`, `:empty`, `open`, `:checked`, `aria-*`) over classes, IDs, or data attributes.

## 2. HTML / CSS / JS Rules

- **HTML**
  - Use meaningful semantic elements.
  - Avoid `id`, `class`, and `data-*` wherever possible.
  - No framework-specific markup or attributes.

- **CSS**
  - Use modern features (custom properties, `:has()`, `:empty`, container queries, `clamp()`, `color-mix()`, etc.).
  - CSS controls UI and data state; no JS-duplicated state.
  - Prefer composable tokens and “CSS API” patterns over one-off rules.

- **JS**
  - Data-only: fetch, normalize, and deliver JSON or config.
  - No UI state, no DOM querying for styling, no templating.
  - Configuration lives in data (JSON/modules), not hardcoded in markup.

## 3. How to Contribute

1. **Open an issue** describing the bug, idea, or enhancement.
2. **Fork and branch**: `feature/short-description` or `fix/short-description`.
3. Keep changes small, focused, and **architecture-compliant**.
4. Update or add minimal documentation where behavior changes.
5. Open a Pull Request and:
   - Link the related issue.
   - Briefly describe the change, assumptions, and any trade-offs.

## 4. PR Checklist

Before submitting:

- [ ] Follows HTML/CSS/JS separation rules above.
- [ ] No framework dependencies introduced.
- [ ] No new IDs/classes/data-* used as primary state hooks.
- [ ] Behavior is driven by HTML semantics + CSS, not JS UI logic.
- [ ] Docs updated if the public “CSS API” changed.

By keeping contributions small, standards-based, and declarative, we preserve cssapi.dev as a clean, trustworthy reference for a CSS-driven UI API.
