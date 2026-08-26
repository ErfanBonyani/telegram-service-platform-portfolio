# Project Case Study

## Context

The project began as a focused Telegram bot and evolved into a multi-service operational platform. The central challenge was not merely adding menu buttons; it was keeping user identity, payments, orders, contracts, documents, notifications, and administrator actions consistent while the live database and operational workload continued to grow.

## Product challenges

1. **Operational clarity:** Large administrative lists had to remain usable as order volume and workflow stages increased.
2. **Concurrent ownership:** Multiple administrators needed to work simultaneously without silently claiming the same request.
3. **Data preservation:** Schema changes had to retain existing users, orders, subscriptions, and audit history.
4. **External-source reliability:** Official exam information required browser-backed retrieval, defensive parsing, caching, and explicit no-data behaviour.
5. **Traceable communication:** Administrators needed verified identity, assigned ownership, message history, contracts, reminders, and document follow-up.
6. **Safe releases:** Production updates required backups, staged tests, integrity checks, service verification, and rollback readiness.

## Implemented solution

- Built bilingual user and administrator journeys.
- Added page-based queues grouped by operational stage.
- Added atomic claim and release actions with visible administrator ownership.
- Added authorized advance, cancellation, deletion, and re-queue controls.
- Introduced complete user identity on operational cards.
- Added direct administrator messaging with auditable history and reusable message templates.
- Implemented contracts, reminders, exam document requests, user uploads, review, and approval states.
- Scoped registrations, subscriptions, and state records by country and city.
- Added eight-country exam discovery while preserving the original Turkey flow.
- Localized Persian-facing dates without modifying canonical source values.
- Added browser-backed official-source retrieval and persistent cache recovery.
- Established repeatable backup, staging, migration, deployment, and log-review procedures.

## Validation approach

Candidate releases are compiled and tested in an isolated staging directory before production promotion. Validation includes the automated regression suite, database-safety checks, manual workflow acceptance, and service/log review.

The production-operated v1.1.5 baseline passed 23 documented regression tests. The broader v1.3.0 release candidate subsequently passed the complete current test suite, a 500-request-per-section load scenario, and atomic assignment validation with 20 concurrent administrators. Production and staging status are reported separately to avoid representing a validated candidate as an already deployed release.

## Outcome

The result is a functioning production service with a validated next release that improves high-volume administration, concurrent ownership, traceable customer operations, contract and document follow-up, multi-country exam registration, and release safety. The project demonstrates product analysis, workflow design, Python backend development, database evolution, browser automation, Linux operations, testing, and practical debugging.

## My contribution

I defined requirements, designed user and administrator workflows, coordinated implementation, performed acceptance and regression testing, validated migrations, deployed and operated the service on Linux, investigated production issues, and verified release readiness. I used AI-assisted engineering tools while manually checking requirements, security boundaries, database preservation, test results, and runtime behaviour.

## What is intentionally not public

Application source, database schema implementation, production configuration, credentials, server topology details, customer records, payment artefacts, private course content, and recovery material are excluded from the public portfolio.
