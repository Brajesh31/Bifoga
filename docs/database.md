# 🗄️ Data, Persistence and Privacy

## 1. Current state

The project has no database, local-storage persistence, cookie-based application state, or server-side data store defined in the repository.

Page content is stored in version-controlled HTML and CSS. The tab helper changes temporary DOM visibility. The contact form contains input controls but its placeholder action is not backed by a handler in this repository.

## 2. Data inventory

| Data | Current location | Persistence |
|---|---|---|
| Page copy and labels | `docs/index.html` | Git repository |
| Styling | `src/input.css`, `docs/style.css` | Git repository |
| Logo | `docs/img/logo.png` | Git repository |
| Tab visibility | Browser DOM | Temporary page state |
| Contact field values | Browser form controls | No project-provided storage |
| Visitor account data | Not implemented | None |
| Booking records | Not implemented | None |

## 3. Contact form privacy boundary

Do not claim that submissions are received, encrypted, emailed, stored, or deleted. Those behaviors require an actual handler and an explicitly designed data lifecycle.

Before collecting enquiries, define:
- Which fields are necessary and why.
- The visitor-facing privacy notice and consent requirements.
- Server-side validation and abuse prevention.
- Who can access submissions.
- Encryption in transit and at rest where data is stored.
- Retention and deletion schedules.
- Audit logging that avoids unnecessary personal data.
- Backup, restoration, and breach response procedures.

## 4. Future database decision

A database is not automatically required for a contact workflow. First evaluate whether a managed form service or secure email relay can meet the requirement with less operational risk. If a database becomes necessary, document the schema, access model, migrations, backup policy, retention, and data subject request process before launch.

## 5. Diagram

See [Data Flow](data-flow.md) and [System Design](system-design.md). The proposed storage branch in those diagrams is not part of the current application.
