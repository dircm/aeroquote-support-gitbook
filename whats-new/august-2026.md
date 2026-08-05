---
description: >-
  Advanced performance models for more realistic flight times (winds, climb and
  descent), model search when adding aircraft, and internal fuel burn on
  estimates.
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

* **Internal only** — for your team on estimate screens. **Not** on customer quote views or customer PDFs
* Unit follows **Settings → Localization** (default fuel unit for prices, e.g. litres or gallons)
* Figures are a **planning estimate**, not a guarantee of uplift or actual burn
* Pricing still follows your rates and cost rules
* Blank (**—**) can mean the plan did not return a fuel figure for that leg; times and distances can still be valid
* **est.** means burn was derived from cruise performance × time when a full plan figure was not available

See [Using the Estimator](../guides/requests/using-the-estimator.md), [Creating a Quote from scratch](../guides/quotes/creating-a-quote.md), and [Default Units](../guides/settings/default-units.md).

***

## What you need to do

Nothing required for most accounts once advanced models are linked for your fleet.

1. On **Aircraft → Details**, confirm the green **Using advanced performance model** banner for tails that should use the new engine — or **Link model** / **Change model** if something looks wrong  
2. On a Request or Quote Builder, add an aircraft and check block times on a familiar route  
3. Glance at the **Fuel** column on internal estimates (team only)  
4. Adjust display units under **Settings → Localization** if you prefer gallons or litres  
5. Contact support with the registration and route if a model is missing or times look off  
