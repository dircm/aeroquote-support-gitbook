---
description: Create requests, get instant estimates, and generate quotes for charter flights.
---

# Creating a Request (Operators)

Requests are the starting point for every job. Use the Request page to record inbound charter enquiries, get instant cost estimates across your fleet, and generate quotes — all in one step.

Looking for the Broker edition? [Find it here](creating-a-request-brokers.md).

{% embed url="https://vimeo.com/825790504" %}
Create a Request training video
{% endembed %}

---

## Opening the Request Page

1. Click **Requests** in the sidebar
2. Click **Add new Request**

To edit an existing request, click on it from the request list.

---

## Step 1: Enter Request Details

The left panel captures the basic information for the enquiry.

### Status

Set the request status:

| Status | Meaning |
|--------|---------|
| **Active** | Currently being worked on |
| **Not Interested** | Customer declined or no longer needed |
| **Callback** | Follow up with the customer later |

{% hint style="info" %}
Once a quote has been generated from a request, the status is automatically set to **Quote Generated** and a link to the quote is shown instead of the status dropdown.
{% endhint %}

### Passenger Count

Enter the total number of passengers. This is used for:

- Aircraft capacity validation (warnings shown if exceeded)
- Per-passenger cost calculations
- Airport fee estimates

### Contact

Search for an existing contact by name or email, or create a new one directly from the request page.

The selected contact's email and phone number are displayed below the search field. When a quote is generated, this contact is automatically linked to it.

### Job Notes

Add any special requirements, timing details, or customer instructions. These notes are:

- Saved with the request
- Included in RFQ emails sent to external operators
- Carried through to the quote as operator notes

### Terms & Conditions

Select a Terms & Conditions template from your saved templates. This will be applied to the quote when generated.

---

## Step 2: Add Flight Legs

The flights section is where you build the itinerary. A map on the right updates in real time as you add legs.

### Adding a Charter Flight

1. **Search for the departure airport** — type an ICAO code, IATA code, or airport name
2. **Search for the arrival airport** — same search
3. **Set the departure date and time** — shown in the departure airport's local timezone
4. Click **Add Flight** to add another leg after the current one

{% hint style="info" %}
When adding subsequent flights, the departure date automatically defaults to the next day at 8:00am local time.
{% endhint %}

### Adding a Return Flight

Click **Add Return Flight** to add a leg with the departure and arrival reversed from the previous flight. This creates a charter leg (not a ferry).

### Loading from the Route Library

Click **Load Route** to search your saved routes. Selecting a route pre-fills the departure and arrival airports, and optionally the duration if a custom duration is configured for the aircraft.

### Selecting an FBO / Facility

If an airport has FBOs (Fixed Base Operators) on file, you can select one for departure or arrival:

1. Click the facility selector on the flight leg
2. Choose from available FBOs — each shows name, contact details, and website
3. The selected FBO is shown on the flight leg

### Ferry Legs

AeroQuote **automatically calculates ferry legs** between charter flights when the aircraft needs to reposition. Ferry legs appear in the cost breakdown for each aircraft and are factored into the total price and flight time.

- Ferry legs are shown with a **Ferry** badge in the flight breakdown
- You can **remove individual ferry legs** from an aircraft's estimate if they are not needed
- Check **Return to base before next flight** to add a return ferry between legs

### Managing Flights

- **Reorder** flights by dragging them
- **Delete** a flight by clicking the delete button on that leg

---

## Step 3: Review Estimates

Once you have at least one complete flight (departure, arrival, and date), AeroQuote automatically calculates cost estimates for every aircraft in your fleet. The aircraft table shows:

| Column | Description |
|--------|-------------|
| **Aircraft** | Tail number/name with thumbnail image |
| **Operator** | Shown for external aircraft |
| **Availability** | Green if available, warnings if conflicts exist |
| **Operational** | Warnings for range, runway, or capacity issues |
| **Price** | Estimated total price |
| **Charter Time** | Total charter flight duration |
| **Ferry Time** | Total ferry/repositioning duration |
| **Flights** | Number of flight legs |

### Expanding the Flight Breakdown

Click on an aircraft row to expand the per-flight cost breakdown. Each flight shows:

- **Flight type** — Charter or Ferry badge
- **Route** — departure and arrival ICAO codes
- **Departure time** — local and UTC
- **Duration** — estimated flight time
- **Cost items** — itemised costs (landing charges, fuel uplift, parking, etc.) with toggles to include or exclude individual costs from the total

### Search and Filter

Use the search field above the aircraft table to filter by aircraft registration, name, or operator.

---

## Step 4: Review Cautions

AeroQuote flags potential issues with coloured badges on each aircraft row.

### Availability Warnings

- **Yellow** — Aircraft has an overlapping quote for the same period
- **Red** — Aircraft has an overlapping booking

Hover over the badge to see which quotes or bookings conflict.

### Operational Warnings

- **Passenger capacity** — Passenger count exceeds the aircraft's maximum
- **Runway length** — Departure or arrival runway is too short for the aircraft
- **Aircraft range** — Flight distance exceeds the aircraft's maximum range
- **iFlightPlanner warnings** — Routing issues from advanced flight planning calculations

Hover over the badge for details.

{% hint style="warning" %}
Operational warnings are advisory — they do not prevent you from selecting the aircraft, but should be reviewed before generating a quote.
{% endhint %}

---

## Step 5: Select Aircraft

Check the aircraft you want to include in the quote. Each selected aircraft becomes an option on the generated quote.

### External Aircraft and RFQ

If you select aircraft belonging to an external operator, a **Create RFQ** toggle appears. When enabled:

1. Before the quote is generated, a modal asks you to review the RFQ notes
2. An email is sent to each external operator with the flight details and your notes
3. A Request for Quote record is created to track responses

---

## Step 6: Save or Generate Quote

Two actions are available at the bottom of the page:

### Save Request

Saves the request without generating a quote. Use this when:

- You're still waiting for customer confirmation
- You want to come back to it later
- You need more information before quoting

The request stays in **Active** status and can be edited at any time.

### Generate Quote

Creates a quote with the selected aircraft as options. This:

1. Creates a Quote record with all flights, costs, and selected aircraft options
2. Links the contact to the quote
3. Updates the request status to **Quote Generated**
4. Redirects you to the Quote Builder to finalise and send

{% hint style="info" %}
The **Generate Quote** button is disabled until you have at least one flight and one aircraft selected.
{% endhint %}

---

## Tips

- Use the **Route Library** for frequently flown routes to speed up data entry
- Review **availability warnings** to avoid double-booking aircraft
- Add **job notes** with customer requirements — they carry through to the quote and RFQ emails
- For multi-leg charters, add all legs before selecting aircraft so estimates include the full trip
- You can **copy an existing request** to create a new one with the same flights and notes pre-filled

---

## Next Steps

- [Create a Quote from a Request](../quotes/create-a-quote-from-a-request-operators.md) — Generate and send a quote
- [Custom Routes & Route Library](../custom-items/custom-routes-and-route-library.md) — Set up reusable routes
