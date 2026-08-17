# A Z Hotel — Canonical Source Context

This file consolidates the uploaded A Z Hotel source package for Codex. Treat it as product/source context, not as verified production truth. Where statements conflict, prefer the newer Master Project Summary dated 18 August 2026, preserve uncertainty labels, and do not invent hotel facts.

## North Star
Turn A Z Hotel into a digitally intelligent hotel with a guest-facing companion, an operator control layer, and a credible path from demonstration to deployed production.

The required outcome is one project that opens directly to A Z Hotel, runs cleanly, contains the required assets, and is deployable without the recipient reconstructing context.

## Product surfaces
1. Guest Companion — customer-facing mobile experience for discovery, requests, hotel information and assistance.
2. Hotel Operations Dashboard — staff/management surface for requests, status, insights and action.
3. Digital Key Concept — future concept only unless a certified live integration exists.

## Core problem
Guest-side friction: hotel information, recommendations, service requests and answers are fragmented; guests wait for simple answers; staff repeat work; language/availability adds friction.

Operator-side blindness: requests can be lost across shifts/channels; management lacks one live view of unresolved work, response time and recurring failures.

System opportunity: capture guest intent once, route it correctly, track completion, surface exceptions and learn from aggregate demand. The product must reduce work rather than add bureaucracy.

## MVP production boundaries
### Guest Companion
- Hotel-branded direct opening route.
- Stay information, FAQs, local recommendations, service request creation, multilingual-ready UI, clear escalation to staff.
- Do not promise 24/7 human response unless verified.
- Do not expose internal data.
- Stay-specific actions need appropriate room/stay association.

### Operations Dashboard
- Unified request queue.
- Status, owner, priority, timestamps, filters, guest/context view, simple performance metrics, audit trail.
- Role-based access and data minimization.
- Automated actions must be reviewable/reversible.

### Intelligence layer
- Approved hotel knowledge retrieval.
- Response drafting, intent classification, translation assistance, routing suggestions and trend summaries.
- Escalate ambiguity, safety, money, complaints, access and identity.
- Never invent hotel policy or availability.

### Digital Key
Concept only until lock vendor, mobile wallet/NFC/BLE architecture, identity proofing, revocation, security testing, emergency-mode and liability are resolved. Keep physical access logic deterministic and human-controlled.

## Target guest journey
1. Guest opens A Z Hotel directly — no chooser or developer landing page.
2. Interface requests only minimum context needed: language, room/stay association, request type.
3. Guest receives a verified answer or submits a structured service request.
4. System confirms receipt, shows status and routes exceptions to staff.
5. Completion is recorded; optional feedback closes the loop.

## Target staff journey
1. Staff see prioritized unified queue at shift start.
2. Every request has owner, timestamp, status, context and escalation rule.
3. Operator resolves/reassigns request; guest sees status change.
4. Management sees unresolved exceptions and recurring failure patterns rather than vanity metrics.

## Technical architecture principle
Recommended layers: responsive guest web app/PWA + authenticated staff dashboard; application API for authentication, stay/room context, request lifecycle, knowledge queries, notifications, integrations and audit logging; relational store for users/stays/rooms/requests/status/content/feedback/consent; constrained AI orchestration; environment separation, secrets management, monitoring, alerting, backups, rollback and incident logging.

AI may interpret and recommend. Deterministic services must own identity, permissions, money, room access, status transitions and audit records.

## Core data model
At minimum support equivalents of:
- Hotel
- User / Guest
- Stay / Reservation
- Room
- Service Request
- Request Assignment / Status History
- Knowledge Item
- Feedback
- Review / Review Request
- Housekeeping Task
- Maintenance Issue
- Incident
- Local Recommendation
- Direct Booking Lead
- Marketing Content
- Notification
- Hotel Setting
- Audit / AI Interaction record

## Reliability / bounded self-correction
Do not implement unrestricted self-modification. If monitoring or remediation is included, it must be bounded, logged, reversible and guarded by a kill switch.

Suggested checks from the source package:
- Frequent: uptime, key endpoints, synthetic guest request, dashboard availability.
- 15-minute class: error rate, latency, queue backlog, notification/integration health.
- Hourly: broken links, stale content flags, unresolved critical requests, response-quality sample.
- Daily: backups, restore sample, dependency/security scan, retention tasks, analytics integrity.
- Weekly: knowledge freshness, permissions, SLA trend, false-answer review, cost/capacity.

Never autonomously change authentication, authorization, payment, digital-key logic, retention policy or guest-facing/legal policy.

## Security, privacy and safety controls
- Data minimization; encryption in transit/at rest where production data is used; role-based access; short retention; access logs.
- Approved-source retrieval, provenance/confidence and staff escalation for policy/service answers.
- Prompt-injection defenses: separate instructions from data, sanitize retrieved content, constrain tools, allowlist actions, monitor anomalies.
- Manual fallback, visible system state, exportable queue, incident procedures.
- Timeouts, circuit breakers, idempotent retries and graceful degradation for integrations.
- Keep digital key outside MVP unless vendor/security conditions are satisfied.

## Delivery standard / definition of done
A recipient can open the project, see A Z Hotel immediately, understand the demo without explanation, run it locally with one documented command, and deploy it through a documented production path.

