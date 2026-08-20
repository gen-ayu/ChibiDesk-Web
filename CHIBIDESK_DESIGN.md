# ChibiDesk — Design & Website Specification

## 1. Purpose & Scope

`CHIBIDESK_DESIGN.md` defines the visual direction, design language, content architecture, and user experience (UX) expectations for the official **ChibiDesk Website** and its relationship with the **ChibiDesk Windows Application**.

The website and the desktop application belong to the same product family. A user transitioning between the application and the website should immediately recognize that both are unified parts of the same cohesive ecosystem.

> **Guiding Principle: Brand Consistency, Not UI Duplication**  
> The website shares core visual DNA with the desktop application (color palette, typography, border styling, density, and accent interactions), but remains engineered specifically as a world-class, responsive web platform rather than a literal clone of the desktop UI.

---

## 2. Core Design Philosophy

ChibiDesk design is:
* **Dark-First**: Engineered with deep, near-black backgrounds for visual comfort and high-contrast asset presentation.
* **Minimal & Purposeful**: Prioritizes content clarity over decorative noise. Every visual element must serve a distinct purpose.
* **Modern & Technical**: Crisp 1px structural borders, deliberate spacing, and high-density information architecture.
* **Polished & Premium**: Subtle depth, controlled hover elevations, and responsive micro-interactions.
* **Lightweight & High-Performance**: Instant page transitions, lean payloads, and zero bloat.
* **Slightly Playful**: Warm, energetic orange accents celebrating creative desktop customization and character art.
* **Intuitive**: Simple, predictable navigation requiring no more than 1–2 clicks to find anything.

---

## 3. ChibiDesk Visual Identity & Color Architecture

The website inherits the visual palette extracted directly from the ChibiDesk desktop application.

### Primary Visual Hierarchy

```text
Background
└── Near-black / deeply recessed (--bg-base: #0F0F0F)
      └── Surfaces
            └── Dark grey panels & cards (--bg-sidebar: #121212 / --bg-surface: #181818)
                  └── Structural Borders
                        └── Subtle 1px dark grey lines (--border: #2A2A2A)
                              └── Typography & Content
                                    └── Primary white (--text-primary: #FFFFFF) & muted grey (--text-secondary: #888888)
                                          └── Brand Accent & Focus
                                                └── ChibiDesk Orange (--dock-orange: #FF6B00)
```

### Color Tokens

| Token Name | Value | Role / Usage |
| :--- | :--- | :--- |
| `--bg-base` | `#0F0F0F` | Body background, deeply recessed foundation. |
| `--bg-sidebar` | `#121212` | Navigation header background, side panels, modal shells. |
| `--bg-surface` | `#181818` | Elevated cards, showcase containers, preview panels. |
| `--bg-surface-hover` | `#222222` | Card hover state, active panel highlights. |
| `--bg-input` | `rgba(0, 0, 0, 0.4)` | Form fields, search bars, dropdown containers. |
| `--border` | `#2A2A2A` | Standard structural 1px borders and section separators. |
| `--border-subtle` | `rgba(255, 255, 255, 0.05)` | Inner dividers, grid lines, secondary borders. |
| `--text-primary` | `#FFFFFF` | Primary headings, titles, active navigation labels. |
| `--text-secondary` | `#888888` | Paragraph body copy, feature explanations, metadata. |
| `--text-muted` | `#555555` | Placeholders, timestamps, disabled indicators. |
| `--dock-orange` | `#FF6B00` | **Primary Brand Accent**, CTAs, active toggles, focal rings. |
| `--dock-orange-hover` | `#E66000` | Hover state for primary buttons and interactive accents. |
| `--bg-selected` | `rgba(255, 107, 0, 0.12)` | Selected card background, active nav highlight. |
| `--accent-glow` | `rgba(255, 107, 0, 0.25)` | Subtle drop shadow on hero elements and active controls. |

---

## 4. Design Characteristics & Layout Rules

The website reflects a modern desktop utility translated into a web context:

