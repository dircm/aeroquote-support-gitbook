---
description: >-
  Use the Request estimator to compare aircraft costs after choosing which
  aircraft to estimate, review internal fuel burn when shown, then generate a
  quote.
---

# Using the Estimator

The **Estimator** (Request page) calculates costs for the **aircraft you add** for a set of flight legs. Use it to compare options before you click **Generate Quote**. Estimates are not run for the full fleet until you choose aircraft.

***

## Step 1: Open or create a request

1. Click **Requests** in the sidebar
2. Click **Add New Request**, or open an existing request
3. Enter customer details and flight legs (departure, arrival, date/time)

## Step 2: Add aircraft to estimate

Until you add aircraft, the estimates area shows **+ Add Aircraft to see estimates**.

1. Click **+ Add Aircraft to see estimates** (or **+ Add Aircraft** / **+ Add more Aircraft** once some are already added)
2. In the modal, review aircraft thumbnails and details
3. Click an aircraft to add it — already-added aircraft do not appear in the list
4. Repeat for each option you want to compare

{% hint style="info" %}
You can add aircraft before or after the route is complete. Estimates appear for chosen aircraft once departure and arrival are set on each leg.
{% endhint %}

## Step 3: Review estimates

For each **chosen** aircraft, AeroQuote calculates:

* Block time and distance for the **legs on the request** (charter legs you entered, plus any **homebase ferry** legs you accepted from the amber banners)
* Fuel, landing, parking, and sector charges (as cost lines)
* Total estimated cost per aircraft
* **Fuel** (burn) column when the aircraft uses an **advanced performance model** — planned burn for the sector, for your team only

Expand a row for the flight/routing breakdown, per-leg fuel where shown, and cost lines. Remove an aircraft from the list when you no longer want it estimated.

### Homebase ferry banners

If a selected aircraft has a homebase and the route does not start or end there, amber **Yes, add ferry** / **No** banners appear on the Request. Positioning legs are added to the itinerary **only when you accept**. Declining keeps estimates on charter legs only. See [Creating a Request (Operators)](creating-a-request-operators.md#homebase-ferry-banners-optional).

### Fuel burn column (internal)

| Detail | Behaviour |
| ------ | --------- |
| Where | Request estimator, Quote Builder, Booking Builder |
| Audience | Your team only — **not** on customer quote views or PDFs |
| Unit | **Settings → Localization** (default fuel unit, e.g. L or gal) |
| **—** | Plan did not return a burn figure for that leg; times can still be valid |
| **est.** | Burn derived from cruise performance × time when a full plan figure was missing |

Fuel burn is a **planning estimate**, not a guarantee of uplift. Pricing still follows your rates and cost rules. Aircraft on **standard AeroQuote performance** may show **—** in the Fuel column.

When you **Generate Quote** (or create a booking from the same kind of estimate), planned burn for advanced-performance aircraft is **saved on each flight leg**. You will see it again next to duration on the quote Options and Details steps, on the booking itinerary, and on crew/manifest views — still internal only. See [Advanced performance models](../aircraft/advanced-performance.md).

## Step 4: Compare and adjust

1. Review estimate rows for the aircraft you added
2. Expand flights to see cost breakdowns (fuel, fees, margin)
3. Use maintenance or operational cautions when shown for the proposed dates
4. **Add Flight** / **Add Return Flight**, **Load Route**, or edit times and airports — estimates **refresh only for the aircraft still on the list**

## Step 5: Generate a quote

1. Ensure at least one aircraft remains in the estimates list (chosen aircraft are the ones that become quote options)
2. Click **Generate Quote**
3. Complete the Quote Builder and create the quote

See [Create a Quote from a Request (Operators)](../quotes/create-a-quote-from-a-request-operators.md) for the next steps.

***

{% hint style="success" %}
**Tip:** If no estimates appear after adding aircraft, check that the route has departure and arrival on each leg, and that aircraft have flight performance data and costings configured.
{% endhint %}
