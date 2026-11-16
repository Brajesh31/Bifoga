# ⚠️ Current Limitations

This page records boundaries visible in the repository. It is intended to prevent documentation and marketing copy from promising capabilities that the code does not provide.

## 1. Product and functionality

- The repository contains a static landing page, not a complete AI consultation platform.
- No AI model integration or inference endpoint is present in the reviewed source.
- No booking engine or appointment scheduling service is included.
- No account creation or authentication flow is included.
- No payment processing is included.
- The contact form action points to a placeholder path; no matching handler is present.

## 2. Architecture

- No backend service is defined.
- No database schema or migration system is present.
- No formal API endpoints are implemented.
- No server-side validation or persistence layer is present.
- The browser helper is a small DOM interaction, not an application state-management system.

## 3. Engineering and quality

- The package scripts do not declare a dedicated test suite.
- There is no browser end-to-end test suite in the current repository.
- A formal production build/release pipeline is not established by the package scripts.
- Accessibility and performance scores must be measured, not assumed.
- Static hosting configuration and security headers depend on the eventual hosting provider.

## 4. Documentation caveat

Some documents describe future design requirements. They are explicitly labelled as future considerations and must not be read as evidence that those capabilities have shipped.

## 5. Reassessment triggers

Update this document when a real backend, API, database, form service, automated tests, deployment pipeline, or AI integration is added. Remove a limitation only after verifying the relevant code and operational behavior.
