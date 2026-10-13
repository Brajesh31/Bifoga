# Troubleshooting

## Styles or the logo are missing

Serve `docs/` from a local HTTP server and verify that `/style.css` and `/img/logo.png` resolve relative to the document root.

## Tailwind changes do not appear

Run `npm run tailwind` and confirm it is watching `src/input.css` and writing `docs/style.css`.

## Service tabs do not switch

Confirm `main.js` is loaded and that the tab markup uses matching element IDs. The current page has a prototype-level mismatch between some tab labels and panel identifiers that should be corrected as part of future UI work.

## Contact submission fails

The `/action_page.php` endpoint is not provided by this repository. Use a reviewed backend endpoint before enabling submissions.
