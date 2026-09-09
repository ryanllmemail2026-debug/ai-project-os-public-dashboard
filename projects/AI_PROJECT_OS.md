# AI Project Operating System

**Status:** Active development. Fresh-chat continuity has been proven on a real project; zero-relay automation is the current frontier.

## The problem

Long-running AI projects often fail for a surprisingly non-technical reason: the important context lives inside conversations.

When that happens, changing chats or changing AI providers can erase:

- why the project started;
- what decisions were made;
- what was rejected and why;
- what evidence proves a milestone;
- what remains open;
- what the exact next task is.

The human owner becomes the memory system and the relay between models.

## What I am building

AI Project OS is a provider-neutral continuity and coordination layer for long-running AI-assisted projects.

Its purpose is to move project memory out of fragile chat context and into durable, machine-readable state.

A fresh AI session should be able to recover:

```text
problem + intent
      ↓
requirements + corrections
      ↓
decisions + reasoning
      ↓
work performed + evidence
      ↓
current state + open loops
      ↓
exact next action
```

without requiring the owner to reconstruct the history manually.

## Core design ideas

### Durable memory outside chats
Project state, handoffs, decision history, archives, open loops, and proof references live in durable files rather than depending on one conversation.

### Retrieval ladder
A fresh agent starts with the smallest useful context and only reads deeper when needed:

1. quick current-state reminder;
2. latest handoff;
3. relevant archived history;
4. deeper project reference;
5. code, commits, tests, logs, or source evidence when proof is required;
6. ask the owner only when the answer was never captured or a genuinely new decision is required.

### Provider-neutral roles
The architecture is intended to let ChatGPT, Claude, Codex, and future providers fill interchangeable implementation, review, or research roles instead of becoming separate project brains.

### Evidence-based completion
Important milestones are tied to durable evidence rather than a model simply saying a task is complete.

### Human gates where they matter
The continuity health model explicitly distinguishes routine automation from owner-level gates such as money, credentials, destructive actions, privacy/publication exposure, permissions, and major architecture decisions.

## Proven milestone

AI Project OS was rolled into a separate real project — **YouTube Research Brain** — and a fresh-chat recovery test passed.

A new session was able to recover the current project state, latest technical evidence, stale/superseded files, do-not-redo boundaries, and the exact next task without the owner re-explaining the project.

That matters because the project is not only documenting a theory of continuity; it has been tested against a live, evolving technical project.

## Current build

The current World 6 work focuses on reducing manual relay even further.

A deterministic, read-only continuity health checker has been implemented to report:

- whether the required memory package exists;
- whether the retrieval manifest is valid;
- whether current-state files agree;
- whether proof is present;
- what the next action is;
- whether the owner is actually needed.

The next stage is validating that checker in the existing CI/security workflow and continuing toward routine zero-relay project continuity.

## Tools and concepts

- Python
- JSON + Markdown as durable project state
- GitHub / GitHub Actions
- deterministic validation
- multi-agent / multi-provider workflows
- human-in-the-loop controls
- evidence and proof tracking
- context minimization
- project continuity and recovery
- workflow orchestration

## What this project demonstrates

AI Project OS is my attempt to solve a problem I kept experiencing while building with AI:

> How do you get the speed of conversational AI without making the conversation itself the database, project manager, memory system, and source of truth?

The answer I am working toward is a lightweight operating layer where models can change, chats can disappear, and the project still knows where it is and why.
