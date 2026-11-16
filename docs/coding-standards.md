# 📐 Coding Standards

## HTML

- Prefer semantic HTML5 elements.
- Keep IDs unique and stable.
- Use headings in logical order.
- Use buttons for actions and links for navigation.
- Associate labels with form controls.
- Provide appropriate alternative text for images.
- Avoid malformed nesting and obsolete presentational markup.

## JavaScript

- Use clear function and variable names.
- Keep functions focused and side effects explicit.
- Validate elements before accessing properties.
- Avoid global variables unless the page's current architecture requires them.
- Prefer safe text insertion over HTML string injection.
- Keep interactions keyboard accessible.
- Do not add a library for a trivial DOM operation.

## CSS and Tailwind

- Keep authored CSS in `src/input.css`.
- Use the configured Tailwind pipeline.
- Avoid editing generated CSS as the source of truth.
- Preserve visible focus styles.
- Check responsive behavior and contrast.
- Avoid unnecessary animation and respect reduced-motion preferences.

## Dependencies and configuration

- Use npm and the committed lockfile.
- Keep `package.json` and `package-lock.json` synchronized.
- Document new scripts and environment variables.
- Never commit secrets or machine-specific configuration.

## Documentation

- Use meaningful emojis, not decorative noise.
- Use consistent heading hierarchy.
- Add diagrams only when they clarify actual behavior.
- Label proposed architecture clearly.
- Do not invent test results, APIs, screenshots, metrics, or capabilities.
- Update the documentation hub when adding or renaming guides.
