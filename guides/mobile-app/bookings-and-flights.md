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

### Flight Status

Mark the flight as **Departed** or **Arrived**. See [Flight Status](flight-status.md) for details.
