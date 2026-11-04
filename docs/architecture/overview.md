# Architecture Overview

## Current state
The repository currently contains an initial FastAPI application with a root route and health endpoint. PostgreSQL, Redis, workflow automation, AI retrieval, identity, and cloud infrastructure are planned and not yet implemented.

## Target logical architecture

    Web Client
        |
        v
    FastAPI API ---- Identity and Tenant Context
        |
        +---- Domain Services ---- PostgreSQL
        |                    +---- Redis / Background Jobs
        +---- Workflow Integration ---- n8n
        +---- AI Orchestration ---- LLM / Vector Store

Cross-cutting concerns: security, audit logging, metrics, tracing, privacy controls.

## Design principles
1. Establish tenant identity before accessing tenant-owned data.
2. Enforce authorization server-side; never trust tenant IDs supplied by clients alone.
3. Keep external integrations behind explicit interfaces and timeouts.
4. Make webhook processing idempotent and validate authenticity.
5. Store secrets outside source control.
6. Add infrastructure only when a concrete requirement justifies it.

## Initial deployment shape
The first local runtime is a single FastAPI container. PostgreSQL and Redis will be added in later milestones with health checks, persistent development volumes, and documented backup behavior.
