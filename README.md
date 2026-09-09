# Ryan McConihe — Applied AI Systems Portfolio

**AI systems builder · investigations + operations background · aspiring solopreneur**

I build practical AI-assisted systems around messy real-world problems: too much information, fragile workflows, expensive re-analysis, lost project context, weak evidence trails, and repetitive human relay.

I am not trying to make every problem an LLM problem. My approach is usually:

**define the problem → preserve the evidence → automate deterministic work → add AI where judgment helps → validate the result → keep humans in control of consequential decisions**

## Featured builds

### 1. YouTube Research Brain — working system / major milestone shipped

A budget-first research system designed to capture source evidence once, preserve it, make a large historical archive searchable, and reserve expensive AI analysis for material that actually deserves it.

**Verified milestone:** a production workflow built, audited, published, and remotely verified a searchable lexical index representing **29,521 catalog videos** in Turso/libSQL.

What it demonstrates:

- Python + GitHub Actions workflows
- SQLite / Turso / libSQL search infrastructure
- transcript and metadata evidence preservation
- resumable long-running processing
- deterministic validation before AI escalation
- cost-aware classification / selective enrichment architecture
- automated Gitleaks, Semgrep, and OSV security checks

[Read the case study →](projects/YOUTUBE_RESEARCH_BRAIN.md)

---

### 2. AI Project OS — active systems build

A provider-neutral operating layer for long-running AI projects so project memory does not disappear when a chat fills up or a model changes.

The system keeps durable project state, decisions, evidence, open loops, handoffs, retrieval instructions, and next actions outside conversational memory.

**Proven milestone:** the continuity model was rolled into YouTube Research Brain and a fresh AI session successfully reconstructed the real project's state, evidence, stale boundaries, and exact next task without me re-explaining the history.

Current work includes a deterministic continuity-health checker and reducing manual relay between AI tools and projects.

What it demonstrates:

- multi-agent / multi-provider workflow design
- durable state in JSON + Markdown
- deterministic validation
- evidence-based completion gates
- human-in-the-loop decision boundaries
- context minimization and retrieval design
- AI workflow orchestration

[Read the case study →](projects/AI_PROJECT_OS.md)

## How I build

A few principles repeat across the projects:

- **Problem first.** Start with an expensive or frustrating workflow, not a model feature.
- **Evidence before confidence.** Important conclusions should be traceable and testable.
- **Cheap before expensive.** Rules, structured data, search, caching, and deterministic processing come before broad LLM usage.
- **Preserve the source.** Derived intelligence can improve without recreating the underlying evidence.
- **Human gates for real decisions.** Money, permissions, privacy exposure, destructive actions, and major product choices stay human-controlled.
- **Provider-neutral when possible.** A useful system should survive a change in models or vendors.
- **Label maturity honestly.** Prototype, proven milestone, and production are different things.

[Read all building principles →](BUILDING_PRINCIPLES.md)

## Where I am headed

My background is not a traditional software-engineering path. It comes from investigations, insurance/regulated operations, finance-adjacent work, research, and years of making decisions from incomplete information.

That is increasingly what I want to combine with AI: **find painful information-heavy business problems, understand the actual workflow, and build focused systems that make the work cheaper, faster, more reliable, or easier to reason about.**

Long term, I am interested in building products and small AI businesses — not just using AI as a productivity tool.

## Public-safe by design

The implementation repositories behind these projects remain private. This portfolio intentionally exposes architecture, verified milestones, design decisions, and non-sensitive technical concepts without publishing credentials, private source data, internal handoffs, or sensitive implementation details.

## Live portfolio

The repository also powers a GitHub Pages portfolio:

**https://ryanllmemail2026-debug.github.io/ai-project-os-public-dashboard/**
