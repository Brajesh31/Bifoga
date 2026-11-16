# 🚀 Future Scope

## 1. Product direction

The current repository provides a static EnClose landing page. Future work should be prioritized around validated user needs and a realistic operating model, not a long list of features that the project cannot currently support.

## 2. Potential increments

| Priority | Candidate improvement | Required groundwork |
|---|---|---|
| High | Repair and verify navigation/tab interactions | Align control IDs, panel IDs, keyboard behavior and accessible state |
| High | Make the contact journey real or remove the misleading form | Select a service, define data handling, implement and secure endpoint |
| High | Improve responsive and accessibility behavior | Manual audit, contrast review, keyboard testing |
| Medium | Add a repeatable production build | Define output directory and build artifact |
| Medium | Add automated HTML/link checks | Select tooling and define CI acceptance criteria |
| Medium | Add optimized screenshots and a social preview | Capture genuine current UI states and optimize assets |
| Later | Booking integration | Product requirements, scheduling provider, privacy and security design |
| Later | AI consultation integration | Model/provider selection, server-side secret handling, safety, cost and evaluation plan |
| Later | User accounts or dashboards | Strong justification, threat model, data model and support ownership |

## 3. Suggested delivery phases

### Phase 1: Trustworthy landing page
- Resolve broken local references.
- Ensure page sections and navigation targets agree.
- Make interactions keyboard accessible.
- Remove or clearly mark non-functional submission paths.
- Verify mobile layout and basic metadata.

### Phase 2: Reliable engineering workflow
- Add static validation and link checking.
- Add a documented production build if required by hosting.
- Add dependency and workflow security checks.
- Capture real screenshots after the page is stable.

### Phase 3: Service integration
- Define actual service requirements with stakeholders.
- Choose an appropriate backend or managed service.
- Define data minimization, privacy, retention, and incident response.
- Implement server-side validation and abuse controls.
- Test failure, retry, and accessibility states.

### Phase 4: AI or booking capabilities, only if approved
- Specify user outcomes and success criteria.
- Evaluate providers and operational costs.
- Keep credentials server-side.
- Add model evaluation, monitoring, and fallback behavior.
- Conduct privacy, safety, and security reviews before launch.

## 4. Prioritization rule

Do not add a complex feature merely because it appears on a roadmap. Each item should have an owner, user problem, acceptance criteria, risk assessment, and evidence that the project can maintain it.
