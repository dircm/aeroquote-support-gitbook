---
description: Step-by-step guide to creating a booking using the Booking Builder.
---

# Creating a Booking

The Booking Builder walks you through creating a booking in five steps — from selecting a customer through to assigning passengers, cargo, and crew. You can also create bookings directly from accepted quotes.

---

## Opening the Booking Builder

There are two ways to start:

- **From the Bookings page** — Click the **Create Booking** button in the top right
- **From a Quote** — Click the **Generate a Booking** button on any accepted quote's detail page (flight and aircraft details will be pre-filled)

---

## Step 1: Booking Details

Set the customer and any notes for the booking.

### Contact

Search for an existing contact by name or email. Start typing and select from the dropdown.

{% hint style="info" %}
If the contact doesn't exist yet, you can create one inline without leaving the builder.
{% endhint %}

### Internal Notes (optional)

Notes visible only to your team. Use these for operational reminders, special instructions, or coordination details.

### Customer Notes (optional)

Notes that will be visible to the customer on confirmations and the online booking view. Your operator's default notes are pre-filled here — edit or remove as needed.

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

When you select an airport, the departure time defaults to 8:00 AM the next day in that airport's timezone.

### Selecting an FBO

If an airport has FBO facilities on file, a facility selector appears after selecting the airport. Choose the appropriate FBO for departure or arrival — this information carries through to the booking and any customer communications.

### Route Library

Click **Load Route** to search your saved routes. Selecting a route auto-fills the departure and arrival airports, saving time on frequently flown routes.

### Multi-Leg Itineraries

- **Add Flight** — Adds a new flight leg after the current one
- **Add Return Flight** — Creates a return leg with the departure and arrival airports swapped
- **Delete** — Removes a flight leg

The interactive map updates as you add flights, showing your complete route.

Click **Next** to continue.

---

## Step 3: Aircraft

Select one or more aircraft for this booking.

### Available Aircraft

The builder displays your fleet with calculated estimates based on the flights you entered:

| Column | Description |
|--------|-------------|
| **Aircraft** | Registration, type, and image |
| **Price** | Estimated charter price |
| **Charter Time** | Total flying time for all legs |
| **Ferry Time** | Positioning time to/from homebase (if applicable) |

Click an aircraft to select it. You can select multiple aircraft if the booking requires more than one.

### Availability and Operational Cautions

The builder checks for potential issues and displays caution indicators:

- **Availability cautions** — The aircraft may have conflicting bookings or maintenance scheduled
- **Operational cautions** — Range limitations, runway requirements, or other operational considerations

{% hint style="warning" %}
Review caution indicators before proceeding. Click on a caution to see the details.
{% endhint %}

Click **Next** to continue.

---

## Step 4: Passengers, Cargo & Crew

This step is optional — you can add passengers, cargo, and crew now or after the booking is created.

### Passengers

Search for existing contacts to add as passengers, or create new ones inline. Each passenger requires a name and weight for weight and balance calculations.

### Cargo

Add cargo items with a name and weight. You can:

- Search your **cargo presets** for commonly carried items
- Create a custom cargo entry with name, weight, and handling notes

### Crew

Search your staff list to assign air crew (pilots and cabin crew) to the booking.

### Ground Crew

Search your staff list to assign ground crew — staff who support the flight on the ground but are not on the flight manifest.

### Auto-Assignment

If you selected a single aircraft, passengers, cargo, and crew are automatically assigned to all flight legs for that aircraft.

If you selected multiple aircraft, a dropdown appears for each section letting you choose which aircraft to auto-assign to — or select **Don't assign** to handle assignment manually after the booking is created.

Click **Next** to continue.

---

## Step 5: Booking Summary

Review all the details before creating the booking:

- **Contact** — Name, email, and phone
- **Passengers** — Names and weights
- **Cargo** — Names and weights
- **Aircraft** — Selected aircraft with flight leg details, durations, and departure times

{% hint style="success" %}
Use the step indicators at the top to jump back to any previous step if you need to make changes.
{% endhint %}

Click **Create Booking** to finalise. AeroQuote creates the booking, assigns all passengers, cargo, crew, and ground crew, then opens the new booking's detail page.

---

## After Creating a Booking

Once created, you can:

- [Add or edit passengers and cargo](passengers-and-cargo.md) on the Passengers & Cargo tab
- [Assign crew to specific flights](crew-assignment.md) on the Crew tab
- [Send a confirmation](sending-confirmations.md) to the customer from the Send tab
- [Track flight status](booking-status.md) on the Status tab

---

## Tips

{% hint style="info" %}
**Creating from a quote?** The builder pre-fills the contact, flights, and aircraft from the quote. Review and adjust as needed — dates and aircraft selection may need updating if time has passed since the quote was issued.
{% endhint %}

- Complete the Flights step accurately — aircraft pricing and ferry times are calculated from these details
- You can always add passengers, cargo, and crew after the booking is created if you don't have the details yet
- Use the Route Library for repeat routes to save time
- Select FBOs when known — they appear on customer confirmations and help crew with ground handling coordination
