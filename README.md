# Telegram Service Platform — Portfolio Showcase

> A production-operated, bilingual Telegram service platform designed for educational commerce, exam-registration workflows, customer support, and administrative operations.

[نسخه فارسی](README.fa.md) · [Case Study](PROJECT_CASE_STUDY.md) · [Architecture](docs/ARCHITECTURE.md) · [Release History](docs/RELEASE_HISTORY.md)

## Project snapshot

| Item | Current portfolio status |
|---|---|
| Latest documented release | v1.1.5 |
| Production runtime | Linux VPS with managed services |
| User interfaces | Persian and German |
| Automated regression suite | 23 passing tests |
| Official exam coverage | 8 countries and 47 documented centres |
| Source availability | Private and proprietary |

## What the platform does

The application brings several real operational workflows into one Telegram interface:

- phone-verified onboarding and channel-membership checks;
- bilingual menus and user guidance;
- educational product catalogues and protected delivery;
- Toman and USDT receipt-based payment workflows;
- unique tracking codes and self-service order tracking;
- role-based administration for sales, content, support, and operations;
- support tickets and direct administrator-to-user communication;
- exam-registration requests, payment review, document requests, uploads, approval, and fulfilment;
- official Goethe B2 date retrieval with Persian calendar presentation for Persian users;
- country- and city-scoped notifications;
- administrative pagination, audit trails, backups, and safe database migrations.

## Exam-registration capability

The current release supports Turkey, Georgia, Russia, Indonesia, Malaysia, Pakistan, Oman, and Thailand. Forty-seven officially documented centres are represented in the catalogue.

Dates are never fabricated. Structured dates are displayed only when returned by the official source. If a central source has no active date, the interface presents the official reference link instead. Persian users see localized Solar Hijri dates, while canonical source values remain available internally for matching and order integrity.

## Engineering highlights

- Asynchronous Telegram workflows with clear state transitions
- SQLite migrations designed to preserve existing production data
- Persistent browser integration for official-source retrieval
- Restart-safe caching with bounded stale-while-refresh behaviour
- Duplicate-delivery protection for purchased content
- Role-aware administrative navigation and paginated work queues
- Audited administrator messages and operational actions
- Backup, restore, integrity-check, and rollback procedures
- Regression testing before staging and production deployment

## Technology overview

Python, Aiogram, asyncio, SQLite, aiosqlite, Playwright/CDP, aiohttp, Pydantic Settings, systemd, unittest, Linux, and Git-based release management.

## My role

I led requirements definition, user-flow design, acceptance testing, production deployment, migration validation, operational troubleshooting, and iterative product improvement. Development followed an AI-assisted engineering workflow with manual verification at each release stage.

## Privacy and intellectual property

This public repository is documentation-only. It intentionally contains no application source code, tests, dependency manifest, environment template, credentials, customer data, database, payment record, browser profile, server address, deployment secret, or private educational content.

The production source code is maintained privately. See [SECURITY.md](SECURITY.md) and [NOTICE.md](NOTICE.md).

## Independent-project notice

This is an independent portfolio project and is not affiliated with or endorsed by Telegram, Goethe-Institut, SpotPlayer, or any other referenced third party. Third-party names describe interoperability or external sources only.

---

© 2026 Erfan Bonyani. All rights reserved.
