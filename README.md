# PowerClick Cookie Observer (server-side GTM tag)

Refreshes [PowerClick](https://powerclick.io)'s first-party `__spore_*` cookies from your server container, so the visitor ID keeps
its 400-day lifetime in browsers that cap cookies set by scripts (Safari: 7 days), and reports which attribution
cookies arrived to PowerClick's cookie health report.

## Setup

1. Server container: **Templates → Tag Templates → Search Gallery → PowerClick Cookie Observer**.
2. **Tags → New → PowerClick Cookie Observer**. Enter your PowerClick **Account ID**. Leave **Refresh existing
   cookies on every hit** on.
3. Trigger it on the `powerclick` event and on your site's main funnel events (for example `view_item`,
   `add_to_cart`, `begin_checkout`). No consent condition is needed: PowerClick's cookies only exist after consent.

## Permissions

- **Reads cookies:** PowerClick's `__spore_*` cookies and the ad platforms' own click cookies (read only).
- **Sets cookies:** PowerClick's `__spore_*` cookies only.
- **Reads event data / request:** `page_location`, `user-agent`, `referer`.
- **Sends HTTP requests:** `https://ingest.powerclick.io/*`, `https://ingest.clickspore.io/*`.
