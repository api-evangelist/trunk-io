# Trunk (trunk-io)

Trunk builds developer experience and CI reliability tooling. Its platform spans Code Quality (a meta-linter and static analysis manager driven by the trunk CLI), a flake-aware parallel Merge Queue, and Flaky Tests detection/CI Analytics. Test results are uploaded from CI via the Trunk Analytics CLI/GitHub Action, and an HTTP REST API at api.trunk.io exposes Flaky Tests and Merge Queue control plus Svix-powered webhooks.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/trunk-io/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/trunk-io/refs/heads/main/apis.yml)

## Tags

- Developer Tools
- CI/CD
- Code Quality
- Flaky Tests
- Merge Queue

## Timestamps

- **Created:** 2026-06-20
- **Modified:** 2026-06-20

## APIs

### Trunk Flaky Tests API

REST API for querying Flaky Tests state - fetch test-case details, list quarantined tests, list unhealthy (FLAKY/BROKEN) tests, list tests that failed in a time range, and link external Jira/Linear tickets to a test case. Authenticated with the x-api-token header.

- **Human URL:** [https://docs.trunk.io/flaky-tests/reference/api-reference](https://docs.trunk.io/flaky-tests/reference/api-reference)
- **Base URL:** `https://api.trunk.io/v1`

#### Tags

- Flaky Tests
- Test Analytics
- Quarantine

#### Properties

- [Documentation](https://docs.trunk.io/flaky-tests/flaky-tests)
- [API Reference](https://docs.trunk.io/flaky-tests/reference/api-reference)
- [OpenAPI](openapi/trunk-io-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/trunk-io.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/trunk-io.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Trunk Test Uploads (Analytics CLI)

CI test-result ingestion surface. The trunk-analytics-cli (and the trunk-io/analytics-uploader GitHub Action) uploads JUnit XML, Bazel BEP, and XCResult test reports to Trunk for flaky-test detection, authenticated with an organization slug (--org-url-slug) and API token (--token / TRUNK_API_TOKEN).

- **Human URL:** [https://docs.trunk.io/flaky-tests/uploader](https://docs.trunk.io/flaky-tests/uploader)
- **Base URL:** `https://api.trunk.io`

#### Tags

- Test Uploads
- CI Integration
- JUnit

#### Properties

- [Documentation](https://docs.trunk.io/flaky-tests/uploader)
- [Documentation](https://docs.trunk.io/flaky-tests/get-started/ci-providers/github-actions)

### Trunk Merge Queue API

REST API to control the flake-aware parallel Merge Queue - submit, cancel, restart, and inspect pull requests; set impacted targets; create, get, update, and delete queues; and read merge-queue testing details and Prometheus metrics. Authenticated with the x-api-token header.

- **Human URL:** [https://docs.trunk.io/merge-queue/reference/merge](https://docs.trunk.io/merge-queue/reference/merge)
- **Base URL:** `https://api.trunk.io/v1`

#### Tags

- Merge Queue
- Pull Requests
- CI/CD

#### Properties

- [Documentation](https://docs.trunk.io/merge-queue)
- [API Reference](https://docs.trunk.io/merge-queue/reference/merge)
- [OpenAPI](openapi/trunk-io-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/trunk-io.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/trunk-io.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Trunk Webhooks

Svix-powered outbound webhooks for subscribing to Flaky Tests events (test_case.status_changed, test_case.monitor_status_changed, test_case.investigation_completed) and Merge Queue events (pull_request.* and pull_request_batch.* such as merged, queued, testing, failed, canceled). Used to trigger downstream workflows like GitHub Issues creation.

- **Human URL:** [https://docs.trunk.io/flaky-tests/webhooks](https://docs.trunk.io/flaky-tests/webhooks)
- **Base URL:** `https://api.trunk.io`

#### Tags

- Webhooks
- Events
- Svix

#### Properties

- [Documentation](https://docs.trunk.io/flaky-tests/webhooks)

### Trunk Code Quality CLI

Meta-linter and static analysis manager exposed through the trunk CLI and a local daemon (no public REST API). Commands include trunk init, trunk check, and trunk check --all; it hermetically installs and runs third-party linters, formatters, and security scanners, operating in Hold The Line mode by default and serving real-time annotations to IDE extensions.

- **Human URL:** [https://docs.trunk.io/code-quality](https://docs.trunk.io/code-quality)
- **Base URL:** `https://docs.trunk.io/code-quality`

#### Tags

- Code Quality
- Meta-Linter
- Static Analysis

#### Properties

- [Documentation](https://docs.trunk.io/code-quality)
- [Documentation](https://docs.trunk.io/cli)

## Common Properties

- [GitHub Organization](https://github.com/trunk-io)
- [LinkedIn](https://www.linkedin.com/company/trunkhq)
- [Website](https://trunk.io/)
- [Documentation](https://docs.trunk.io)
- [Plans](plans/trunk-io-plans-pricing.yml)
- [Rate Limits](rate-limits/trunk-io-rate-limits.yml)
- [Fin Ops](finops/trunk-io-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
