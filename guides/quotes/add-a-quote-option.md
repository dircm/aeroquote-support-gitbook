---
description: >-
  Add another aircraft option on a quote, optionally auto-generate flight legs
  from existing charter legs, and delete a middle leg with optional route stitch.
---

# Add a Quote Option

On an open quote’s **Options** (or **Flight**) step you can add more aircraft options for the customer to compare, without rebuilding the whole quote from a Request.

{% hint style="info" %}
**Add Option** sits in the **top-left** of the Options step toolbar — same row as **Admin View** / **Customer View**. It is only shown in **Admin View**.
{% endhint %}

## Prerequisites

* An open quote (draft or editable)
* You are on the **Options** step (tab may show as **Flight** when there is only one option)
* To auto-generate legs, the new option needs an **aircraft**, and at least one **other** option on the quote must already have **charter** flight legs

***

## Step 1: Open Options

1. Open the quote from **Quotes** or the Dashboard
2. Click the **Options** (or **Flight**) tab
3. Stay in **Admin View** (not Customer View)

## Step 2: Add Option

1. Click **Add Option** (top-left, next to the Admin / Customer view toggle)
2. In **Option Settings**, select an **Aircraft** (search by registration or name)
3. Optionally set **Title**, notes, margin, price, banner, and payload
4. Click **Save**

AeroQuote creates the new option and attaches it to the quote.

***

## Auto-generate flight legs from existing charter legs

If **another option on the same quote already has charter legs**, and you selected an **aircraft** on the new option, AeroQuote asks whether to build a full estimated itinerary for the new aircraft from those charter legs.

### The prompt

After **Save**, a notification appears:

**Generate flight legs**

> Other options on this quote already include charter legs. Auto-generate a full estimated itinerary for this option (including ferry legs and costs for the selected aircraft) from those charter legs?

| Action | What happens |
| --- | --- |
| **Generate legs** | Builds an estimated itinerary for the **new** aircraft from the other option’s **charter** route (same approach as when aircraft are estimated on a Request / Quote Builder) |
| **Skip** | Keeps the new option **empty** of legs — you can add flights manually with **Add Flight Item** |

### What “Generate legs” creates

* **Charter** legs matching the **departure → arrival** sequence of charter legs already on the source option
* **Ferry / positioning** legs when the new aircraft’s homebase is not already at the next charter departure (and similarly for return to base where the estimator includes them)
* **Durations, costs, and day/overnight** figures recalculated for the **selected** aircraft
* Planned fuel burn on legs when the aircraft uses advanced performance planning (internal only)

{% hint style="info" %}
**Source option:** When more than one other option has charter legs, AeroQuote uses the **first option on the quote (by order)** that has charter legs. Perfect multi-option merge is not required for typical “add another aircraft on the same trip” workflows.
{% endhint %}

### When the prompt does **not** appear

* The new option was saved **without** an aircraft
* No other option on the quote has charter flight legs yet
* You are only **editing** an existing option (not creating a new one)

In those cases, create the option as usual, then use **Add Flight Item** or change aircraft after flights exist.

***

## Delete a flight leg (and optional route stitch)

On the Options itinerary you can remove a single flight leg from an option.

### Delete without neighbours

1. Click **Edit** on the flight item (pencil / edit control on the leg card)
2. Click **Delete** on **Flight Leg Settings**
3. The leg is removed immediately

This applies when the leg is the **only** flight, or the **first** or **last** flight in the option (no previous *and* next flight neighbour).

### Delete a middle leg — update previous destination?

If the leg sits **between** two other flights (there is a previous flight and a next flight), AeroQuote asks how to keep the route continuous:

**Update previous destination?**

> This flight sits between two other legs. Update the previous flight’s destination to the next flight’s departure airport (and recalculate that leg’s costs/times), or delete this leg only?

| Action | What happens |
| --- | --- |
| **Update previous destination** | Deletes the middle leg, then sets the **previous** leg’s **arrival** to the **next** leg’s **departure** airport, and recalculates duration and costs for that previous leg |
| **Delete only** | Deletes the middle leg and leaves neighbouring airports unchanged |

**Example:** Legs are `X → A`, `A → B`, `B → Y`. Deleting the middle leg with **Update previous destination** leaves `X → B` and `B → Y`.

{% hint style="warning" %}
After a delete (with or without stitch), AeroQuote may also offer to **adjust onward flight times** if parking gaps would otherwise overlap. That schedule bump is a separate confirmation — you can apply or keep current times.
{% endhint %}

***

## Related

* [Add a stop between two airports](add-a-stop-between-two-airports.md) — insert a via airport on an existing leg
* [Edit the Price of a Quote option](edit-the-price-of-a-quote.md) — margin and price after costs change
* [Cost Management](cost-management.md) — per-leg cost breakdown
* [Creating a Quote from scratch](creating-a-quote.md) — Quote Builder before the quote exists
* [Quote Details Page](quote-details-page/) — tabs including Options
