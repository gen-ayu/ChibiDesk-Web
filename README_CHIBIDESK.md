# ChibiDesk

> **Desktop customization, simplified.**  
> A lightweight Windows desktop application designed to bring animated and visual overlays directly onto your desktop.

---

## 📖 Essential Documentation Suite

Before contributing code, writing copy, or making architectural decisions, review the project documentation in the following order:

| Document | Purpose | Key Focus |
| :--- | :--- | :--- |
| 📘 [`CHIBIDESK_INFO.md`](./CHIBIDESK_INFO.md) | **Product & Brand Context** | What ChibiDesk is, the product vision, public positioning, supported formats, and web hub purpose. |
| 🎨 [`CHIBIDESK_DESIGN.md`](./CHIBIDESK_DESIGN.md) | **Visual & Design Bible** | Color tokens, dark theme hierarchy, typography, asset rules, UI components, and anti-generic principles. |
| 🤖 [`AI_INSTRUCTIONS.md`](./AI_INSTRUCTIONS.md) | **AI & Contributor Rules** | Critical operational rules: never inventing data, protecting unreleased info, security, performance, and verification. |

---

## 📂 Project Architecture

```
ChibiDesk/
├── CHIBIDESK_INFO.md       # Product vision & public positioning
├── CHIBIDESK_DESIGN.md     # Visual design system & component specs
├── AI_INSTRUCTIONS.md      # Rules of engagement & accuracy standards
├── README.md               # Repository entry point
│
├── index.html              # Main application entry point
├── overlay.html            # Desktop overlay rendering window
├── src/                    # Application source code
│   ├── main.ts             # Main window UI logic
│   ├── overlay.ts          # Transparent overlay canvas manager
│   ├── previewController.ts# Asset preview & inspector controller
│   └── styles.css          # Core design tokens & Tailwind styles
├── src-tauri/              # Rust / Tauri desktop backend & window controls
├── public/                 # Static assets, branding, and icons
├── package.json            # Node.js dependencies and scripts
└── vite.config.ts          # Vite bundler configuration
```

---

## 🚀 Quickstart & Development

### Prerequisites
* [Node.js](https://nodejs.org/) (v18+ recommended)
* [Rust](https://www.rust-lang.org/) & Cargo (for Tauri desktop builds)

### Installation
```bash
# Install frontend dependencies
npm install
```

### Running Locally
```bash
# Start Vite development server
npm run dev

# Run full Tauri desktop application
npm run tauri dev
```

### Production Build
```bash
# Build frontend web bundle
npm run build

# Build Windows desktop application package
npm run tauri build
```

---

## 🛡️ Contribution Principles
1. **Source of Truth**: The project documentation defines all public commitments. When in doubt, ask rather than invent.
2. **Code ≠ Public Roadmap**: Never expose internal development experiments or unreleased features without explicit authorization.
3. **Maintain Identity**: Always adhere to the dark-first, orange-accented aesthetic defined in [`CHIBIDESK_DESIGN.md`](./CHIBIDESK_DESIGN.md).
