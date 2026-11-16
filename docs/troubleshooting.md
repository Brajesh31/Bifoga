# 🧯 Troubleshooting

## 1. The page does not load

- Confirm the static server is serving the `docs/` directory.
- Open the local URL printed by the server.
- Inspect the browser network panel for 404 or blocked requests.
- Do not assume the site works correctly from a `file://` URL.

## 2. Styles are missing or outdated

1. Confirm `docs/style.css` exists.
2. Check the stylesheet path in `docs/index.html`.
3. If Tailwind source changed, run `npm run tailwind`.
4. Confirm the watcher reads `src/input.css` and writes `docs/style.css`.
5. Hard-refresh the browser if stale CSS is cached.

## 3. Logo or image is missing

- Verify the file exists in the repository.
- Check path casing.
- Resolve relative paths from the served HTML document.
- Do not reference an asset that has not been committed.

## 4. Tailwind classes do not appear

Check `tailwind.config.js` content paths. New HTML files must be included in the scan. Keep the watcher running while editing and inspect generated `docs/style.css`.

## 5. Service tabs do not switch

The existing source has several known wiring issues:
- The page's script reference is written as a stylesheet link.
- Tab calls pass `Eat` and `Drinks`, while the actual panel IDs are `consultation` and `education`.
- The helper's loop for tab styling uses the panel count.
- The tab controls should be reviewed for semantic and keyboard behavior.

These are documented defects, not fixes performed by this documentation work.

## 6. Contact submission fails

The `/action_page.php` endpoint is not provided by this repository. A static host does not create that endpoint. Use a reviewed form provider or backend implementation before enabling real submissions.

## 7. npm installation fails

- Check Node.js and npm versions.
- Use `npm ci` with the committed lockfile.
- Read the first meaningful npm error.
- Do not delete `package-lock.json` to bypass dependency resolution.
- Review package changes before committing.

## 8. CI fails

Open the failing workflow run and inspect the exact step. The current CI checks syntax, package metadata, and required files; the dependency audit can fail when high-severity advisories exist. A failing audit should be investigated, not suppressed without review.
