# EXPLAIN — TODO / Future features

> Features described here are **not yet implemented**. This file is a reference for future development sessions.

---

## Ethics & GDPR section

A new top-level navigation section (alongside Research, Administration, Help) with three pages.

### Review Board (`review-board.html`)

For lab managers / platform admins. Manages the review board of EXPLAIN.

- List of registered reviewers (name, institution, expertise, status)
- Select one or more reviewers to send a review request to
- Select the experiment / documents to submit for review
- Send everything by email (compose a message, attach relevant docs)
- Track sent review requests (pending / completed / rejected)

### Review (`review.html`)

For reviewers. Their personal workspace to submit validations.

- List of review requests assigned to them
- For each: view the experiment description and attached documents
- Submit a validation decision (Approved / Rejected / Revision requested)
- Leave comments visible to the lab manager
- Timeline of past reviews

### Documents (`documents.html`)

For lab managers. Central document review dashboard per project/experiment.

- Table of all documents sent for review, grouped by experiment
- Status per document (Pending / Reviewed / Rejected)
- Download or preview each document
- **Notification badge** on the sidebar nav item when one or more documents are awaiting review
  - Badge should update in real time (or on page load)
  - Should disappear once all pending documents are reviewed

---

## Notes

- The Ethics & GDPR section should sit between Administration and Help in the sidebar
- Nav item for Documents should show a red/orange badge with the count of pending review documents
- Reviewers may be external (not necessarily registered as researchers on EXPLAIN)
- Email sending is currently a stub — integrate with the Mailing template system when that is built


---

## Researcher registration page

A registration / onboarding page for new researchers joining EXPLAIN.

- Account creation form: name, email, password (or Renater SSO)
- Lab affiliation selector (from list of active labs)
- CGU acceptance checkbox
- Account must be validated by the lab admin before access is granted
- Confirmation email sent on submission
- Similar flow to the subject registration but targeted at researchers

---

## Dashboard as the universal welcome page

Replace `welcome.html` with the dashboard as the landing page for all user types.

- The dashboard (`dashboard.html`) becomes the first page seen after login for everyone
- Remove the separate `welcome.html` (or repurpose it as a redirect to dashboard)
- The dashboard content should adapt based on the user role:
  - **Lab Manager** — full dashboard as currently built (KPI cards, charts, pool composition)
  - **Researcher** — simplified view: their experiments, upcoming sessions, no accounting/pool stats
  - **Accountant** — accounting-focused view: payment summary, pending payments, total disbursed
  - **Lab Assistant** — upcoming sessions and calendar view
- The nav active state should point to "Dashboard" (currently pointing to "Welcome")
- Update all internal links that currently point to `welcome.html` to point to `dashboard.html`
- The hub.html dev switcher button on `welcome.html` should move to `dashboard.html`
