---
description: Price a scheduled route — per-leg or flat fares, through-booking discounts, fare classes with adjustments, operator-only fares, seat caps, and scheduled price changes.
---

# Fares & Pricing

This guide sets what customers pay on a route: the **base fare** (per-leg or flat) plus **fare classes** that adjust on top of it. Everything here lives on the route editor's **Stops & pricing** and **Fares & checkout** tabs.

## Prerequisites

* A route created (see [Creating a Route](creating-a-route.md))
* [Tax configured](tax-setup.md) — a helper under the fare inputs tells you whether fares are entered tax-inclusive or pre-tax

## How pricing fits together

The **base price** for any segment comes from the route's pricing model — the sum of the per-leg fares the customer flies, or one flat amount. **Fare classes** then apply a **fare adjustment** on top: the default class is locked at **+$0.00 — base fare**, a premium class adds a positive adjustment, and a discount class uses a negative one.

## Step 1: Choose the pricing model

On the **Fares & checkout** tab, the **Pricing model** card offers:

* **Per-leg fares** *(default — leave **Flat fare** unticked)* — each leg carries its own fare; a segment's price is the sum of the legs flown
* **Flat fare** — tick **Flat fare** and enter the **Flat fare amount**: a single price regardless of how many legs the passenger flies. Per-leg inputs on the Stops tab hide while it's on (your leg fares are preserved, so unticking restores them)

## Step 2: Set per-leg fares

On the **Stops & pricing** tab, each non-origin stop card has a **Leg fare** input — the price of the leg *arriving* at that stop:

| # | Airport | Flight time | Leg fare |
| --- | --- | --- | --- |
| 1 | Dubbo (origin) | — | — |
| 2 | Walgett | 1h 0m | $200 |
| 3 | Lightning Ridge | 1h 0m | $250 |

A customer booking Dubbo → Walgett pays $200; a through booking Dubbo → Lightning Ridge defaults to the sum, $450.

{% hint style="warning" %}
A leg left blank is treated as **not offered** — any segment crossing it can't be booked on the storefront. Set a fare on every leg you intend to sell.
{% endhint %}

## Step 3: Discount through bookings (optional)

Below the stop timeline, expand **Through-booking pricing**. Every multi-leg combination shows a row with its default (the leg sum) and an override field — e.g. override Dubbo → Lightning Ridge from $450 to $400 to reward end-to-end bookings. Leave a row blank to use the sum.

## Step 4: Add fare classes

Most operators sell at least two tiers — a cheap, restrictive "Saver" and a flexible "Flexi". On the **Fares & checkout** tab, click **+ Add fare class** and fill in:

* **Name** and **Description** (shown on checkout cards)
* **Fare adjustment** — the amount added to the base fare. The **default** class is fixed at **+$0.00 — base fare**; use positive adjustments for premium tiers and negative ones for discount fares
* **Refundable** — when ticked you can also set an **Admin fee ($)** deducted on refund
* **Changeable** — with a change **Cutoff (min before dep)**
* **Transferable** — whether the ticket can be renamed to another passenger
* **Check-in cutoff (min)** and **Validity (days)**
* **Terms** — free-form fare rules, shown behind a "View fare rules" link on the storefront
* **Show on public storefront** — untick to make the class operator-only (see below)

Mark one class as the **default** — it's pre-selected when customers land on a departure.

## Operator-only fare classes (Community Fares, comps)

Untick **Show on public storefront** on a class to hide it from customers while keeping it available to staff in the **Add passenger…** modal (tagged "(operator-only)"). The standard pattern for subsidised resident fares:

1. Keep a public "Standard" class at **+$0** (base fare, e.g. $300)
2. Add a "Community Fare" class with a negative adjustment (e.g. **−$220** for an $80 effective fare) and untick **Show on public storefront**
3. When a verified resident calls, staff issue the ticket manually on that class and record the eligibility evidence in the payment notes (see [Day-of Operations](day-of-operations.md#issue-a-manual-booking))

## Per-leg seat capacity (weight-limited sectors)

A short or hot-and-high strip on **any** leg can limit payload below the aircraft's seat count. Each non-origin stop card has a **Seat capacity** field that caps the inbound leg; blank inherits the route default.

Inventory is tracked **per leg** and a through booking consumes a seat on every leg it crosses — so with a 9-seat default and leg 2 capped at 6: up to 9 Dubbo → Walgett tickets sell, up to 6 Walgett → Lightning Ridge, and through bookings cap at 6 (the smaller leg binds). The storefront's "seats left" count automatically reflects the binding leg.

Caps must be positive and no greater than the route's default capacity. When you change a cap on a published route, future fully-unsold departures are re-stamped; departures with seats already sold on that leg are left alone (a warning tells you which dates didn't pick up the change).

## Scheduled price changes

To raise a fare on a future date without touching tickets already sold:

1. On the fare class, click **Schedule a price change**
2. The current row's **Offered until** is set to tomorrow, and a duplicate row is created starting the day after — edit its adjustment before saving

New bookings pay the price in force on the **booking date** (not the flight date); issued tickets keep their original fare. You can also set **Offered from** / **Offered until** manually on any class to time-box seasonal fares and promotions.

## Copy fare classes from another route

Once you have a fare schema you like, don't re-enter it per route:

1. Save the new route once so it exists
2. At the bottom of the **Fare classes** card, pick the source from the **Copy from route…** dropdown and click **Copy**
3. Every class is appended — name, adjustment, refund/change rules, terms, date windows, and the storefront flag. Save to persist.

Per-leg fares, through-booking overrides, and schedules are **not** copied — they're specific to each route's airports and timetable. Copies are independent snapshots; later edits to the source don't propagate.

## Next steps

* [Schedules & Publishing](schedules-and-publishing.md) — put the route on sale
* [Tax Setup](tax-setup.md) — how fare inputs are interpreted and what customers see at checkout
