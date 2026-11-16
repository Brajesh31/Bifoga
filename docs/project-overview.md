# ✨ Project Overview

## 1. Purpose

EnClose is a static landing-page concept for an AI consultation and education offering. It communicates a business-facing message about AI adoption, introduces Consultation and Education as service categories, and presents a contact section.

The repository demonstrates the frontend presentation of that idea. It is not a complete AI consulting platform and does not implement AI inference, customer onboarding, payments, scheduling, or contact management.

## 2. Goals visible in the source

- Present the EnClose brand using the existing logo and gradient treatment.
- Explain why AI adoption is relevant to businesses and professionals.
- Provide navigation to page sections.
- Show two service categories using a tab-like interface.
- Display a contact form layout.
- Keep the page deployable as static files.

## 3. Non-goals of the current repository

The current project does not include an AI assistant, model, inference endpoint, booking calendar, CRM, lead database, email notification service, user authentication, payment processing, content-management system, or contact-submission backend.

These capabilities require separate implementation. A static page describing a service does not mean that service is technically available.

## 4. Intended audience

The intended audience is a business owner, professional, student, or organization exploring AI consultation and education. The codebase is also useful for frontend learners practising HTML structure, utility CSS, basic DOM interaction, and static hosting.

## 5. Technology summary

| Layer | Current technology | Role |
|---|---|---|
| Markup | HTML5 | Page structure and form layout |
| Styling | Tailwind CSS | Utilities and generated styles |
| Layout helpers | W3.CSS | Existing layout classes |
| Browser behavior | Vanilla JavaScript | Service-panel helper |
| Typography | Google Fonts | Inconsolata |
| Development | Node.js and npm | Local scripts |
| Delivery | Static hosting | Serve files in `docs/` |

## 6. Visitor journey

1. Visitor opens the landing page.
2. Navigation links move between anchored sections.
3. Visitor reads the AI adoption message.
4. Visitor selects a service category.
5. Visitor reaches the contact section.
6. The form cannot complete a real submission until a backend is implemented.

## 7. Prototype success criteria

A valid demonstration should load the page and local assets, display the brand and introduction, allow keyboard and pointer navigation, switch service panels once the DOM wiring is corrected, and clearly identify the contact form as unavailable until its endpoint exists.

## 8. Quality boundary

Visual presentation alone is not enough for production. The current form target, script inclusion, tab identifiers, and malformed markup need correction. Accessibility, privacy, security, browser compatibility, and content review should be completed before collecting enquiries.
