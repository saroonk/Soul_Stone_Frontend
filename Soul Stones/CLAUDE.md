# SoulStones — Claude Context

Premium Indian gemstone e-commerce storefront. Plain HTML/CSS/JS, no build tools, no dependencies. Structured for later Django conversion (swap points marked with `<!-- Django: ... -->` comments).

## File structure

```
Soul Stones/
├── index.html              ← single-page homepage (main working file)
├── static/css/styles.css   ← all styles + CSS custom properties
├── static/js/main.js       ← all interactivity (IIFE, zero dependencies)
├── static/images/          ← product images (GM*.webp — watermarked placeholders)
├── templates/nav.html      ← header snippet for Django {% include %}
├── templates/footer.html   ← footer snippet for Django {% include %}
├── DESIGN.md               ← full design system reference
└── PRODUCT.md              ← brand/product context
```

## Design system

### Colors (CSS custom properties in `:root`)
- `--bg: #F7F3EA` — off-white page background
- `--surface: #FFFDF8` — card/lift surface
- `--black: #16120B` — statement grounds (announcement bar, stats band, footer)
- `--gold: #C9A24B` — bright gold: buttons, accents ON BLACK only
- `--gold-deep: #876521` — deep gold: headings/labels ON LIGHT only (never `--gold` on light, fails contrast)
- `--gold-soft: #E8D5A8` — champagne: hovers
- `--ink: #1A160F` — body text
- `--muted: #8A7B6C` — secondary text

**Two-Golds Rule:** `--gold` on black. `--gold-deep` on light. Never swap them.

### Typography
- `--font-display: "Gloock"` — **weight 400 ONLY** (no other weight exists; browser will fake-bold if you set 600/700). Use only at large editorial scale (≥ ~1.5rem). Section titles, hero title, stat figures.
- `--font-body: "Inter"` — all UI, body copy, card titles (Inter 600 for card titles, 500 for nav links, 400 for body)
- `--font-script: "Cormorant Garamond italic 500"` — **hero accent line only, once per page** (One Script Rule — never in UI, buttons, or cards)
- Google Fonts: `Gloock&family=Inter:wght@400;500;600&family=Cormorant+Garamond:ital,wght@1,500`

### Spacing
- `--section: clamp(56px, 8vw, 96px)` for section padding-block
- `.section + .section { padding-top: 0 }` prevents double-padding between adjacent sections

## JS architecture (main.js)

IIFE, `"use strict"`, zero dependencies. All logic fires in `DOMContentLoaded`.

**Key constants:**
- `WHATSAPP_NUMBER = "91XXXXXXXXXX"` — placeholder, replace before launch
- `IMG = "static/images/"` — product image path prefix
- `PRODUCTS[]` — 11-item hardcoded array (replace with Django context on port)
- Cart persisted to `localStorage` as key `ss_cart`

**Functions at init:**
`renderChips`, `renderGrid`, `renderRail`, `renderReviews`, `renderVideos`, `renderDrawer`, `updateCartBadge`, `bindSort`, `bindCategoryFilters`, `bindHeaderScroll`, `bindMobileNav`, `bindDropdowns`, `bindSearch`, `bindAnnouncement`, `bindReveal`, `bindNewsletter`, `bindGlobalClicks`

**Patterns:**
- `$()` = local `querySelector` alias
- Cart uses event delegation on `[data-add]`, `[data-inc]`, `[data-dec]`, `[data-remove]`, `[data-close-drawer]`
- `bindHeaderScroll()` sets `data-elevated="true"` on `#siteHeader` after 10px scroll
- `bindMobileNav()` calculates `.primary-nav top` from `header.offsetHeight` (announcement bar height changes on dismiss)
- `bindSearch()` toggles `.is-open` on `#searchBar` (CSS max-height animation); input focused 80ms after open
- `bindAnnouncement()` adds `.dismissed` on scroll past 72px → `transitionend` sets `hidden`
- `bindDropdowns()` handles Collections + Profile panels; closes on outside click / Escape

## Header structure

