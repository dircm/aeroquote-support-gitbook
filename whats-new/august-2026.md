---
description: >-
  Advanced performance models for more realistic flight times (winds, climb and
  descent), model search when adding aircraft, internal fuel burn on estimates
  and on saved quotes and bookings for your team, auto-generate option flight
  legs, smarter middle-leg delete on quotes, Add a Stop ranking, and a
  homebase ferry auto-add toggle on Requests and builders.
---

# August 2026

## Advanced performance for flight planning

AeroQuote can plan sector times and distances with an **advanced performance model** per aircraft. That model uses climb and descent profiles and route winds so block times on Requests, Quotes, and Bookings better match real flying — especially for jets and multi-leg trips.

### What you may notice

* Some sectors show slightly longer or shorter times than before — expected when winds and climb/descent are included
* Multi-leg itineraries may shift a little as each leg is planned more precisely
* Cost and pricing still use **your** rates and rules; only the planning inputs (time, distance, and fuel burn where shown) improve
* You can mix aircraft on advanced performance with aircraft on **standard AeroQuote performance data**

### Per aircraft control (Details)

Open **Aircraft**, select the registration, then **Details**.

| Banner / action | Meaning |
| --------------- | ------- |
| Green **Using advanced performance model** | This aircraft uses advanced planning for estimates |
| **Change model** → **Update model** | Pick a different catalogue model; the aircraft record stays the same; next estimate uses the new model |
| **Revert** → confirm **Revert?** | That aircraft returns to standard AeroQuote performance data |
| Blue **Link model** (if not linked) | Search and attach an advanced model for the first time |

See [Advanced performance models](../guides/aircraft/advanced-performance.md) and [Aircraft Details](../guides/aircraft/aircraft-details.md).

***

## Aircraft type search when adding aircraft

When you **Add Aircraft**, type search looks up the advanced model catalogue first (labelled **Search aircraft database (iFlightPlanner)** in the product).

* Type at least **2 characters** (make, model, or ICAO). Two-character terms search ICAO only for an exact match
* Pick a model from the results to continue with advanced performance data when available
* If **no models are found**, you can choose a **native AeroQuote aircraft type** (fallback) and finish setup as usual

Registration type lookup (guess from tail number) still works the same way.

See [Add Your First Aircraft](../getting-started/add-your-first-aircraft.md).

***

## Fuel burn on internal estimates

Requests, the **Quote Builder**, and the **Booking Builder** can show a **Fuel** column for aircraft on advanced performance planning.

### Important limits

* **Internal only** — for your team. **Not** on customer quote or booking views, or customer PDFs  
* Unit follows **Settings → Localization** (default fuel unit for prices, e.g. litres or gallons)  
* Figures are a **planning estimate**, not a guarantee of uplift or actual burn  
* Pricing still follows your rates and cost rules  
* Blank (**—**) can mean the plan did not return a fuel figure for that leg; times and distances can still be valid  
* **est.** means burn was derived from cruise performance × time when a full plan figure was not available  

See [Using the Estimator](../guides/requests/using-the-estimator.md), [Creating a Quote from scratch](../guides/quotes/creating-a-quote.md), and [Default Units](../guides/settings/default-units.md).

***

## Planned fuel burn on quotes and bookings

When you create a quote or booking from an advanced-performance estimate, AeroQuote can **save planned fuel burn on each flight leg** (alongside duration). You no longer need to re-run the estimator just to see burn for that itinerary.

### Where your team sees it

| Place | What you see |
| ----- | ------------ |
| **Quote → Options** | On each leg: duration and **· Fuel …**. On the option title bar (left): **Charter** time, **Ferry** time, and **Fuel** total for the option |
| **Quote → Details** | Fuel next to duration in the flight table; option **Total fuel** under the table when legs have data |
| **Booking → Itinerary** | Fuel next to duration on each flight |
| **Crew booking link** | Fuel next to duration (team / crew view) |
| **Flight manifest PDF** | Planned fuel under duration on each leg |

### What is not shown to customers

Customer quote links, customer booking pages, and customer quote PDFs do **not** include planned fuel burn.

### Notes

* Only **new** estimates written after this feature is live store burn on legs. Older quotes/bookings stay blank until you re-estimate or recreate them from a fresh plan.  
* Changing only the **duration** on a saved leg does **not** clear or rescale planned burn (it keeps the last planned figure).  
* Changing your fuel unit under Localization updates how burn is **displayed**; stored values stay in the plan’s original unit.  

See [Advanced performance models](../guides/aircraft/advanced-performance.md), [Creating a Quote from scratch](../guides/quotes/creating-a-quote.md), and [Booking Manifests](../guides/bookings-operators/booking-manifests.md).

***

## Quote Options: auto-generate legs and smarter flight delete

On an open quote’s **Options** step:

### Add Option (top-left)

**Add Option** is in the **top-left** of the Options toolbar (same row as **Admin View** / **Customer View**), not under the itinerary.

### Auto-generate flight legs for a new option

When you create a **new option** with an **aircraft**, and another option on the quote already has **charter** legs, AeroQuote asks whether to **auto-generate a full estimated itinerary** for the new aircraft from those charter legs (including ferry positioning and costs). Choose **Generate legs** or **Skip**.

### Delete a middle flight — stitch previous destination

When you **delete a flight leg** that sits between two other legs, AeroQuote asks whether to **update the previous flight’s destination** to the **next flight’s departure** (and recalculate that leg’s times/costs), or **delete only**.

See [Add a Quote Option](../guides/quotes/add-a-quote-option.md).

***

## Homebase ferry auto-add toggle

On **Requests**, **Quote Builder**, and **Booking Builder**, use:

**Automatically add repositioning (ferry) flights for Aircraft with a homebase**

* **On** (default) — classic estimates: homebase positioning ferries when the route does not start and/or end at homebase  
* **Off** — estimates use only the charter legs you entered  

See:

* [Creating a Request (Operators)](../guides/requests/creating-a-request-operators.md#repositioning-ferry-flights-toggle)
* [Using the Estimator](../guides/requests/using-the-estimator.md)
* [Creating a Quote from scratch](../guides/quotes/creating-a-quote.md)
* [Creating a Booking](../guides/bookings-operators/booking-builder.md)

***

## What you need to do

Nothing required for most accounts once advanced models are linked for your fleet.

1. On **Aircraft → Details**, confirm the green **Using advanced performance model** banner for tails that should use the new engine — or **Link model** / **Change model** if something looks wrong  
2. On a Request or Quote Builder, add an aircraft and check block times on a familiar route  

3. Glance at the **Fuel** column on internal estimates (team only)  
4. Create a quote and open **Options** — check **Charter / Ferry / Fuel** on the option header and **· Fuel** on each leg  
5. After converting to a booking, confirm fuel on **Itinerary** and (if used) the crew manifest  
6. Adjust display units under **Settings → Localization** if you prefer gallons or litres  
7. Contact support with the registration and route if a model is missing or times look off  
8. On a Request or Quote/Booking Builder, use the ferry auto-add toggle if you need charter-only estimates without homebase positioning  
