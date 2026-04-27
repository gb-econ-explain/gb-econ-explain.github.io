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

