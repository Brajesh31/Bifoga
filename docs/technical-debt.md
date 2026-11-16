# 🧾 Technical Debt Register

This register captures verified gaps and engineering risks visible in the current static website. Items should be rechecked before work begins because source code may change.

| ID | Area | Observed issue | Impact | Suggested action |
|---|---|---|---|---|
| TD-01 | Script loading | The page references `main.js` using a stylesheet link | Browser helper may not load as intended | Use a proper script element and verify loading |
| TD-02 | Tab IDs | Controls pass `Eat` and `Drinks`; panels use `consultation` and `education` | Panel lookup can fail | Align control targets and panel IDs |
| TD-03 | Tab state | Helper loops by panel count when updating tab links | Active styling can become inconsistent | Iterate over controls and panels independently |
| TD-04 | HTML validity | Education heading contains malformed closing markup | Invalid document structure | Correct markup and run HTML validation |
| TD-05 | Navigation | `#book` link has no matching section | Dead navigation target | Add real booking information or remove/retarget link |
| TD-06 | Contact form | Placeholder `/action_page.php` has no handler | No verified submission delivery | Implement a secure endpoint or remove misleading form |
| TD-07 | Asset reference | Page references a map image absent from the repository tree | Broken image request | Add a licensed asset or remove the reference |
| TD-08 | Footer | Footer region is empty | Incomplete page structure | Add verified content or remove empty region |
| TD-09 | External resources | W3.CSS and Google Fonts are remote dependencies | Availability, privacy and CSP dependency | Review self-hosting/pinning trade-offs |

## Prioritization

Fix user-visible broken navigation and resource loading first. Treat the form/backend gap as a product and privacy decision, not a cosmetic code fix. Do not close an item until the change is implemented and verified in a browser.

## Ownership

Assign an owner and target milestone in an issue before scheduling work. Update this register when an item is fixed, deferred, or superseded.
