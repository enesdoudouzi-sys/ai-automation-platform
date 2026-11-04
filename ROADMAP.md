# Product and Learning Roadmap

Milestones combine delivery with learning. A milestone is complete only when acceptance criteria are met and documented.

## 0. Foundation — current
Learn: Git, Python, FastAPI, HTTP, Pydantic, pytest, Docker basics.
Deliver: repository conventions, health endpoint, configuration, container build, CI.
Acceptance: API starts locally; health endpoint responds; tests pass; CI runs on pushes and pull requests.

## 1. API and domain model
Learn: REST design, validation, error handling, OpenAPI, SQL.
Deliver: versioned API, PostgreSQL integration, migrations, first business domain.
Acceptance: CRUD behavior is tested; schema changes are versioned; no secrets are committed.

## 2. Identity and tenant boundaries
Learn: OAuth2/OIDC, authorization, secure token handling, multi-tenant isolation.
Deliver: user identity, organizations, roles, tenant-scoped data access.
Acceptance: tests prove one tenant cannot access another tenant's records.

## 3. Workflow automation
Learn: n8n, webhooks, retries, idempotency, queues, Redis.
Deliver: signed webhook workflow with observable execution state.
Acceptance: invalid signatures are rejected; retries do not duplicate business actions.

## 4. AI and retrieval
Learn: LLM APIs, embeddings, chunking, RAG evaluation, vector search, prompt-injection risks.
Deliver: document ingestion and source-grounded question answering.
Acceptance: answers expose sources; untrusted document instructions are not treated as system instructions.

## 5. Cloud and delivery
Learn: AWS or Azure, Terraform, registries, deployment pipelines, Kubernetes concepts.
Deliver: reproducible infrastructure and deployed non-production environment.
Acceptance: deployment is repeatable; secrets stay outside Git; rollback is documented.

## 6. Security and operations
Learn: OWASP Top 10, threat modeling, GDPR principles, logging, metrics, backups.
Deliver: security baseline, audit events, dashboards and recovery procedures.
Acceptance: threat model and data lifecycle are documented; critical paths have tests and monitoring.

## 7. Portfolio release
Learn: technical writing and release management.
Deliver: architecture diagrams, demo, bilingual overview, setup guide and release notes.
Acceptance: a reviewer can understand the architecture and reproduce the demo.

## Certificates and learning evidence
Prioritize free official learning paths and practical evidence. Course completion badges are not the same as paid, proctored vendor certifications. Record completed modules and links in docs/learning/.
