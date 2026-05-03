# La Vie Beauty — We2 Concept Package

Three-page concept presentation for La Vie Beauty Salon & Spa (Brighton Beach, Brooklyn) — built as a redesign (Scenario B) of the existing site at https://beautysalonlavie.com.

## Files

| File | Purpose |
|---|---|
| `index.html` | The new website concept — provided by the client, integrated with We2 cross-nav at top |
| `guide.html` | Bilingual EN/RU walkthrough — opens with **"What we found on the old site"** then 8 feature blocks for the new build |
| `pricing.html` | Interactive 9-block calculator with Telegram submit |
| `screenshots/` | 8 placeholder PNGs for guide feature blocks (replace with real screenshots when ready) |
| `findings/` | Old-site screenshots used in the "What we found" block |
| `team/` | Margarita & Danil portraits |

## Open order

1. Client lands on `guide.html` first
2. Cross-nav at the bottom takes them to `index.html?from=guide` (live site) or `pricing.html`
3. On the live site, a discreet top bar appears (only when arrived from concept) with **Guide ← / → Pricing** to navigate back
4. Pricing has its cross-nav embedded in the top bar

## Pricing — 9 blocks

1. Site (always included) — $1,000
2. Hosting — 3 options:
   - We2 subdomain — free
   - Transfer existing `beautysalonlavie.com` — free
   - New server + full migration — $150
3. Photos slider 0–20 @ $10/image
4. **Stylist portraits — flat $200 for all 5** (NEW — separate from photos slider)
5. Notifications — Telegram or WhatsApp ($50) / both ($80)
6. Reviews — Google ($100) / custom ($400 + $5/mo)
7. **Services & bookings admin panel — $1,000** (rewritten scope: services CRUD + bookings inbox + old/new prices)
8. Visitor session replay & heatmaps — $80
9. Care plans — Basic $99/mo · Standard $199/mo (both with annual save 20%)

## Telegram

- Bot token / chat ID unchanged from the system default
- Quote message header: `🛎 *New quote — La Vie Beauty*`

## Scenario B specifics

The "What we found" block in `guide.html` includes:
- **One device-frame screenshot** of the old team grid with red annotation pins (`old_team_desktop.png`)
- **Three text-only finding cards** for: no online booking, mobile broken, small-details-that-signal-abandoned (typo, © 2018, dev instructions in login modal)

## What still needs the client's input

- 8 real screenshots for `screenshots/` — placeholders are in place. Naming:
  - `hero_desktop.png` (1600×1000)
  - `theme_mobile.png` (540×1170)
  - `cursor_desktop.png` (1600×1000)
  - `services_desktop.png` (1600×1000)
  - `pricing_mobile.png` (540×1170)
  - `booking_mobile.png` (540×1170)
  - `booking_success_desktop.png` (1600×1000)
  - `contact_desktop.png` (1600×1000)
- Final pricing decisions on the portrait pack ($200 — adjustable if client requests differently)

## QA checklist before sending to client

- [ ] EN/RU toggle works on guide and pricing
- [ ] Dark/light toggle works on guide and pricing
- [ ] Cross-nav on `guide.html` (bottom pills) lands on `index.html?from=guide` and `pricing.html`
- [ ] Cross-nav on `pricing.html` (top bar) lands on `guide.html` and `index.html?from=pricing`
- [ ] Top bar on `index.html` only appears when `?from=guide` or `?from=pricing` (or referrer matches)
- [ ] Pricing calculator: tap a card → adds to bottom-bar quote → expand details → send opens modal → submit posts to Telegram
- [ ] All 9 pricing blocks render in correct order
- [ ] Mobile-tested at 380px / 600px / 820px

## Replacing screenshots later

Drop the new PNGs into `screenshots/` with the exact filenames listed above. No code changes needed — `guide.html` references them by relative path.
