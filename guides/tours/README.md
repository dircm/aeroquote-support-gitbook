---
description: Sell scenic flights and tour experiences on a branded public storefront — tours, departure slots, online payment, manifests, and refunds.
---

# 🚁 Tour Packages

The Tour Packages module turns AeroQuote into a scenic-tour storefront. You build a **tour** (the product — price per seat, duration, weight limits, add-ons, photos), publish **departure slots** customers can book, and take payment online. Paid bookings flow into the same operations infrastructure you use for charter — bookings, manifests, crew assignment — so a Sunday-morning tour shows up on the same dispatch tooling as your Monday charter.

## Who it's for

* Helicopter and fixed-wing operators selling scenic flights by the seat
* Operators selling experience packages with add-ons (doors-off seats, champagne, photography)
* Anyone who wants customers to book and pay online without a phone call

## How it relates to charter and Scheduled Flights

| | Charter (Quotes → Bookings) | [Scheduled Flights](../scheduled-flights/README.md) | Tour Packages |
| --- | --- | --- | --- |
| Customer buys | The whole aircraft | Seats on a route between airports | Seats on a scenic experience |
| Departs / arrives | Anywhere you quote | Airport to airport | Returns to its departure point |
| Published as | Created per enquiry | Departures from a schedule | Bookable time slots per tour |
| Customer pays | On your quote terms | Storefront checkout | Storefront checkout |

Publishing slots does **not** create operational bookings — a slot is just a bookable time on your storefront. The operational **Booking** (with its flight item, manifest, and crew assignment) is created the moment a customer pays, one per paid booking. That keeps unsold slots off your dispatch screens entirely.

## Prerequisites

* The **Tour Packages** module enabled — open **Settings → Application Modules** and find the Tour Packages card. While the module is in pre-launch the card shows a **Coming soon** pill; talk to your AeroQuote rep to be switched on. Tour Packages requires the **Bookings** module.
* A **departure airport** in your operator's airport list — tours depart from a single home base.
* A payment provider is **optional to start**: without one the storefront runs in test mode (a yellow banner shows; bookings record as paid but no money moves). Connect Square or Westpac PayWay before selling for real — see [Payments, Tax & Payouts](payments-tax-and-payouts.md).
* A scenic route library entry is optional but recommended — it gives the storefront a route map with your points-of-interest. See [Custom Routes & Route Library](../custom-items/custom-routes-and-route-library.md).

## Where everything lives

Once enabled, a **Tour Packages** group appears in the left sidebar: **Tours**, **Flight Board**, **Departures**, **Bookings**, **Sales**, **Payouts**, **Payment Provider**, **Tax**, **Travel Agents**, and **Branding**.

## Setup checklist

Work through these guides in order the first time:

1. [Payments, Tax & Payouts](payments-tax-and-payouts.md) — connect a payment provider and set your tax jurisdiction
2. [Building a Tour](building-a-tour.md) — the product: pricing, weight limits, add-ons, waiver, photos
3. [Departures & Slots](departures-and-slots.md) — publish bookable times with a recurring schedule and auto-extend
4. [Storefront & Branding](storefront-and-branding.md) — layout, colours, confirmation email, and a test booking
5. [Bookings, Manifests & Refunds](bookings-manifests-and-refunds.md) — day-of operations and money-back
6. [Travel Agents (Tours)](travel-agents.md) — let agencies book on customers' behalf

{% hint style="success" %}
Run your first sale in **test mode** — build the tour, publish slots, and complete a booking through your own storefront before connecting a payment provider. Everything works end to end; no money moves.
{% endhint %}
