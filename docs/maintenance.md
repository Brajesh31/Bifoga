# 🔧 Maintenance Guide

## Routine maintenance

### When HTML changes
- Verify semantic structure and heading order.
- Check navigation targets and form labels.
- Check local image and stylesheet paths.
- Review keyboard operation and responsive reflow.

### When CSS changes
- Edit `src/input.css`.
- Run `npm run tailwind`.
- Review generated `docs/style.css`.
- Test focus visibility, contrast, and narrow viewport behavior.

### When JavaScript changes
- Run `node --check main.js`.
- Test all interaction paths in a browser.
- Check console errors and keyboard support.
- Avoid unsafe DOM insertion.

### When dependencies change
- Update package metadata and lockfile together.
- Review package purpose, maintenance status, license, and security advisories.
- Run CI and inspect the resulting diff.

## Periodic review

At a practical cadence, review:
- Dependency advisories and unused packages.
- External fonts and stylesheets.
- Broken links and stale documentation.
- Accessibility and performance.
- Hosting configuration and TLS status.
- Security reporting and support instructions.

## Documentation ownership

The documentation should be updated in the same change as the implementation. Remove outdated instructions only after confirming that no current workflow depends on them.
