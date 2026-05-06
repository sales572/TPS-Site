# Toronto Pallet Services — Blog Spec

This document describes how the blog should be built. Hand this to your developer along with the three blog post files (`blog-post-1.md`, `blog-post-2.md`, `blog-post-3.md`).

---

## 1. Two page types

The blog has two kinds of pages.

### A. Blog list page
URL: `/blog`

This is what visitors see when they click "Blog" in the nav. It shows all posts.

**Layout**
- Hero banner at the top: same gradient (navy → dark green) as the About and Products pages
- Hero title: "Insights & Resources"
- Hero subtitle: "Pallet industry guides, buyer tips, and behind-the-scenes stories from the TPS team."
- Below the hero: a 3-column grid of post cards (newest first)
- On tablet: 2 columns. On phone: 1 column.

**Each post card shows**
- Featured image banner (see Section 4 below)
- Category tag (small, gold uppercase text — e.g., "BUYER'S GUIDES")
- Post title (large, dark, 2–3 lines max)
- One-line excerpt (gray, 1–2 lines)
- Publish date (small, gray, bottom of card)

**Filtering**
- Above the grid, show three category filter pills: "All Posts", "Industry Insights", "Buyer's Guides", "Behind the Scenes"
- Clicking a pill filters the grid to that category. "All Posts" is the default selection.

### B. Individual post page
URL: `/blog/[post-slug]`

This is what visitors see when they click a post.

**Layout, top to bottom**
1. Same site header and nav
2. Hero banner: same gradient, but smaller height (~40% of homepage hero). Shows the post title (large, white, centered) and the publish date + category below it.
3. Post body: max-width 720px, centered. Uses the same Barlow font as the rest of the site. Headings are dark green (#1a3d08). Body text is dark gray (#1a2332) at 17px with 1.7 line-height.
4. "Back to all posts" link at the bottom of the article (centered, gold underline)
5. CTA section: same gradient as the About page CTA. Text: "Need pallets, crates, or lumber for your business?" Gold "Request a Quote" button below.
6. Site footer

**Body content rules**
- H2 headings: 28px, weight 600, dark green
- H3 headings: 20px, weight 600, dark navy
- Paragraphs: 17px, line-height 1.7
- Links inside body: gold (#d4a017), underlined on hover
- Lists: standard bullets, with 8px spacing between items
- Images inside posts (if any): full width of the body container, with rounded corners and a 32px margin top/bottom

---

## 2. Categories

Three categories total. Don't add more without explicit instruction.

| Category | Color tag | What it covers |
|---|---|---|
| Industry Insights | Gold | Regulations, certifications, sustainability, market trends |
| Buyer's Guides | Green | How to choose, comparisons, sizing decisions |
| Behind the Scenes | Brown | Process, facility, recycling, team |

Each post is assigned exactly one category.

---

## 3. The three launch posts

Three posts are ready to publish. Files: `blog-post-1.md`, `blog-post-2.md`, `blog-post-3.md`.

| Post | Category | Slug |
|---|---|---|
| What is ISPM-15? A guide to heat-treated pallets for export | Industry Insights | `what-is-ispm-15-heat-treated-pallets` |
| Standard 48×40 vs custom pallets: how to choose | Buyer's Guides | `standard-vs-custom-pallets` |
| 5 questions to ask before choosing a pallet supplier | Buyer's Guides | `5-questions-pallet-supplier` |

Each markdown file starts with a metadata block (title, slug, category, date, excerpt) followed by the article body.

---

## 4. Featured image banners

Each post needs a featured image (used on the list card and at the top of the post page).

**Banner style — instructions for designer/dev**
- Dimensions: 1200 × 630 pixels (standard for social sharing)
- Background: solid dark green `#1a3d08`
- Subtle pattern overlay (optional): faint diagonal lines at 5% opacity
- Post title centered, white, Barlow font, weight 600, ~52px
- Small "TPS" wordmark in the bottom-right corner, gold (#d4a017)
- No photos needed — text-on-color is the consistent style

If your dev has access to a tool like Figma or Canva, they can build a single template and just swap the title for each post. Takes 2 minutes per post.

---

## 5. Where it lives in the nav

The "Blog" item already exists in your nav. After launch, link it to `/blog`.

---

## 6. SEO basics for your developer

- Each post page should have a unique `<title>` tag (use the post title)
- Each post page should have a unique meta description (use the excerpt from the markdown file)
- The blog list page `<title>` should be: "Pallet Industry Insights & Guides | Toronto Pallet Services"
- All post URLs use the slug shown in the table above (lowercase, hyphens, no special characters)
- Featured images should have descriptive `alt` text — e.g., "ISPM-15 heat-treated pallet guide"

---

## 7. Post publishing workflow (after launch)

For each new post going forward:
1. Write the post in markdown (same format as the launch posts)
2. Generate a featured image banner using the template
3. Add to the CMS or hand to developer with the metadata block filled in
4. Verify it appears on the blog list page and the URL works

Aim for one post per month minimum. Posting consistently for 6 months is more valuable than posting heavily for 2 months and then stopping.
