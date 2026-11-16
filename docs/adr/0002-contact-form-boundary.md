# ADR 0002: Contact form capability boundary

- **Status:** Accepted
- **Date:** 2026-11-17

## Context

The page includes a contact-form layout, but the repository does not contain the server-side route or third-party integration referenced by the placeholder form action.

## Decision

Documentation and public project descriptions must treat the form as presentation markup only until a working handler is implemented and verified. No successful delivery, storage, privacy, or security guarantee may be claimed.

## Consequences

- Visitors must not be told that a message has been delivered when no service confirms it.
- Sensitive information must not be requested through the current form.
- A future implementation requires server-side validation, abuse controls, clear error/success feedback, and a privacy notice.
- Any new service must be documented and tested before the capability is described as live.

## Revisit when

A real form provider or backend is selected, configured, and deployed.
