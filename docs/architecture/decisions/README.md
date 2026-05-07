# Architecture Decision Records (ADR)

This folder contains records of significant architectural decisions made during the project.

## What is an ADR?

An **Architecture Decision Record** is a short document that captures:

- **Context** — what situation forced us to make a decision
- **Decision** — what was decided
- **Consequences** — what becomes easier and what becomes harder as a result
- **Alternatives** — what other options were considered and why they were rejected

Format inspired by [Michael Nygard's original proposal](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions).

## Why bother?

Three months from now, when looking at the code, you will not remember **why** something was done a particular way. ADRs are a written memory.

They also help any future contributor (or a recruiter reviewing the project) understand the reasoning behind the architecture, not just the architecture itself.

## Naming convention

Examples:
- `0001-backend-and-database-from-day-one.md`
- `0002-leaflet-over-maplibre.md`
- `0003-postgis-for-spatial-queries.md`

Numbers are sequential and never reused, even if a decision is later superseded.

## Status of an ADR

Each ADR has one of three statuses:

- **Proposed** — under discussion
- **Accepted** — current decision
- **Superseded by ADR-NNNN** — replaced by a newer decision (with link)

A superseded ADR is **never deleted** — it stays as part of the history.

## List of ADRs

*(none yet — first ADR coming soon)*