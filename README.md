# Telegram Service Platform — Portfolio Showcase

> A production-operated, bilingual Telegram service platform for educational commerce, exam-registration workflows, customer support, and multi-stage administrative operations.

[نسخه فارسی](README.fa.md) · [Case Study](PROJECT_CASE_STUDY.md) · [Architecture](docs/ARCHITECTURE.md) · [Release History](docs/RELEASE_HISTORY.md)

## Project snapshot

| Item | Current portfolio status |
|---|---|
| Production baseline | v1.1.5 |
| Validated release candidate | v1.3.0 — staging tests passed; production promotion pending |
| Production runtime | Linux VPS with managed systemd services |
| User interfaces | Persian and German |
| Validation | Automated regression suite plus concurrency and load scenarios |
| Scale scenario | 500 queued requests per section; atomic claim validation with 20 concurrent administrators |
| Official exam coverage | 8 countries and 47 documented centres |
| Source availability | Private and proprietary |

## What the platform does

- Phone-verified onboarding and channel-membership checks
- Bilingual menus and user guidance
- Educational product catalogues and protected delivery
- Toman and USDT receipt-based payment workflows
- Unique tracking codes and self-service order tracking
- Role-based administration for sales, content, support, and operations
- Support tickets and auditable administrator-to-user communication
- Multi-stage exam-registration workflow covering payment, contracts, documents, review, and fulfilment
- Official Goethe B2 date retrieval with Persian calendar presentation for Persian users
- Country- and city-scoped exam monitoring and notifications
- Administrative pagination, stage queues, audit trails, backups, and safe database migrations

## Operational workflow

The v1.3.0 release candidate strengthens high-volume administration. Requests are grouped by stage, administrators can atomically claim or release work, and each request shows its assigned administrator and verified user identity. Authorized operators can advance, cancel, delete, or re-queue a request while preserving auditability. Contract text, reminders, document follow-up, and frequently used response templates are integrated into the workflow.

Concurrency validation covers atomic assignment with 20 administrators so that the same request cannot be silently claimed by multiple operators. Load scenarios cover queues containing 500 requests per operational section.

## Official-source exam capability

The platform covers Turkey, Georgia, Russia, Indonesia, Malaysia, Pakistan, Oman, and Thailand, with 47 officially documented centres represented in the catalogue.

Dates are never fabricated. Structured dates are displayed only when returned by the official source. If no active central date is available, the interface presents the official reference link instead. Persian users see localized Solar Hijri dates, while canonical source values remain available internally for matching and order integrity.

Retrieval uses a persistent browser session, defensive parsing, restart-safe caching, bounded stale-while-refresh behaviour, and safe handling of expired Telegram callbacks.

## Engineering highlights

- Asynchronous Telegram workflows with explicit state transitions
- SQLite migrations designed to preserve existing production data
- Persistent browser integration for official-source retrieval
- Restart-safe caching with bounded stale-while-refresh behaviour
- Duplicate-delivery and repeated-side-effect protection
- Role-aware navigation, paginated queues, and atomic administrator assignment
- Audited administrator messages and operational actions
- Backup, restore, integrity-check, and rollback procedures
- Staged regression, concurrency, and load testing before production promotion

## Technology overview

Python, Aiogram, asyncio, SQLite, aiosqlite, Playwright/CDP, aiohttp, Pydantic Settings, systemd, unittest, Linux, and Git-based release management.

## My role

I led requirements definition, user and administrator workflow design, acceptance testing, Linux deployment, migration validation, operational troubleshooting, release verification, and iterative product improvement. Development followed an AI-assisted engineering workflow with manual validation of requirements, security boundaries, database safety, test results, and production behaviour.

## Delivery status

The documented v1.1.5 baseline is production-operated. The broader v1.3.0 candidate has passed the complete automated suite and dedicated concurrency/load validation in staging. It is described separately here so the portfolio does not present a staged candidate as an already deployed production release.

## Privacy and intellectual property

This public repository is documentation-only. It intentionally contains no application source code, tests, dependency manifest, environment template, credentials, customer data, database, payment record, browser profile, server address, deployment secret, or private educational content.

The production source code is maintained privately. See [SECURITY.md](SECURITY.md) and [NOTICE.md](NOTICE.md).

## Independent-project notice

This is an independent portfolio project and is not affiliated with or endorsed by Telegram, Goethe-Institut, SpotPlayer, or any other referenced third party. Third-party names describe interoperability or external sources only.

---

© 2026 Erfan Bonyani. All rights reserved.
