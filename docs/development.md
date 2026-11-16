# 🛠️ Development Guide

## 1. Source-of-truth files

- Edit page markup and copy in `docs/index.html`.
- Edit browser interaction in `main.js`.
- Edit Tailwind input and authored global CSS in `src/input.css`.
- Configure Tailwind scanning in `tailwind.config.js`.
- Treat `docs/style.css` as generated output from the configured Tailwind command.
- Keep `package.json` and `package-lock.json` synchronized.

## 2. Local environment

```bash
npm ci
npx serve docs
```

For CSS work, run `npm run tailwind` in a separate terminal.

## 3. Coding practices

### HTML
- Prefer semantic elements and native controls.
- Use unique IDs and keep anchor destinations synchronized.
- Maintain heading order and meaningful link text.
- Add useful image alternative text.

### JavaScript
- Keep functions small and explicit.
- Validate DOM assumptions before manipulating elements.
- Avoid unsafe insertion of user-controlled HTML.
- Keep control state accessible to keyboard and assistive-technology users.

### CSS
- Make authored changes in `src/input.css`.
- Keep responsive behavior in mind.
- Preserve visible focus styles and sufficient contrast.
- Regenerate `docs/style.css` after source changes.

## 4. Verification checklist

Check navigation anchors, service tabs, text wrapping, image loading, mobile layout, keyboard focus, and the contact form boundary using a local HTTP server. Keep test data synthetic. Inspect browser console and network requests.

Run `node --check main.js` after JavaScript changes. The CI workflow performs this basic syntax check.

## 5. Documentation and diagrams

Update the relevant guides when markup, behavior, assets, scripts, dependencies, or hosting assumptions change. Keep current-state diagrams separate from future service designs.

## 6. Pull request expectations

Use the repository template and include a concise problem statement, implementation summary, verification steps, accessibility/security considerations, and genuine screenshots for visible changes.

## 7. Avoid unnecessary architecture

Do not add a framework, server, database, or dependency just to increase the file count. Any such addition should solve a demonstrated need and include a maintenance and security plan.
