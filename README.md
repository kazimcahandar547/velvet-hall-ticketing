# Velvet Hall — Interactive Venue Ticketing System

A responsive, front-end-only theatre ticket selection project for Web & Mobile I (WM1).

## Run
Open `index.html` in a modern browser. No build step, dependencies, backend, or internet connection required. For a local server, run `python -m http.server 8000` in this folder and open `http://localhost:8000`.

## Venue and pricing
- Orchestra (VIP): 4 rows × 16 seats = 64 seats; $120 each.
- Mid Hall (Premium): 5 rows × 18 seats = 90 seats; $85 each.
- Balcony (Standard): 4 rows × 20 seats = 80 seats; $50 each.
- Total: **234 seats**. A deterministic subset is marked unavailable.

## Features
- Repeated seat buttons generated from `ZONES` in `script.js`.
- Inspect seats to view section, row, seat number and price **without adding to cart**.
- Explicit Add to Cart, duplicate prevention, ticket removal, live totals and seat-state synchronization.
- Cart stored under `velvet-hall-cart-v1` in browser `localStorage` and restored on refresh.
- Seven visible navigation actions: zoom in/out, move in four directions, reset/center.
- Optional bonus: mouse-wheel zoom and click/drag panning, with zoom and pan bounds.
- Responsive layout, keyboard-focus styling, semantic seat buttons and accessible labels.

## Test checklist
1. Click an available Orchestra seat: details change; cart remains empty.
2. Click ADD TO CART: seat turns green; item and price appear in cart.
3. Click the same seat again: button says ALREADY IN CART and is disabled.
4. Add a seat in Balcony: total reflects both categories.
5. Remove the Orchestra seat: map changes to available/inspected; total updates.
6. Refresh: remaining Balcony seat is restored in cart and highlighted on map.
7. Click a grey unavailable seat: it is disabled and cannot be added.
8. Use all arrow, zoom and reset buttons.
9. Scroll over the map and drag empty space; verify map moves and buttons still work.
10. Test browser widths at 1440px, 768px and 375px.

## Submission notes
The instructor requires a public GitHub repository with **at least three genuine, meaningful commits per week over four weeks**, a self-narrated 4–6-minute demo video uploaded to OneDrive with automatic subtitles, and a 1–2-page PDF report. Do not fabricate commit history. Use your real name, ID, URLs and actual final commit hash in the report. The final submitted commit must match the video demonstration.

## Project files
- `index.html` — semantic interface and application panels.
- `styles.css` — visual design, seating map and responsive layout.
- `script.js` — venue data, generated seats, cart, persistence and navigation.
- `REPORT_TEMPLATE.pdf` — submission summary with placeholders for personal and submission-specific details.
