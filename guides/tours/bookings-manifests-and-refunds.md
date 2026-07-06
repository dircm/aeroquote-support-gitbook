---
description: Manage paid tour bookings — notifications, the day-of-flight manifest, the Flight Board, full refunds with slot release, and the Sales dashboard.
---

# Bookings, Manifests & Refunds

Every paid storefront booking lands in one operator list — find it, work the day-of manifest, assign aircraft and crew, and refund when you must.

## Prerequisites

* At least one paid (or test-mode) booking — see [the customer journey](storefront-and-branding.md#the-customer-journey)

## Booking notifications

Every paid tour booking emails your admin users (and desktop-alerts them if browser notifications are on). Opt in or out per recipient under **Settings → Notifications → Booking events → New tour booking placed**.

## Step 1: Find a booking

1. Click **Tour Packages → Bookings**
2. Filter by tour, status (paid / refunded / cancelled), or the **Departure from** / **Departure to** date range
3. Click **View** on the row

The detail page shows the tour and slot, a status pill, the participant **Manifest**, add-ons and totals broken into base price and tax, and the Square payment id for cross-referencing in Square's dashboard.

## Step 2: Work the day-of-flight manifest

1. On the morning of the flight, filter **Bookings** to today's departures
2. Open each booking — the **Manifest** section lists every participant with their declared weight and waiver acceptance status
3. Cross-check weights on a calibrated scale at check-in. If someone is materially heavier than declared, rebook them onto a tour with a higher weight cap, or refund on the spot and let them re-book

{% hint style="warning" %}
Waiver acceptance is per participant — three passengers means three ticks at checkout, and a no-show's acceptance doesn't transfer to a replacement.
{% endhint %}

## Step 3: Assign aircraft and crew

**Tour Packages → Flight Board** is the dispatcher view of **booked** departures only — empty future slots never appear. Alert chips at the top ("need aircraft", "need crew") highlight unassigned departures; click into a departure to open its Booking and the Assign Aircraft & Crew tooling — the same assignment flow used for charter bookings.

## Step 4: Refund a booking

**Refund booking** on the detail page issues a **full refund** of every line item — fare, add-ons, surcharge, and tax:

1. Open the booking (status **Paid**) and click **Refund booking**
2. Confirm in the dialog — refunds aren't reversible from AeroQuote's side
3. AeroQuote asks Square to refund (test-mode bookings refund locally — no real money involved), releases the slot capacity so the seat can re-sell, and flips the status to **Refunded**

Worth knowing:

* **There is no separate cancel action** — every cancellation runs through the refund flow, including test-mode bookings where nothing was actually charged
* **If you cancelled the slot first**, the refund still releases capacity but the slot stays off the storefront — click **Reopen** on the slot if the freed seat should re-sell
* **Customer notification** — Square sends its own refund receipt; AeroQuote doesn't send an additional refund email, so a personal note from your team is good service
* A booking still **Paid** past its departure date is effectively complete — AeroQuote doesn't auto-flip it, keeping it queryable for tax and accounting

## Sales reporting

**Tour Packages → Sales** shows bookings, passengers, and revenue over a rolling 7 / 30 / 90-day window, revenue ranked by tour, and your most recent paid bookings. Refunds are shown but excluded from revenue. For monthly P&L or Square reconciliation, use [Payouts](payments-tax-and-payouts.md#step-3-reconcile-payouts) or export from Square's dashboard.

## Next steps

* [Travel Agents (Tours)](travel-agents.md) — bookings placed on customers' behalf
* [Departures & Slots](departures-and-slots.md) — slot cancel/reopen mechanics
