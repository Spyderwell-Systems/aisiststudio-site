# Spyderwell Web Standards v1.0 (Draft)

Status: proposed; review before merge. Applies to Spyderwell web properties, not necessarily automation repositories.

## Principles
- Prefer progressive enhancement, semantic HTML, native browser capabilities and minimal dependencies. Do not introduce a framework without a documented need.
- Use Google's Modern Web Guidance as a living reference: https://github.com/GoogleChrome/modern-web-guidance . Validate advice against current browser support and project requirements; do not treat generated guidance as a substitute for tests.
- Keep source human-readable: two-space indentation for HTML/CSS/JS, consistent formatting, meaningful names, and one concern per module. Avoid minifying source files in Git.
- Prefer semantic landmarks, one meaningful h1 per page, hierarchical headings, explicit labels, descriptive link text and native buttons for actions. Test keyboard and screen reader behavior.
- Target WCAG 2.2 AA; provide visible focus, sufficient contrast, reduced-motion handling and accessible state for interactive controls.
- Use CSS custom properties for design tokens, mobile-friendly layouts and external stylesheets by default. Preserve distinct visual identities for each site. Avoid growing override chains; explain exceptions.
- Prefer vanilla JS for simple static sites. Avoid inline scripts for substantial behavior. Never expose credentials or private data in public assets.
- Maintain per-page title, description, canonical URL and relevant structured data; verify JSON-LD and keep sitemap/robots consistent with actual published pages.
- Optimize images/fonts and test Core Web Vitals: LCP <=2.5s, INP <=200ms, CLS <=0.1 at p75 where field data exists. Do not claim a score without measurement.
- Document actual Netlify settings, domain/DNS ownership, build/publish directory, environment variables by name only, and rollback process; do not infer settings from repository files.

## Review gates
1. Source formatting and HTML validation.
2. Link, image alt text, heading and metadata review.
3. Keyboard navigation, focus, contrast and reduced-motion review; automated accessibility scan plus manual checks.
4. Mobile and desktop visual comparison, including no-JS behavior.
5. Netlify preview verification and explicit approval before merging/deploying.

## Commenting and learning
Comments should explain intent, non-obvious tradeoffs and browser constraints, not restate syntax. Record architectural decisions in docs/DECISIONS.md. Include concise educational notes where they clarify HTML/CSS/JS choices.

## Change policy
Keep existing site behavior and brand unless explicitly approved. Prefer small reversible PRs. Review this standard quarterly and when browser/platform guidance materially changes.
