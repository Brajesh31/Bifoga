# EnClose

EnClose is a static marketing landing page for an AI consultation and education concept. It presents a responsive navigation bar, branded hero area, service tabs, and a contact form. The page uses HTML, Tailwind CSS, W3.CSS, Google Fonts, and a small JavaScript tab helper.

> **Prototype note:** The contact form currently points to `/action_page.php`, and no backend is included. Do not enter sensitive information.

## Features

- Home, services, booking, and contact navigation anchors.
- Consultation and education service tabs driven by `openMenu` in `main.js`.
- Tailwind-generated styling in `docs/style.css`.
- Logo asset in `docs/img/logo.png`.
- Responsive utility classes and W3.CSS layout helpers.

## Requirements

- Node.js and npm.
- Internet access for the external W3.CSS and Google Fonts resources when previewing the page.

## Development

Install the lockfile dependencies, then use a static server to serve `docs/`:

```powershell
npm ci
npx serve docs
```

To rebuild Tailwind while editing:

```powershell
npm run tailwind
```

The `prettier` script formats HTML files. Open `docs/index.html` through a local server rather than relying on `file://` paths, because the page uses root-relative assets and form targets.

## Project layout

- `docs/index.html` - landing page markup.
- `docs/style.css` - generated Tailwind and custom styles.
- `docs/img/logo.png` - hero logo.
- `main.js` - service-tab behavior.
- `src/input.css` - Tailwind input and custom CSS.

See [docs/architecture.md](docs/architecture.md) and [docs/troubleshooting.md](docs/troubleshooting.md).

## License

MIT licensed. See [LICENSE](LICENSE).

Last updated: 2026-10-18 07:32 UTC
