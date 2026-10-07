# Zoo Repairs — Starlink Installation

A modern, high-performance static landing page for Zoo Computer Repairs' Starlink Satellite Installation and Home/Business Network Optimization services across Greater Brisbane and South East Queensland.

---

## Overview

This project is an Astro static application built to deliver an ultra-fast, accessible, and conversion-optimized experience for customers seeking professional Starlink dish mounting, roof cabling, and whole-property WiFi mesh configuration.

---

## Tech Stack

- **Framework:** [Astro](https://astro.build/) ^7.3.6 (Static Site Generation / `output: 'static'`)
- **Language:** TypeScript (Strict mode enabled)
- **Styling:** Vanilla CSS with custom design tokens, CSS Grid/Flexbox layouts, and hardware-accelerated micro-interactions
- **Typography:** Google Fonts (`Outfit` for headings, `Inter` for body)
- **Build Output:** Static HTML/CSS/JS (`dist/`)

---

## Features

- **Custom Dark Technology Aesthetic:** Curated color system featuring deep space backgrounds (`#070B14`, `#0B1120`, `#0F172A`), royal blue CTA primary buttons (`#3B82F6` / `#2563EB`), dark slate secondary buttons (`#1E293B` / `#475569`), and Starlink cyan accents (`#0EA5E9`).
- **Comprehensive Content Sections:**
  1. **Header:** Zoo Repairs brand logo, quick phone trigger (`0477 319 160`), desktop navigation links, and quote action.
  2. **Hero:** Core value proposition, key service badges, and embedded lead capture quote form.
  3. **Trust & Proof Bar:** IT credentials, direct billing notice, warranty, and same-week dispatch.
  4. **Why Professional Installation:** Clear breakdown of IT networking technician advantages over traditional TV antenna installers.
  5. **Core Services Grid:** 6 comprehensive installation steps (Site survey, mounting, cabling, router setup, mesh coverage, Ethernet integration).
  6. **DIY Risks & Pitfalls:** Common self-installation failure points with content-driven natural card heights and value summary card.
  7. **Pricing Factors:** Transparent cost factors (roof type, mounting hardware, cable routing, mesh WiFi).
  8. **Regional Queensland Info:** Speeds (100+ Mbps), latency (25–30 ms), zero-markup direct Starlink billing model, and coverage notes.
  9. **Starlink vs NBN:** Practical comparison between Starlink, Sky Muster satellite, NBN Fixed Wireless, and NBN FTTP.
  10. **Service Offerings:** Breakdown of residential, commercial, relocation, and mesh WiFi packages.
  11. **Service Areas:** 8 South East Queensland regional coverage areas (Brisbane, Logan, Ipswich, Redland Bay, Moreton Bay, Gold Coast, Sunshine Coast, Scenic Rim).
  12. **FAQ Accordion:** 8 interactive FAQ items addressing DIY viability, costs, mounting locations, timelines, power requirements, and weather resilience.
  13. **Final CTA Banner:** Bottom conversion banner with direct phone and online quote actions.
  14. **Mobile Call Bar:** Fixed bottom quick-contact bar for mobile devices.
- **Card Micro-Interactions:** Subtle card hover elevation (`translateY(-4px)` with cyan border glow and shadow depth).
- **Accessibility:** Full keyboard navigation support, visible `:focus-visible` focus rings, semantic HTML5 landmarks, and `prefers-reduced-motion` compliance.
- **Structured Data:** Built-in JSON-LD schemas (`LocalBusiness`, `Service`, `FAQPage`) for search engine optimization.

---

## Project Structure

```text
zoo-starlink-installation/
├── public/
│   └── assets/
│       └── zoologo.png          # Zoo Computer Repairs brand logo
├── src/
│   ├── components/
│   │   ├── layout/
│   │   │   ├── Header.astro     # Responsive desktop navbar & mobile drawer
│   │   │   ├── Footer.astro     # Site footer, service links & hardware note
│   │   │   └── MobileCallBar.astro # Fixed bottom mobile contact bar
│   │   ├── sections/            # 12 modular landing page sections
│   │   │   ├── Hero.astro
│   │   │   ├── TrustBar.astro
│   │   │   ├── WhyProfessional.astro
│   │   │   ├── ServiceGrid.astro
│   │   │   ├── DiyPitfalls.astro
│   │   │   ├── PricingFactors.astro
│   │   │   ├── RegionalInfo.astro
│   │   │   ├── StarlinkVsNbn.astro
│   │   │   ├── ServiceOfferings.astro
│   │   │   ├── ServiceAreas.astro
│   │   │   ├── FaqAccordion.astro
│   │   │   └── CtaBanner.astro
│   │   └── ui/                  # Reusable UI primitives
│   │       ├── Badge.astro
│   │       ├── Button.astro
│   │       └── QuoteForm.astro
│   ├── layouts/
│   │   └── Layout.astro         # Document shell, SEO meta & JSON-LD schemas
│   ├── pages/
│   │   └── index.astro          # Landing page entry point
│   └── styles/
│       └── global.css           # Global tokens, typography & resets
├── astro.config.mjs             # Astro static configuration
├── package.json
└── tsconfig.json                # TypeScript strict configuration
```

---

## Local Development

### Prerequisites

- Node.js (v18.14.1 or later)
- npm

### Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/rob82aus/Starlink.git
cd Starlink
npm install
```

### Start Development Server

```bash
npm run dev
```

The local development server will start at `http://localhost:4321`.

---

## Production Build

To build the static production bundle:

```bash
npm run build
```

The pre-rendered static files will be generated into the `dist/` directory:
- `dist/index.html`
- `dist/_astro/` (bundled and minified CSS/JS assets)
- `dist/assets/` (static images and public assets)

---

## Production Preview

To test the generated production build locally:

```bash
npm run preview
```

---

## SEO & Metadata

- **Page Title:** `Starlink Installation Brisbane | Expert Dish Mounting & WiFi Setup`
- **Meta Description:** `Professional Starlink installation across Brisbane & SE QLD. Roof mounting, neat cable routing, whole-home mesh WiFi & network setup. Call 0477 319 160.`
- **Canonical URL:** `https://www.zoorepairs.com.au/computer-services/starlink-installation/`
- **Social Sharing:** Open Graph and Twitter Card metadata (`summary_large_image`).
- **Structured Data (JSON-LD):**
  - `LocalBusiness`: Business identity, contact number (`+61477319160`), Brisbane geo-coordinates, operating hours, and service areas.
  - `Service`: Service catalog for Starlink mounting and networking optimization.
  - `FAQPage`: 8 search-indexed FAQ entities.

---

## Quote Form

The embedded quote form (`src/components/ui/QuoteForm.astro`) includes:
- Client-side validation for full name, Australian phone number format, suburb, and installation requirements.
- Honeypot anti-spam field.
- Interactive loading state with spinner on submission.
- Real-time field error clearing and inline alerts.

*Note: The form currently functions as a client-side interface; no backend API endpoint, webhook, or external CRM service is connected in this repository.*

---

## Deployment Status

- **Status:** **Build-ready, deployment not yet configured.**
- The project generates clean, standalone static assets in `dist/` ready for hosting on Cloudflare Pages, a Cloudflare Worker static asset route, reverse-proxy subpath configuration, or any standard static web server.

---

## Target Production URL

- **Target URL:** `https://www.zoorepairs.com.au/computer-services/starlink-installation/`

---

## Repository

- **GitHub:** [https://github.com/rob82aus/Starlink.git](https://github.com/rob82aus/Starlink.git)
- **Default Branch:** `main`
