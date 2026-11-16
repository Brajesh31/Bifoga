# 🌐 Deployment Guide

## 1. Deployment model

The current application can be hosted as static files. The page source is in `docs/`, with the HTML entry point at `docs/index.html`. The repository does not identify a confirmed production hosting provider or a complete automated deployment workflow.

Deploy the contents of `docs/` as the static site root. Verify that the deployed host preserves the expected paths for the stylesheet, logo, and any other local assets.

## 2. Pre-deployment preparation

1. Start from a clean checkout.
2. Run `npm ci`.
3. Run `npm run tailwind` if Tailwind source changed.
4. Serve `docs/` locally.
5. Verify navigation, service tabs, responsive layout, and keyboard access.
6. Check all local asset paths.
7. Review external W3.CSS and Google Fonts requests.
8. Confirm no secret or private data is included.
9. Confirm the contact form is not advertised as operational without a real handler.

## 3. Static host requirements

- Serve the page over HTTPS.
- Set the document root to the contents of `docs/`.
- Support the expected asset paths and correct MIME types.
- Configure an appropriate cache policy for HTML and versioned/static assets.
- Redirect HTTP to HTTPS.
- Configure security headers after testing them against the page's inline/external resources.

## 4. Contact form warning

The current form action is `/action_page.php`, and no matching PHP handler or backend service is included in this repository. Deploying the static page does not make the form functional. Do not accept real enquiries until a reviewed endpoint, server-side validation, abuse protection, privacy notice, and success/error feedback are implemented.

## 5. Post-deployment verification

- Open the deployed URL over HTTPS.
- Confirm the page, stylesheet, logo, fonts, and scripts load.
- Test navigation and interactive controls.
- Test a narrow viewport and keyboard-only operation.
- Inspect console and network failures.
- Confirm the deployed commit matches the intended release.

## 6. Rollback

Use the hosting provider's rollback or redeploy capability to restore the last known-good static artifact. Verify the restored site. Provider-specific commands should be added here only after the actual host is confirmed.
