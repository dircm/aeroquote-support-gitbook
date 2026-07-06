---
description: Choose a storefront layout, brand the tours storefront, reword the confirmation email, and walk the customer journey from browse to paid confirmation.
---

# Storefront & Branding

Give your tours storefront its own look, choose how the landing experience sells, and rewrite the confirmation email in your own voice — then run a test booking end to end.

## Prerequisites

* An enabled tour with published slots (see [Departures & Slots](departures-and-slots.md))
* A storefront URL slug — set on **Tour Packages → Branding** (your storefront lives at `/tour/<your-slug>`)

## Step 1: Pick a storefront layout

1. Click **Tour Packages → Tours**
2. In the **Public storefront** card at the top, note your storefront URL and pick a layout:
   * **Standard list** — a dense functional grid. Best when your own marketing site is the homepage and you deep-link customers straight to a tour's detail page
   * **Landing page** — a polished marketing layout with a full-bleed scenic hero, image-forward tour cards, and a contact strip. Best when AeroQuote *is* your tours homepage

Switching is instant — open the storefront URL in another tab to preview. Both layouts share the same detail and checkout pages, so existing deep links keep working whichever you pick.

## Step 2: Brand the storefront

1. Click **Tour Packages → Branding** (the **Storefront** tab)
2. Set the **Public URL slug**, brand colours (primary accent, hero text, button colours), a **tagline**, typography (`font-family` plus an optional stylesheet URL), and header/footer colours
3. Watch the **live preview** on the right, then click **Save branding**

Tours branding is its own column set, independent of [Scheduled Flights branding](../scheduled-flights/storefront-and-custom-domain.md) — any field you leave blank inherits the scheduled-flights value, so single-identity operators configure once over there and never touch this page. One local exception: a blank button colour falls back to the *tours* accent colour, so a red tours brand always gets a red button.

{% hint style="info" %}
Clearing a colour field makes the swatch beside it show black — a quirk of the browser's native colour input. The storefront uses the inherited/default value, which the live preview shows correctly.
{% endhint %}

## Step 3: Reword the confirmation email (optional)

1. At the top of the Branding page, switch the toggle to **Booking email** — the live preview switches to the email
2. Edit any of the three blocks in the rich-text editor (toolbar formatting — no Markdown needed):
   * **Intro** — the opening line
   * **On the day / pre-tour instructions** — meeting point, parking, what to wear; the block most operators rewrite
   * **Sign-off** — the closing line
3. Type `{operator}` anywhere to insert your operator name; leave a block empty to keep its default
4. Click **Save branding**

The booking summary, participant list, and PDF link are fixed — only your prose changes. Tour-specific lines (waiver confirmation, weight-limit note) are still appended automatically. New emails use the wording immediately; already-sent emails are unchanged.

## The customer journey

Send customers to `/tour/<your-slug>` (or link them straight to a tour):

1. **Browse** — every enabled tour with thumbnail, price, duration, and passenger cap
2. **Detail** — hero image, gallery, scenic route map, description, weight limits, cancellation policy, and a slot picker showing upcoming departures
3. **Checkout** — one panel per seat (name, declared weight, optional email and phone), add-on pickers, the waiver checkbox per participant, then the card payment form. Weight limits are enforced here, before any charge
4. **Confirmation** — a bookmarkable page on a signed link (not guessable), plus the confirmation email with the booking reference, departure details, participant manifest, total paid, and a tax-invoice PDF link

## Step 4: Run a test booking

Before connecting a payment provider, the checkout shows a yellow test-mode banner — bookings record as paid but no money moves.

1. Open your storefront URL in a private browser window
2. Book a real upcoming slot end to end, including an add-on and the waiver
3. Confirm the email arrives and the booking appears in **Tour Packages → Bookings**

## Next steps

* [Payments, Tax & Payouts](payments-tax-and-payouts.md) — connect a provider and go live
* [Bookings, Manifests & Refunds](bookings-manifests-and-refunds.md) — the operator side of every sale
