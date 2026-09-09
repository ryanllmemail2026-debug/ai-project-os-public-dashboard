# YouTube Second Brain — Primary Build

**Ryan McConihe · Applied AI systems · investigations + operations background**

My primary public project is **YouTube Second Brain**: a budget-first research and knowledge system designed to capture source evidence once, preserve it, make a large historical archive searchable, and reserve expensive AI reasoning for the material that actually warrants it.

## Verified milestone

The historical-search production stage represented **29,521 catalog videos**, passed validation and quality auditing, executed real lexical search probes, published the complete index to **Turso/libSQL**, independently verified the remote data, and produced a production evidence artifact.

That milestone answered a concrete product question:

> **Can a large historical YouTube research archive become reliably searchable without repeatedly reprocessing everything?**

**Yes.**

### What the system demonstrates

- Python + GitHub Actions workflows
- SQLite / Turso / libSQL search infrastructure
- transcript and metadata evidence preservation
- resumable long-running processing
- deterministic validation before AI escalation
- cost-aware classification and selective enrichment
- automated Gitleaks, Semgrep, and OSV security checks
- evidence-first retrieval and human verification

[Read the full YouTube Second Brain case study →](projects/YOUTUBE_RESEARCH_BRAIN.md)

---

## Supporting build — Endless Thread

**Endless Thread** is the project-memory and recovery system I am building to keep long-running AI work from losing decisions, evidence, history, open loops, and exact next actions when chats, models, or tools change.

A real recovery test was run against YouTube Second Brain: a fresh AI session successfully reconstructed the project's current state, strongest evidence, stale boundaries, do-not-redo rules, and exact next task without me re-explaining the project history.

It demonstrates:

- multi-model / multi-provider workflow design
- durable state in JSON + Markdown
- structured handoffs and archive indexing
- deterministic validation and stale/conflict detection
- evidence-based completion gates
- human-in-the-loop decision boundaries
- context minimization and progressive retrieval
- AI workflow orchestration

[Read the Endless Thread case study →](projects/ENDLESS_THREAD.md)

## How I approach AI systems

My background is not traditional software engineering. It comes from investigations, insurance and regulated operations, finance/property workflows, research, and years of making decisions from incomplete information.

That is why my systems tend to emphasize:

**problem definition → source evidence → deterministic processing → selective AI → validation → human control**

[Read my building principles →](BUILDING_PRINCIPLES.md)

## Public-safe by design

The implementation repositories remain private. This public portfolio exposes non-sensitive architecture, verified milestones, and design choices without publishing credentials, private source data, internal handoffs, or sensitive implementation details.

## Live portfolio

https://ryanllmemail2026-debug.github.io/youtube-second-brain/
