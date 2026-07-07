# Go Dental — Premium Corporate Website

A world-class, production-ready marketing website for **Go Dental**, Karachi's
premier multi-specialty corporate dental chain.

> **Tagline:** *"Clean, Low-Price, Hi-Tech Dentistry for All."*

Built as a fast, dependency-free static site (vanilla HTML, CSS, JS) — no build
step, no frameworks, no npm install required. Just open and deploy.

---

## ✨ Highlights

- **7 fully-designed pages** with consistent premium design system
- **Brand-accurate palette** — Lime Green `#79c142` + Corporate Navy `#2c3e50`, white-led
- **WhatsApp-first booking** — every service button opens WhatsApp with a tailored, pre-filled message to `+92 333 2498977`
- **Premium interactions** — scroll reveal, animated counters, button ripple, card lift, smooth scroll, FAQ accordion
- **WCAG-minded accessibility** — semantic HTML, skip link, ARIA labels, keyboard-friendly accordion, focus styles, reduced-motion support
- **SEO-complete** — per-page meta, Open Graph, Twitter cards, canonical URLs, and JSON-LD Schema (Dentist, MedicalBusiness, FAQPage, ContactPage)
- **Mobile-first responsive** — perfect from 360px to 4K, glassmorphic mobile menu
- **Zero stock images** — all visuals built with CSS + inline SVG (fast, crisp, on-brand)

---

## 📁 Structure

```
ZCodeProject/
├── index.html            # Home (hero, trust, why, services, tech, hygiene, experience, gallery, locations, testimonials, FAQ, CTA)
├── about.html            # Mission, three core pillars, values
├── services.html         # Service grid + deep-dives (implants, ortho, cosmetic) + quick-enquiry bar
├── why-choose-us.html    # 8 reasons, tech deep-dive, stats, testimonials
├── clinics.html          # Both branches w/ maps, hours, centralized channels
├── contact.html          # Quick cards, WhatsApp-powered form, branch panel, Marham portal
├── faq.html              # 10-question accordion + FAQPage schema
├── README.md
└── assets/
    ├── css/styles.css    # Full design system (tokens, components, responsive)
    └── js/main.js        # Nav, scroll-reveal, counters, FAQ, ripple, WhatsApp wiring, form
```

---

## 🦷 Services (with bespoke WhatsApp messages)

| Service | WhatsApp message |
|---|---|
| Consultation & Diagnostics (**FREE**) | `Hello Go Dental. I'd like to book a FREE consultation.` |
| Preventative Dentistry | `Hello Go Dental. I'd like to book a Preventative Dentistry appointment.` |
| Restorative & Cosmetic | `Hello Go Dental. I'd like to inquire about Cosmetic Dentistry.` |
| Specialist — Implants | `Hello Go Dental. I'm interested in Dental Implants.` |
| Specialist — Orthodontics | `Hello Go Dental. I'd like information about Braces/Orthodontics.` |

All messages use proper URL encoding via the official `https://wa.me/<number>?text=<msg>` API.

---

## 🔧 Running locally

No build needed. Either:

1. **Double-click `index.html`** to open in your browser, or
2. Serve it for a truer experience:
   ```bash
   # Python (if installed)
   python -m http.server 8080
   # or Node
   npx serve .
   ```
   Then visit `http://localhost:8080`.

---

## ✏️ Customisation cheatsheet

| What | Where |
|---|---|
| WhatsApp number | `assets/js/main.js` → `WA_NUMBER` (currently `923332498977`) |
| Brand colours | `assets/css/styles.css` → `:root { --c-primary, --c-navy … }` |
| Fonts | `<link>` in each page `<head>` + `--font-display/--font-body` in CSS |
| Branch details | `clinics.html`, `contact.html`, footer blocks on all pages |
| Social links | Footer `footer__social` block on each page |

---

## 📞 Brand facts (source: blueprint)

- **Branches:** Tipu Sultan (Kathiawar Bldg, 75300) · Gulshan-e-Iqbal (SB 17)
- **Phones:** (021) 34371712 · +92 333 2498977 · +92 332 2436044 · (021) 34980400
- **Toll-free:** 0800 71212
- **Domain:** www.godental.com.pk
- **Online portal:** Marham Medical Portal (042-34500888)
- **Social:** Facebook (7.4K+), Instagram @godentalpk
- **Hours:** Tipu Sultan Mon–Sun 9 AM–9 PM; Gulshan opens daily 9 AM

---

© Go Dental. Designed as a production-ready commercial website.
