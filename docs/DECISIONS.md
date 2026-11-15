# Architecture decisions

## ADR-001 — Preserve lightweight static sites
Status: proposed (2026-11-15)

Decision: Keep current static HTML/CSS/JS architecture unless a demonstrated feature requirement warrants a build system or framework.

Rationale: Small sites benefit from low maintenance, transparent source and simpler deployments. Revisit if content scale, reusable templates or automated validation requirements justify additional tooling.
