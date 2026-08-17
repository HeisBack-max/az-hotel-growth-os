# Codex Execution Contract — A Z Hotel Growth OS

## Mission
Build a production-quality V1 of **Hotel Growth OS**, powered by AgenticAngels, with **A Z Hotel — Phnom Penh** as the automatically loaded default hotel.

Do not stop at planning or architecture discussion. Work directly in this repository: create and modify files, install dependencies, run commands, test, fix failures, and iterate until the application is demonstrable and the quality gates pass.

## Starting point
This is a clean build. There is no application architecture to preserve. Treat materials placed under `reference/` as product requirements, evidence, prototypes, and source context. Inspect them before implementing relevant features. Make reasonable engineering decisions without asking routine preference questions.

## Product experience
Opening the application must immediately show a polished A Z Hotel experience. No generic SaaS landing page, tenant selector, setup wizard, fake onboarding, developer screen, or empty dashboard.

The visual language should be premium minimalist hospitality: clean, contemporary, local, personal, uncomplicated, trustworthy, affordable without looking cheap. Avoid generic admin, crypto, excessive gradients, visual noise, and AI gimmicks.

## Core product
Implement a coherent application with:

1. **Management Command Center** — arrivals, departures, occupancy, current guests, unresolved requests, rooms needing attention, housekeeping, maintenance, sentiment, recovery cases, review opportunities, direct-booking opportunities, overnight alerts, and a specific operational AI brief.
2. **Guest Companion** — mobile-first, no guest account required, with towels, room cleaning, water, AC/broken-item reporting, help, transport, local recommendations, stay extension, hotel contact, late-arrival and emergency information. Support English, Khmer, and Simplified Chinese with extensible localization.
3. **Service Requests** — type, guest, room, timestamp, priority, status, assignee, notes, completion time and escalation. Support New, Accepted, In Progress, Waiting, Completed and Escalated. Surface overdue work.
4. **Guest Recovery** — positive/negative stay feedback; negative feedback creates a management recovery case and suppresses automated review solicitation until resolved.
5. **Reputation** — feedback, reviews, review candidates/history, rating metrics, recovery cases, conversion metrics and AI-assisted response drafts. No fabricated reviews or deceptive review gating.
6. **A Z Local** — curated Phnom Penh guide for Eat, Coffee, Drinks, Essentials, Pharmacy, SIM/Phone, Laundry, Transport, Attractions, Nearby, Late Night and Local Tips.
7. **Direct Booking / Return Guest** — extension requests, direct inquiries, future-stay interest, previous/repeat guests, contact preference, lead status and repeat opportunities.
8. **Marketing** — lightweight content ideas, local/room content, short-video concepts, captions, calendar and campaign tracking.
9. **AI Concierge** — safe answers for reliable hotel/local information; escalate serious complaints, emergencies, payment disputes, security issues, uncertain policy and danger. Configure provider by environment variables and provide deterministic fallback behavior without an API key.
10. **Housekeeping** — Occupied, Vacant Clean, Vacant Dirty, Cleaning, Inspection Needed, Maintenance, Out of Service; support clean now/later, DND and towels-only instructions.
11. **Maintenance** — AC, plumbing, electrical, Wi-Fi, furniture, bathroom, door/lock, lighting and other; track room, severity, report time, status, assignment, completion and recurrence.
12. **Incidents / after-hours** — lightweight operational incident records plus editable emergency, after-hours and late-arrival information. Do not claim legal/security/fire compliance.
13. **Analytics** — only decision-useful metrics such as open requests, resolution time, recovery, rating, review conversion, direct leads, extensions, housekeeping turnaround, maintenance frequency, sentiment, booking-source mix and repeat guests.

## Data architecture
Support equivalents of Hotel, User, Guest, Room, Stay/Reservation, ServiceRequest, HousekeepingTask, MaintenanceIssue, GuestFeedback, Review, ReviewRequest, Incident, LocalRecommendation, DirectBookingLead, MarketingContent, Notification, HotelSetting and AIInteraction/audit history.

Keep the data architecture extensible to multiple hotels, but automatically seed/load A Z Hotel and do not expose multi-tenancy complexity in the default UI.

## Authentication
Implement sensible staff authentication with simple Owner, Manager and Staff roles. Development/demo access must be frictionless. Document demo credentials. Keep production architecture secure.

## Demo data
Seed enough realistic A Z Hotel data that every primary screen is meaningful on first launch. Include arrivals/departures/current guests, towel request, AC issue, housekeeping work, late arrival, satisfied guest, negative recovery case, direct inquiry, repeat guest, maintenance problem, positive review, local-guide usage, extension opportunity and overnight alert. Use professional realistic names, never lorem ipsum or joke data.

Use rooms roughly 101–106, 201–206, 301–306 and 401–406 unless stronger reference material establishes a better inventory.

## Terminology
Product-facing language must be hospitality language: hotel, guest, room, stay, reservation, arrival, departure, booking, checkout and housekeeping. Remove residential language such as tenant, unit, lease, rent, residence and subletting.

## Technical baseline
Choose the strongest maintainable implementation. A strong default is Next.js + React + strict TypeScript + Tailwind + accessible components + PostgreSQL + Prisma/equivalent + schema validation + modern server/API patterns. If local development would otherwise require unavailable infrastructure, provide a documented practical local/demo path without compromising the production architecture.

Implement validation, loading states, meaningful empty states, error handling, accessibility, responsive layouts, database constraints, clean server/client boundaries and reusable components.

## No fake functionality
Every visible primary button, form, toggle, filter, navigation item and workflow must work. Remove decorative controls, TODO UI, placeholder links, dummy forms and dead buttons. Prefer a smaller functional feature over a larger fake one.

## Critical tests
Verify application startup, demo/staff access, dashboard, guest companion, localization, service-request creation/update, feedback/recovery, review-candidate flow, housekeeping update, maintenance reporting, direct inquiry, database seed, desktop and mobile layouts. Add automated tests for critical logic where appropriate.

## Quality gate
Before declaring completion, run the repository-appropriate equivalents of dependency installation, database validation/migrations/seed, lint, typecheck, tests and production build. Run the application and inspect major routes and mobile layouts. Fix failures and rerun checks. Missing external AI credentials are not a reason for the application to fail; use deterministic fallback behavior.

## README
Maintain an excellent README covering product purpose, A Z default setup, stack, prerequisites, install, environment, database, migrations, seed, development, production build/start, tests, deployment, demo credentials, AI configuration and fallback behavior.

## Priority
1. App runs.
2. Core hotel workflows work.
3. Seeded A Z experience loads immediately.
4. Guest mobile companion is excellent.
5. Management dashboard surfaces action clearly.
6. Requests and recovery work.
7. Housekeeping and maintenance work.
8. Reputation/direct-booking workflows work.
9. Visual polish.
10. Analytics and marketing enhancements.

## Autonomy
Do not repeatedly ask which framework to use, whether to continue, or whether to fix errors. Inspect available material, infer the strongest reasonable solution, implement it, document material assumptions, and continue. Ask only when proceeding is literally impossible without missing information.

## Definition of done
Another competent person can clone the repository, follow README instructions, install/configure/seed it, launch it, immediately see A Z Hotel populated with realistic workflows, use the guest and management experiences, and run the documented quality checks successfully. It should feel like V1 of a real commercial product, not a prototype or documentation exercise.