Repository must contain canonical source, assets, configuration examples, tests, docs and deployment files. No placeholder brand, template selector, dead navigation, missing assets or console errors. Secrets are never committed; provide `.env.example` only. Seed/demo data must be separated from production data.

Quality gates:
- Functional: primary guest/staff journeys complete without dead ends.
- Responsive: common mobile/desktop viewports and keyboard navigation work.
- Accessibility: semantic structure, labels, focus visibility, contrast and basic screen-reader flow.
- Security: no exposed secrets, authorization/input handling tested, logs avoid sensitive content.
- Reliability: health checks, structured logs, error tracking, backup/rollback plan and synthetic monitoring.
- Content: facts/policies approved or visibly marked provisional.
- Deployment: working preview/production target with TLS/environment config and smoke tests when authorization exists.

## Pilot sequence
Use the newer structure unless management directs otherwise:
- 7-day proof of value for guest-service / visitor-management workflow.
- If justified, expand to a 30-day controlled operational pilot.
- Digital-key assessment remains a separate later track.

## Success metrics from source package
- Request completion rate: baseline then target >=90% for in-scope categories.
- Median first response: set with A Z Hotel after staffing discovery.
- Median resolution time: improve against baseline.
- Escalation accuracy: >=95% in reviewed pilot sample.
- Answer correctness: >=98% for reviewed factual responses, zero tolerance for dangerous access/safety errors.
- Staff adoption: >=80% during pilot shifts.
- Guest satisfaction: baseline first, improve without coercive prompting.
- System availability: >=99.5% excluding agreed maintenance during pilot.

## Commercial / meeting narrative
Position this as one operating layer that makes guest service faster and gives management visibility in real time — not another generic hotel website and not criticism of the team.

Discovery questions include:
- Where do guest requests arrive and where do they get lost?
- Which questions consume staff time repeatedly?
- What PMS, messaging, lock and housekeeping systems are actually in use?
- Which guest data may be processed, by whom, and for how long?
- Which one workflow would create undeniable value in a small pilot?

Demonstration order:
1. Guest Companion — submit an actual example request.
2. Operations Dashboard — show routing, ownership, status and resolution.
3. Digital Key — concept only, with explicit security/vendor dependencies.

## Evidence and assumptions that MUST remain labelled
Public listings suggest approximately 27–28 rooms, but this requires management confirmation.

Some listings refer to a 24-hour front desk/security/amenities, but these are not operating facts until management confirms them.

Firsthand/source observations in the package describe a lean team, no continuously staffed overnight reception, physical room cards and CCTV, with entry/elevator supervision potentially inconsistent. Treat these as observations requiring validation, not accusations or guaranteed facts.

A resident-reported unauthorized-access/property-loss concern appears in the source package. It is explicitly unverified and must never be presented as a finding of fault.

Do not assume pools, gyms, spas, parking, room service, 24-hour desk, security presence, NFC/Bluetooth/mobile-key capability, elevator APIs or online card revocation.

## Management-confirmation checklist
Before production claims or a live pilot, confirm:
- Room count and floor layout.
- Staffing by time of day.
- Named owner/manager approval path.
- Main/side entrance procedure.
- Visitor policy/practice.
- Room-card vendor and revocation capability.
- Who can issue/revoke cards.
- CCTV zones, retention and export method.
- Incident log/process.
- On-call person, contact method and acknowledgement expectation.
- What may be tested / expressly excluded.
- Success measures.
- Actual PMS, messaging, housekeeping, website/booking and lock systems.
- Approved hotel facts, policies, service hours, escalation contacts and guest-facing content.
- Hosting, domain/subdomain, data region, authentication method and notification channel.
- Retention, consent, access roles, incident owner and acceptable logs.

## Risk register themes
- Entry routine inconsistency -> management-approved entry routine and shift log.
- Visitor approval informality -> named approval, time window, entry/exit status.
- Lost/compromised card inconsistency -> record, revoke where supported, replace and log.
- CCTV preservation delay -> checklist for time range, cameras, custodian, export ID, retention deadline.
- Overnight single-person dependency -> named on-call contact, acknowledgement and severity rules.
- Privacy -> minimum data, restricted access, explicit retention/deletion.
- Demo mistaken for live system -> persistent concept/fictional-data labeling where relevant.
- Staff burden -> keep routines lightweight and gather feedback.

## Product positioning
A Z Hotel should feel clean, contemporary, useful, local, personal, uncomplicated and trustworthy; affordable without looking cheap. Avoid corporate-chain aesthetics, generic admin software, crypto styling and excessive futurism.

## Codex build mandate
Take ownership of this repository and finish it as a production-ready A Z Hotel Intelligence / Hotel Growth OS product. Audit existing files and changes. Make A Z Hotel the default experience on launch. Unify Guest Companion and Operations Dashboard into one coherent product; keep Digital Key clearly concept-only unless certified integration exists. Eliminate placeholders, dead routes, missing assets, console errors and ambiguous setup. Implement secure configuration, tests, health checks, structured logging, accessible responsive UI, deployment configuration and rollback instructions. Do not claim integrations or hotel facts that are not verified. Keep identity, permissions, payments, room access and policy changes deterministic and human-controlled. Run the product, test all primary journeys, fix failures, and continue until acceptance criteria pass or a genuine external authorization/dependency blocks progress.
