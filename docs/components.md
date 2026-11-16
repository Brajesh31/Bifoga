# 🧱 Page Components and UI Inventory

## 1. Scope

The current project is a single static HTML page. The term *component* in this guide means a visible page region or reusable UI pattern, not a React/Vue component. No component framework is installed or declared in the current package metadata.

## 2. Page-level regions

| Region | Purpose | Review points |
|---|---|---|
| Navigation | Gives visitors access to page sections | Link targets, focus visibility, mobile layout |
| Home/intro | Introduces the EnClose offering | Heading hierarchy, concise value proposition |
| Services | Presents consultation and education content | Accurate descriptions, working tab/panel relationship |
| Booking destination | Navigation target for booking-oriented content | Do not imply a booking engine exists |
| Contact region | Presents contact details/form layout | Form endpoint is not implemented in this repository |
| Footer | Closing information and secondary navigation | Ensure links and legal details are real |

## 3. Menu and tab interaction

The browser helper `openMenu(evt, menuName)` is intended to switch visible panels. The markup must provide:
- A control associated with each panel.
- A real panel element with the exact requested ID.
- A clear selected state.
- Keyboard operation consistent with the chosen interaction pattern.
- A semantic relationship such as `aria-controls` and `aria-selected` when implementing tabs.

The current page's panel naming and tab labels should be checked before extending this pattern. Do not document the interaction as fully accessible or fully tested until it has been verified in a browser and with keyboard-only navigation.

## 4. Responsive design

Check at least:
- Narrow mobile viewport.
- Larger mobile or small tablet viewport.
- Desktop viewport.
- Zoomed text and increased browser font settings.

Avoid fixed widths that cause horizontal scrolling. Images should preserve their aspect ratio and have meaningful alternative text when they convey information. Decorative images should use empty alternative text.

## 5. Visual consistency

- Keep heading hierarchy consistent.
- Use link text that describes the destination.
- Maintain sufficient contrast for text, controls, and focus indicators.
- Do not communicate status by color alone.
- Ensure touch targets are comfortably operable.
- Avoid animation that cannot be paused or that causes distracting motion.

## 6. Adding a new page region

Before adding a region, define its visitor purpose, content owner, location in reading order, navigation requirement, responsive behavior, accessibility expectations, and any data dependency. If the region requires backend data, document that dependency explicitly rather than simulating a working service in static markup.
