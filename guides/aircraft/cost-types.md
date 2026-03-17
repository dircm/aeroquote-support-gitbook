---
description: Understand each aircraft cost type available when configuring sector charges.
---

# Cost Types

When adding or editing costs on the Aircraft Costings page, you choose from several cost types. Each type determines how the charge is calculated and applied to flights in your quotes and bookings.

---

## Per Flight Hour

Charged for every hour of flight time on a sector. Use this for costs that scale with how long the aircraft is in the air.

**Common uses:** engine maintenance reserves, insurance per flight hour, crew hourly costs

**How it's calculated:** hourly rate × flight duration (in hours)

---

## Per Landing / Sector

A flat charge applied once per landing or flight sector. Use this for fixed costs that occur each time the aircraft lands.

**Common uses:** handling fees, landing fees, navigation charges, airport services

**How it's calculated:** flat rate × number of sectors

---

## Per Passenger

Charged per passenger on each charter sector. Use this for costs that scale with the number of passengers carried.

**Common uses:** passenger facility charges, catering per head, insurance per passenger, terminal fees

**How it's calculated:** per-passenger rate × number of passengers × number of charter sectors

{% hint style="info" %}
Per-passenger charges only apply to charter flights, not ferry/repositioning flights.
{% endhint %}

---

## Per Distance

Charged based on the distance flown. When you select Per Distance, you choose the distance unit:

### Per Kilometer

Rate applied per kilometer of great-circle distance between airports.

### Per Nautical Mile

Rate applied per nautical mile of great-circle distance between airports. This is the most common unit in aviation.

### Per Mile

Rate applied per statute mile of great-circle distance between airports.

**Common uses:** enroute navigation charges, fuel surcharges, airway fees

**How it's calculated:** distance rate × distance flown (in the selected unit)

{% hint style="info" %}
Distance is calculated as the great-circle distance between the departure and arrival airports for each sector.
{% endhint %}

---

## Daily Charge

A flat charge applied for each calendar day of the trip. Use this for costs that accrue on a per-day basis regardless of flying activity.

**Common uses:** crew per diem, aircraft daily insurance, daily parking/hangarage

**How it's calculated:** daily rate × number of trip days

{% hint style="info" %}
Daily charges are applied at the option level, not per individual flight. The number of days is calculated from the first departure to the last arrival.
{% endhint %}

---

## Overnight Charge

A flat charge for each night the aircraft stays away from its homebase. Use this for costs related to overnight accommodation or away-from-base operations.

**Common uses:** crew accommodation, overnight parking, overnight hangarage, security

**How it's calculated:** overnight rate × number of nights away

{% hint style="info" %}
Like daily charges, overnight charges are applied at the option level. A night is counted when the aircraft is away from its homebase overnight.
{% endhint %}

---

## Ground Time

Charged per hour that the aircraft is on the ground between flights. Use this when you want to recover costs for the aircraft waiting between sectors.

**Common uses:** aircraft standby charges, ground handling during turnarounds, opportunity cost

**How it's calculated:** hourly rate × ground time (in hours) between consecutive flights

You can optionally set a **maximum charge** to cap the ground time cost. This is useful when you want to charge for short waits but not penalise long overnight stops.

{% hint style="info" %}
Ground time charges appear as separate rows in the itinerary between consecutive flights, making them easy to identify and adjust.
{% endhint %}

---

## Cost Rules (Flight Type Filtering)

For most cost types (except Daily, Overnight, and Ground Time), you can choose which flight types the cost applies to:

| Rule | Description |
|------|-------------|
| **All Sectors** | Applies to both charter and ferry flights (default) |
| **Charter Only** | Applies only to revenue/charter flights |
| **Ferry Only** | Applies only to repositioning/ferry flights |

{% hint style="success" %}
**Example:** You might set handling fees as "All Sectors" since you pay them at every airport, but set catering charges as "Charter Only" since ferry flights carry no passengers.
{% endhint %}

---

## Setting Up Costs

To add or edit aircraft costs:

1. Go to **Aircraft** from the sidebar
2. Click on an aircraft and navigate to the **Costings** tab
3. Scroll to **Aircraft costs that you will pay**
4. Click **Add new** to add a cost, or click the pencil icon to edit an existing one
5. The wizard guides you through: **Cost Type → Cost Rules → Amount → Name**

The cost name is auto-generated from your selections but can be customised.

---

## Next Steps

- [Costings](costings.md) — Configure pricing models and rates
- [Cost Simulator](cost-simulator.md) — Test how your costs affect quotes
- [Cost Management](../quotes/cost-management.md) — Manage costs on individual quotes
