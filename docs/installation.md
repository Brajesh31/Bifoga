# 🚀 Installation and Local Setup

## 1. Prerequisites

- Git.
- Node.js with npm.
- A modern browser.
- A terminal with permission to install npm packages.

The repository does not currently declare a formal Node.js `engines` range. Use a maintained Node.js LTS release compatible with the locked dependencies.

## 2. Clone the repository

```bash
git clone https://github.com/Brajesh31/Bifoga.git
cd Bifoga
```

## 3. Install dependencies

Use the committed lockfile for a reproducible installation:

```bash
npm ci
```

If installation fails, inspect the npm error and Node.js version before changing package metadata. Do not delete the lockfile as a troubleshooting shortcut.

## 4. Preview the website

The page is served from the `docs/` directory:

```bash
npx serve docs
```

Open the local URL printed by the command. Use an HTTP server rather than a `file://` URL because the page contains root-relative paths and browser resource requests.

## 5. Develop Tailwind styles

In a second terminal:

```bash
npm run tailwind
```

The configured script watches `src/input.css` and writes `docs/style.css`. Keep the watcher running while changing Tailwind source. The generated stylesheet is part of the deployed page.

## 6. Format HTML

The package defines a `prettier` script:

```bash
npm run prettier
```

Review the resulting diff before committing. Formatting should not silently change content or remove meaningful markup.

## 7. Verify before committing

- Page loads through the local server.
- CSS and logo load without 404 responses.
- Navigation links reach their intended sections.
- Service tabs are checked against their actual IDs.
- Contact form is not treated as a working submission service.
- Keyboard focus is visible.
- Layout works at narrow and wide viewports.
- Browser console has no new errors.

See [Testing](testing.md), [Development](development.md), and [Troubleshooting](troubleshooting.md).
