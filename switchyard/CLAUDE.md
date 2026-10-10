# CLAUDE.md: Switchyard development harness

Switchyard is a self-hosted, OpenAI-compatible LLM gateway (Node.js 24 + TypeScript + Fastify, Postgres/pgvector, Redis, Redpanda/Kafka, OpenTelemetry). Read `README.md` and `docs/architecture.md` for context.

## Golden rules
1. **Spec-driven.** Never implement a feature without an approved spec in `docs/specs/NNN-name/` (`spec.md` with `Status: Approved`). If none exists, propose one with `/spec` and stop.
2. **One task at a time.** Implement only the next unchecked task in `tasks.md`. Do not start the next one in the same turn unless asked.
3. **Test first.** For every task, write or adjust the failing test that proves the linked acceptance criterion, then the code.
4. **Decisions become ADRs.** If you face a non-trivial technical choice (library, data model, protocol, trade-off), stop and propose an ADR with `/adr` (Status: Proposed). Don't silently decide.
5. **Stay in scope.** Don't refactor or add features outside the current task. Note ideas in the spec's "Open questions" instead.
6. **Verify before done.** Run `pnpm verify`. A task is done only when it passes; then tick the checkbox in `tasks.md`.
7. **English only** in code, comments, docs, commits.

## Commands
- `pnpm dev`: gateway in watch mode · `pnpm dev:worker`: usage worker
- `pnpm verify`: lint + typecheck + unit tests + build (must pass)
- `pnpm test:int`: integration tests (Testcontainers; needs Docker)
- `pnpm test:contract`: OpenAI SDK contract tests
- `docker compose up -d`: full local stack

## Architecture rules
- `src/core` holds canonical types, errors and ports (interfaces). It must not import from `src/infra` or `src/modules`.
- `src/modules/*` implement features and depend on ports, not on concrete infra.
- `src/infra/*` implements ports (db, redis, kafka, telemetry).
- Build the Fastify app in `src/app.ts` with injectable dependencies so tests can use fakes.
- Public errors use the OpenAI error shape: `{ error: { message, type, code } }`.
- Never log prompt/response content or secrets. Span attributes must be sanitized.
- Never retry upstream after the first streamed byte has been sent to the client (ADR-0008).

## Code style
- TypeScript strict, no `any` (use `unknown` + Zod parsing at boundaries).
- Small pure functions for logic (routing, pricing, PII detection) so they're easy to unit-test.
- Biome for lint/format. Conventional Commits with spec id: `feat(cache): add semantic lookup [spec-009]`.

## SDD artifacts
- `docs/specs/NNN-name/spec.md`: problem, user stories, EARS acceptance criteria (`AC-n`), non-goals, open questions, status.
- `docs/specs/NNN-name/design.md`: components, contracts, data, sequence diagram, related ADRs, risks.
- `docs/specs/NNN-name/tasks.md`: small tasks (≤ ~2h), each linked to ACs and naming its test.
- `docs/adr/NNNN-title.md`: MADR format (see `0000-template.md`).

## Definition of done (per spec)
All ACs covered by tests · `pnpm verify` and CI green · docs/README updated · related ADRs Accepted · metrics/traces added for new behaviour.
