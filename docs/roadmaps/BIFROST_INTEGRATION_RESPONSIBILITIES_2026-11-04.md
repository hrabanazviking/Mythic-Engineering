# Mythic Engineering: Cross-Repository Knowledge and Project Protocol

**Repository:** hrabanazviking/Mythic-Engineering  
**Date:** 2026-11-04  
**State:** Planned, not implemented.

## Shared roadmap and operating boundaries

- Canonical full roadmap: https://github.com/hrabanazviking/bifrost-viewer/blob/main/docs/roadmaps/BIFROST_SECOND_BRAIN_MASTER_EXPANSION_ROADMAP_2026-11-04.md
- Local copy: [BIFROST_SECOND_BRAIN_MASTER_EXPANSION_ROADMAP_2026-11-04.md](BIFROST_SECOND_BRAIN_MASTER_EXPANSION_ROADMAP_2026-11-04.md)
- This document is a **proposal**, not a report of implemented features.
- Keep this application independent. All Second Brain access must be optional, versioned, permission-scoped and disabled by default.
- Never store private documents, account identities, OAuth configuration, access tokens, API keys, secrets, live logs, or database contents in public GitHub.
- Bifröst Viewer is the knowledge-service coordinator; Skein and Skry expose their own stable public functions. Consumers must not query private PostgreSQL directly.

## Objective

Document a reusable engineering convention for optionally integrating any Mythic Engineering application with the Second Brain without creating another global app or scattering credentials.

## Implementation responsibilities

1. Treat this roadmap as the shared reference for development guidance, not mandatory code dependencies for unrelated projects.
2. Define standard optional KnowledgeProvider capability: discover, authenticate, query, retrieve cited evidence, append only if authorized, health, disconnect.
3. Define standard project-status event payloads so Bifröst Project Longhouse can track repos, workstreams, checkpoints and agents.
4. Specify explicit ownership, read/write permission scopes and no-cross-corpus defaults.
5. Provide a short sanitized template each project can adopt, with synthetic fixtures and no personal credentials.
6. Document no-copy clean-room feature research, dependency/license due diligence, restore-before-migrate and reproducibility rituals.
7. Add a convention for distinguishing implemented features, experiments, proposed roadmap items and observed run-time measurements.

## Acceptance tests

- [ ] Other projects can add optional knowledge integration without sharing privileged DB access.
- [ ] One project registry becomes discoverable without requiring every project to ingest its own Markdown copy.
- [ ] Clean-room and secret scanning are included in acceptance gates.

## Suggested implementation process

1. Audit installed source and actual local changes first, particularly unpublished agent work.
2. Map the existing public extension points, resource budgets and security boundary.
3. Add a small, independently testable optional adapter and sanitized fixtures.
4. Exercise permission denial, network loss, stale output, retry/idempotence and recovery.
5. Document new stable contracts and record the limitation before deployment.
6. Confirm the core application's tests and offline operation remain intact.

The canonical Bifröst roadmap sets the shared protocol vision; this repository retains ownership of its own integration implementation.
