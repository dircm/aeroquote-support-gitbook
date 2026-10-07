---
description: Step-by-step guide to creating a flight using the flight builder.
---

# Creating a Flight

The flight builder walks you through creating a flight — type, details, itinerary, aircraft, passengers, cargo, and crew. You can also create flights directly from accepted quotes.

***

## Opening the flight builder

**From the Flights page** — Click the **Create Flight** button in the top right

***

## Step 1: Type

Choose the kind of flying this record is for:

| Type | When to use it |
| ---- | -------------- |
| **Charter** | Customer flying. Contact and customer notes are required. |
| **Repositioning** | Moving the aircraft with no charter customer. |
| **Maintenance** | A maintenance or engineering flight. |
| **Training** | A training flight. |

Charter is the default. Repositioning, maintenance, and training hide contact and customer notes so the record stays operational. More types (private, other) are coming so all of your flying can live in this list.

Click **Next** to continue.

***

## Step 2: Flight Details

Set the customer and any notes. Charter requires a contact before you can continue.

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

***

## Step 3: Flights

Build the flight itinerary by adding one or more flight legs.

### Adding a Flight

For each flight leg, enter:

| Field                     | Required | Description                                       |
| ------------------------- | -------- | ------------------------------------------------- |
| **Departure airport**     | Yes      | Search by airport name, city, or ICAO/IATA code   |
| **Arrival airport**       | Yes      | Search by airport name, city, or ICAO/IATA code   |
| **Departure date & time** | Yes      | Date and time in the departure airport's timezone |

When you select an airport, the departure time defaults to 8:00 AM the next day in that airport's timezone.

### Selecting an FBO

If an airport has FBO facilities on file, a facility selector appears after selecting the airport. Choose the appropriate FBO for departure or arrival — this information carries through to the booking and any customer communications.

### Route Library

Click **Load Route** to search your saved routes. Selecting a route auto-fills the departure and arrival airports, saving time on frequently flown routes.

### Multi-Leg Itineraries

* **Add Flight** — Adds a new flight leg after the current one
* **Add Return Flight** — Creates a return leg with the departure and arrival airports swapped
* **Delete** — Removes a flight leg

The interactive map updates as you add flights, showing your complete route.

### Repositioning (ferry) flights toggle

On the **Flights** step:

**Automatically add repositioning (ferry) flights for Aircraft with a homebase**

| Toggle | What estimates include |
| --- | --- |
| **On** (default) | Classic behaviour — homebase positioning ferries when the route does not start and/or end at homebase |
| **Off** | Only the charter legs you entered |

Changing the toggle recalculates estimates for aircraft you have added.

Click **Next** to continue.

***

## Step 4: Aircraft

Add one or more aircraft for this booking. Estimates run only for aircraft you add — not the full fleet automatically.

### Adding aircraft

1. With an empty list, click **+ Add Aircraft to see estimates**
2. In the modal, choose aircraft by thumbnail and details (already-added aircraft are excluded)
3. Use **+ Add Aircraft** or **+ Add more Aircraft** when more of the fleet is still available
4. Remove an aircraft from the list if it should not be on the booking

### Estimate columns

For each **added** aircraft, the builder shows estimates based on the flights you entered:

| Column           | Description                                       |
| ---------------- | ------------------------------------------------- |
| **Aircraft**     | Registration, type, and image                     |
| **Price**        | Estimated charter price                           |
| **Charter Time** | Total flying time for all legs                    |
| **Ferry Time**   | Positioning time to/from homebase when ferry auto-add is on (if applicable) |
| **Fuel**         | Planned fuel burn for advanced-performance aircraft (internal only; not on customer views). Unit from Settings → Localization. May show **—** or **est.** — see [Using the Estimator](../requests/using-the-estimator.md) |

You can add multiple aircraft if the booking requires more than one.

After the booking is created, planned burn (when stored) appears next to **duration** on the booking **Itinerary**, on the crew itinerary link, and under duration on the **flight manifest** PDF. It is not shown on customer booking pages.

### Availability and Operational Cautions

The builder checks for potential issues and displays caution indicators:

* **Availability cautions** — The aircraft may have conflicting bookings or maintenance scheduled
* **Operational cautions** — Range limitations, runway requirements, or other operational considerations

{% hint style="warning" %}
Review caution indicators before proceeding. Click on a caution to see the details. Cautions will not stop you from proceeding with the booking generation, they are only for your information.
{% endhint %}

Click **Next** to continue.

***

## Step 5: Passengers, Cargo & Crew

This step is optional — you can add passengers, cargo, and crew now or after the booking is created.

### Passengers

Search for existing contacts to add as passengers, or create new ones inline. Each passenger requires a name and weight for weight and balance calculations.

### Cargo

Add cargo items with a name and weight. You can:

* Search your **cargo presets** for commonly carried items
* Create a custom cargo entry with name, weight, and handling notes

### Crew

Search your staff list to assign air crew (pilots and cabin crew) to the booking.

### Ground Crew

Search your staff list to assign ground crew — staff who support the flight on the ground but are not on the flight manifest.

### Auto-Assignment

If you selected a single aircraft, passengers, cargo, and crew are automatically assigned to all flight legs for that aircraft.

If you selected multiple aircraft, a dropdown appears for each section letting you choose which aircraft to auto-assign to — or select **Don't assign** to handle assignment manually after the booking is created.

Click **Next** to continue.

***

## Step 6: Flight Summary

Review all the details before creating the flight:

* **Contact** — Name, email, and phone
* **Passengers** — Names and weights
* **Cargo** — Names and weights
* **Aircraft** — Selected aircraft with flight leg details, durations, and departure times

{% hint style="success" %}
Use the step indicators at the top to jump back to any previous step if you need to make changes.
{% endhint %}

Click **Create Flight** to finalise. AeroQuote creates the flight, assigns all passengers, cargo, crew, and ground crew, then opens the new flight's detail page.

***

## After Creating a Flight

Once created, you can:

* [Add or edit passengers and cargo](passengers-and-cargo.md) on the Passengers & Cargo tab
* [Assign crew to specific flights](crew-assignment.md) on the Crew tab
* [Send a confirmation](sending-confirmations.md) to the customer from the Send tab
* [Track flight status](booking-status.md) on the Status tab

***

## Tips

{% hint style="info" %}
**Creating from a quote?** [Learn here.](create-a-booking-from-a-quote.md)
{% endhint %}

* Complete the Flights step accurately — aircraft pricing and ferry times are calculated from these details
* You can always add passengers, cargo, and crew after the booking is created if you don't have the details yet
* Use the Route Library for repeat routes to save time
* Select FBOs when known — they appear on customer confirmations and help crew with ground handling coordination
