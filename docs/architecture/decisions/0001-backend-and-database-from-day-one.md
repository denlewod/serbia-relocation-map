# ADR-0001: Backend and database from day one

- **Status:** Accepted
- **Date:** 2026-05-07
- **Deciders:** Yury (project author)

## Context

The project is a non-commercial pet project with a stated goal of practicing full-stack development end-to-end (BO-3 in Vision & Scope). The MVP requires:

- Interactive map with multiple data layers (heatmap + POI)
- User-facing features like search, filter combinations, location detail cards
- A feedback form (planned for Release 2)
- Regular ingestion and serving of open data from external sources

Two architectural patterns were considered for the initial setup:

**Option A — Static-first:**
- Frontend-only application (React + Leaflet)
- Data shipped as GeoJSON files in the repository
- Data refresh handled via local scripts or GitHub Actions, committed back to the repo
- No backend, no database

**Option B — Full-stack from day one:**
- Frontend (React + Leaflet) + Backend (Node.js + Fastify) + Database (PostgreSQL with PostGIS)
- Data ingestion handled by scheduled backend jobs
- Database serves as the single source of truth for spatial data

## Decision

We adopt **Option B (full-stack from day one)**.

## Rationale

The decision is driven primarily by **BO-3 (skill development and portfolio)**, which is a project Driver in the priority matrix.

A static-first approach would not provide hands-on experience with:
- Database design and spatial querying (PostGIS)
- Backend API design (REST or GraphQL)
- Server-side data ingestion and scheduled jobs
- Authentication patterns (anticipated for future releases)
- Backend deployment, environment management, and DevOps practices

These are exactly the skills the project aims to build. Choosing the static path would optimize for delivery speed at the cost of the primary learning goal.

The author is explicitly not in a hurry (Schedule is Degree of Freedom, not a Driver), which makes the additional complexity of Option B affordable.

## Consequences

### Positive

- Full coverage of the modern full-stack development cycle
- Database as a foundation enables future features (user-saved scenarios, feedback forms, UGC) without rearchitecting
- Hands-on experience with PostGIS — a sought-after skill for any geo-related role
- Stronger portfolio artifact: shows architectural thinking, not just frontend skills

### Negative

- Increased setup time before the first user-visible feature
- More moving parts → higher operational complexity
- Free-tier constraints become more relevant (Supabase auto-pauses inactive projects after 7 days; Render free tier sleeps after inactivity)
- Higher risk of project abandonment due to complexity (mitigated by treating Schedule as flexible)

### Neutral

- The split between frontend and backend hosting (Vercel + Render) is a deliberate choice to learn working with multiple platforms

## Alternatives considered

**Option A (Static-first)** was rejected for the reasons described in Rationale.

A hybrid approach — start static, add backend later — was discussed but rejected because:
- Migrating from static to backend mid-project requires refactoring data access patterns
- Postponing the most valuable learning component contradicts the project's stated priorities

## Related decisions

- Future ADR will document specific technology choices within this architecture (e.g., Fastify vs Express, Supabase vs self-hosted Postgres)

## References

- Vision & Scope document, section 1.3 (Business Objectives) and section 4.2 (Project Priorities)