* **Controlled Spacing**: Tight, deliberate spacing (`4px`, `8px`, `12px`, `16px`, `24px`, `32px`, `48px`). Avoid massive 80px+ empty voids.
* **Controlled Radii**: Precision borders with `4px`–`6px` for badges/inputs and `8px`–`10px` for cards/modals. Avoid excessive pill-shaped containers.
* **Subtle Borders**: Use 1px solid borders (`--border: #2A2A2A`) to define surfaces cleanly without relying on heavy drop shadows.
* **Copywriting Tone**: Clear, honest, and benefit-driven.
  * ❌ **Prohibited**: Unsupported marketing claims such as *"the world's fastest"* or *"the #1 desktop customization app"*.
  * ✅ **Approved**: Direct, functional positioning (*"Desktop customization, simplified."*).

---

## 5. Anti-Generic AI Design Standards

The website must **never** look like a generic AI-generated SaaS template.

### What to Actively Avoid:
* ❌ **NO Generic Purple/Cyan Gradient Blobs**: Stick strictly to dark surfaces (`#0F0F0F`, `#181818`) with ChibiDesk Orange (`#FF6B00`).
* ❌ **NO Excessive Glassmorphism**: Avoid heavy background blurs that reduce text readability and hurt rendering performance.
* ❌ **NO Random Glowing Circles & Neon Grids**: Avoid decorative geometry that has no functional meaning.
* ❌ **NO Stock Photography**: Do not use generic stock office photos or fake team images.
* ❌ **NO Fabricated Content**: Never display fake user reviews, fictitious download numbers, or made-up testimonials.
* ❌ **NO Giant Empty Cards**: Keep information density balanced, purposeful, and structured.

---

## 6. Typography & Text Hierarchy

Typography prioritizes readability, hierarchy, consistency, and fast loading performance.

* **Primary Font**: `Inter`, sans-serif (Weights: 400 Regular, 500 Medium, 600 Semi-Bold, 700 Bold).
* **Technical Font**: `JetBrains Mono` or `Fira Code` (Used for version tags, file formats, resolution specs, and shortcut tags).

### Scale & Hierarchy
* **Hero Title**: `36px` to `48px` / Line-height: `1.15` / Weight: `800` (Tight letter tracking: `-0.02em`).
* **Section Heading (H1)**: `24px` to `28px` / Line-height: `1.25` / Weight: `700`.
* **Feature Sub-heading (H2)**: `18px` to `20px` / Line-height: `1.3` / Weight: `600`.
* **Card / Panel Heading (H3)**: `14px` to `15px` / Line-height: `1.4` / Weight: `600`.
* **Body Copy**: `13px` to `14px` / Line-height: `1.55` / Weight: `400` (Color: `--text-secondary`).
* **Captions & Metadata**: `11px` to `12px` / Line-height: `1.4` / Weight: `500`.
* **Tags & Badges**: `10px` to `11px` / Weight: `600` / Uppercase tracking `+0.05em`.

---

## 7. Animation & Motion Guidelines

Motion must support content comprehension and feel snappy, not theatrical.

### Approved Motion:
* **Micro-interactions**: Snappy hover color shifts (150ms–200ms ease-out).
* **Entrance Effects**: Subtle vertical fade-ins (10px–15px offset, 300ms ease-out) on scroll entry.
* **Interactive Previews**: Smooth tab switching and overlay demonstration toggles.
* **Accent Highlights**: Controlled, subtle glow transitions on primary CTA hovers.

### Prohibited Motion:
* ❌ Constant looping background motion or distracting floating particles.
* ❌ Excessive parallax scrolling effects that disrupt reading.
* ❌ Long blocking loading animations or page-transition delays.

> **Accessibility Requirement**: Always respect `prefers-reduced-motion: reduce` by disabling non-essential transitions and transform animations.

---

## 8. Application Screenshots & Visual Assets

