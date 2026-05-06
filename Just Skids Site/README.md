# Just Skids Recycling — Website Handoff

A one-page marketing website for Just Skids Recycling, the recycling division of the Toronto Pallet Services network.

---

## Folder contents

| File | What it is |
|---|---|
| `index.html` | The complete website — HTML, CSS, and a mockup form handler all in one file |
| `hero-warehouse.jpg` | Background image for the hero section |
| `justskidslogo-symbol.png` | Cropped logo (recycle symbol only) — used in the page header |
| `justskidslogo-full.png` | Original full logo (with "Just Skids Recycling" wordmark) — for other uses |
| `README.md` | This file |

Drop everything in the same folder and `index.html` will work as-is.

---

## What's done

- Full page structure: header, hero, about, products (4 cards), services (3 cards), quote form, footer
- Sticky top navigation with smooth-scroll anchors
- Two-column quote form on a cream background
- Real contact info: phone (416-232-0339), email (justskids@gmail.com), address, hours
- Mobile responsive — breakpoints at 1000px, 820px, 800px, 700px, 600px, 480px
- All four product card "Request a Quote" buttons scroll to the form
- Hero badge "Part of the Toronto Pallet Services Network" links to https://tpspallets.com
- Brand colors locked: #2d6e10 (green), #1a3d08 (dark green), #1a5d1a (heading green), #a0522d (CTA brown)
- Font: Barlow (loaded from Google Fonts)

---

## What's left to wire up

### 1. Product photos (4 needed)
The product card image references in `index.html` point to filenames that don't exist yet:

- `product-grade-a.jpg`
- `product-custom-recycled.jpg`
- `product-combo-48x40.jpg`
- `product-combo-custom.jpg`

The client is reshooting these as individual pallet shots (not stack views). Photos should be roughly 4:3 landscape (e.g., 800x600px). Drop them into the same folder once received.

Until photos arrive, you can use a placeholder color or a gray box — the cards will still render, just without imagery.

### 2. Form submission (currently a mockup)
The form at the bottom currently shows a fake confirmation message. It does not send data anywhere. Wire it up using one of:

- **Formspree** (formspree.io) — easiest. Free for low volume. Replace the form action and remove the JS handler.
- **Web3Forms** (web3forms.com) — free alternative.
- **Custom backend** that emails justskids@gmail.com.

The script tag at the bottom of `index.html` has a TODO comment with example Formspree code.

### 3. Verify TPS link URL
The hero badge links to `https://tpspallets.com`. Confirm this is the correct production URL for the parent company.

### 4. SEO and analytics
The current `index.html` has a basic `<title>` and `<meta description>`. Add as needed:
- Open Graph / Twitter Card meta tags
- Favicon (use the cropped logo symbol)
- Google Analytics or similar tracking
- Structured data (LocalBusiness schema would help GTA SEO)

---

## Design notes

- The page intentionally uses the same cream `#f7f6f1` for both the Products section and the Form section — creates a visual rhythm down the page (white → cream → white → cream).
- Brown buttons (`#a0522d`) are the *only* CTA color. Three button styles in use:
  - Solid brown pill: header CTA, form submit
  - Outlined brown pill: product card "Request a Quote"
  - These ladder by visual weight (sticky → secondary → primary close)
- The TPS network badge in the hero is a **clickable link**, not just decoration. Clicking it sends visitors to the parent company.

---

## Browser support

Tested on modern Chrome, Safari, Firefox, Edge. CSS uses standard flex and grid — no IE11 support needed.
