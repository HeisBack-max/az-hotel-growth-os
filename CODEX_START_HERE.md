# Codex: Start Here

Read `AGENTS.md` and `reference/MASTER_SOURCE_CONTEXT.md` first. Then begin implementation immediately.

Do not stop at planning. Do not ask routine questions. Build the application in this repository from scratch, using the reference material as the source context. A Z Hotel must open as the default experience.

Execution order:
1. Scaffold the production application and choose a maintainable stack consistent with `AGENTS.md`.
2. Implement the A Z Hotel branded default route and realistic seeded data.
3. Implement the mobile Guest Companion and the staff Operations Dashboard as one connected system.
4. Make service requests flow end-to-end from guest submission to staff queue/status/resolution.
5. Add housekeeping, maintenance, guest recovery, reputation, direct-booking and local-guide workflows according to `AGENTS.md`.
6. Keep Digital Key explicitly concept-only unless a certified integration is present.
7. Add deterministic fallback behavior for AI-dependent features when no API key exists.
8. Add authentication/demo access, validation, error/loading states, accessibility and responsive behavior.
9. Add database schema/migrations/seed data, `.env.example`, tests and deployment configuration.
10. Run the app. Run lint, typecheck, tests and production build. Fix failures. Inspect major desktop/mobile routes. Repeat until the definition of done in `AGENTS.md` is satisfied or a genuine external authorization/dependency blocks progress.

Do not claim unverified hotel facts or integrations. Preserve explicit uncertainty and concept/demo boundaries from the reference material.

When finished, report only what was actually completed, architecture, commands, demo credentials, checks and actual results, plus genuine external blockers.
