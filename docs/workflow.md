# 🔄 Application and Development Workflow

## 1. Browser loading sequence

1. Visitor requests the static site.
2. The host returns `docs/index.html`.
3. The browser requests local CSS, JavaScript, and the logo.
4. The page also requests external W3.CSS and Google Fonts resources referenced by the markup.
5. The browser parses, styles, and renders the page.
6. The browser-side helper is available for the intended service-panel interaction when correctly loaded.
7. The visitor navigates through page anchors or service controls.
8. The contact form action points to a backend route not included in this repository.

## 2. Current browser flow

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
    H -->|Contact form| K[Placeholder form action]
    K --> L[No backend implementation]
```

## 3. Tab interaction sequence

```mermaid
sequenceDiagram
    actor Visitor
    participant Page
    participant Helper as openMenu
    participant DOM
    Visitor->>Page: Activate service control
    Page->>Helper: Pass event and panel name
    Helper->>DOM: Hide menu panels
    Helper->>DOM: Find requested panel by ID
    Helper->>DOM: Show requested panel
    Helper->>DOM: Update active tab styling
    Note over Helper,DOM: Existing markup and script references contain mismatches
```

## 4. Contact form boundary

```mermaid
flowchart TD
    A[Visitor enters values] --> B[HTML form]
    B --> C{Real endpoint implemented?}
    C -->|No, current state| D[No verified delivery]
    C -->|Future service exists| E[HTTPS request]
    E --> F[Server-side validation]
    F --> G[Abuse prevention]
    G --> H[Process and return status]
```

Do not rely on the current form for actual business enquiries until a secure endpoint has been implemented and tested.

## 5. Development workflow

```mermaid
flowchart TD
    Clone[Clone repository] --> Install[npm ci]
    Install --> Edit[Edit HTML, JS or CSS source]
    Edit --> Styles{Tailwind source changed?}
    Styles -->|Yes| Watch[Run npm run tailwind]
    Styles -->|No| Preview[Serve docs directory]
    Watch --> Preview
    Preview --> Verify[Check assets, links and behavior]
    Verify --> A11y[Keyboard and responsive review]
    A11y --> Review[Review diff and docs]
    Review --> Commit[Commit changes]
```

## 6. Diagram maintenance

Editable versions of the current system, navigation, form boundary, asset delivery, and development workflow are in [diagrams/](diagrams/README.md). Update them when the implementation changes.
