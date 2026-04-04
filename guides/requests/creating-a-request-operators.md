---
description: Step-by-step guide to creating a Request for Operators.
---

# Creating a Request (Operators)

Requests are the first step in your quoting workflow. Use them to record inbound charter enquiries, get instant price estimates across your fleet, and generate quotes with a single click.

{% embed url="https://vimeo.com/825790504" %}
Create a Request training video
{% endembed %}

---

## Opening a New Request

1. Click **Requests** in the sidebar
2. Click **Add new Request**

The Request page opens as a single workspace — details, flights, and aircraft estimates are all visible on one screen.

---

## Request Details

The top-left section captures the basic enquiry information:

### Status

Set the request status:

| Status | Meaning |
|--------|---------|
| **Active** | Currently being worked on |
| **Not Interested** | Customer declined or not proceeding |
| **Call Back** | Follow up required |

Once a quote has been generated from the request, the status shows **Quote Already Created** with a link to the quote.

### Total Passengers

Enter the expected number of passengers. This is used to:
- Check aircraft capacity — the estimates table flags aircraft that can't accommodate this number
- Calculate weight-related costs

### Contact

Search for an existing contact by name or email. If the contact doesn't exist, you can create one inline without leaving the page.

The contact carries through when you generate a quote — they become the main contact on the quote.

### Job Notes

Internal notes for your team. These notes carry through to the quote when generated.

### Terms & Conditions Template

Select a T&C template from your saved templates, or leave as **Use Default Template**. This determines which terms are shown to the customer on the online quote view.

---

## Interactive Map

The right side of the details section shows an interactive map that updates in real time as you add flights. It displays your complete route with all departure and arrival points.

---

## Flights

The flights section sits below the details area. Add one or more charter flight legs to define the itinerary.

### Adding a Flight

For each flight leg, enter:

| Field | Required | Description |
|-------|----------|-------------|
| **Departure Location** | Yes | Search by airport name, city, or ICAO/IATA code |
| **Arrival Location** | Yes | Search by airport name, city, or ICAO/IATA code |
| **Departing At** | Yes | Date and time in the departure airport's timezone |

When you select a departure airport, the time defaults to 8:00 AM the next day in that airport's local timezone.

### Selecting an FBO

If an airport has FBO facilities on file, a **Choose Facility** link appears below the airport field. Click it to open a facility picker showing available FBOs with images and map locations.

If an FBO is already selected, its name appears with an **FBO** badge — click to change it.

### Route Library

Click **Load Route** to search your saved routes by name. Selecting a route auto-fills the departure and arrival airports. The route displays as a read-only field showing the route name and ICAO codes.

### Custom Airports

If an airport isn't in the database, type its name and select the option to create a custom airport. The new airport is saved for future use.

### Multi-Leg Itineraries

- **Add Flight** — Adds a new flight leg after the current one
- **Add Return Flight** — Creates a return leg with the departure and arrival airports swapped
- **Load Route** — Search and load a pre-saved route
- **Delete** — Remove a flight leg (click the trash icon)
- **Drag to reorder** — Rearrange flight legs by dragging

---

## Aircraft Estimates

Once all flights have departure and arrival locations, AeroQuote automatically calculates price estimates for every active aircraft in your fleet. The estimates table shows:

| Column | Description |
|--------|-------------|
| **Aircraft** | Image, registration, and type. Click to select. |
| **Cautions** | Availability and operational warnings (see below) |
| **Customer Price** | Estimated charter price |
| **Charter Time** | Total flying time for charter legs |
| **Ferry Time** | Positioning time to/from homebase |
| **Flights** | Number of flight legs |

{% hint style="info" %}
**Estimates recalculate automatically** whenever you change a flight, add a leg, or update the passenger count. There's no need to manually trigger a recalculation.
{% endhint %}

### Selecting Aircraft

Click an aircraft image to select it — a checkmark overlay appears. You can select multiple aircraft. Selected aircraft become options on the quote when you click **Generate Quote**.

### Availability and Operational Cautions

Each aircraft shows caution badges:

**Availability cautions:**
- **Red** — Aircraft is already scheduled in an accepted quote during this period
- **Amber** — Aircraft is booked in a confirmed booking during this period
- **Green** — No scheduling conflicts

**Operational cautions:**
- **Red** — Aircraft cannot complete the mission (runway too short, passenger count exceeds capacity)
- **Amber** — Flight distance may exceed aircraft range
- **Green** — No operational issues

Click a caution badge to see the specific details.

### Expandable Flight Details

Click the flights count row to expand the cost breakdown for each aircraft. This shows:

- Each flight leg (Charter or Ferry) with departure and arrival airports
- Duration per leg
- Total cost breakdown
- Individual cost line items that can be toggled on/off, edited, or added to

### External Aircraft

If your fleet includes aircraft from external operators, they appear in the table with an external operator badge. You can toggle **Create RFQ** per external aircraft to send a Request for Quote to the external operator.

---

## Saving and Generating

Floating action buttons appear in the bottom-right corner:

### Save Request

Click **Save Request** to save the current state of the request — flights, aircraft selections, notes, and contact. You can return to it later and continue working.

### Generate Quote

Once you've selected at least one aircraft, click **Generate Quote** to create a formal quote. This:

1. Creates a new quote with the contact, flights, and notes from the request
2. Adds each selected aircraft as a separate option on the quote
3. Carries over all cost estimates and flight details
4. Opens the new quote's detail page automatically
5. Updates the request status to **Quote Already Created**

{% hint style="success" %}
**Generating a quote doesn't delete the request.** The request remains linked to the quote — you can always navigate back to it from the quote.
{% endhint %}

### Send Emails and Edit Quote

If you've selected external aircraft with RFQ enabled, an additional option appears to **Send Emails and Edit Quote**. This sends Request for Quote emails to external operators and generates the quote in one step. You can review and edit the notes that will be included in the emails before sending.

---

## Duplicating a Request

You can create a new request based on an existing one. This copies the flights, notes, and passenger count — useful for repeat enquiries or similar routes.

---

## Tips

{% hint style="info" %}
**Requests are for speed.** Unlike the Quote Builder (which walks through steps), the Request page shows everything at once so you can get estimates in seconds. Use Requests for initial pricing, then generate a quote when you're ready to send to the customer.
{% endhint %}

- Enter flights first — aircraft estimates calculate automatically once departure and arrival airports are set
- Use the Route Library for repeat routes to save time
- Check caution badges before selecting aircraft — resolve conflicts early
- Save frequently if you're working on a complex multi-leg itinerary
- The contact and notes carry through to the quote, so fill them in on the request to save time later
