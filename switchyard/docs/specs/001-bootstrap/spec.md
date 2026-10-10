# Spec 001: Project bootstrap

- **Status:** Draft (review, then change to Approved)
- **Owner:** @OWNER
- **Related ADRs:** 0001, 0002 (Node + TS + Fastify), 0011 (OpenTelemetry)

## Problem
We need a runnable, tested, observable skeleton so every following feature starts from the same quality baseline.

## User stories
- As a **contributor**, I want one command to start the full local stack, so I can develop without manual setup.
- As a **maintainer**, I want CI to block broken code, so `main` is always releasable.
- As an **operator**, I want health/readiness endpoints and telemetry from day one.

## Acceptance criteria (EARS)
- **AC-1** WHEN a developer runs `docker compose up -d`, THE stack SHALL start the gateway, Postgres (with pgvector), Redis, Redpanda, Ollama and grafana/otel-lgtm.
- **AC-2** WHEN `GET /healthz` is called, THE gateway SHALL respond `200 {"status":"ok"}`.
- **AC-3** WHEN `GET /readyz` is called AND Postgres and Redis are reachable, THE gateway SHALL respond 200; IF any dependency is unreachable, THEN it SHALL respond 503 listing the failing dependency.
- **AC-4** WHEN the gateway starts with an invalid `config/switchyard.yaml` or missing required env vars, THE process SHALL exit with a non-zero code and a human-readable validation error.
- **AC-5** WHEN any HTTP request is handled, THE gateway SHALL emit an OpenTelemetry span and a JSON log line containing the same trace id.
- **AC-6** WHEN a pull request is opened, THE CI SHALL run lint, typecheck, unit tests and build, and fail on any error.
- **AC-7** WHEN the process receives SIGTERM, THE gateway SHALL stop accepting connections and exit within 10 s.

## Non-goals
- Any `/v1/*` proxy behaviour (spec 002).
- Authentication (spec 004).

## Open questions
- Should Ollama be in a separate compose profile (`--profile ollama`) to keep the default stack light?