* **Real Visuals Only**: Always use verified, genuine application screenshots or authentic UI component renders.
* **Never Fabricate Screenshots**: Do not generate fictional or imaginary interface mockups.
* **Contextual Demonstrations**: Show the application in real desktop context (Library, Inspector, Preview, Customization controls, Desktop overlays, Media controls) so visitors understand: *"This is what I will actually get."*
* **Image Optimization**: All images must be properly compressed (WebP/SVG), served with explicit dimensions to avoid Cumulative Layout Shift (CLS), and lazy-loaded below the fold.

### Asset Directory Structure
```text
/public
  ├── /branding      (logo.svg, logo.png, favicon.ico)
  ├── /screenshots   (Real application views: library, inspector, preview)
  ├── /icons         (Crisp SVG line icons with 1.5px stroke)
  └── /images        (Promotional graphics and feature diagrams)
```

---

## 9. Unique Brand Touches

To give ChibiDesk a distinctive, memorable web presence without gimmicks, incorporate subtle branded touches:
* **Desktop-Inspired UI Shells**: Framed showcase containers that subtly echo the native desktop app window style.
* **Interactive Media Inspector**: A live on-page preview widget allowing visitors to toggle sample animations and observe overlay scaling.
* **ChibiDesk-Specific Iconography**: Tailored icon set matching the desktop utility's asset management tools.
* **Signature Orange Focus Rings**: Crisp 2px orange focus and selection indicators (`rgba(255, 107, 0, 0.3)`).

---

## 10. Suggested Website Architecture

The website is structured into clear, purposeful areas:

```text
Home (/)
│
├── Navigation (Logo, Features, Download, Docs, Community, CTA)
├── Hero (Tagline, Teaser, Primary & Secondary CTAs, App Showcase)
├── Product Showcase (Library, Inspector, Live Preview, Overlays)
├── Why ChibiDesk (Problem vs. ChibiDesk Solution)
├── Feature Overview (Confirmed public capabilities presented as benefits)
├── Download CTA Section
└── Community & Feedback CTA

Download (/download)
│
├── Official Windows Installer (.exe / .msi)
├── Version, File Size, Release Date
├── System Requirements (Confirmed Windows 10/11 64-bit)
└── Release Notes & Checksums

Changelog (/changelog)
│
└── Chronological Public Release History (Added, Improved, Fixed)

Documentation (/docs)
│
├── Getting Started
├── Installation Guide
├── Asset Management & Formats (GIF, APNG, MP4, WebM)
├── Overlay Positioning & Layout Persistence
└── Settings & Troubleshooting

FAQ (/faq)
│
└── Verified Answers on Compatibility, Performance, and Safety

Feedback (/feedback)
│
├── Bug Report Form
├── Feature Request Form
└── UI/UX & General Feedback

Community (/community)
│
├── Official Discord Server
└── Official GitHub Repository

About (/about)
│
└── Project Vision & Creator Information

Legal (/privacy, /terms, /licenses)
│
└── Privacy Policy, Terms of Service, Open-Source Licenses
```

*Note: The website should launch only with sections that are fully verified and ready. Unfinished sections should not be published.*

---

## 11. Section-by-Section Design Specifications

### Navigation Bar
* **Behavior**: Sticky at top with subtle backdrop blur (`rgba(15, 15, 15, 0.85)` + 12px blur) and 1px bottom border (`--border: #2A2A2A`).
* **Left**: ChibiDesk Logo + Bold Brand Wordmark.
* **Center**: Links to `Features`, `Download`, `Changelog`, `Documentation`, `Community`.
* **Right**: `Download Beta` (or `Coming Soon`) Button.
* **Mobile**: Responsive hamburger drawer maintaining dark surface styling.

### Hero Section
* **Tagline**: `Desktop customization, simplified.`
* **Supporting Description**: A lightweight Windows application designed to bring animated and visual overlays directly onto your desktop without complicated workflows or resource drain.
* **Primary Action**: `Download Beta` (Orange button `#FF6B00`, hover `#E66000`). *(Falls back to `Coming Soon` or `Join Waitlist` if beta is not yet live).*
* **Secondary Action**: `Explore ChibiDesk` (Dark surface button with subtle border).
* **Focal Element**: Real, high-resolution application screenshot or live interactive preview frame showing active desktop overlays.

