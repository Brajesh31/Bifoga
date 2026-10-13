# Interfaces

There is no HTTP API. The browser page exposes:

- hash navigation to `#home`, `#services`, `#book`, and `#contact`;
- service-tab calls to `openMenu(event, menuName)` in `main.js`;
- a contact form whose current action is `/action_page.php`.

The form action is a placeholder and should not be treated as an implemented service contract.
