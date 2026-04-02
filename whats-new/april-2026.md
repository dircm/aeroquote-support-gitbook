---
description: >-
  Bookings & Flight Tracking, Live Dashboard, Mobile App, and Custom Route
  Durations.
---

# April 2026

## Bookings & Flight Tracking

A brand new Bookings module takes your operations beyond quoting. Convert accepted quotes to bookings, manage the full flight lifecycle, and track every flight in real time.

### Automatic Flight Tracking (FlightRadar24)

AeroQuote detects departures and arrivals automatically using FlightRadar24 integration. No crew input needed — just assign an aircraft registration or flight number.

* **Departure detection** — Detects ground movement and takeoff automatically
* **In-flight tracking** — Live position updates with altitude, speed, and ETA
* **Arrival detection** — Records landing and saves the full flight track
* **Source tracking** — Every status event shows its source (FlightRadar24, crew manual, GPS)

Enable Flight Tracking in **Settings → Integrations**. See [Booking Status](../guides/bookings-operators/booking-status.md) for the full guide.

### QR Code Boarding Passes

Generate QR code boarding passes for passengers and include them in customer emails and flight manifests. Crew scan them at the aircraft using the mobile app to check passengers in. See [Passengers & Cargo](../guides/bookings-operators/passengers-and-cargo.md).

### Passenger & Cargo Check-In

Check in passengers and cargo per flight — manually via the mobile app or by scanning QR boarding passes. Check-in progress is visible on the Bookings Dashboard and in the activity feed. All check-in activity is audited.

### Booking Completion Emails

When all flights in a booking are complete, AeroQuote automatically sends a completion summary email with:

* Block off, departed, arrived, and block on times for every flight
* Actual flight duration
* Planned vs actual duration variance (operator version only)
* Flight track map (when tracking data is available)

See [Sending Confirmations](../guides/bookings-operators/sending-confirmations.md) for details.

### Ground Crew

Assign ground crew to bookings — staff who support flights on the ground but are not on the flight manifest. Ground crew receive push notifications for departures and arrivals and can check in passengers via the mobile app (v2).

See [Crew Assignment](../guides/bookings-operators/crew-assignment.md).

***

## Live Bookings Dashboard

A full-screen, dark-mode operations display built for dispatch offices and ops rooms.

* **Live flight map** — Aircraft positions with registration labels and position trails
* **Booking cards** — Altitude, speed, ETA, check-in progress, and crew for every active flight
* **Activity feed** — Check-ins, departures, and arrivals stream in as they happen
* **Summary cards** — Count of in-progress, upcoming, and ground time bookings
* **Auto-refresh** — Dashboard stays current without manual intervention

Access the [Bookings Dashboard ](../guides/dashboard/bookings-dashboard.md)from the [Dashboard](../guides/dashboard/bookings-dashboard.md) page.

***

## Mobile App

A purpose-built app for iOS and Android, designed for crew in the field.

* **Next Flight dashboard** — Countdown to departure with route, aircraft, and passenger details
* **Passenger check-in** — Tap to check in or scan QR boarding passes
* **Flight status recording** — Confirm departures and arrivals with a tap, update ETAs from the field
* **Push notifications** — Receive alerts when departures and arrivals are detected
* **Offline support** — Everything works without connectivity and syncs automatically
* **Calendar sync** — Flight legs appear in your crew's device calendar

Available on the App Store and Google Play.

***

## Custom Route Durations per Aircraft

You can now set **custom flight durations per aircraft** for routes in your Route Library. This overrides the default duration calculated from the aircraft's performance profile, giving you precise control over flight times for routes where real-world experience differs from the calculated estimate.

This is especially useful for:

* **Scenic flights** where the actual flight time is well-known from repeated operations
* **Routes with known wind or altitude factors** that consistently affect duration
* **Helicopter operations** where the speed profile differs from fixed-wing calculations

Custom durations are used automatically in both the Request estimator and the Quote Builder when the route is loaded.

See [Custom Routes & Route Library](../guides/custom-items/custom-routes-and-route-library.md) for the full guide.

***

## Availability

Bookings & Flight Tracking is **free until May 31, 2026** during the evaluation period. After that, it's available as a paid module from **Settings → Modules**.
