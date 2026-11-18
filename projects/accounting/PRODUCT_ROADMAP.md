# MOHSSINE ACCOUNTING — Product Roadmap

## Vision
Build a professional Moroccan accounting web application for small and medium businesses and accounting firms (fiduciaires). The product must support multiple organizations and, for accounting firms, multiple client companies with strict data separation.

## Product principles
- Moroccan accounting and tax workflows first; validate accounting rules with a qualified Moroccan accountant before production use.
- French-first interface, with Arabic support planned.
- Reliable calculations, traceable changes, secure access, and exportable records.
- Never present indicative or incomplete journal entries as certified accounting output.
- Keep the existing AI Digital Product Creator application unchanged.

## MVP phases

### Phase 0 — Foundation (current)
- Separate accounting application from the existing product creator.
- Document product scope, architecture, and release milestones.
- Work on a dedicated Git branch before merging changes to main.

### Phase 1 — Product and interface
- Professional responsive dashboard and navigation.
- Company profile: legal name, ICE, IF, RC, address, fiscal year, currency.
- Accounting-firm workspace with client/company selection.
- Clear onboarding and sample/demo data.

### Phase 2 — Secure application platform
- Backend API and PostgreSQL database.
- Authentication, password reset, and session management.
- Organization-based multi-tenancy and role-based access control.
- Database row-level security and audit trail.
- Automated backups and recovery procedures.

### Phase 3 — Core accounting data
- Moroccan chart of accounts, configurable by company.
- Customers, suppliers, products/services, and tax codes.
- Sales and purchase invoices, credit notes, payment status.
- Numbering sequences and document attachments.

### Phase 4 — Double-entry accounting
- Balanced journal entries with debit and credit lines.
- General journal, general ledger, and trial balance.
- Posting controls, period closing, and traceable corrections.
- No silent edits to posted accounting entries.

### Phase 5 — Moroccan tax and financial reports
- VAT tracking and configurable VAT reports.
- General balance sheet (Bilan) and income statement (CPC).
- Exports to PDF and Excel/CSV.
- Tax rules and report formats reviewed against current Moroccan requirements before release.

### Phase 6 — Firm workflows and launch readiness
- Multiple staff users and permissions.
- Client portfolio, review/approval workflow, and reminders.
- Bank statement import and reconciliation.
- Monitoring, security testing, user documentation, support, and subscription/billing readiness.

## Proposed technical direction
- Frontend: TypeScript web application (Next.js or an equivalent supported framework).
- Backend/data: PostgreSQL with a secure API; Supabase is a candidate for database, authentication, and file storage.
- Hosting: a production web host for the application and managed database hosting. GitHub remains the source-code and CI/CD home.
- GitHub Pages may continue to host the current static prototype, but it is not sufficient for a secure multi-user commercial accounting service.

Final technology choices will be confirmed before implementation. Secrets and database credentials must never be committed to this repository.

## Initial release boundary
The first usable release should focus on one company per workspace, company settings, customers/suppliers, invoices, VAT calculations, and balanced journal entries. Accounting-firm multi-client workflows and advanced reports follow after the core accounting engine is tested.

## Quality gates before commercial use
- Test calculations and accounting entries with a Moroccan accounting professional.
- Verify debit equals credit for every posted journal entry.
- Test tenant isolation and role permissions.
- Test backups and restore.
- Review privacy, security, retention, and applicable legal obligations in Morocco.
- Clearly label unfinished or unvalidated tax features; do not claim regulatory certification without evidence.
