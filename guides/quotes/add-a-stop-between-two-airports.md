---
description: >-
  Adding stops between flights can be used to add a technical stop (example: a
  fuel uplift) or if the customer requests it.  AeroQuote makes this process so
  easy.
---

# Add a stop between two airports

Use **Add a Stop** when you need an intermediate airport on an existing quote leg — for example a fuel uplift, a tech stop, or a passenger pick-up or drop mid-route. AeroQuote splits the leg into two flights and recalculates times, distance, and costs.

{% embed url="https://screen.studio/share/TMBN9ahw" %}

## Prerequisites

* An open quote with at least one flight leg that has both a **departure** and **arrival** airport set
* You are on the quote **Options** (itinerary) step so you can see the flight timeline

***

## Step 1: Find the flight leg

1. Open the quote
2. Go to the **Options** step (the itinerary / option cards)
3. Find the flight leg you want to split — it shows **Depart** and **Arrive** airports with duration between them

## Step 2: Open Add a Stop

1. On the flight timeline, look **between** the depart and arrive points
2. Hover over the blue **+** marker on the connector (the flight duration label sits there)
3. The label changes to **Add a Stop**
4. Click the **+** / **Add a Stop** control

The **Insert a stop between:** dialog opens. It shows the current departure and arrival airports for that leg.

## Step 3: Choose the intermediate airport

Pick the stop airport in either of these ways:

### Use a suggested airport

1. Review the **Suggested airports and dist from midpoint** list
2. Click a suggestion (ICAO, name, and distance from the route midpoint are shown)

### Search for any airport

1. In the search field, type the airport name or ICAO code
2. Click the airport in the results list

Selecting an airport closes the dialog and inserts the stop.

## Step 4: Review the updated itinerary

After you insert the stop, AeroQuote:

1. Splits the original flight into **two** legs (origin → stop, then stop → destination)
2. Recalculates **duration**, **distance**, and **costs** for each new segment
3. Applies your operator **default parking duration** on the ground at the stop (see [Default units](../settings/default-units.md))

Check:

* Arrival and departure times on both new legs
* Parking time at the intermediate airport
* Option price and cost totals
* Any operational **cautions** on the new segments

{% hint style="info" %}
**Aeroquote tip:** Add a Stop inserts an **airport** via point. For a scenic or multi-waypoint **path** without a landing (same origin/destination circuit), use [Custom Routes & Route Library](../custom-items/custom-routes-and-route-library.md) or [map-based route editing](map-route-editing.md) instead.
{% endhint %}

## When to use Add a Stop

* Technical or fuel stops on long sectors
* Passenger on/off at an intermediate airport
* Overnight or turnaround at a via point without rebuilding the whole option

## Related

* [Adding a stop in a booking](../bookings-operators/adding-a-stop-between-two-airports-in-a-booking.md) — same idea on operational bookings
* [Default units](../settings/default-units.md) — default parking duration used when a stop is added
* [Map-based route editing (Quotes)](map-route-editing.md) — change the flight path without adding a landing
* [Custom Routes & Route Library](../custom-items/custom-routes-and-route-library.md) — save reusable scenic routes
