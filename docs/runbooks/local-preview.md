# ▶️ Runbook: Local Preview

## Purpose

Start the static EnClose website locally and inspect the page without changing the production deployment.

## Steps

1. Clone the repository and enter its root directory.
2. Confirm Node.js and npm are installed.
3. Install locked dependencies:

   ```bash
   npm ci
   ```

4. Start a static server:

   ```bash
   npx serve docs
   ```

5. Open the local URL printed by the server.
6. If editing Tailwind styles, run the watcher in another terminal:

   ```bash
   npm run tailwind
   ```

7. Refresh the page and inspect the browser console and network panel.

## Troubleshooting

- If the page is not found, confirm the server root is `docs/`.
- If styles are missing, check the HTML stylesheet path and the existence of `docs/style.css`.
- If a local image is missing, verify its path relative to the HTML document.
- If npm installation fails, check Node/npm compatibility and rerun `npm ci` after reviewing the error.

## Exit criteria

The page loads, local assets resolve, navigation works as expected, and no new console errors appear. This runbook does not validate production hosting.
