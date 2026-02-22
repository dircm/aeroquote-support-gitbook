---
description: View, edit, and manage individual cost line items on your quotes.
---

# Cost Management

AeroQuote now gives you full visibility and control over every cost that makes up a quote. Each flight, ground time, and option displays an itemised cost breakdown that you can expand, edit, and customise.

---

## What's New

Previously, flight costs were summarised as a single total. With this update:

- Every cost is displayed as its own **line item** (flight costs, landing charges, parking charges, fuel uplifts, and more)
- You can **add custom costs** to any flight or option
- You can **toggle individual costs** on or off without deleting them
- You can **edit amounts** on any cost item
- **Ground time charges** now appear as a separate row between flights in the itinerary
- Cost breakdowns carry through from **quotes to bookings** automatically

---

## Viewing Cost Breakdowns

### On a Flight Item

Each flight item in your quote now has an expandable cost section.

1. Open a quote and navigate to the **Options** tab
2. Find a flight item card
3. Click the cost summary bar (e.g. "3 costs — $1,250") to expand

When expanded, you'll see each cost line item:

| Column | Description |
|--------|-------------|
| **Name** | The cost type (e.g. "Flight Costs", "Landing Charges") |
| **Amount** | The cost in your operator currency |
| **Toggle** | Include or exclude this cost from the total |

### On an Option

Option-level costs (day charges, overnight charges, and custom charges) appear in a separate cost section below the flight items within the option.

---

## Adding a Custom Cost

You can add your own cost items to any flight or option:

1. Expand the cost breakdown on a flight item or option
2. Click **Add Cost**
3. Enter:
   - **Name** — A description (e.g. "Handling Fee", "De-icing")
   - **Amount** — The cost in cents
4. Click **Save**

The new cost is immediately included in the flight and option totals.

{% hint style="info" %}
Custom costs you add are marked differently from system-generated costs. You can edit or delete custom costs at any time. System-generated costs can be toggled off but not deleted.
{% endhint %}

---

## Editing a Cost Amount

1. Expand the cost breakdown
2. Click the amount field on any cost item
3. Enter the new amount
4. The total recalculates automatically

{% hint style="warning" %}
Editing a system-generated cost (like landing charges) will override the calculated value. If you recalculate the flight, the system value will be restored.
{% endhint %}

---

## Toggling Costs On or Off

Each cost item has a toggle to include or exclude it from the total:

1. Expand the cost breakdown
2. Click the toggle next to any cost item
3. The flight and option totals update immediately

This is useful when you want to:
- Temporarily exclude a cost for a special quote
- See the impact of individual costs on the total
- Keep a cost on record without including it in the price

---

## Ground Time Charges

Ground time charges represent the cost of the aircraft waiting on the ground between flights. These appear as separate rows in the itinerary between consecutive flights.

### How Ground Time is Calculated

1. AeroQuote calculates the time gap between one flight's arrival and the next flight's departure
2. The ground time hourly rate is looked up from the aircraft's sector charges
3. The charge is calculated: **hourly rate x (ground time minutes / 60)**

### Setting Up Ground Time Rates

To configure ground time charging for an aircraft:

1. Go to **Aircraft** from the sidebar
2. Click on an aircraft
3. Navigate to the **Costings** tab
4. Add a **Ground Time** sector charge with an hourly rate

{% hint style="info" %}
If no ground time rate is configured for an aircraft, no ground time charges will appear.
{% endhint %}

---

## Cost Summary View (Operators)

The **Summary** step of the quote builder shows a complete cost breakdown for each option:

- Option-level costs (day charges, overnight charges, custom charges)
- Per-flight cost breakdowns with all line items
- Ground time charges between flights
- Total cost per option

This gives you a clear picture of where costs come from before setting your price.

---

## Costs in Bookings

When a quote is converted to a booking, all cost items are automatically copied:

- Flight cost items carry over to the booking flight items
- The same cost breakdown is available on the booking side
- You can view costs on the booking for reference

---

## Tips

{% hint style="success" %}
**Use the cost breakdown to verify quotes** — Before sending a quote to a customer, expand the costs on each flight to make sure landing charges, fuel, and other costs look correct.
{% endhint %}

- Add custom costs for items not automatically calculated (handling fees, permits, catering)
- Toggle off costs you've negotiated away rather than deleting them — you'll have a record if you need to add them back
- Check ground time charges on multi-leg trips to make sure the wait time costs are reasonable
- The option total always reflects only the costs that are toggled "on"
