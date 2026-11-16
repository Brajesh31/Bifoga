# 🧭 Usage Guide

## 1. What a visitor can do

Bifoga's current website content is branded **EnClose** and presents an AI consultation and education offering. The repository contains a static landing page rather than a complete booking, learning-management, or AI consultation platform.

The visible page is organized around:
- Home and introductory content.
- Services content with consultation and education descriptions.
- A booking-oriented navigation destination.
- Contact-oriented content and a form layout.

The page should be treated as an informational front end. A visitor should not be promised a confirmed appointment, payment, account, or AI response unless a real service is connected and verified.

## 2. Local preview

From the repository root:

```bash
npm ci
npx serve docs
```

Open the local address printed by the static server. If the `serve` package is not installed globally or locally, use an approved static server of your choice. Do not open the page through a file URL when testing navigation and asset paths intended for an HTTP server.

In another terminal, run the Tailwind watcher if you are changing styles:

```bash
npm run tailwind
```

## 3. Navigation and page sections

Use the navigation links in `docs/index.html` to move between the page's named sections. When changing section IDs, update both the navigation destination and the target element. Anchor fragments are case-sensitive in practice and should be checked after edits.

The page's current JavaScript helper is `openMenu(evt, menuName)`. It hides elements with the `menu` class and displays the element whose ID is passed to it. The current markup and helper must be reviewed together before relying on tab switching: the existing tab labels and panel IDs have historically been inconsistent. This guide does not claim that the interaction has been repaired.

## 4. Contact form expectations

The HTML contains a contact-form presentation, but the repository does not include the server endpoint referenced by its placeholder action. Therefore:
- Do not enter sensitive or confidential information.
- Do not tell visitors that a message has been delivered.
- Do not use the form as a production lead-capture mechanism until a real endpoint exists.
- A future implementation must provide server-side validation, abuse protection, error feedback, privacy disclosures, and an accessible success state.

## 5. Editing page content

1. Edit the existing page in `docs/index.html`.
2. Preserve semantic heading order and meaningful link text.
3. Keep images in tracked asset directories and use paths that work from the deployed page location.
4. Update `src/input.css` for authored styles.
5. Run the Tailwind watcher when changing utility classes.
6. Check the page at narrow and wide viewport sizes.
7. Test keyboard navigation and visible focus.
8. Verify all local asset and section links.

## 6. Visitor support

For questions about the project, use the repository's GitHub issue and support channels. Do not publish private contact details or expose credentials in issues.
