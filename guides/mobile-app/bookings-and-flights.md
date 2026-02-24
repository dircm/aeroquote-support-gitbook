# Bookings & Flights

<!-- 📸 PLACEHOLDER: Screenshot of the Bookings list screen with aircraft filter chips visible -->
<!-- Suggested filename: .gitbook/assets/mobile-bookings-list.png -->

## Bookings List

The Bookings screen shows all your active bookings. Each booking card displays:

* **Booking code** and **status badge**
* **Route summary** (e.g. YBBN → YSSY → YBBN)

### Filtering by Aircraft

Use the aircraft filter chips at the top of the list to show only bookings for a specific aircraft. Tap **All** to reset the filter.

### Pull to Refresh

Pull down on the bookings list to manually trigger a data sync from the server.

## Booking Detail

Tap a booking to see its details, including all flight legs. Each flight leg is tappable to open the full **Flight Detail** screen.

## Flight Detail

The Flight Detail screen is the heart of flight operations in the app. It shows everything about a single flight leg:

<!-- 📸 PLACEHOLDER: Screenshot of the Flight Detail screen showing route info, aircraft card, map, and passenger manifest -->
<!-- Suggested filename: .gitbook/assets/mobile-flight-detail.png -->

### Route Information

* Departure and arrival **ICAO codes** and **city names**
* **Local departure time** and **Zulu (UTC) time**
* **Flight duration**
* **FBO / Facility** — If an FBO or facility is assigned, a chip appears under the airport name. Tap it to see facility details and get directions.

### Aircraft Card

Shows the assigned aircraft with its **image**, **registration**, and **type**. If no image is available, a placeholder icon is shown.

### Route Map

A static map showing the flight path between departure and arrival airports. Tap to open an interactive full-screen map.

### Passenger Manifest

Lists all passengers and cargo assigned to the flight, with a check-in progress badge (e.g. "3/5"). See [Passenger Check-In](passenger-check-in.md) for details.

#### Passenger Details

Tap the **chevron** (›) next to any passenger to open their contact sheet, which shows:

* **Name** and **initials avatar**
* **Check-in status** badge
* **Weight** — displayed with the unit (kg or lb). Tap to edit (see below)
* **Phone** and **email** contact details
* **Quick actions** — Call, Message, or Email with one tap

#### Editing Passenger Weight

1. Open a passenger's contact sheet by tapping the chevron
2. Tap the **weight row** (or "Set weight" if no weight is recorded)
3. Enter the weight value and select the unit (**kg** or **lb**)
4. Tap **Save** — the update is sent to the server immediately

#### Adding a Passenger to a Flight

Tap the **➕ person icon** next to the "Passenger Manifest" heading to add a passenger from the booking's contact list:

1. A search sheet appears showing all booking contacts not already on this flight
2. Search by name to filter the list
3. Tap a contact to add them to this flight

{% hint style="info" %}
A passenger can be added to multiple flight legs in the same booking. If they should only be on one leg, remove them from the other leg first (see below).
{% endhint %}

#### Removing a Passenger from a Flight

1. Open the passenger's contact sheet (tap the chevron)
2. Tap **Remove from Flight** at the bottom
3. Confirm the removal in the dialog

The passenger is removed from this flight leg only — they remain in the booking's contact list and can be re-added later.

### Sharing a Booking

On the Booking Detail screen, tap the **share icon** (top-right, next to the booking code) to share the customer booking link via your device's native share sheet (Messages, Email, AirDrop, etc.).

{% hint style="info" %}
The share button only appears for bookings that have a customer booking URL configured.
{% endhint %}

### Flight Status

Mark the flight as **Departed** or **Arrived**. See [Flight Status](flight-status.md) for details.
