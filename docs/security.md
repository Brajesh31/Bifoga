# 🔐 Security Guide

## 1. Current threat boundary

Bifoga's current EnClose site is a static front end. The repository does not contain a backend, database, authentication system, payment processing, or implemented contact-form service. The absence of a backend reduces some server-side attack surface, but it does not make the website automatically secure.

## 2. Security principles

### Client-side code is public
Anything delivered in HTML, CSS, or JavaScript can be inspected by visitors. Never place private keys, passwords, tokens, database credentials, or privileged service credentials in browser code.

### Validate future submissions on the server
HTML validation improves user experience but is not a security boundary. If a contact endpoint is introduced, validate every field on the server, enforce size limits, normalize input safely, and reject unexpected content.

### Avoid unsafe DOM insertion
When displaying user-controlled content, use safe text APIs such as `textContent`. Do not concatenate untrusted values into `innerHTML` or executable code.

### Use HTTPS
Serve the production site over HTTPS. Redirect HTTP to HTTPS at the hosting layer and configure secure headers where the host supports them.

## 3. Contact form is not a working backend

The existing form references a placeholder action. No matching endpoint is included in this repository. Do not collect sensitive information through it or claim that it securely transmits submissions.

Before enabling a real endpoint, add:
- Server-side validation and output encoding.
- CSRF protection where the architecture requires it.
- Abuse prevention and rate limiting.
- Spam controls that do not create unnecessary accessibility barriers.
- Clear privacy notice and retention policy.
- Safe error handling that does not reveal internal details.
- Monitoring that avoids logging unnecessary personal data.

## 4. Dependency security

- Use `npm ci` for reproducible installs.
- Review dependency changes in `package-lock.json`.
- Remove dependencies that are no longer needed.
- Review advisories before upgrading or accepting exceptions.
- Do not run untrusted install scripts without review.
- Prefer minimal permissions in CI workflows.

## 5. GitHub and secret hygiene

- Never commit real secrets.
- Keep example values obviously synthetic.
- Enable GitHub secret scanning and push protection where available.
- Rotate credentials immediately if they are exposed.
- Use narrowly scoped workflow permissions.
- Pin third-party actions to reviewed immutable commit SHAs in security-sensitive workflows.

## 6. Static hosting controls

Consider the following host-level controls after validating compatibility:
- Content Security Policy.
- Strict-Transport-Security.
- X-Content-Type-Options.
- Referrer-Policy.
- Permissions-Policy.
- Appropriate cache-control behavior.

A Content Security Policy must be tested against the actual inline scripts, styles, fonts, and external assets. Do not paste a restrictive policy blindly and assume the page will continue to work.

## 7. Reporting a vulnerability

Please do not publish exploit details or secrets in a public issue. Follow the private reporting instructions in the root `SECURITY.md`. Include the affected path, impact, reproduction steps, and a safe proof of concept. Do not include real visitor data.
