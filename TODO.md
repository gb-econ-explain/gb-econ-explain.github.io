# EXPLAIN — TODO / Future features

> Features described here are **not yet implemented**. This file is a reference for future development sessions.

---

## Ethics & GDPR section

A new top-level navigation section (alongside Research, Administration, Help) with three pages.

### Review Board (`review-board.html`)

For lab managers / platform admins. Manages the review board of EXPLAIN.

- Add a button to send to review on the right menu.
- Add a button to produce the certificate for validated reviews.
- Add a status for reviews for which the certificate has been produced, like "Archived".

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

## Dashboard

- The dashboard content should adapt based on the user role:
  - **Lab Manager** — full dashboard as currently built (KPI cards, charts, pool composition)
  - **Researcher** — simplified view: their experiments, upcoming sessions, no accounting/pool stats
  - **Accountant** — accounting-focused view: payment summary, pending payments, total disbursed
  - **Lab Assistant** — upcoming sessions and calendar view
- The nav active state should point to "Dashboard" (currently pointing to "Welcome")
- Update all internal links that currently point to `welcome.html` to point to `dashboard.html`
- The hub.html dev switcher button on `welcome.html` should move to `dashboard.html`

---

## Acknowledgment page

A static page accessible from the Help section (or footer).

- **"How to cite EXPLAIN"** section: standard citation format (APA, BibTeX, etc.) for researchers who used the platform in their studies
- **Project history**: narrative of how the platform was built, key milestones, funding sources
- **Project team**: list of contributors with name, role, institution

---

## Accounting — per-experiment accountant authorisation

Allow lab managers to specify which accountant service can access and extract payment data for a given experiment.

- In the **experiment settings page**, add a field "Payment managed by" with a selector of authorised accountant services (e.g. University_Acc, S2C2H — CNRS payment service, or custom)
- In the **accounting page**, accountants only see the experiments they are authorised for
- The authorisation is set per experiment, not globally
- Example use case: payments for experiment A go through the university accountant, payments for experiment B go through CNRS S2C2H

---

## Session editing — before invitations are sent

If a session has been created but invitations have not yet been sent, it should be fully editable: quotas, filters, date/time, slots, group size, minimum needed, etc.

Once invitations are sent, the session becomes locked (current behaviour: date/time cannot be modified if session is public).

Add a clear visual indicator on the session detail page showing whether the session is still editable or locked, and why.

