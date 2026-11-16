# 🔌 API Reference

## Current API status

**There is no application HTTP API in this repository.** The current project is a static HTML/CSS/JavaScript website. It does not define REST routes, GraphQL operations, RPC methods, authentication endpoints, or a backend service.

This document records the actual browser-side interfaces so contributors do not confuse a JavaScript helper or HTML form with a network API.

## 1. Browser-side helper

### `openMenu(evt, menuName)`

| Attribute | Detail |
|---|---|
| Kind | Browser-side JavaScript function |
| Defined in | `main.js` |
| Purpose | Hide elements with class `menu`, then display the element whose ID is `menuName` |
| Inputs | An event-like object with `currentTarget`, and a string element ID |
| Network request | None |
| Persistence | None |
| Authentication | None |

The helper directly manipulates element styles and a tab-link class. It assumes the expected DOM elements exist. It does not validate the requested ID or return a structured result.

Example of the existing call pattern used by the page:

```html
<button onclick="openMenu(event, 'panel-id')">Open panel</button>
```

The actual panel ID must exist in the document. Before adding or changing calls, verify the helper's assumptions and ensure the tab controls are keyboard accessible.

## 2. HTML form boundary

The page includes a contact form with visitor-entered fields. Its current action points to a placeholder path. No matching PHP, Node.js, serverless, or third-party form handler is present in this repository.

Consequently, there is no supported request schema, response schema, HTTP status catalogue, authentication mechanism, rate limit, or delivery guarantee to document.

## 3. Future API contract checklist

If a backend is added, document each endpoint with:
- HTTP method and path.
- Purpose and ownership.
- Authentication and authorization requirements.
- Request headers, parameters, and JSON schema.
- Example request with synthetic data.
- Success response and status code.
- Validation and error response examples.
- Rate limits, retry behavior, and idempotency rules.
- Personal-data fields and retention policy.
- Logging and monitoring expectations.

Do not publish an endpoint in this reference until it exists in code or is defined by an approved API specification.
