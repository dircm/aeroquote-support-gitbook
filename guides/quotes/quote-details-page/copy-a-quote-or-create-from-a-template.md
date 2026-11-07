---
description: >-
  Re-use a previous quote or a quote template for a repeat trip, and optionally
  reprice the new quote using your current aircraft and airport rates.
---

# Copy a quote or create one from a template

Repeat work, such as the same route every year, doesn't need to be quoted from scratch. You can copy a previous quote, or keep a template for the route, and create a new quote from it in a few clicks.

## Copy to new Quote and Create new Quote

Both buttons open the same window:

* **Copy to new Quote** is in the header of **Quote Details** on any quote.
* **Create new Quote** appears on a quote template ("Create a new Quote from this template").

In the window:

1. Select the date and time of the first **charter** flight for the new quote. All flights move by the same amount, so the itinerary keeps its shape.
2. Choose whether to tick **Reprice using current rates** (see below). It is **off** by default.
3. Click **Create**. The new quote opens on its **Quote Details** step.

The original quote or template is **never changed**. Contacts are not copied.

{% hint style="info" %}
**Save as Template turns the current quote into the template.** To keep a quote you've already sent, click **Copy to new Quote** first, then click **Save as Template** on the copy. Templates are listed under the **Templates** tab of the Quotes list.
{% endhint %}

## Without repricing (default)

The new quote keeps exactly the same costs and prices as the original, with the new dates. This is how copying has always worked. Review and adjust costs yourself before sending.

## With "Reprice using current rates"

Tick the box to recalculate the new quote from the rates currently saved in Aeroquote, for the new dates:

| Recalculated | Kept from the original |
| --- | --- |
| Flight costs, from the aircraft's current hourly or sector charges | Aircraft, airports and facilities |
| Movement (landing) charges | Flight times, including any you changed by hand |
| Parking charges for the new dates | Passenger numbers, routes and notes |
| Day and overnight charges | Fuel uplift and other costs you entered |
| Option cost, price and tax | Cost items you added (counted once) and charges you unticked (they stay unticked) |

{% hint style="warning" %}
"Current rates" means the aircraft charges and airport charge rules **saved in your account today**. Aeroquote doesn't add inflation, and doesn't fetch new tariffs from airports or suppliers. Update your aircraft and airport charges first if they have changed. Flights are **not** re-planned: flight times, weather/wind and fuel prices are not looked up again.
{% endhint %}

### How the price is set

* **Aircraft with a price margin:** price = new cost + that margin.
* **Other aircraft:** the option keeps the same price-to-cost ratio as the original. If cost rises 10%, price rises 10%. The aircraft's minimum customer price still applies.
* **If the original has no usable price** to scale from, the price is left as it was and flagged for you to review.

### What is not repriced

These are kept as they were and listed in a warning so you can check them:

* Options where you **manually overrode the cost**. Their cost and price stay exactly as on the original.
* **Day or overnight charges you overrode** by hand. They are kept and still show as overridden.
* Flights with **fuel uplift costs**. Review fuel pricing.
* Flights on **external (RFQ) aircraft**. These are priced by the other operator.

If a quote can't be repriced safely (for example, an aircraft or airport has been removed), no new quote is created and a message explains why. You can then copy without repricing, or fix the original first.

### Review before sending

After creating a repriced quote, a summary stays on screen until you close it. It shows the cost and price **before → after**, plus any warnings. Check the options, flights and price on the new quote before you send it to your customer.

There's no separate button to reprice an existing quote. Repricing only happens when you create a new quote this way.

## Example: an annual charter on the same route

1. Open last year's quote for the route and click **Copy to new Quote**, keeping the date. On the copy, click **Save as Template** and give it a clear name, such as "Annual charter – Route A to B".
2. When rates change, update your aircraft charges and airport charges.
3. Next year, open the template from the **Templates** tab and click **Create new Quote**.
4. Pick the new first charter date, tick **Reprice using current rates**, and click **Create**.
5. Review the before → after summary and any warnings, adjust if needed, then send.
