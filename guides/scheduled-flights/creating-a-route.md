---
description: Create a scheduled-flight route — stops, durations, seat capacity, public vs private visibility, flight numbers, display names, and route documents.
---

# Creating a Route

A **route** is a recurring city-pair or multi-stop sequence you fly — the template that individual bookable **departures** are generated from. This guide creates one and tours the route editor.

## Prerequisites

* The Scheduled Flights module enabled (see the [module overview](README.md))
* Airports in your directory for every stop
* [Tax configured](tax-setup.md) so fare inputs are interpreted correctly

## Step 1: Create the route

1. Click **Scheduled Flights → Routes** in the left sidebar
2. Click **+ New Route**
3. Enter a **Route name** — an internal label (e.g. "340" or "DBO-LHG"). Customers never see this.
4. Optionally pick an **Aircraft type** — the model you expect to operate. Individual tails are assigned per departure later.

## Step 2: Add the stops

1. Search for the **origin airport** and select it — it's added as stop 1 with an **ORIGIN** badge
2. Search for the next airport and select it — it's added with a **Flight duration** input
3. For a multi-leg run, keep adding airports. Intermediate stops show a **VIA** badge; the last stop shows **DESTINATION**. Example: Dubbo (origin) → Walgett (via, 40 min) → Lightning Ridge (destination, 25 min).
4. Remove any stop with the **×** button (minimum two stops)
5. Set the **seat capacity**
6. Click **Create route**

Departure *times* are not set here — they come from the recurring schedule (see [Schedules & Publishing](schedules-and-publishing.md)). Pricing isn't set here either — it lives on the **Fares & checkout** tab (see [Fares & Pricing](fares-and-pricing.md)).

## Step 3: Tour the route editor

You land on the route editor — a tabbed wizard. The active tab is reflected in the URL (`?tab=stops`) so you can deep-link or refresh without losing your place.

* **Basics** — name, flight number, aircraft type, durations, default seat capacity, route status, and visibility
* **Stops & pricing** — the vertical stop timeline where you add, reorder, or remove airports and set per-leg fares
* **Fares & checkout** — pricing model, fare classes, public airport display names, and the passenger fields collected at checkout
* **Operations** — schedules, auto-extend, crew/aircraft timing, route documents, and publish controls

## Editing stops later

On the **Stops & pricing** tab each stop is a card in a vertical timeline:

* **↑ / ↓** — move a stop one slot up or down
* **✕** — remove a stop (minimum two)
* **Insert stop here** — appears between any two cards, so you can splice a new airport into an existing rotation without rebuilding

A **Route preview** banner above the timeline shows the full ICAO chain at a glance (e.g. `YSDU → YWLG → YLRD`). Changes don't affect already-materialised departures until you publish a new batch.

## Public vs private routes

On the **Basics** tab, **Visibility** controls whether the route is sold publicly:

* **Public** *(default)* — listed on your storefront and sold through the ticket flow. Manual publishing lands departures in **Draft** so you can review before customers see them; auto-extend publishes directly.
* **Private** — hidden from the storefront entirely (customers get a 404). Use for FIFO contracts, government tasking, or recurring charter-style jobs. Departures still appear on the **Flight Board** and **Departures** list with a "Private" badge, each backed by a normal **Booking** where you load passengers and cargo manually. Private departures materialise straight to **Published** — there's nothing to gate.

You can switch visibility at any time; existing departures keep their current status.

## Flight number (optional)

On the **Basics** tab, set a **Flight number** (e.g. `AL340` — a 2–3 letter code plus 1–5 digits) if the route has a published callsign. Every departure inherits it automatically, and [flight tracking](../bookings-operators/flight-tracking/README.md) can follow the callsign even before a tail is assigned.

## Passenger fields collected at checkout

On the **Fares & checkout** tab, tick which fields the storefront collects per passenger. Name is always required and email always shown; the rest are per-route toggles:

* **Date of birth**, **Gender**, **Passport details** (number + expiry, both required when ticked — enable for international routes)
* **Passenger weight** (kg) — flows through to the departure manifest for weight & balance
* **Luggage weight** (kg) — with an optional **included luggage allowance** for the route; anything over is flagged as **excess** on the manifest
* **Reason for flying** — a *Resident / Service provider–work / Other* question built for subsidised remote services
* **Purchase order number** — one **PO number** per booking, for agencies that need it on paperwork

## Public display names (optional)

If "Bankstown Airport" should read "Sydney (Bankstown)" on your storefront, set an **override display name** per airport on the **Fares & checkout** tab. Overrides are operator-scoped and apply across all your routes.

## Route documents (optional)

Attach PDFs from your [Documents library](../documents/README.md) — terms of carriage, baggage policy, safety briefings:

1. On the **Operations** tab, find **Route documents** and click **Manage documents…**
2. Click a document in the library panel to attach it; use the arrows to reorder; **Remove** detaches it without deleting from your library

Attached documents appear on the public departure page ("Travel documents") before purchase, and on the customer's ticket page after.

## Duplicate a route

Need a near-copy — the same sector with different capacity or a variant fare structure? Click **Duplicate** in the route editor header. The copy carries the basics (name suffixed "(copy)"), all stops, and all fare classes, and is created **inactive** with a fresh slug. Schedules and departures are **not** copied, so give the copy its own recurrence before publishing.

## Next steps

* [Fares & Pricing](fares-and-pricing.md) — set what customers pay
* [Schedules & Publishing](schedules-and-publishing.md) — make departures bookable
