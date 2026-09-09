# YouTube Second Brain

**Status:** Working system with a completed historical-search production milestone; Tier 1 classification is the next major build area.

## The problem

Useful research disappears into watch history, bookmarks, notes, and long transcripts. Reprocessing the same source repeatedly with expensive models is wasteful, and a growing archive becomes useless if it cannot be searched reliably.

The goal is simple:

> Capture useful source evidence once, preserve it, make it searchable, and spend expensive AI reasoning only where it adds value.

## What I designed and built

The system is an evidence-first research pipeline built around a budget-conscious architecture:

1. capture YouTube metadata and transcript evidence;
2. preserve source evidence rather than repeatedly re-fetching or re-analyzing it;
3. maintain a control plane for processing state;
4. build a searchable historical catalog;
5. classify cheaply before deeper enrichment;
6. reserve more expensive AI analysis for selected material.

A simplified architecture:

```text
YouTube sources
    ↓
metadata + transcript capture
    ↓
canonical evidence archive
    ↓
historical lexical search
    ↓
Turso / libSQL hot search layer
    ↓
Tier 1 classification
    ↓
selective AI enrichment
    ↓
reusable research answers
```

## Production milestone

The historical lexical-search stage passed its production completion gate.

The verified build represented **29,521 catalog videos**, passed local validation and quality auditing, exercised real lexical search probes, published the complete index to **Turso/libSQL**, independently verified the remote data, and produced a production evidence artifact.

That milestone answered the important product question:

> Can the historical YouTube catalog actually be searched without reprocessing everything?

**Yes.**

## Engineering and product choices

### Evidence before enrichment
Source evidence is treated as a durable asset. Derived analysis can change as models improve; the original evidence should not have to be recreated.

### Cheap before expensive
Transcript capture itself is designed to use **zero AI tokens**. Deterministic processing and lower-cost classification come before deeper model analysis.

### Resumable processing
Long-running work is structured so transient runner, bridge, or network failures do not require starting over. The production path includes resumable shard inventory and cache persistence.

### Integrity gates
The workflow includes row-count checks, quality audits, probe searches, remote verification, and evidence artifact creation before a major stage is treated as complete.

### Security baseline
The private implementation repo uses automated security checks including **Gitleaks**, **Semgrep**, and **Google OSV-Scanner**.

## Tools and concepts

- Python
- GitHub Actions
- SQLite / Turso / libSQL
- YouTube metadata and transcript processing
- Google Drive as a canonical evidence layer
- deterministic processing before LLM escalation
- classification and selective enrichment
- resumable workflows
- validation and evidence artifacts
- automated security scanning

## What this project demonstrates

This is not a chatbot wrapper. It is a practical attempt to answer a systems question:

**How do you turn a huge, messy body of source material into durable, searchable research infrastructure without letting AI cost or context size explode?**

The project is still being developed. The stable historical-search foundation is complete; the next major work is Tier 1 classification and selective enrichment.