### Feature Presentation (Benefit-Driven)
Focus on user benefits rather than internal technical jargon:
* **One-Click Placement**: Place GIFs, APNGs, MP4s, and static artwork directly onto your desktop instantly.
* **Effortless Workspace Organization**: Import and manage your media collection in a fast, organized local library.
* **Zero-Lag Performance**: Lightweight background execution engineered for minimal CPU/RAM overhead.
* **Automatic Layout Persistence**: Your customized overlay positions and sizes remain locked and saved across restarts.
* **Local-First Privacy**: Your assets stay strictly on your local machine.

### Download Hub
* Clear, unmistakable Windows download card.
* Displays verified installer details: Target OS (`Windows 10/11 64-bit`), Build Version, Release Date, SHA-256 Checksum, and Direct Installer link.
* *Binaries are distributed through official release infrastructure (e.g. GitHub Releases), not committed into the website repository.*

### Feedback UX
* Simple, low-friction entry point for community suggestions and issue reports.
* **Categories**: `Bug Report`, `Feature Request`, `UI/UX Feedback`, `General Feedback`.
* **Form Fields**: Category selector, message text area, optional email address, and automatic app version string (when opened from the desktop app).
* **Privacy**: Data minimization; no unnecessary personal info collected.

---

## 12. UI Component Style Standards

### Primary Action Button
* **Background**: `--dock-orange` (`#FF6B00`)
* **Text**: `#FFFFFF`, font-weight `600`, font-size `13px`
* **Padding**: `8px 18px` / Border radius: `6px`
* **Hover**: Background `--dock-orange-hover` (`#E66000`), translateY(-1px), shadow `0 4px 14px rgba(255, 107, 0, 0.3)`.

### Secondary Surface Button
* **Background**: `--bg-surface` (`#181818`)
* **Border**: `1px solid var(--border)` (`#2A2A2A`)
* **Text**: `--text-primary` (`#FFFFFF`), font-size `13px`
* **Hover**: Background `#222222`, border `#3A3A3A`.

### Surface Cards & Feature Panels
* **Background**: `--bg-surface` (`#181818`)
* **Border**: `1px solid var(--border)` (`#2A2A2A`)
* **Border Radius**: `8px`
* **Padding**: `20px` to `24px`
* **Hover (Interactive)**: Border shifts to `#383838`, background shifts to `#1D1D1D`.

### Input Fields
* **Background**: `rgba(0, 0, 0, 0.4)`
* **Border**: `1px solid var(--border)` (`#2A2A2A`)
* **Border Radius**: `6px`
* **Text**: `#FFFFFF`, placeholder `#555555`
* **Focus State**: Border `--dock-orange` (`#FF6B00`), outline none, ring `0 0 0 2px rgba(255, 107, 0, 0.2)`.

---

## 13. Responsive Design & Accessibility Standards

* **Responsive Adaptation**:
  * Desktop (Primary): Multi-column layouts, rich sidebars, high-density showcase.
  * Laptop/Tablet: Fluid single-to-dual column reflow, preserved component density.
  * Mobile: Intentional single-column vertical flow with full-width touch-friendly actions (min 44px hit targets).
* **Accessibility**:
  * Semantic HTML structure (`<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`).
  * Full keyboard navigability with visible focus indicators (`:focus-visible`).
  * Contrast ratios meeting or exceeding WCAG AA standards.
  * Informative `aria-label` and `alt` attributes on all non-text content.

---

## 14. Performance & Security Best Practices

* **Core Web Vitals**: Aim for green metrics across LCP, FID/INP, and CLS.
* **Lean Bundle**: Rely on native CSS and lightweight TypeScript over bulky third-party animation frameworks.
* **Security & Secret Handling**: Never hardcode API keys, SMTP credentials, webhook URLs, or service secrets into frontend code. Use server-side endpoints and secure environment variables for form handling.
