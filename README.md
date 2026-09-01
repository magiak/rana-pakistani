# RANA Pakistani Restaurant

Website for **RANA Pakistani Restaurant** — an authentic Pakistani restaurant in Prague 8, Czech Republic. A modern single-page redesign built from a Claude Design concept.

## About

RANA serves traditional Pakistani cuisine — karahi, biryani, tandoori grills, curries and fresh naan — with dine-in, table reservations and Prague-wide delivery on Wolt.

- **Address:** Na Dědince 515/12, 180 00 Praha 8
- **Phone:** +420 721 809 084
- **Email:** rezervace@ranapakistani.cz
- **Delivery:** [Order on Wolt](https://wolt.com/cs/cze/prague/restaurant/rana-pakistani-restaurant)
- **Facebook:** [Pákistánská Restaurace Rana](https://www.facebook.com/pages/P%C3%A1kist%C3%A1nsk%C3%A1-Restaurace-Rana-Wwwpakistanicz/512073632147219)

### Opening hours

| Day | Hours |
|-----|-------|
| Monday | 11:30 – 16:00 |
| Tue – Fri | 11:30 – 22:30 |
| Sat – Sun | 12:00 – 22:30 |

## Tech Stack

Single-page static website:

- HTML5 + CSS3 (custom properties, grid, flexbox) — no build step
- Google Fonts (Cormorant Garamond + DM Sans, `latin-ext` for Czech diacritics)
- One small self-contained vanilla-JS component: the **flip-book menu** (see below). The rest of the page (sticky header, smooth scrolling) is pure CSS.
- Local images in `images/` (no external hotlinking)

## Full menu (flip-book)

Clicking **"Open the full menu & lunch specials"** (or *Menu* / *Lunch* in the nav) opens a book-style overlay with a real 3-D page-turn animation:

- Two-page spread on desktop, single page on mobile (rebuilds on breakpoint change; the book is sized in JS to always fit the viewport)
- Category quick-nav tabs, an always-visible footer pager (prev / page count / next), click-to-turn, swipe on touch, and keyboard control (← → / Esc)
- Content auto-scales to each page so nothing overflows
- Fully self-contained — no libraries, no external requests

The menu content is transcribed from RANA's **own printed menu** (the scanned pages on `ranapakistani.cz/main-menu/`), the **2025 lunch menu** (`/lunch-menu/`) and the **drinks list** (`/drinks/`) — so all dishes, descriptions and prices are the restaurant's real **dine-in** figures.

## Hosting

- Hosted on **GitHub Pages** from the `main` branch
- Repository: [magiak/rana-pakistani](https://github.com/magiak/rana-pakistani)
- Custom domain: **rana.lukaskmoch.cz** (configured via `CNAME`)

## Local Development

Open `index.html` directly in a browser — no server or build step needed.

## Project Structure

```
.
├── index.html      # Full website (HTML + inline CSS)
├── images/         # Photography (hero, dishes, gallery)
├── CNAME           # Custom domain configuration for GitHub Pages
├── .gitignore
└── README.md
```

## Content notes (verify before pitching)

This site was generated from a design concept, then populated with real data where available. A few items should be confirmed with the owner before it goes to the client:

- **Menu dishes, descriptions and prices** (both the six featured cards and the full flip-book menu) are transcribed from RANA's own printed à-la-carte menu, plus the 2025 lunch menu and the drinks list on `ranapakistani.cz`. These are the **dine-in** prices; Wolt/delivery prices may differ. The printed menu is undated in places — confirm the current figures with the owner before pitching.
- **"For over 20 years"** is the restaurant's own wording, taken from their current website ("We cook for you. For over 20 years."), so it is safe to use. The specific founding year **"Since 2003"** was an inference from it, was never stated by the restaurant, and has been **removed** from the site.
- **`rezervace@ranapakistani.cz`** and the reservation-by-email flow come from the concept — confirm the address is live.
- **All photos are the restaurant's own.** The hero, About and gallery images are RANA's own food photography taken from their existing website (`ranapakistani.cz`); the menu-card photos come from their **Wolt** listing. No stock imagery is used.
- Real **interior, storefront and additional dish photos** were also collected from `ranapakistani.cz` (their old site) and can be dropped into a "Step inside" venue section if desired — though most are low-resolution and would benefit from a reshoot.
- **Map** points to the coordinates in the design (50.11556176, 14.47244222 — Prague 8). Verify it lands on the correct entrance.
