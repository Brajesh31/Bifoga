# ❓ Frequently Asked Questions

## Is EnClose a complete AI consultation product?

No. This repository contains a static landing-page concept describing consultation and education. It does not include an AI model, chatbot, inference API, or consulting workflow.

## Does the website accept booking requests?

No booking engine or calendar integration is included. The booking-oriented navigation destination should not be interpreted as a working appointment system.

## Does the contact form send an email?

There is no form-processing backend in this repository. The form action points to a placeholder path. Do not use it for real enquiries.

## Does the project use a database?

No. There is no database schema, connection, migration, or persistent application storage.

## How do I preview the page?

Run `npm ci`, then `npx serve docs`. Open the URL printed by the server.

## How do I rebuild styles?

Run `npm run tailwind`. The watcher reads `src/input.css` and writes `docs/style.css`.

## Where is the page logic?

Page markup is in `docs/index.html`; the small browser-side menu helper is in `main.js`.

## Why are tabs not working?

The current markup and helper have ID mismatches, and the HTML references the JavaScript file incorrectly. See [Features](features.md) and [Troubleshooting](troubleshooting.md). Application code is not changed by this documentation update.

## Where can I find architecture diagrams?

See the [diagram catalogue](diagrams/README.md). Editable Mermaid source files are stored in `docs/diagrams/`.

## How do I report a security issue?

Use the private process described in the root [SECURITY.md](../SECURITY.md). Do not publish secrets or exploit details in a public issue.
