# AI Automation Platform

**A secure, multi-tenant AI automation platform for small and medium-sized businesses.**

> Project status: **Foundation / early development**. Features described in the roadmap are planned, not yet implemented.

## Vision

Build a maintainable platform that helps SMEs connect business systems, automate repeatable workflows, and use AI capabilities with clear security boundaries and operational visibility.

## Initial technology direction

| Layer | Planned technology |
|---|---|
| API | Python, FastAPI, Pydantic |
| Persistence | PostgreSQL |
| Cache and background jobs | Redis |
| Workflow automation | n8n, webhooks |
| AI capabilities | LLM integrations, RAG, vector search |
| Runtime | Docker |
| Cloud and infrastructure | AWS or Azure, Terraform |
| Quality and delivery | Pytest, GitHub Actions |
| Security | OAuth2/OIDC, OWASP practices, GDPR-conscious design |

Technology choices will be validated incrementally. We will avoid introducing infrastructure before the product needs it.

## Repository structure

The initial implementation will be developed in small, reviewable increments. The target structure is documented in [docs/architecture/overview.md](docs/architecture/overview.md).

## Getting started

The backend setup instructions will be added with the first FastAPI implementation. Until then, there is no runnable application.

## Development principles

- Small, focused changes with meaningful commits.
- Automated tests for application behavior.
- Configuration through environment variables.
- Never commit credentials, tokens, or production data.
- Document architectural decisions and trade-offs.
- Treat security, privacy, accessibility, and observability as design requirements.

## Roadmap

See [ROADMAP.md](ROADMAP.md) for the learning and delivery plan.

## Language

The primary documentation is maintained in English, with German learning notes and explanations added alongside it where useful.

## License

License selection is pending. Do not assume this repository is licensed for redistribution or commercial reuse until a license is added.
