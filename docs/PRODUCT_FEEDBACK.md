# Product Feedback & Issues

Issues and product feedback encountered during the Fabric Apps Hackathon 2026.

## Environment & Deployment

- **Rayfin Daily environment instability** — Functions testing was unavailable for approximately one week during the hackathon, blocking end-to-end testing of User Data Functions. This was acknowledged by the Rayfin team and led to the deadline extension from July 31 to August 7.

- **`rayfin up` deployment failures on Daily environment** — Intermittent deployment failures during the hackathon period required retries and manual intervention to successfully publish the app.

- **Functions deployment limitations in preview** — Encountered constraints around the Functions preview that limited the scope of what could be deployed as User Data Functions vs. client-side logic. Workaround: implemented dual-mode data loading (backend GraphQL + local seed fallback).

## Authentication

- **Authentication friction with `npx rayfin login`** — Tenant-switch scenarios required workarounds; `az login` alone was insufficient, needed explicit `@microsoft/rayfin-cli login` for MCAPS tenant. This added onboarding friction for the team.

## Documentation & Developer Experience

- **Bundle size guidance gap** — No documentation on recommended bundle size limits for Rayfin-hosted static frontends; discovered the 500 KB+ chunk warning only at build time. Suggestion: add code-splitting guidance to the Rayfin docs.

- **Limited examples for Graph/visualization apps** — Most Rayfin samples focus on CRUD forms. More examples showing SVG rendering, interactive visualizations, or canvas-based UIs inside Fabric Apps would help teams building data exploration experiences.
