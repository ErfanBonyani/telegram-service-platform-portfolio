# Public Release History

This is a non-technical summary. Internal source changes and deployment details are intentionally omitted.

## v1.1.0 — Administrative usability

- Improved administrative navigation and order identification.
- Added pagination and clearer work queues.
- Preserved historical administrator messages during migration.

## v1.1.1 — Remaining administrative lists

- Extended pagination and consistent navigation across additional request lists.
- Reduced the difficulty of following growing exam-registration queues.

## v1.1.2 — Identity, contact, and documents

- Added complete Telegram identity to operational request cards.
- Added direct administrator-to-user contact actions and message audit history.
- Added exam document request, upload, review, and approval workflows.

## v1.1.3 — Multi-country exam registration

- Expanded the official catalogue to eight countries and 47 documented centres.
- Scoped orders, subscriptions, and monitoring state by country and city.
- Preserved the original Turkey experience and Persian date localization.
- Enforced official-source-only date presentation.

## v1.1.4 — Retrieval responsiveness

- Removed unnecessary waiting from the first official-source retrieval.
- Reduced network-log noise and handled expired Telegram interactions safely in the exam flow.

## v1.1.5 — Persistent performance

- Added restart-safe persistence for successful official exam responses.
- Added bounded stale-while-refresh behaviour for responsive user views.
- Added fast browser-origin establishment with a reliability fallback.
- Suppressed harmless repeated-message update errors in exam pages.
- Passed 23 automated regression tests before and after production installation.
