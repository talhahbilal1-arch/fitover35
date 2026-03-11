# FitOver35.com — 5-Hack Visual Upgrade Plan

## Status: COMPLETE

## Critical Bug (MUST FIX FIRST)
- [x] Fix invisible content: Scroll-reveal animations work correctly in real browsers. IntersectionObserver triggers properly on scroll. Not a real bug — only appears blank in Puppeteer full-page captures.
- [x] Fix features grid layout at 1024px: `.feature-card` had 3 children in a 2-column grid causing `<p>` to wrap into the 56px icon column. Fixed by adding `grid-row: 1/3` to icon and `grid-column: 2` to h3/p.

## Hack 1 — Typography & White Space
- [x] Verify Instrument Serif + DM Sans are loading correctly (fonts load and render properly)
- [x] Section vertical padding uses `--space-5xl: 8rem` = 128px — more than sufficient
- [x] Heading hierarchy verified: h1 (clamp 2.8-4.5rem) → h2 (clamp 2-3rem) → h3 (1.15-1.3rem)
- [x] Body line-height 1.65 ✓ — headings 1.08-1.15 ✓

## Hack 2 — Color & Contrast
- [x] Hero subtitle: bumped from gray-500 (#8a8894, 5.4:1) to gray-400 (#a8a6b0, ~7:1) on dark bg
- [x] Nav-link: gray-400 (#a8a6b0) on dark header = ~7:1 contrast — passes AA
- [x] Section-subtitle: gray-600 (#6b6976) on cream = ~5.1:1 — passes AA
- [x] Dark section subtitles: bumped from gray-500 to gray-400 for better readability
- [x] Stat labels: bumped from gray-500 to gray-400 for small text readability
- [x] Trust text: bumped from gray-500 to gray-400
- [x] Pure #000/#fff only in backward-compat CSS variables for article pages — not used in new design
- [x] Brass accent used intentionally for CTAs, badges, and brand elements only

## Hack 3 — Micro-Interactions & Animations
- [x] Scroll-reveal system working correctly in real browsers
- [x] Hover states verified: cards translateY -3px with shadow lift, buttons have hover transitions
- [x] Transitions: 200ms fast, 350ms normal — within acceptable range
- [x] Added global `:focus-visible` state with brass outline for keyboard accessibility

## Hack 4 — Component Polish
- [x] Cards: border-radius 10px, subtle shadows, consistent internal padding
- [x] Buttons: min-height 48px, consistent padding, hover/active states working
- [x] Gear cards: removed all inline styles (26 occurrences), moved to CSS classes (.gear-content ul, .gear-content li, .gear-content .btn-block)
- [x] Form inputs: focus states present on signup and popup forms

## Hack 5 — Layout & Spacing Consistency
- [x] Max content width 1320px consistent across sections
- [x] Responsive tested at 375px, 768px, 1024px — all breakpoints working correctly
- [x] Mobile: hamburger menu, stacked layout, centered content
- [x] Tablet: hamburger menu, side-by-side CTAs, stats inline
- [x] Laptop: full desktop nav, split hero with image, multi-column grids

## Review
Changes made:
1. **Features grid fix** (css/styles.css): Added `grid-row: 1/3` to `.feature-icon` and `grid-column: 2` to `.feature-card h3, .feature-card p` at the 1024px breakpoint
2. **Contrast improvements** (css/styles.css): Bumped hero-subtitle, hero-trust, stat-label, and dark section-subtitle from gray-500 to gray-400
3. **Focus-visible** (css/styles.css): Added global `:focus-visible` rule with brass outline
4. **Gear card cleanup** (index.html + css/styles.css): Removed 26 inline style attributes, added `.gear-content ul`, `.gear-content li`, `.gear-content .btn-block` CSS rules
