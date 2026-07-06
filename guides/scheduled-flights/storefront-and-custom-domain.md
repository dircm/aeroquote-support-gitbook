---
description: Brand your public booking storefront, reword the confirmation email, serve it on your own domain, and run an end-to-end test booking.
---

# Storefront & Custom Domain

Your storefront is the public site where customers browse departures and buy tickets. It works immediately at `fly.aeroquote.com/fly/your-slug` — this guide brands it, optionally puts it on your own hostname, and verifies the whole flow with a test booking.

## Prerequisites

* A route with published departures (see [Schedules & Publishing](schedules-and-publishing.md))

## Step 1: Brand the storefront

1. Click **Scheduled Flights → Branding**
2. Set the **Storefront slug** — the path in your default URL (`/fly/your-slug`). Lowercase letters, numbers, and hyphens; keep it short and memorable.
3. Fill in the brand fields — the **live preview** on the right updates as you type:
   * **Primary accent colour** and **Hero / accent text colour**
   * **Button colour** and **Button text colour**
   * **Tagline** — optional strapline in the header
   * **Show logo / Show name / Show tagline** — untick any element your artwork already carries
   * **Font family (CSS value)** and an optional **Font stylesheet URL** (paste a Google Fonts link)
   * **Header & footer** background and text colours
4. Click **Save branding** — changes apply on the next page load of the public site

{% hint style="success" %}
To match your existing website, inspect it in your browser's DevTools and copy the `font-family`, header/footer colours, and CTA button colours straight into the matching fields.
{% endhint %}

## Step 2: Reword the confirmation email (optional)

At the top of the Branding page, switch the **Storefront / Booking email** toggle to **Booking email**. Three blocks are editable in a rich-text editor (no code to learn), each falling back to a sensible default when left empty:

* **Intro** — the opening line
* **At the airport / pre-flight instructions** — the block most operators rewrite (meeting points, check-in windows)
* **Sign-off**

Type `{operator}` anywhere to insert your operator name. Route-specific lines (e.g. passport requirements) are still appended automatically. The preview shows the email exactly as customers will receive it.

## Step 3: Point your own domain (optional)

The default URL keeps working forever — a custom hostname like `book.yourairline.com` is purely for branding. Subdomains are recommended; apex domains need ALIAS/ANAME support at your DNS provider.

1. Click **Scheduled Flights → Custom Domain**
2. Enter the hostname (no `https://`) and click **Save domain** — the status pill shows **Pending** with DNS instructions
3. At your DNS provider, add a **CNAME** for the hostname pointing at the target shown on the page, TTL 300
4. Wait a few minutes for propagation, then click **Verify now** — the status flips to **Verified**

Only **verified** hostnames are served — unknown hostnames fall through to normal routing, so there's no risk of traffic hijacking. One verified domain per operator; switching domains re-issues verification automatically.

If verification won't pass, check propagation from a terminal: `dig CNAME book.yourairline.com +short`.

## Step 4: Make a test booking

Before sharing the URL, run the happy path yourself:

1. Open your storefront URL (shown on the Branding page)
2. Click a departure a few days out, pick a fare class, and click through to checkout
3. Fill in passenger details with a real email you control
4. On the payment step:
   * **Test mode** (no provider connected) — click **Complete test booking**; no card needed
   * **Provider connected (sandbox)** — use your provider's test card
5. Confirm you land on the ticket page with a QR code, and the confirmation email arrives with the booking reference
6. Open the departure under **Scheduled Flights → Departures** and confirm the purchase, passenger, and Activity entries are all there

## What your customers receive

Every completed checkout (test or real) delivers:

* **Confirmation email** — booking reference, flight details, total paid, and a signed link per passenger
* **Ticket page** — a public signed-URL page with the QR code and your branding; the link is the only way in, no login
* **Printable PDF boarding pass**, **Apple Wallet pass** (`.pkpass` attachment), **Google Wallet** save link, and a **calendar (.ics)** download
* **Receipt / tax invoice PDF** — every passenger, fare lines, and the tax breakdown

All of these carry the **same QR token**, so crew check-in scanning works identically across paper, phone screen, and wallet passes.

**Group bookings:** when more than one seat is booked, the checkout shows a **"Main contact (receipt holder)"** picker. Only the chosen passenger gets the consolidated receipt link; everyone still gets their own ticket and wallet pass.

**Live updates:** wallet passes aren't static — [rescheduling or cancelling a departure](day-of-operations.md) updates or voids every pass automatically, with lock-screen notifications on iPhone. There are no certificates or wallet accounts for you to configure.

**Lost confirmation?** Point customers at the **Find my booking** page (`/fly/your-slug/lookup`, or `/lookup` on your custom domain). They enter their booking reference and checkout email and a fresh confirmation is dispatched.

## Next steps

* [Day-of Operations](day-of-operations.md) — the Flight Board, manual bookings, and changes
* [Travel Agents](travel-agents.md) — let agents book on your storefront with commission
