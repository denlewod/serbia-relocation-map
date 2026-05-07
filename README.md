# Serbia Relocation Map

> Interactive map of Serbia with multi-layer data for relocation decision support.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Status: Pre-MVP](https://img.shields.io/badge/Status-Pre--MVP-orange.svg)](#current-status)

---

## What is this

A web application that helps people considering relocation to Serbia choose a city and neighborhood based on multiple factors — rent prices, safety, ecology, infrastructure, healthcare, leisure, internet quality, and more.

Inspired by [dubson.org](https://dubson.org/) (similar tool for Spain), but for Serbia.

**Core idea:** instead of cross-referencing Numbeo, real estate sites, expat forums and Telegram chats, get a single interactive map with switchable layers and heatmaps.

## Why this exists

This is a non-commercial pet project with three goals:

1. **Personal:** help me and my wife choose a place to live in Serbia.
2. **Useful:** make a tool that other relocators can use too.
3. **Learning:** practice full-stack development, DevOps and SDLC end-to-end on a real project.

## Current status

🚧 **Pre-MVP** — currently in analysis and planning phase.

- [x] Vision & Scope document
- [ ] Use Cases
- [ ] User Stories for Release 1
- [ ] Data Sources Catalog
- [ ] Architecture documentation
- [ ] First code commit
- [ ] MVP deployed

## Documentation

| Document | Location | Status |
|---|---|---|
| Vision & Scope | [Google Docs](https://docs.google.com/document/d/1qZQrRfsqElZusRKWUQFgk9zrYkP_TsOiGwWpL12R6UM/edit) | ✅ v1.0 |
| Architecture Decisions (ADR) | [`docs/architecture/decisions/`](./docs/architecture/decisions/) | 🔄 In progress |
| Data Sources Catalog | [`docs/data-sources.md`](./docs/data-sources.md) | ⏳ Planned |
| Use Cases | [`docs/use-cases/`](./docs/use-cases/) | ⏳ Planned |

Project board: [GitHub Projects](https://github.com/denlewod/serbia-relocation-map/projects)

## Planned tech stack

| Layer | Technology | Reason |
|---|---|---|
| Frontend build | Vite | Fast, modern bundler |
| Frontend framework | React + TypeScript | Industry standard, strong types |
| Map library | Leaflet | Open-source, lightweight, OSM-friendly |
| Styling | Tailwind CSS | Fast prototyping, utility-first |
| Backend | Node.js + Fastify | Modern, performant Node framework |
| Database | PostgreSQL + PostGIS | Geo-spatial queries support |
| Hosting (frontend) | Vercel | Free tier, GitHub integration |
| Hosting (backend) | Render | Free tier with auto-deploy |
| Database hosting | Supabase | Postgres + PostGIS, free tier |
| CI/CD | GitHub Actions | Free for public repos |
| Testing | Vitest + Playwright | Unit + E2E |

This stack may change as the project evolves. Decisions are tracked in [Architecture Decision Records](./docs/architecture/decisions/).

## Geography of MVP

Release 1 covers three cities:
- **Belgrade** (Београд)
- **Novi Sad** (Нови Сад)
- **Niš** (Ниш)

Other cities and broader country coverage are planned for later releases.

## How to contribute

This is currently a solo learning project, but feedback and ideas are welcome:

- Open an [issue](https://github.com/denlewod/serbia-relocation-map/issues) for bug reports or feature suggestions
- Reach out to the author via GitHub

## License

MIT License — see [LICENSE](./LICENSE) for details.

## Author

**Yury** — Systems Analyst, currently based in Almaty, Kazakhstan.

- GitHub: [@denlewod](https://github.com/denlewod)

---

*Last updated: May 2026*