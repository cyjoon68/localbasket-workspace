# LocalBasket Workspace

Hyperlocal order and inventory control service.

Repos:
- `localbasket-workspace`: parent workspace and submodule root.
- `localbasket-fe`: Expo app, `ky` API client.
- `localbasket-be`: Kotlin Spring REST API.

Architecture:
- MySQL: order and inventory state.
- Redis: hot store stock cache.
- RabbitMQ: dispatch and stock event fanout.
- GitHub Actions + ArgoCD: CI and GitOps deployment.
- Datadog, Grafana, Sentry: logs, metrics, errors.

Resume bullets:
- Built order risk scoring API that routes risky hyperlocal orders to inventory review.
- Split FE/BE into Git submodules with `develop` default branch and public repo workflow.
- Designed ops baseline with MySQL, Redis, RabbitMQ, CI, GitOps, and observability.

Run:
- `docker compose up -d`
- `cd localbasket-be && ./gradlew test`
- `cd localbasket-fe && npm install && npm run typecheck`
LocalBasket git submodule workspace
