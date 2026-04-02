---
description: Step-by-step guide to creating a quote using the Quote Builder.
---

# Creating a Quote

The Quote Builder walks you through creating a quote in four steps — from selecting a customer through to choosing aircraft and reviewing pricing. You can also create quotes directly from a Request, which pre-fills the flight details.

---

## Opening the Quote Builder

There are two ways to start:

- **From the Quotes page** — Click the **Create Quote** button in the top right
- **From a Request** — Select one or more aircraft on a Request and click **Generate Quote** (flight details will be pre-filled)

---

## Step 1: Quote Details

Set the customer and basic quote information.

### Contact

Search for an existing contact by name or email. Start typing and select from the dropdown.

{% hint style="info" %}
If the contact doesn't exist yet, you can create one inline without leaving the builder.
{% endhint %}

### Job Notes (optional)

Internal notes for your team. Use these for special instructions, coordination details, or context about the enquiry. These notes are not visible to the customer.

### Total Passengers

Enter the expected number of passengers. This is used to check aircraft capacity — the builder will flag any aircraft that can't accommodate this number.

### Terms & Conditions Template (optional)

Select a T&C template from your saved templates. If left blank, your operator's default template is used. These terms are displayed to the customer when they view the quote online.

Click **Next** to continue.

---

## Step 2: Flights

Build the flight itinerary by adding one or more flight legs.

### Adding a Flight

For each flight leg, enter:

| Field | Required | Description |
|-------|----------|-------------|
| **Departure airport** | Yes | Search by airport name, city, or ICAO/IATA code |
| **Arrival airport** | Yes | Search by airport name, city, or ICAO/IATA code |
| **Departure date & time** | Yes | Date and time in the departure airport's timezone |

When you select an airport, the departure time defaults to 8:00 AM the next day in that airport's local timezone.

### Selecting an FBO

If an airport has FBO facilities on file, a facility selector appears after selecting the airport. Choose the appropriate FBO for departure or arrival — this information appears on the quote sent to the customer.

### Route Library

Click **Load Route** to search your saved routes. Selecting a route auto-fills the departure and arrival airports, saving time on frequently quoted routes.

### Custom Airports

If an airport isn't in the database, you can create it inline from the search dropdown. The new airport is saved for future use.

### Multi-Leg Itineraries

- **Add Flight** — Adds a new flight leg after the current one
- **Add Return Flight** — Creates a return leg with the departure and arrival airports swapped
- **Delete** — Removes a flight leg
- **Drag to reorder** — Rearrange flight legs by dragging them into the correct order

The interactive map updates as you add flights, showing your complete route.

{% hint style="info" %}
**Return to homebase** — Check this box on a flight to automatically include a ferry positioning flight back to the aircraft's homebase in the pricing calculation.
{% endhint %}

Click **Next** to continue.

---

## Step 3: Aircraft

Select one or more aircraft to include as options on the quote. Each selected aircraft becomes a separate option for the customer to choose from.

### Available Aircraft

The builder calculates pricing for every aircraft in your fleet based on the flights you entered:

| Column | Description |
|--------|-------------|
| **Aircraft** | Registration, type, and image |
| **Customer Price** | Estimated price to the customer |
| **Cost to You** | Your estimated operating cost |
| **Charter Time** | Total flying time for charter legs |
| **Ferry Time** | Positioning time to/from homebase |

Click an aircraft to select it. You can select multiple aircraft — each becomes a separate option on the quote.

### Search and Filter

Use the search box to filter aircraft by registration, name, or external operator.

### Availability and Operational Cautions

The builder checks for potential issues and displays caution badges next to each aircraft:

**Availability cautions:**
- **Red** — Aircraft is already scheduled in an accepted quote during the requested period
- **Amber** — Aircraft is booked in a confirmed booking during the requested period
- **Green** — No scheduling conflicts

**Operational cautions:**
- **Red** — Aircraft cannot complete the mission (runway too short, passenger count exceeds capacity)
- **Amber** — Flight distance may exceed aircraft range
- **Green** — No operational issues

{% hint style="warning" %}
Review caution indicators before proceeding. Click on a caution to see the specific details.
{% endhint %}

### Cost Breakdown

Expand any aircraft option to see the full cost breakdown per flight leg:

- **Flight costs** — Fuel, hourly rate, sector charges
- **Landing and handling** — Airport-specific fees
- **Parking and overnight** — Ground time charges for multi-day trips
- **Ferry flights** — Positioning costs (shown separately from charter legs)

You can edit individual cost items — toggle costs on or off, change amounts, or add new line items. This is useful for adjusting estimates before creating the quote.

### External Aircraft and RFQ

If you have aircraft from external operators in your fleet, you can toggle **RFQ** (Request for Quote) per aircraft. This flags the option to send an RFQ to the external operator after the quote is created.

Click **Next** to continue.

---

## Step 4: Quote Summary

Review all the details before creating the quote:

- **Contact** — Name, email, and phone
- **Aircraft options** — Each selected aircraft with:
  - Total customer price and operator cost
  - Flight details table with departure/arrival times in both local and Zulu (UTC)
  - Flight type (Charter or Ferry) and duration per leg

{% hint style="success" %}
Use the step indicators at the top to jump back to any previous step if you need to make changes.
{% endhint %}

Click **Create Quote** to finalise. AeroQuote creates the quote with all selected aircraft as options, assigns the contact, and opens the new quote's detail page.

---

## After Creating a Quote

The quote is created in **Draft** status. From the quote detail page you can:

- Edit pricing, add or remove options, and adjust cost line items — see [Edit the Price of a Quote](edit-the-price-of-a-quote.md)
- Manage individual cost items — see [Cost Management](cost-management.md)
- Send the quote to the customer with your document template attached
- Set a quote validity date — see [Edit Quote Valid Till Date](quote-details-page/edit-quote-valid-till-date.md)
- Require T&C acceptance online — see [Require T&Cs to be Accepted Online](require-t-and-cs-to-be-accepted-online.md)

Once the customer accepts, you can [convert the quote to a booking](../bookings-operators/create-a-booking-from-a-quote.md).

---

## Tips

{% hint style="info" %}
**Creating from a Request?** The builder pre-fills flights and may pre-select aircraft from the Request. Review and adjust as needed — this is the fastest way to generate quotes.
{% endhint %}

- Complete the Flights step accurately — aircraft pricing, ferry times, and cautions are all calculated from these details
- Use the Route Library for repeat routes to save time and ensure consistency
- Select multiple aircraft to give your customer options — each becomes a separate option they can compare
- Check caution badges before finalising — availability conflicts and operational issues are easier to resolve before sending the quote
- Use the cost breakdown editor to fine-tune estimates on the Aircraft step rather than editing after creation
