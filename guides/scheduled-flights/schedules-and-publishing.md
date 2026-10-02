---
description: Turn a route into bookable departures — recurring schedules, timezones and daylight saving, manual publishing, and auto-extend with horizon warnings.
---

# Schedules & Publishing

A route with no schedule has no departures. This guide adds a **recurring schedule** (which days, what time) and **publishes** departures — the concrete, bookable instances customers see.

## Prerequisites

* A route with stops and fares (see [Creating a Route](creating-a-route.md) and [Fares & Pricing](fares-and-pricing.md))

## Step 1: Add a recurring schedule

1. Open the route editor and switch to the **Operations** tab
2. Under **Recurrence schedules**, click **+ Add schedule**
3. In the modal, set:
   * **Days of week** — tick the days the flight operates
   * **Departure time** — the *local* time at the departure airport (24-hour)
   * **Timezone** — defaults to the departure airport's own timezone, which is almost always right
   * **Effective from / until** — optional; leave blank for "always", or set them to time-box a seasonal schedule
4. Save the modal

Multiple schedules per route are fine — e.g. Mon/Wed/Fri mornings on one schedule and Tue/Thu afternoons on another. Each row has **Edit**, **Suspend / Resume**, and **Remove** buttons; suspended schedules are skipped when publishing while existing departures are left alone.

## Timezones & daylight saving

The departure time is a local wall-clock time in the schedule's timezone — AeroQuote works out the correct instant for every date:

* **Daylight saving is handled by the zone, not by you.** An 08:00 departure in a DST-observing zone (e.g. `Australia/Sydney`, `America/Los_Angeles`) stays 08:00 local across clock changes — no second schedule needed.
* **Non-DST regions need the matching zone.** Central Australia runs ACST year-round: use `Australia/Darwin` (permanent UTC+9:30), *not* `Australia/Adelaide`. In the US, Arizona operators should use `America/Phoenix`.

{% hint style="success" %}
Rule of thumb: trust the airport-defaulted timezone. Only override it if your crew genuinely brief in a different zone.
{% endhint %}

## Step 2: Publish departures

Schedules are templates — **publishing** materialises real departures out to a date window. Each departure gets its own Booking, flight item, and per-leg seat inventory, so manifests, crew assignment, and [flight tracking](../bookings-operators/flight-tracking/README.md) work exactly as for charter.

On the **Operations** tab, under **Publish departures**:

1. Set **Days ahead** (default 30)
2. Click **Publish next 30 days**

You'll see *"Created X new departures, skipped Y that already existed"* — re-running never creates duplicates.

On **public** routes, manually published departures land in **Draft** so you can review fares and capacity before customers see them; flip them to Published from the **Departures** list. **Private** routes materialise straight to Published.

## Step 3: Turn on auto-extend (recommended once live)

Rather than remembering to publish more departures, let the nightly job keep a rolling window topped up. On the **Operations** tab, in the **Schedule horizon & auto-extend** card:

1. Tick **Auto-extend this route**
2. Set **Always keep this many days available** — 30 for short-term routes, 60 for steady operations, 180+ to publish like an airline (range 7–365)
3. Set **Warn me when horizon drops below** (default 14 days)
4. Save

The card shows the route's **current horizon** as a coloured badge — green (healthy), amber (below the warning threshold), red (no future departures).

Auto-extended departures land directly in **Published** status — the point of auto-extend is "don't make me click publish". If you want a draft-review step, use manual publishing instead. The job respects each schedule's **effective until** date and never generates past it.

## The daily horizon advisory email

A daily check emails you one digest per operator when any route needs attention:

* A route's horizon is **below its warning threshold** (or it has no future departures at all) — whether or not auto-extend is on
* Auto-extend is on but a schedule's **effective until** falls inside the auto-extend window — extend or remove the end date before departures dry up

If nothing's wrong, no email.

## Next steps

* [Storefront & Custom Domain](storefront-and-custom-domain.md) — brand the pages customers book on
* [Day-of Operations](day-of-operations.md) — run the departures you've just published
