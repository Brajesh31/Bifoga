# 🔄 Runtime workflow

## Browser loading sequence

1. Visitor requests the static site.
2. Host returns `docs/index.html`.
3. Browser requests local CSS and the logo.
4. Browser requests remote W3.CSS and Google Fonts.
5. Page renders navigation, hero, introduction, services, and contact area.
6. JavaScript should provide service tab interaction once it is loaded correctly.
7. Visitor navigates using anchors or chooses a service tab.
8. The form points to a backend route not included in this repository.

## Current browser flow

```mermaid
flowchart TD
    A([Open site]) --> B[Request index.html]
    B --> C[Load local CSS]
    B --> D[Load JavaScript]
    B --> E[Load logo and external resources]
    C --> F[Render page]
    D --> G[Service tab helper]
    E --> F
    G --> F
    F --> H{Visitor action}
    H -->|Navigation link| I[Move to anchor]
    H -->|Service tab| J[Show selected panel]
    H -->|Contact form| K[Submit to placeholder path]
    K --> L[No backend implementation]
```

## Tab interaction sequence

```mermaid
sequenceDiagram
    actor Visitor
    participant Page
    participant Helper as openMenu
    participant DOM
    Visitor->>Page: Click service tab
    Page->>Helper: Pass event and panel name
    Helper->>DOM: Hide menu panels
    Helper->>DOM: Find requested panel by ID
    Helper->>DOM: Show requested panel
    Helper->>DOM: Update active tab styling
    Note over Helper,DOM: Current HTML passes IDs that do not match the panel IDs
```

## Contact form boundary

```mermaid
sequenceDiagram
    actor Visitor
    participant Page as index.html
    participant Browser
    participant Endpoint as /action_page.php
    Visitor->>Page: Enter contact values
    Page->>Browser: Submit form
    Browser->>Endpoint: POST
    Note over Endpoint: Endpoint is not present in repository
```

Do not rely on this form for actual business enquiries until a secure endpoint has been implemented and tested.
