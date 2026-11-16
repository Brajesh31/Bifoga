# ADR 0001: Static-first website architecture

- **Status:** Accepted
- **Date:** 2026-11-17

## Context

The repository currently contains a static HTML page, browser-side JavaScript, Tailwind CSS tooling, and static assets. It does not contain a backend, database, authentication service, or application API.

## Decision

Retain the static-first architecture while the website's requirements can be met by static content and small browser interactions. Do not introduce a framework or server merely for appearance or documentation completeness.

## Consequences

Positive:
- Simple hosting and deployment model.
- Small runtime surface.
- No server-side secrets or database to operate.
- Easy local preview using a static server.

Trade-offs:
- Dynamic submissions and personalized workflows need a separate service.
- No server-side persistence or authentication is available.
- More complex content may eventually justify a build system or component architecture.

## Revisit when

A validated requirement needs server-side processing, protected data, dynamic accounts, booking, payments, or AI inference.
