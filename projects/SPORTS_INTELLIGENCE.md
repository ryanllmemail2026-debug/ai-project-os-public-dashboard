# Sports Intelligence

**Status:** Early-stage experimental build. Architecture and scaffolding exist; no live ingestion yet.

## The problem

Sports picks and predictions are everywhere, but the evidence trail is usually poor.

People remember winners, forget losers, quote lines after they moved, and compare predictions that were never normalized into the same market language. That makes it difficult to answer basic questions such as:

- Who is actually accurate over time?
- In which markets are they strongest or weakest?
- What did they say before the event?
- What line was available when they said it?
- Did their pick beat the closing line?

## What I am designing

An evidence-first sports intelligence pipeline that preserves the original claim before scoring it.

```text
YouTube / podcast transcript
        ↓
LLM-assisted claim extraction
        ↓
normalization
        ↓
validation
        ↓
accepted prediction
        ↓
result grading + closing-line value
        ↓
source-level performance metrics
```

## Design principles

### Preserve the original evidence
No recommendation should exist without a record of who said it, what they said, the market/line, and when it was said.

### Separate extraction from validation
An LLM can propose a candidate pick, but deterministic validation should decide whether the team, market, timing, and duplicate rules are valid.

### Normalize before comparing
Equivalent markets need canonical representations before performance can be scored fairly.

### Keep modeling separate from source data
Raw NFL schedules/data are treated as source inputs. Any predictive models belong in a separate modeling layer so the system does not confuse data access with prediction.

### Control cost from the start
The first validated grading workflow is being designed around a near-zero incremental-cost target before adding expensive modeling or enrichment.

## Planned / scaffolded components

- claim extraction
- market and team normalization
- validation and deduplication
- schema-versioned SQLite storage
- result grading
- units / win-loss-push tracking
- closing-line value
- per-source metrics
- weekly summaries

## Current reality

This project is intentionally shown as **experimental** rather than finished.

The repository contains architecture and implementation scaffolding, but the current documented state is **Stage 0 — no live ingestion yet**. It is included here because it demonstrates how I approach a new problem: define the evidence model, validation rules, cost boundaries, and grading logic before scaling ingestion.
