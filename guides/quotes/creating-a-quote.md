---
description: Step-by-step guide to creating a quote using the Quote Builder.
---

# Creating a Quote from scratch

The Quote Builder walks you through creating a quote in four steps — from selecting a customer through to choosing aircraft and reviewing pricing. You can also create quotes directly from a Request, which pre-fills the flight details.

***

## Opening the Quote Builder

**From the Quotes page** — Click the **Create Quote** button in the top right

***

## Step 1: Quote Details

Set the customer and basic quote information.

### Contact (optional)

Search by name or email using **Add contact (search name or email)**. Start typing and select from the dropdown.

{% hint style="info" %}
If the contact doesn't exist yet, you can create one inline without leaving the builder. You can also leave contact blank and add main contacts later on the quote **Quote Details** step.
{% endhint %}

### Job Notes (optional)

Internal notes for your team. Use these for special instructions, coordination details, or context about the enquiry. These notes are not visible to the customer.

### Total Passengers (optional)

Enter the expected number of passengers. This is used to check aircraft capacity — the builder will flag any aircraft that can't accommodate this number.

### Terms & Conditions Template (optional)

Select a T\&C template from your saved templates. If you leave **Use Default Template**, your operator's default template is used. These terms are displayed to the customer when they view the quote online.

Click **Next** to continue.

***

## Step 2: Flights

Build the flight itinerary by adding one or more flight legs.

### No date yet (TBC)

If the customer only wants a price, tick **Customer just wants a price — no travel date yet (TBC)**. Dates are hidden from the customer (shown as TBD). You can set a real date later from the quote.

### Adding a Flight

For each flight leg, enter:

| Field | Required | Description |
| --- | --- | --- |
| **Departure Location** | Yes | Search by airport name, city, or ICAO/IATA code |
| **Arrival Location** | Yes | Search by airport name, city, or ICAO/IATA code |
| **Departure date & time** | Yes\* | Rough date and time in the departure location's timezone (\*not required when TBC is on) |

When you select a location, the departure time defaults to 8:00 AM the next day in that airport's local timezone.

### Selecting an FBO

If a location has FBO facilities on file, use **Choose Facility** (or the FBO link) after selecting the airport. Choose the appropriate FBO for departure or arrival — this information can appear on the quote sent to the customer.

### Route Library

Click **Load Route** to search your saved routes. Selecting a route auto-fills the departure and arrival locations, saving time on frequently quoted routes.

### Custom Airports

If an airport isn't in the database, you can create it inline from the search dropdown. The new airport is saved for future use.

### Multi-Leg Itineraries

* **Add Flight** — Adds a new flight leg after the current one
* **Add Return Flight** — Creates a return leg with the departure and arrival locations swapped
* **Delete** — Removes a flight leg
* **Drag to reorder** — Rearrange flight legs by dragging them into the correct order

The interactive map updates as you add flights, showing your complete route.

{% hint style="info" %}
**Return to base before next flight** — Check this box on a flight to include a ferry positioning flight back to the aircraft's homebase before the next leg in the pricing calculation.
{% endhint %}

Click **Next** to continue.

***

## Step 3: Aircraft

Add one or more aircraft to estimate and include as options on the quote. Each added aircraft becomes a separate option for the customer to choose from. AeroQuote does **not** estimate the full fleet until you add aircraft.

### Adding aircraft

1. With an empty list, click **+ Add Aircraft to see estimates**
2. In the **Add Aircraft** modal, pick aircraft by thumbnail and details (already-added aircraft are hidden)
3. Use **+ Add Aircraft** in the header or **+ Add more Aircraft** under the list when more of the fleet remains
4. Remove an aircraft from the list when you no longer want it estimated or quoted

### Estimate columns

For each **added** aircraft, the builder calculates pricing from the flights you entered:

