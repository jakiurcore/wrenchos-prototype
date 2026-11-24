# WrenchOS: clickable prototype

A self-contained, desktop-first prototype of WrenchOS, a workshop management system (ERP + CRM) for repair shops. All data is fictional and lives only in the visitor's browser. Nothing is sent anywhere, and reloading the page resets the demo.

## Files

| File | What it is |
|---|---|
| `index.html` | The full prototype. Open this one. |
| `design-system.html` | Component and style sheet (colors, type, badges, buttons, inputs). |
| `LICENSES.txt` | Third-party license (Preact, MIT). |

Every page is a single HTML file with no build step and no server code. The only outside request is the Inter font from Google Fonts. If that request is blocked, the page falls back to the system font.

## Hosting

Upload the folder to any static host:

- **Netlify Drop:** drag the folder onto app.netlify.com/drop to get a public link in seconds.
- **Vercel / Cloudflare Pages / GitHub Pages:** deploy the folder as a static site.
- **S3, an existing web server or an intranet:** copy the files across.
- **Offline:** double-click `index.html`. It also works from `file://`.

Viewing on a screen at least 1280 px wide is recommended.

## Walking a client through it

Click **Demo guide** in the top bar. It walks through the John Smith story in 10 steps:

1. Dashboard
2. Find John Smith
3. Open his 2020 Toyota Corolla
4. Book an appointment
5. Build and send an estimate
6. Approve it as the customer
7. Convert it to a repair order
8. Do the work as Mike, the technician
9. Complete, invoice and take payment
10. Check the results

Steps tick themselves off as you go. **Restart demo data** resets everything.

Use **Viewing as** in the top bar to switch between Owner, Advisor, Technician and Super Admin.

## Link options

Add these to the URL to preset the demo, e.g. `index.html?startScreen=customer&currency=EUR`.

| Parameter | Values | Default |
|---|---|---|
| `startScreen` | `dashboard`, `customer` (John Smith), `vehicle` (Corolla), `appointments`, `comms` | `dashboard` |
| `demoStart` | `RO-5001 completed`, `Estimate approved` | `RO-5001 completed` |
| `currency` | `USD`, `EUR`, `GBP`, `CAD`, `AUD`, `AED`, `BDT` | `USD` |
| `taxRate` | number, e.g. `8` | `8` |
| `laborRate` | number, e.g. `120` | `120` |
| `dataState` | `live`, `loading`, `empty`, `error` (shows the edge-case states) | `live` |
