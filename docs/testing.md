# 🧪 Testing and Verification Strategy

## 1. Current test baseline

The repository currently contains a static HTML/CSS/JavaScript page and npm development tooling. No dedicated unit-test framework, browser automation suite, test directory, or application test command is declared in the package scripts. This guide defines repeatable manual checks and a safe path for adding automated checks without claiming that they already exist.

## 2. Local verification

Install the exact dependency graph:

```bash
npm ci
```

Run the Tailwind watcher in a separate terminal when validating style-source changes:

```bash
npm run tailwind
```

Serve the static page over HTTP:

```bash
npx serve docs
```

## 3. Manual smoke-test matrix

| Area | Check | Expected result |
|---|---|---|
| Page load | Open the served page | HTML renders without a blank page |
| Assets | Inspect logo, stylesheet, fonts and images | Every referenced local asset resolves |
| Navigation | Activate each navigation link | The intended section is reached |
| Tabs | Activate every tab using mouse and keyboard | The matching panel is visible; no console exception |
| Contact form | Inspect form behavior without sending real personal data | No false success message or claim of delivery |
| Responsive | Test narrow and wide viewports | No unintended horizontal overflow |
| Keyboard | Tab through controls | Focus is visible and order is logical |
| Console | Inspect browser developer console | No uncaught JavaScript errors or missing resource errors |
| Links | Follow internal and external links | Targets are valid and accurately described |

## 4. Accessibility checks

- Navigate the entire page without a mouse.
- Confirm every interactive element can receive focus.
- Confirm focus indicators are visible.
- Verify headings are nested in a logical order.
- Check form controls have programmatic labels.
- Verify images have appropriate alternative text.
- Check color contrast for text and controls.
- Confirm tab panels expose the correct relationship to their controls.
- Test browser zoom and reflow.

Automated accessibility tools can help find issues, but they do not replace keyboard and screen-reader testing.

## 5. Static quality checks

The following checks are suitable for a future CI workflow:
- `node --check main.js`
- Confirm the expected HTML, CSS, JS and logo files exist.
- Parse package metadata as JSON.
- Check Markdown links and image paths.
- Validate YAML workflow syntax.
- Review Mermaid diagrams in GitHub's renderer.

Do not report a check as passed until it has actually run in CI or locally.

## 6. Regression evidence

For UI changes, record:
- Browser and viewport used.
- Steps performed.
- Expected and observed result.
- Console/network errors.
- Screenshot evidence when available and actually captured.

## 7. Future automated test options

A small static site can begin with HTML validation and link checks. Add Playwright or another browser runner only when there are meaningful interaction flows to automate. Keep dependencies proportionate to the size of the project and document setup commands before making CI depend on them.
