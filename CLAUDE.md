# QNET Site — Project Context

This is the website for QNET (Queen's Nuclear Engineering Team), a student design
club at Queen's University. Static site: raw HTML/CSS/JS, no framework, no build step.

## What you're here to do
You are being used to make alterations to this existing site. Match the established
design system exactly — do not introduce new patterns, libraries, or frameworks.
When in doubt, copy the existing implementation from index.html, school.html, or
sponsors.html rather than inventing something.

## Design system
- Background: #050505 (dark)
- Queen's colors: gold #fabc0f, blue #002552, red #b90e32
- Font: Inter
- Nav: fixed notch nav (pill-shaped, centered, hovers to expand), `assets/Atom Logo.png` centered
- Layout: vertical snap slideshow — `.vertical-slideshow > .slide`, each 100vh
- Cards: dark glass — rgba(18,18,18,0.85), backdrop-filter blur,
  border rgba(255,255,255,0.07), border-radius 22px, accent left-border in a Queen's color
- Background layers: 4 nebula blobs (blurred radial gradients in Queen's colors)
  + 3 star layers, fixed, z-index 0
- Scroll reveal: `.reveal` + IntersectionObserver, stagger classes `stagger-1`–`stagger-4`
- Also present sitewide: custom cursor (random Queen's color dot), back-to-top button,
  fixed social footer, Google Analytics gtag calls on social links

## Shared components (copy verbatim, do not rewrite)
Notch nav, mobile menu, footer, and the JS blocks (custom cursor, scroll reveal,
back-to-top, hamburger) are shared across pages. Source of truth: index.html,
school.html, sponsors.html.

## Assets
- `assets/Atom Logo.png` — nav logo
- `assets/White NET Full Logo.svg` — full logo (index.html hero)
- `assets/QNET outline white.svg` — outline logo
- `teamphoto/` — member photos

## Hard rules
- NEVER alter people's data: names, roles, photos, LinkedIn URLs, degree info, bios, badges.
- Preserve existing asset paths exactly.
- Keep line endings LF (see .gitattributes).
- Don't add dependencies or build tooling.

## Subagents available (.claude/agents/)
- `site-mapper` — read-only; maps structure/content, finds where things live
- `code-editor` — the only agent with write access; makes scoped changes
- `visual-reviewer` — checks rendered layout/design consistency
- `responsive-tester` — mobile/tablet breakpoint checks
- `link-checker` — broken internal links and asset paths
- `seo-content-checker` — meta tags, heading structure, alt text

Prefer delegating: site-mapper to find, code-editor to change, then the QA agents to verify.