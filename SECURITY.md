# 🔐 Security Policy

## Supported scope

The repository currently contains a static EnClose landing page and development tooling. It does not include a project-owned application backend, database, authentication system, payment processor, AI inference service, or contact-form handler.

The contact form action currently points to a placeholder path. Do not submit personal, confidential, or credential information through it.

## Reporting a vulnerability

Please report suspected vulnerabilities privately through [GitHub Security Advisories](https://github.com/Brajesh31/Bifoga/security/advisories/new). If that channel is unavailable, contact the repository owner through the GitHub profile at [@Brajesh31](https://github.com/Brajesh31).

Include:
- Affected file, dependency, workflow, or deployed URL.
- Impact and conditions required.
- Reproduction steps and a safe proof of concept.
- Suggested mitigation, if known.

Do not include real visitor data, access tokens, passwords, or other secrets in reports.

## Response expectations

The repository is maintained on a best-effort basis. The maintainer will assess the report, request clarification if needed, and coordinate a fix or mitigation. No fixed response-time SLA is promised.

## Current security boundaries

- Browser code is public and must not contain private credentials.
- There is no server-side validation or storage for the current form.
- External W3.CSS and Google Fonts resources are loaded by the page.
- Static hosting security headers depend on the hosting provider.
- CI dependency auditing is configured, but an enabled workflow is not evidence that every dependency is vulnerability-free.

## Production readiness

Before enabling data collection or promoting the site as a production service, implement and review server-side validation, abuse protection, privacy disclosures, data retention/deletion, HTTPS, security headers, and incident response. See [docs/security.md](docs/security.md).
