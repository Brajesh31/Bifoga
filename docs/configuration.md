# ⚙️ Configuration Guide

## 1. Configuration model

Bifoga's current application is a static browser-delivered website. It does not have a server-side runtime configuration layer, database connection, authentication provider, or deployed API configuration.

Configuration is currently split across source files and build tooling:

| Location | Responsibility | When to change it |
|---|---|---|
| `package.json` | Project metadata and npm scripts | When scripts or development dependencies change |
| `package-lock.json` | Exact dependency resolution | Commit updates produced by npm |
| `tailwind.config.js` | Tailwind content scanning and theme configuration | When utility classes or theme extensions change |
| `src/input.css` | CSS entry point and authored global styles | When global styles or Tailwind layers change |
| `docs/index.html` | Page content, links and markup | When page content or structure changes |
| `main.js` | Browser-side menu/tab helper | When the existing interaction changes |
| `.env.example` | Documentation of an optional future contact endpoint setting | Only relevant if a form integration is implemented |

## 2. Runtime environment

The published page is intended to run in a modern browser and be served over HTTP or HTTPS. No Node.js process is required by a static host after the files have been built.

Node.js and npm are development tools used to install dependencies and run the Tailwind watcher. Use a supported, maintained Node.js LTS release compatible with the lockfile and installed Tailwind toolchain. The repository does not currently declare an `engines` range, so do not treat a specific Node version as a tested project guarantee.

## 3. Environment variables

The current page does not read environment variables in browser code. Never put credentials, private API keys, database passwords, or privileged tokens into HTML, CSS, JavaScript, or a public `.env` file.

The existing `.env.example` mentions `CONTACT_FORM_ENDPOINT` as a possible endpoint setting. It is not evidence that the form is wired to a working service. The current form action is a placeholder and must not be represented as a configured integration.

If a future backend is introduced:
1. Define server-side variables in the backend's deployment environment.
2. Validate required variables at process startup.
3. Keep secrets out of client bundles and Git history.
4. Document variable purpose, format, required/optional status, and safe example values.
5. Provide a separate local-development configuration example without real credentials.

## 4. Tailwind CSS workflow

The npm script named `tailwind` runs Tailwind in watch mode, reads `src/input.css`, scans the configured HTML content, and writes the generated stylesheet to `docs/style.css`.

Run:

```bash
npm ci
npm run tailwind
```

Keep generated CSS output and the input stylesheet conceptually separate. Make authored design changes in `src/input.css` and the Tailwind configuration, not by manually patching generated output unless the build strategy is deliberately changed.

## 5. Safe configuration changes

- Review the package diff before committing lockfile changes.
- Do not commit local secrets or machine-specific paths.
- Verify the Tailwind content glob includes every HTML file that uses utility classes.
- Confirm the stylesheet output path matches the stylesheet link in the page.
- Test the production static directory after changing build paths.
- Record any new configuration in this guide and the root README.

## 6. Current configuration gaps

- No formal Node.js engine range is declared.
- No production build script is declared in the current package scripts.
- No server-side configuration loader exists.
- The contact endpoint is not implemented by the repository.
- The Tailwind watcher is a development process, not a production server.

These are observations of the current repository, not claims that the missing capabilities are already available.
