# 🍕 YumVerse — Restaurant Website

A static multi-page website for YumVerse, a modern pizza kitchen based in Beirut. Built with plain HTML & CSS — no frameworks, no build tools.

---

## Pages

| File | Description |
|---|---|
| `main.html` | Homepage — loyalty offer banner, corporate overview, annual stats, and links to all sections |
| `menu.html` | Full menu organized by category (starters, pies, desserts, drinks) with prices and dietary tags |
| `reservation.html` | Booking form with cascading location dropdowns (Country → State → City → Zip) and date/time pickers |
| `catering.html` | Photo gallery, "How It Works" section, and a catering inquiry form |

---

## File Structure

```
├── main.html / main.css
├── menu.html / menu.css
├── reservation.html / reservation.css
├── catering.html / catering.css
├── nav-footer.css          # Shared navbar & footer (used by all pages)
├── trying.html / trying.css  # Prototype/sandbox file
├── fonts/
│   └── Dream-Avenue.ttf    # Custom brand font
└── images/                 # All site images and icons
```

---

## Design System

The site uses CSS custom properties (variables) defined in `:root` for consistent theming:

- `--accent: rgb(231,193,193)` — soft pink for borders and underlines
- `--accent-strong: #e07a7a` — stronger pink for buttons and highlights
- `--ink: #323030` — primary text color
- `--bg-hero: #f7f4ef` — warm off-white for hero sections

**Font:** `Dream-Avenue` (custom TTF) with a system-ui fallback stack.

---

## Key Features

- **Responsive** — flexbox and grid layouts adapt to mobile, tablet, and desktop
- **Shared components** — navbar and footer are styled once in `nav-footer.css` and reused across all pages
- **Reservation logic** — cascading dropdowns built in vanilla JS; past dates are blocked automatically
- **Catering form** — date auto-set to today, dietary checkboxes, and contact fields
- **Accessible markup** — semantic HTML with `aria-label`, `role`, and `alt` attributes throughout

---


## Known Limitations

- Forms are front-end only — no backend or email handling yet
- Location data in the reservation form is hardcoded (USA and Germany only)
- Nav/footer HTML is duplicated across every page (no templating system)
- No mobile hamburger menu
