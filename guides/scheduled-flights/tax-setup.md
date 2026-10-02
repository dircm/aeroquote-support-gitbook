---
description: Configure tax for scheduled-flight ticket sales — jurisdiction presets, inclusive vs exclusive pricing, a separate storefront pricing mode, and compound taxes.
---

# Tax Setup

Tax controls what customers see at checkout (a line-item excise, or a discreet "Includes $X GST" note) and how your fare inputs are interpreted in the route editor. Configure it **before** publishing so prices come out the way you expect.

## Prerequisites

* The Scheduled Flights module enabled — the page lives at **Scheduled Flights → Tax**

## Step 1: Apply a jurisdiction preset

1. Click **Scheduled Flights → Tax** in the left sidebar
2. In the **Preset** dropdown, pick your jurisdiction:
   * **Australia — GST inclusive** — one 10% inclusive GST item
   * **New Zealand — GST inclusive** — one 15% inclusive GST item
   * **United Kingdom — VAT inclusive** — one 20% inclusive VAT item
   * **European Union — VAT inclusive (manual rate)** — one inclusive VAT item at 0%; fill in your country's rate
   * **United States — Federal Excise + state (exclusive)** — Federal Excise 7.5% plus a 0% state/local placeholder
   * **Canada — GST + provincial (exclusive)** — 5% GST plus a 0% provincial placeholder
   * **Custom** — build your own items
3. Click **Apply preset**
4. For presets with placeholder rates (EU, US, CA), enter your number in the **Rate (%)** field on the placeholder row and save
5. Optionally enter a **Country / state code** (e.g. `TX`, `QC`) — shown on customer receipts

The **Live preview** panel computes a sample receipt from your items — change the sample inputs to see the breakdown at different price points.

{% hint style="info" %}
Australian operators: the preset takes 30 seconds and you're done. If you leave **Custom** selected with no items, no tax is applied and fares are treated as final prices.
{% endhint %}

## How the pricing mode changes what you enter

* **Inclusive** (AU/NZ/UK/EU pattern) — the fare you enter is the total the customer pays; the GST/VAT component is reported under the total ("Includes $X GST")
* **Exclusive** (US/CA pattern) — the fare you enter is pre-tax; exclusive taxes are added at checkout as line items. Browse pages always show customers the **tax-included** sticker price (a $100 fare lists as $107.50 with 7.5% federal excise)

A helper line under every fare input in the route editor tells you which interpretation is in force, with a link back to this page.

## Storefront pricing mode (optional)

By default charter quotes and your public storefront share one **Pricing mode**. If your storefront must price differently from your charter quotes — the classic case is Australian consumer law requiring GST-inclusive seat prices while corporate charter quotes stay tax-exclusive — tick **"Storefront prices … use a different tax mode"** under the pricing-mode control and pick a mode for the storefront.

* The same tax items and rates are reused — only whether tax is baked into the advertised price changes
* One switch covers your whole public storefront (scheduled flights, and tours if you sell them); charter quotes keep the operator-wide mode
* Leave it off and the storefront simply inherits the operator-wide mode

## Compound taxes (Quebec TVQ)

Quebec's TVQ is calculated on `(fare + GST)`, not the fare alone:

1. Apply the **Canada** preset
2. Rename the provincial item to `TVQ` and set its rate to `9.975`
3. In the **Compound on** dropdown on the TVQ row, pick **GST**, then save

## Where tax shows up

* **Route editor** — the fare-input helper text ("entered including GST" vs "pre-tax — added at checkout")
* **Browse and departure pages** — always the tax-included sticker price
* **Checkout** — exclusive taxes as line items above the total; inclusive taxes as "Includes $X GST" below it
* **Ticket email and PDF receipt** — each tax item with its name, rate, and amount snapshotted at purchase time

## Troubleshooting

* **"Tax is not configured — fares are treated as final prices"** in the routes editor — you haven't applied a preset or added an active item with a non-zero rate yet
* **Customer charged the wrong amount** — the **Pricing mode** doesn't match how you entered fares. If you advertise $100 including GST but the mode is exclusive, the customer pays $100 *plus* tax. Switching modes applies prospectively — re-enter fares to match the new interpretation.

## Next steps

* [Fares & Pricing](fares-and-pricing.md) — enter fares now that they'll be interpreted correctly
* [Tax Setup (charter)](../settings/tax-setup.md) — the operator-wide tax settings for quotes and bookings
