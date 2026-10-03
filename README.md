# AHLR Venture — Website Documentation

Responsive, single-page website for **AHLR Venture**, connecting customers with verified contractors for home and building services.

> **Tagline:** "Connecting you to reliable contractors"

---

## 🎨 Brand & Visual Identity

- **Deep Navy:** `#0B1424` (Primary brand color, text, dark backgrounds)
- **Gold:** `#D9A02B` (Accent, buttons, architectural roofline motif, verified icons)
- **Light Grey-Blue:** `#F5F7FA` (Section & page backgrounds)
- **White:** `#FFFFFF` (Card surfaces, clean contrast)
- **Typography:** Geometric sans-serif **Jost** (Google Fonts) matching the brand lettering
- **Hero Motif:** Gold roofline line-drawing echoing the house roof geometry from the logo

---

## 📂 Project Structure

```
ahlr-venture/
├── index.html            # Complete self-contained single-page website (HTML + CSS + JS)
├── README.md             # Project guide & configuration notes
└── assets/
    ├── logo.svg          # Standalone SVG brand logo (light background)
    └── logo-white.svg    # Standalone SVG brand logo (dark background)
```

---

## 🚀 How to Run & Preview

1. **Directly in Browser:**
   Double-click `index.html` or open it with any web browser (Chrome, Edge, Firefox, Safari).

2. **Using a Local Server (PowerShell):**
   ```powershell
   cd C:\Users\dadil\.gemini\antigravity\scratch\ahlr-venture
   python -m http.server 3000
   ```
   Then visit `http://localhost:3000`.

---

## ⚙️ Formspree Setup (Replacing Placeholders)

Both forms submit asynchronously without reloading the page and display immediate accessible status messages:

1. **Project Request Form:**
   In `index.html`, locate line ~346:
   ```html
   <form id="project-request-form" action="https://formspree.io/f/YOUR_FORM_ID" method="POST" novalidate>
   ```
   Replace `YOUR_FORM_ID` with your Formspree endpoint ID.
   - On success, it displays: `"Thanks, we'll contact you soon."`

2. **Contractor Application Form:**
   In `index.html`, locate line ~633:
   ```html
   <form id="contractor-signup-form" action="https://formspree.io/f/YOUR_CONTRACTOR_FORM_ID" method="POST" novalidate>
   ```
   Replace `YOUR_CONTRACTOR_FORM_ID` with your Formspree endpoint ID for contractor onboarding.
   - On success, it displays: `"Thanks for applying! We'll review your details and contact you soon."`

---

## 🧭 Sections Overview

1. **Header:** Sticky on scroll, brand logo, navigation links, and a gold "Post a project" button. Responsive mobile menu.
2. **Hero:** Gold roofline line-drawing, headline *"Hire a contractor you can trust."*, value proposition copy, two action buttons, and three quick assurances (*Verified contractors*, *Clear price estimates*, *Genuine reviews*).
3. **Project Request Form:** Beside the hero with service type (8 services dropdown), location, budget range in Indian rupees (₹), start timing, optional details, customer name, customer phone or email, and "Find contractors" button.
4. **How It Works (4 Steps):**
   - 01 Post your project
   - 02 Get matched
   - 03 Compare and choose
   - 04 Hire and track
5. **Services (8 Clickable Tiles):**
   - Civil construction
   - Renovation
   - Plumbing
   - Electrical
   - Painting
   - Carpentry and interiors
   - Tiling and flooring
   - Roofing and waterproofing
   *Clicking any service tile automatically selects that service in the Project Request Form and scrolls smoothly to it.*
6. **Why AHLR:** 4 pillars (*Verified contractors*, *Transparent price estimates*, *Genuine reviews*, *Easy comparison*).
7. **Compare Contractors:** 3 sample contractor cards displaying trade, verified badge, years of experience, rating, estimated price, availability, and a *"Request a quote"* button that selects the trade and scrolls to the form. Clearly flagged with a sample listing badge.
8. **For Contractors:** Invitation banner and dedicated contractor sign-up form.
9. **Footer:** Brand logo, navigation links, copyright, and tagline. Strictly adheres to showing no phone number, address, or email.

---

## ♿ Accessibility & Standards

- Semantic HTML5 landmark elements (`<header>`, `<main>`, `<section>`, `<article>`, `<nav>`, `<footer>`)
- Accessible keyboard focus rings (`:focus-visible` with 2px gold outline)
- WCAG AA/AAA color contrast ratios
- `prefers-reduced-motion` media query support for smooth animations
- Full `aria-live` and `role="alert"` regions for form validation and asynchronous statuses

---

## 🔮 Future Architecture Hooks

The code includes commented hooks ready for future implementation:
- Contractor profiles & directory
- Customer-contractor direct messaging
- Live project tracking & milestone management
- Interactive price estimator & cost calculator
- Verified customer reviews & photo gallery uploads
