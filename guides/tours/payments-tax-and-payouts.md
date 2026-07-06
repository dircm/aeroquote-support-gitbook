---
description: Connect Square or Westpac PayWay, set a card surcharge, configure operator-wide tax, and reconcile Square payouts against your tour bookings.
---

# Payments, Tax & Payouts

Connect a payment provider so customers pay at checkout, set your tax jurisdiction once, and reconcile the deposits that land in your bank.

## Prerequisites

* The Tour Packages module enabled (see the [overview](README.md))
* A Square account (sandbox or live) or a Westpac PayWay merchant facility

## Step 1: Connect a payment provider

1. Click **Tour Packages → Payment Provider**
2. Connect a provider, then make it your **active** provider — one provider is used at checkout at a time:
   * **Square** — click **Connect Square**, sign in on Square's consent screen, and approve. A single-location Square business is auto-selected; otherwise pick the location bookings record against
   * **Westpac PayWay** — enter your PayWay REST API keys (found in the PayWay web app under **Settings → REST API Keys**) and click **Connect Westpac PayWay**

AeroQuote never holds your customer's money — the provider deposits straight into your linked bank account on its normal schedule.

Worth knowing:

* **Card surcharge** is optional — set a percentage and/or fixed amount and customers see it as a separate checkout line item; set both to 0 to absorb the fee
* **Disconnecting is gated for safety** — if you have active tours, pending payments, or future scheduled departures with un-refunded paid tickets, you'll see a blockers list with deep links to resolve first
* **"OAuth state mismatch"** finishing the Square consent flow — the handshake timed out or you switched browsers mid-flow; click **Connect Square** again and stay in one window

## Step 2: Set up tax (once per operator)

1. Click **Tour Packages → Tax**
2. Pick a **jurisdiction preset** (e.g. Australia — GST, US — federal excise + state), or build custom items
3. Fill in the **tax-invoice metadata** — the moment a registration number is set, customer receipts switch from "Receipt" to a proper **Tax Invoice** with itemised tax lines
4. Use the **live preview** sliders to sanity-check a sample fare + add-on + surcharge before you publish

Tax is **operator-wide** — the same editor and items serve tours, scheduled flights, and every checkout. The full walkthrough (presets, inclusive vs exclusive pricing, the separate storefront pricing mode, compound taxes) is in [Tax Setup](../scheduled-flights/tax-setup.md) — everything there applies here.

Tour-specific points:

* **Per-add-on exemption** lives on each tour's edit page — tick **Tax-exempt** on the add-on (e.g. a champagne add-on that's taxable when exempt-fare air transport isn't)
* Settings apply to the **next** booking; existing bookings keep the tax breakdown snapshotted when they were placed, so historical receipts stay correct
* Not sure yet? Leave the preset on **Custom** with no items — no tax applies — and come back after your first sale

## Step 3: Reconcile payouts

**Tour Packages → Payouts** bridges your AeroQuote sales and the money landing in your bank (Square-connected operators):

1. The page lists your most recent Square payouts — date, amount, currency, status
2. Click **View entries** on a payout to expand it — each entry is matched back to the local booking so you can see which tour bookings (and scheduled-flight ticket sales, if you sell both) contributed to the deposit
3. Read each row's **Gross / Fee / Net** — what the customer paid, what Square took, what you banked

Worth knowing:

* **Payouts are operator-wide** — one deposit can mix tour bookings and scheduled-flight sales; both appear here
* **Unmatched entries** (e.g. a manual adjustment made directly in the Square dashboard) are flagged as unmatched
* **Data is live** — each page load asks Square for the latest; up to ~50 recent payouts with up to 100 entries each. For older deposits or bulk export, use Square's own dashboard
* For deeper analysis, bridge the systems with the per-booking Square payment id shown on each [booking detail](bookings-manifests-and-refunds.md)

## Next steps

* [Bookings, Manifests & Refunds](bookings-manifests-and-refunds.md) — where every paid booking lands
* [Tax Setup](../scheduled-flights/tax-setup.md) — the full operator-wide tax editor reference
