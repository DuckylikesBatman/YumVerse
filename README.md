# 🍕 YumVerse — Restaurant Website

A multi-page static restaurant website for **YumVerse**, a modern pizza kitchen based in Beirut. Built with vanilla HTML and CSS, no frameworks or build tools required.

---

## 📁 Project Structure

```
yumverse/
│
├── index (main.html)          # Homepage
├── menu.html                  # Full menu page
├── reservation.html           # Table reservation form
├── catering.html              # Catering inquiry & gallery
│
├── main.css                   # Homepage styles
├── menu.css                   # Menu page styles
├── reservation.css            # Reservation form styles
├── catering.css               # Catering page styles
├── nav-footer.css             # Shared navbar & footer styles
│
├── trying.html / trying.css   # Prototype / sandbox file
│
├── fonts/
│   └── Dream-Avenue.ttf       # Custom brand font
│
└── images/
    ├── logo.png
    ├── pizza-offer.png
    ├── menu-bg-2.png
    ├── reservation-bg.png
    ├── catering-bg.png
    ├── catering.png
    ├── catering-pic-*.png     # Catering gallery images
    ├── pizza-icon.png
    ├── order-icon.png
    ├── stars-icon.png
    ├── catering-icon.png
    ├── house-icon.png
    └── earth-icon.png
```

---

## 📄 Pages Overview

### `main.html` — Homepage
- Loyalty offer banner ("10th pizza on us")
- Corporate overview with mission and highlights
- Annual stats grid (sales, orders, rating, branches, countries)
- Three feature sections linking to Menu, Reservation, and Catering

### `menu.html` — Menu
- Full food and drink menu organized by category
- Categories: Starters, Greens, Classic Pies, White Pies, Signatures, Grandma/Square, Calzone, Desserts, Drinks
- Dietary legend: Vegetarian, Vegan, Gluten-Free, Spicy indicators

### `reservation.html` — Reservations
- Form: name, phone, email, guest count, date, time, location, special requests
- Cascading location dropdowns (Country → State → City → Zip)
- Prevents past date selection
- Client-side form validation with a success alert on submit

### `catering.html` — Catering
- Hero banner image
- Photo gallery with hover zoom effects
- "How It Works" explanation
- Catering inquiry form: event basics, dietary preferences, contact info
- Date auto-set to today, past dates blocked

---

## 🎨 Design System

| Token | Value | Usage |
|---|---|---|
| `--bg-hero` | `#f7f4ef` | Page hero backgrounds |
| `--ink` | `#323030` | Primary text |
| `--ink-soft` | `#5c5858` | Secondary/muted text |
| `--accent` | `rgb(231,193,193)` | Borders, underlines |
| `--accent-strong` | `#e07a7a` | Buttons, highlights |
| `--border` | `#eee` / `#ece9e4` | Card and input borders |

**Font:** `Dream-Avenue` (custom TTF) with system-ui fallback stack.

---

## 🧩 Shared Components (`nav-footer.css`)

Both the navbar and footer are styled from a single shared stylesheet, keeping the look consistent across all pages.

**Navbar** — sticky, frosted-glass effect (`backdrop-filter: blur`), centered links, hover underline animation.

**Footer** — three-column layout with visit info, hours, and a contact block. Includes Instagram and Facebook social icons with gradient hover effects.

---

## 🚀 Getting Started

No build step needed. Just open any HTML file in a browser:

```bash
# Option 1 — open directly
open main.html

# Option 2 — use a local dev server (recommended to avoid font path issues)
npx serve .
# or
python3 -m http.server 8000
```

> **Note:** The custom font (`Dream-Avenue.ttf`) loads via a relative `fonts/` path. A local server prevents browser CORS restrictions on local font files.

---

## ✅ Features

- Fully responsive — mobile, tablet, and desktop layouts
- CSS custom properties (design tokens) for easy theming
- Accessible markup — semantic HTML, `aria-label`, `role` attributes
- No JavaScript frameworks — plain JS only where needed
- Smooth hover transitions on buttons, cards, and gallery images
- Social media links with platform-accurate gradient icons

---

## 🔧 Known Limitations / Future Improvements

- Forms are front-end only — no backend or email integration yet
- Location data in the reservation form is hardcoded (USA and Germany only)
- No mobile hamburger menu — nav collapses on small screens but isn't hidden
- Images are not optimized (no WebP conversion or lazy-loading for all assets)
- Could benefit from a shared HTML include system (e.g., a component for nav/footer) to avoid duplication across pages

---

## 👤 Author

Built as a web development project. Design language: warm, modern, food-forward.
