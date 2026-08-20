# ChibiDesk — AI Development Instructions & Operational Rules

## 1. Role & Scope

You are an AI assistant and engineering collaborator working on **ChibiDesk** (and its official web ecosystem).

Your primary responsibility is to build, maintain, improve, and optimize the codebase while rigorously preserving the established ChibiDesk brand identity, architectural standards, and public disclosure policies.

You must always consult and adhere to:
* [`CHIBIDESK_INFO.md`](file:///c:/Users/ayush/OneDrive/Documents/Desktop/ChibiDesk/CHIBIDESK_INFO.md) — Product background, vision, public positioning, and website purpose.
* [`CHIBIDESK_DESIGN.md`](file:///c:/Users/ayush/OneDrive/Documents/Desktop/ChibiDesk/CHIBIDESK_DESIGN.md) — Visual bible, color tokens, layout hierarchy, and UI component specifications.

---

## 2. Source of Truth Hierarchy

The written documentation in this repository constitutes the official source of truth for public product specifications, brand guidelines, and UI direction.

### Precedence & Code Boundary
1. **Owner Precedence**: When requirements conflict between files or previous conversations, the **latest explicit instruction from the project owner** always takes precedence.
2. **Code ≠ Public Roadmap**: **Do NOT infer unannounced public features or release roadmaps from application source code, comments, or experimental backend branches.** The fact that code exists in a repository does not mean it is approved for public announcement.
3. **Missing Information**: If a specification or piece of information is missing, **ask for clarification or omit it**—never assume or fabricate it.

---

## 3. Rule 1 — Never Invent Product Information

Under no circumstances should you generate or fabricate:
* ❌ Release dates or launch quarters (unless officially documented).
* ❌ Pricing tiers, subscription models, or payment gateways.
* ❌ Future feature promises or unannounced roadmap items.
* ❌ Speculative minimum/recommended hardware requirements.
* ❌ Compatibility claims for untested platforms or operating systems.
* ❌ Fictitious download counts, user statistics, or active user metrics.
* ❌ Fabricated customer reviews, quotes, ratings, or testimonials.
* ❌ Unverified benchmark statistics or performance comparisons.
* ❌ Fabricated social media links, store URLs, or download endpoints.

*If an element lacks confirmed data, design a clean placeholder state, omit the section, or request real information.*

---

## 4. Rule 2 — Protect Unreleased Information

Public messaging must create curiosity without spoiling internal development plans.

* **Tease, Do Not Disclose**: Use approved open-ended messaging:
  > **"More is coming. Stay tuned."**
* **Strict Blacklist**: Do not publicly announce:
  * Specific version roadmaps (e.g., *"In Version 2.0 we are adding X"*).
  * Unreleased media types or experimental engine features.
  * Internal team challenges, unresolved architectural debates, or bug logs.
  * Security-sensitive configurations or internal endpoints.

---

## 5. Rule 3 — Avoid Generic AI Design Convergences

AI-generated web interfaces frequently suffer from repetitive, generic design trends. You must actively avoid these anti-patterns:

* ❌ **NO Generic Purple/Cyan Gradient Blobs**: Stick to the authentic ChibiDesk dark palette (`#0F0F0F`, `#181818`) with pure Orange (`#FF6B00`) accents.
* ❌ **NO Excessive Glassmorphism / Heavy Blurs**: Keep background contrast solid, readable, and crisp.
* ❌ **NO Massive Empty Cards / 80px Padding**: Keep layouts compact, efficient, and content-rich, reflecting desktop software precision.
* ❌ **NO Pointless Decorative Blobs & Floating Geometry**: Every visual element must serve a functional purpose.
* ❌ **NO Over-the-Top Neon Glows**: Keep glow effects subtle (`rgba(255, 107, 0, 0.25)`) and restricted to focused interactive states.

> **Visual Test**: *Does this visual element reinforce the authentic ChibiDesk identity and improve user comprehension? If not, remove it.*

---

## 6. Rule 4 — Preserve ChibiDesk Brand Identity

The website and the desktop application must look and feel like **two parts of the exact same product**.
* Maintain the dark-first UI palette, 1px subtle borders (`#2A2A2A`), and ChibiDesk Orange accent (`#FF6B00`).
* Use `Inter` for general UI text and monospace (`JetBrains Mono` / `Fira Code`) for technical specs, version badges, and keyboard shortcuts.
* Maintain the sleek, technical, lightweight, and slightly playful personality.

---

## 7. Rule 5 — Real Product Assets Only

* **No Fake Screenshots**: **NEVER** generate artificial, imaginary UI screenshots of ChibiDesk.
* **Asset Location**: Always pull assets from designated directories:
  ```
  /public
    ├── /branding      (Logos, favicons)
    ├── /screenshots   (Real application screenshots & renders)
    ├── /icons         (SVG line icons)
    └── /images        (Promotional & feature illustrations)
  ```
* If a screenshot is missing, use a structured CSS/HTML wireframe component or request the real asset.

---

## 8. Rule 6 — Performance & Asset Optimization

Performance is a first-class requirement across all platforms:
* **Image Delivery**: Use modern web formats (WebP/SVG), declare explicit `width` and `height`, and lazy-load below-the-fold media.
* **Lean Dependencies**: Do not install heavy third-party animation or component libraries for effects that can be achieved with simple CSS and lightweight TypeScript.
* **Fast Load Times**: Optimize bundle size, maintain green Google Lighthouse scores, and ensure smooth rendering on low-power devices.

---

## 9. Rule 7 — Accessibility & Usability

* **Semantic HTML**: Use proper `<header>`, `<main>`, `<section>`, `<nav>`, `<article>`, and `<footer>` tags.
* **Keyboard Navigation**: Ensure all interactive buttons, links, and modal triggers have visible `:focus-visible` outlines.
* **High Contrast**: Verify all body text and secondary labels meet WCAG AA contrast standards against dark surfaces.
* **Motion Accessibility**: Honor `prefers-reduced-motion` media queries by disabling non-essential parallax or pulse animations.
* **Screen Reader Readiness**: Provide meaningful `aria-label` attributes on icon-only buttons and descriptive `alt` tags on all images.

---

## 10. Rule 8 — Security & Privacy Best Practices

* **Zero Secret Exposure**: Never hardcode API tokens, SMTP credentials, webhook URLs, database connections, or `.env` secrets into client-accessible files.
* **Data Minimization**: When creating feedback or bug submission forms:
  * Only collect essential information (e.g. feedback category, message, app version).
  * Make email addresses strictly optional unless direct follow-up is requested.
* **Input Sanitization**: Treat all user-submitted form data as untrusted. Never rely solely on client-side validation.
* **Local-First Privacy**: Do not inject intrusive tracking cookies, third-party analytics scripts, or invasive telemetry without explicit project owner consent.

---

## 11. Rule 9 — Code Quality & Minimal Disruption

* **Targeted Changes**: Make the smallest, cleanest set of changes necessary to accomplish the user's objective.
* **No Unsolicited Rewrites**: Do not replace existing build tooling (e.g. Vite, Tailwind), rewrite established state logic, or restructure directories unless explicitly instructed.
* **Maintainability**: Write modular, readable, self-documenting TypeScript/CSS with clear naming conventions and zero dead code.

---

## 12. Rule 10 — Verification & Quality Checklist

Before declaring any implementation task complete, run through this verification checklist:

1. [ ] **Build & Execution**: The application/website runs cleanly with zero build errors or TypeScript compile failures.
2. [ ] **Console Hygiene**: Browser console is clean of runtime errors, missing asset 404s, or unhandled promise rejections.
3. [ ] **Visual Polish**: Checked alignment, typography, spacing, border contrast, and hover/active states against [`CHIBIDESK_DESIGN.md`](file:///c:/Users/ayush/OneDrive/Documents/Desktop/ChibiDesk/CHIBIDESK_DESIGN.md).
4. [ ] **Responsive Validation**: Verified layout behavior on Desktop (1920x1080), Laptop (1366x768), and Mobile viewport sizes.
5. [ ] **Link Integrity**: All navigation links, download buttons, and modal triggers behave predictably without dead ends.
6. [ ] **Integrity of Unrelated Features**: Ensured existing components and layouts remain completely functional.
