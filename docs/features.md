# ✨ Feature Catalogue

This catalogue separates visible page elements from complete working services. The current implementation is a static landing page, not a production AI consultation platform.

## 🧭 Navigation

The page contains navigation for Home, Services, Book a Call, and Contact Us. The `#book` destination does not currently have a matching section ID. Verify all anchors before treating the navigation as complete.

## 🎨 Hero and logo

The hero uses a gradient background and a CSS class that references the existing logo image. The logo is applied as a background image rather than a semantic inline image with alternative text.

## 💡 Introduction

The introduction contains static messaging about AI adoption and the gap between businesses using AI and those that do not. Any quantitative or market claim in this copy should be supported by a reliable source before publication.

## 🧩 Consultation and Education panels

The markup intends to show two service panels. The `openMenu(evt, menuName)` helper hides elements with class `menu`, shows a panel by ID, and attempts to update active tab styling.

Known issues in the current source:
- Click handlers pass `Eat` and `Drinks`.
- Content panel IDs are `consultation` and `education`.
- The HTML references the JavaScript file using a stylesheet link.
- The helper uses panel count while iterating over tab links.
- Controls should be reviewed for semantic button/tab behavior and keyboard access.

No service API or dynamic service catalogue exists.

## 📬 Contact section

The contact area includes Name, Company Name, and Message fields. Its form action is `/action_page.php`, but no matching PHP file or API route is included.

Before using a real endpoint, add privacy disclosure, appropriate consent language, server-side validation, spam prevention, access restrictions, retention/deletion rules, and secure transport.

## 🦶 Footer

The footer element exists but is empty. A future footer may contain verified organization identity, navigation, contact information, privacy policy, and legal notices. Do not invent company details.

## 🚫 Not implemented

There is no live chatbot, AI workflow, booking calendar, contact database, newsletter, payment flow, CRM, login system, analytics integration, or admin dashboard in the current repository.
