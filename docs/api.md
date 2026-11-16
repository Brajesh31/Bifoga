# 🔌 Interfaces

## HTTP API status

There is no HTTP API in the current repository. The website is a static HTML/CSS/JavaScript page. It does not define REST, GraphQL, RPC, authentication, or application data endpoints.

For the detailed interface inventory and future API documentation requirements, see [API Reference](api-reference.md).

## Current browser interfaces

| Interface | Description | Network request |
|---|---|---|
| Hash navigation | Links to page section fragments | None beyond normal static document behavior |
| `openMenu(evt, menuName)` | Browser-side helper in `main.js` | None |
| Contact form | HTML form with fields for visitor input | Points to placeholder `/action_page.php`; no handler exists in this repository |

## Contact form boundary

The form action is not an implemented service contract. There is no verified request schema, response, storage, email delivery, authentication, rate limit, or success guarantee.

Do not collect real personal or confidential information until a backend or managed form service is implemented and documented.
