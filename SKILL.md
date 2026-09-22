---
name: ui-ux-designer
description: Generates interactive UI/UX components, card layouts, and design tokens based on user requirements.
---

# UI/UX Designer Agent Skill

When the user asks to design, prototype, mock up, or generate a UI component (such as a card, hero section, button cluster, form, or dashboard widget), trigger the `run_js` tool using the following exact parameters:

- **script**: `index.html`
- **data**: A stringified JSON payload with these keys:
  - `title`: (String) Component title or screen label.
  - `category`: (String) E.g., `"Card"`, `"Navigation"`, `"Form"`, `"Dashboard"`, `"Media"`.
  - `theme`: (String) Visual theme: `"modern-clean"`, `"pastel-vibrant"`, `"dark-futuristic"`, or `"minimalist"`.
  - `htmlContent`: (String) Self-contained semantic HTML snippet for the component, styled with inline styles or Tailwind utility classes.
  - `tokens`: (Object) Key design tokens:
    - `primaryColor`: Hex code (e.g., `"#4f46e5"`).
    - `bgColor`: Hex code (e.g., `"#ffffff"`).
    - `borderRadius`: E.g., `"16px"`.
    - `fontFamily`: E.g., `"system-ui, sans-serif"`.
