# Autonomous Agent Web Development Framework (AGENTS)

> **The Universal Standard for AI-Assisted Engineering, Autonomous Agents, and Production Web Development.**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Standard: AGENTS](https://img.shields.io/badge/Standard-AGENTS.md-emerald.svg)](AGENTS.md)

This repository provides the universal specification and guidelines for configuring AI coding assistants (Antigravity, Cursor, Windsurf, Copilot, Cline, etc.) to engineer production-ready, accessible, high-performance web applications without common AI mistakes.

---

## 🌟 Key Highlights of the Framework

1. **Mandatory Interactive Discovery Protocol (Section 0):**  
   Before generating code, the AI agent conducts an onboarding interview to capture:
   - Business model, target audience, and offerings.
   - Logo and brand assets to mathematically generate the CSS color palette and typography hierarchy.
   - Functional & non-functional requirements.
   - Preferred cloud provider and database (with recommended defaults: **Cloudflare Pages/Workers** + **Supabase PostgreSQL**).
   - Legal jurisdiction to tailor statutory policies (`/terminos`, `/privacidad`, `/cookies`).

2. **Human-Grade Copywriting (Anti-AI Text Standard):**  
   Enforces a strict ban on generic AI fluff, redundant descriptions, and robotic adjectives. Demands concise, clear, and direct human language.

3. **Zero-Friction Access Standard:**  
   Guarantees that prices, catalogs, shopping carts, and checkouts are never hidden or locked behind mandatory registrations.

4. **Direct In-Place Interaction:**  
   Prioritizes responsive on-page forms, inline pickers, and smooth transitions over disruptive nested modals.

5. **20 Strict Security Rules:**  
   Strict multi-tenant Row-Level Security (RLS), HttpOnly sessions, IP sliding-window rate limiting, anti-IDOR checks, and cryptographically signed consent records.

6. **7-Step End-to-End Methodology:**  
   From brand discovery to Core Web Vitals audit (LCP < 2.5s, CLS < 0.1, INP < 200ms) and WCAG 2.1 AA accessibility compliance.

---

## 📁 Repository Structure

```
.
├── AGENTS.md    # The core instruction standard to place in your project root
├── README.md    # Overview and documentation
└── LICENSE      # Open-source MIT License
```

---

## 🚀 How to Use in Your Project

### Option A: Using with Any AI Coding Assistant
1. Download or clone this repository.
2. Copy `AGENTS.md` into the root directory of your project:
   ```bash
   cp AGENTS.md /path/to/your/project/
   ```
3. When prompting your AI assistant, tell it:  
   *"Follow all rules, protocols, and discovery steps specified in `AGENTS.md`."*

### Option B: Download the Standalone Package
Download the pre-packaged `.zip` directly from the [Releases](https://github.com/santiagoes2009-pixel/agentic-web-framework) section.

---

## 🛠️ Recommended Ecosystem Stack

| Layer | Standard Technology | Why |
| :--- | :--- | :--- |
| **Styling** | Tailwind CSS / CSS Variables | Scalable token-based styling without CSS bloat |
| **Components** | Accessible Headless UI / WAI-ARIA | Modular primitives with keyboard focus control |
| **Motion** | GSAP & Motion (Framer) | Hardware-accelerated transitions under 300ms |
| **Media** | Swiper.js | Mobile-first touch-friendly carousels |
| **Icons** | Lucide Icons (SVG) | High-contrast, clean icons (zero informal emojis) |
| **Edge Hosting** | Cloudflare Pages & Workers | Instant global edge CDN with zero cold starts |
| **Database & Auth** | Supabase (PostgreSQL + RLS) | Strict multi-tenant security and signed sessions |

---

## 🤝 Credits & Acknowledgments

This standard synthesizes best engineering practices from open-source pioneers:
- [Tailwind CSS](https://tailwindcss.com) by Tailwind Labs
- [Lucide Icons](https://lucide.dev) by Lucide Project & Community
- [GSAP](https://gsap.com) by GreenSock
- [Swiper](https://swiperjs.com) by Vladimir Kharlampidi
- [Cloudflare Pages & Workers](https://developers.cloudflare.com/pages/) by Cloudflare
- [Supabase](https://supabase.com) by Supabase Team & PostgreSQL Community
- [W3C Web Accessibility Initiative](https://www.w3.org/WAI/)

---

## 📄 License

Released under the [MIT License](LICENSE). Free for developers, agencies, and autonomous agent frameworks worldwide.