| Column | Description |
| --- | --- |
| **Name** | Registration / tail and image |
| **Customer Price estimate** | Estimated price to the customer |
| **Cost to you estimate** | Your estimated operating cost |
| **Charter Time** | Total flying time for charter legs |
| **Ferry Time** | Total positioning time to/from homebase |
| **Fuel** | Planned fuel burn for advanced-performance aircraft (internal only; not on customer views/PDFs). Unit from Settings → Localization. May show **—** or **est.** — see [Using the Estimator](../requests/using-the-estimator.md) |

### Search in the add modal

Use **Search aircraft** in the add-aircraft modal to filter by registration, name, or external operator.

### Availability and Operational Cautions

The builder checks for potential issues and displays caution badges next to each aircraft:

**Availability cautions:**

* **Red** — Aircraft is already scheduled in an accepted quote during the requested period
* **Amber** — Aircraft is booked in a confirmed booking during the requested period
* **Green** — No scheduling conflicts

**Operational cautions:**

* **Red** — Aircraft cannot complete the mission (runway too short, passenger count exceeds capacity)
* **Amber** — Flight distance may exceed aircraft range
* **Green** — No operational issues

{% hint style="warning" %}
Review caution indicators before proceeding. Click on a caution to see the specific details.  Cautions will not stop you from proceeding with the quote generation, they are only for your information.
{% endhint %}

### Cost Breakdown

Expand any aircraft option to see the full cost breakdown per flight leg:

* **Flight costs** — Fuel, hourly rate, sector charges
* **Landing and handling** — Airport-specific fees
* **Parking and overnight** — Ground time charges for multi-day trips
* **Ferry flights** — Positioning costs (shown separately from charter legs)

You can edit individual cost items — toggle costs on or off, change amounts, or add new line items. This is useful for adjusting estimates before creating the quote.

### External Aircraft and RFQ

If you have aircraft from external operators in your fleet, you can toggle **RFQ** (Request for Quote) per aircraft. This flags the option to send an RFQ to the external operator after the quote is created.

Click **Next** to continue.

***

## Step 4: Quote Summary

Review all the details before creating the quote:

* **Contact** — Name, email, and phone
* **Aircraft options** — Each selected aircraft with:
  * Total customer price and operator cost
  * Flight details table with departure/arrival times in both local and Zulu (UTC)
  * Flight type (Charter or Ferry) and duration per leg

{% hint style="success" %}
Use the step indicators at the top to jump back to any previous step if you need to make changes.
{% endhint %}

Click **Create Quote** to finalise. AeroQuote creates the quote with all selected aircraft as options, assigns the contact, and opens the new quote's detail page.

***

## After Creating a Quote

The quote is created in **Draft** status and opens on the **Quote Details** step. From there you can:

* Move between **Quote Details**, **Options** / **Flight**, **Documents**, and **Send** using the top tabs — see [Quote Details Page](quote-details-page/)
* Edit pricing, add or remove options, and adjust cost line items — see [Edit the Price of a Quote](edit-the-price-of-a-quote.md)
* Manage individual cost items — see [Cost Management](cost-management.md)
* Preview or download a printable itinerary — see [View or print the full quote itinerary](view-or-print-quote-itinerary.md)
* Send the quote to the customer with your document template attached
* Set a quote validity date — see [Edit Quote Valid Till Date](quote-details-page/edit-quote-valid-till-date.md)
* Require T\&C acceptance online — see [Require T\&Cs to be Accepted Online](require-t-and-cs-to-be-accepted-online.md)

Once the customer accepts, you can [convert the quote to a booking](../bookings-operators/create-a-booking-from-a-quote.md).

***

## Tips

{% hint style="info" %}
**Creating from a Request?** [Learn here.](create-a-quote-from-a-request-operators.md)
{% endhint %}

* Complete the Flights step accurately — aircraft pricing, ferry times, and cautions are calculated from these details for the aircraft you add
* Use the Route Library for repeat routes to save time and ensure consistency
* Add multiple aircraft to give your customer options — each becomes a separate option they can compare
* Check caution badges before finalising — availability conflicts and operational issues are easier to resolve before sending the quote
* Use the cost breakdown editor to fine-tune estimates on the Aircraft step rather than editing after creation
