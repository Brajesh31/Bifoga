# ♿ Accessibility Guide

## 1. Goal

The website should be usable by visitors with different sensory, motor, and cognitive abilities. Accessibility is part of page structure and interaction design, not a final visual polish task.

## 2. Semantic HTML

- Use one clear page-level `h1`.
- Maintain a logical heading hierarchy.
- Use landmarks such as `header`, `nav`, `main`, and `footer` where appropriate.
- Use links for navigation and buttons for actions.
- Give each form control a visible or programmatic label.
- Use lists for grouped content and tables only for tabular data.

## 3. Keyboard access

Every interactive element must be reachable and operable by keyboard. Preserve a visible focus indicator. Do not create custom clickable `div` elements when a native button or link is appropriate.

For tab-style controls, implement the expected keyboard behavior and expose selected state and panel relationships. A visual class change alone is not an accessible state announcement.

## 4. Images and media

- Provide useful alternative text for informative images.
- Use empty alt text for purely decorative images.
- Do not put essential information only inside an image.
- Add captions or transcripts for meaningful audio/video content if such media is introduced.

## 5. Color, typography and motion

- Maintain sufficient text and non-text contrast.
- Never use color as the only signal for selected, error, or success states.
- Allow text zoom and reflow without clipping.
- Avoid small text and cramped touch targets.
- Respect `prefers-reduced-motion` for non-essential motion.
- Ensure animations do not flash or distract.

## 6. Forms and feedback

A future working contact form must provide:
- Persistent labels.
- Instructions for required fields.
- Clear inline validation messages.
- Error summaries or focus management when appropriate.
- An announced success or failure status.
- No loss of entered values after a recoverable error.
- Privacy information explaining how submissions are handled.

The current repository does not provide a verified form-processing endpoint. Do not label it as an accessible, working submission flow until both the front end and service have been tested.

## 7. Verification

Use a combination of:
1. Keyboard-only navigation.
2. Browser zoom and reflow checks.
3. Automated accessibility scanning.
4. Screen-reader spot checks.
5. Contrast measurement.
6. Manual review of headings, labels, alt text, and status messages.

Record issues and remediation in GitHub. Automated tools do not prove full conformance.
