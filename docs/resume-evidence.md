# localbasket Resume Evidence

Service summary:
- Kotlin Spring order risk scoring.

Repository evidence:
- Origin workspace: https://github.com/localbasket-labs/localbasket-workspace
- Frontend repo: https://github.com/localbasket-labs/localbasket-fe
- Backend repo: https://github.com/localbasket-labs/localbasket-be
- Personal mirror: https://github.com/cyjoon68/localbasket-workspace

Implementation evidence:
- Frontend: Expo Router, feature-layer API via `ky`, Unistyles UI.
- Backend: domain API contract in `localbasket-be/openapi.yaml`.
- Data: `order_decisions` MySQL migration plus Redis store-risk cache.
- Infra: Dockerfile, GitHub Actions, ArgoCD, Kubernetes, Grafana dashboard stub.
- Ops: MySQL, Redis, RabbitMQ, Datadog-style logging/telemetry, Sentry env boundary.

Interview proof:
- API: `POST /api/orders/decide`, `GET /api/dashboard`.
- Domain rule: short promised delivery windows and high order totals are routed to review.
- Async boundary: order decisions publish to RabbitMQ and store risk is cached in Redis.
- Production angle: separate FE/BE repos, workspace submodules, GitOps manifest, CI rule gates.

Resume bullets:
- Implemented Kotlin Spring order risk scoring with explicit API contract and data schema.
- Built public multi-repo Git submodule workspace with org origin and personal mirror.
- Added CI, Docker, GitOps, observability, and dependency-light self-check gates.

Verification:
- `node scripts/self-check.mjs`
- `cd localbasket-fe && npm run self-check`
- backend self-check in `localbasket-be/scripts`
