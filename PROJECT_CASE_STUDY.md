# Project Case Study

## Context

The project began as a focused Telegram bot and evolved into a multi-service operational platform. The central challenge was not merely adding menu buttons; it was keeping user identity, payments, orders, documents, notifications, and administrator actions consistent while the live database continued to grow.

## Product challenges

1. **Operational clarity:** Large administrative lists had to remain usable as order volume increased.
2. **Data preservation:** Every schema change had to retain existing users, orders, subscriptions, and audit history.
3. **External-source reliability:** Official exam information required browser-backed retrieval, defensive parsing, caching, and explicit no-data behaviour.
4. **Traceable communication:** Administrators needed verified user identity, direct contact actions, message history, and document follow-up.
5. **Safe releases:** Production updates required backups, staged tests, live-database integrity checks, service verification, and rollback readiness.

## Implemented solution

- Built bilingual user and administrator journeys.
- Added page-based administrative queues and status filtering.
- Introduced complete user identity on operational cards.
- Added direct administrator messaging with auditable history.
- Implemented exam document requests, user uploads, review, and approval states.
- Scoped registrations, subscriptions, and state records by country and city.
- Added eight-country exam discovery while preserving the original Turkey flow.
- Localized Persian-facing dates without modifying canonical source values.
- Added browser-backed official-source retrieval and persistent cache recovery.
- Established repeatable backup, staging, migration, deployment, and log-review procedures.

## Validation approach

Each candidate release was compiled and tested in an isolated staging directory before production installation. The production tree was then compiled and tested again. Database integrity, record counts, services, polling startup, and application logs were checked after deployment. The documented v1.1.5 release passed 23 automated regression tests plus manual country, city, date, and repeated-interaction checks.

## Outcome

The result is a functioning production service with clearer administration, safer releases, traceable customer operations, and a user-friendly exam-registration journey. The project demonstrates product analysis, workflow design, Python backend development, database evolution, browser automation, Linux operations, and practical debugging.

## What is intentionally not public

Application source, database schema implementation, production configuration, credentials, server topology details, customer records, payment artefacts, private course content, and recovery material are excluded from the public portfolio.
