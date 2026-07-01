---
description: >-
  Access crew and external-operator flight manifests for operational bookings.
---

# Booking Manifests

A **flight manifest** lists passengers, crew, cargo, and flight legs for a booking. Crew and external operators download manifests from their portals; operators access signed manifest links from operational surfaces.

***

## What the manifest includes

* Booking code and operator details
* Flight legs with times, airports, and aircraft
* Passenger names, weights, and check-in status where recorded
* Crew assignments per leg
* Cargo items and weights
* Facilities and notes relevant to crew

## Crew manifest (signed link)

Crew members with portal access:

1. Log in to the **Crew** portal
2. Open the assigned booking
3. Click **Download Flight Manifest**

The PDF opens in a new tab — suitable for printing or mobile reference.

## External operator manifest

External operators assigned to a booking:

1. Log in to the **External Operator** portal
2. Open the booking
3. Click **Download Flight Manifest**

Only flights relevant to that operator's aircraft are included.

## Operator access

Operators can open signed crew manifest links from operational departure views where a manifest shortcut is shown (e.g. scheduled departures with materialised bookings).

Manifests use cryptographically signed URLs — no separate login required when opening a signed link, but the link must be kept confidential.

## Keeping manifests accurate

Manifests reflect the booking at generation time. After changes:

1. Update passengers, crew, or cargo on the booking
2. Re-download the manifest before the flight

Passenger check-in via the mobile app updates weights and check-in status on subsequent manifest downloads.

***

See [Passengers & Cargo](passengers-and-cargo.md) and [Crew Assignment](crew-assignment.md) for keeping manifest data current.