```
<header.site-header #siteHeader data-elevated>
  <div.announcement-bar #announcementBar>        ← black bar, auto-dismisses on scroll
  <div.shell.header-inner>
    <button.nav-toggle #navToggle>               ← hamburger (mobile only)
    <a.wordmark>Soul<span.wordmark-stones>Stones ← logo
    <nav.primary-nav #primaryNav>
      Home
      <div.nav-item.nav-item--has-dropdown>      ← Collections
        <button.nav-dropdown-btn #collectionsBtn>
        <div.nav-dropdown-panel #collectionsPanel>
      Our Story
      Contact
    <div.header-actions>
      <button.icon-btn #searchBtn>
      <div.nav-item.nav-item--has-dropdown>      ← Profile
        <button.icon-btn #profileBtn>
        <div.nav-dropdown-panel.profile-panel #profilePanel>
      <button.icon-btn.cart-button #cartButton>
        <span.cart-count #cartCount>
  <div.search-bar #searchBar>                    ← full-width, CSS max-height animated
```

Nav links: Home | Collections (dropdown) | Our Story | Contact  
Footer columns: Navigate | Gemstones | Talk to us

## Critical rules — do not break these

1. **Gloock weight 400 only.** Never set `font-weight` other than 400 on any element using `var(--font-display)`.
2. **Mobile dropdown scoping.** All mobile CSS overrides for nav dropdowns MUST be scoped to `.primary-nav .nav-dropdown-panel` / `.primary-nav .nav-item--has-dropdown` — never bare selectors. The profile panel in `.header-actions` must stay `position: absolute` on mobile or it breaks.
3. **Search bar uses CSS class, not `hidden` attribute.** `.is-open` toggles visibility via `max-height` transition. Using the `hidden` attribute blocks CSS transitions.
4. **Cart icon** is `<path d="M16 11V7a4 4 0 0 0-8 0v4"/><rect x="3" y="11" width="18" height="10" rx="2"/>` — a shopping bag with handles. Do not revert to the old trapezoidal path (it looked like a trash can).
5. **Product card images:** No `mix-blend-mode` + `background: var(--surface)`. The old `mix-blend-mode: multiply` made white-bg gem photos invisible on the warm background.
6. **Category tiles:** `object-fit: cover` — do not revert to `contain` (caused letterboxing on the lead tile).

## Placeholders to replace before launch

| Placeholder | File | Replace with |
|---|---|---|
| `WHATSAPP_NUMBER = "91XXXXXXXXXX"` | main.js | Real WhatsApp business number |
| WhatsApp `href` in footer | index.html, templates/footer.html | `https://wa.me/<real-number>` |
| `care@soulstones.example` | footer | Real email |
| `GM*.webp` product images | static/images/ | Clean product photography |
| Stats: 12,400+ / 4.9/5 / 32 years / 100% | index.html stats band | Real figures |
| `REVIEWS[]` array | main.js | Real customer reviews |
| Consultation advisor portrait | index.html `.consult-portrait` | Real photo |
| Video testimonial src/poster | main.js `renderVideos()` | Real video files |
| Lab logos (GIA, IGI, GII, GTL, GRS) | index.html `.certs-inner` | Real certification logos |

## Pending features

- **Search** — bar UI is built and animates, but no search logic is wired. Needs product filtering or Algolia/backend integration.
- **Auth** — profile dropdown (My Orders, Login/Sign up) links to `#`. Auth flow not built.
- **Our Story page** — nav link is `href="#"` placeholder, page doesn't exist yet.
- **Collections page** — "Collections" scrolls to `#categories` on homepage; no dedicated page yet.

## Django conversion checklist

1. `<link href="static/...">` → `{% static 'css/styles.css' %}`
2. `<script src="static/...">` → `{% static 'js/main.js' %}`
3. Wordmark `href="/"` → `{% url 'home' %}`
4. Replace `<!-- Django: {% include 'nav.html' %} -->` comment in index.html with actual `{% include %}`
5. `PRODUCTS` array → Django context → `window.__PRODUCTS__ = {{ products_json }}`
6. `WHATSAPP_NUMBER` → Django settings → template context → data attribute or inline script
7. `<span id="year">` JS trick → `{% now "Y" %}`
