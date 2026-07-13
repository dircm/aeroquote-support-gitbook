---
description: >-
  Live flight tracking for bookings — automatic detection via FlightRadar24,
  crew mobile updates, maps, and multi-leg rotation handling.
---

# 📡 Flight Tracking

Flight tracking connects your **bookings** to live aircraft data so departures, arrivals, ETAs, and flight paths update automatically — with crew able to confirm or override anything from the mobile app.

{% hint style="info" %}
Flight tracking requires the **Bookings** module (or **Scheduled Flights** / **Tour Packages**, which include bookings access) and the **Flight Tracking** toggle in **Settings → Integrations**.
{% endhint %}

***

## What you get

| Capability                                  | Where you see it                                                              |
| ------------------------------------------- | ----------------------------------------------------------------------------- |
| **Automatic block off, departure, arrival** | Booking Status tab, Bookings Dashboard, mobile push notifications             |
| **Live position & ETA**                     | Bookings Dashboard map, booking Status tab, mobile app                        |
| **Saved flight track**                      | Itinerary map, completed booking cards, mobile track view                     |
| **Crew overrides**                          | Mobile app — confirmed times always win over automation                       |
| **Multi-leg rotations**                     | Ground Time status between legs; stalled-leg recovery when coverage is patchy |

***

## How tracking identifies your flight

For each flight leg, AeroQuote looks up the aircraft on FlightRadar24 using, in order:

1. **Assigned registration** on the booking (if set — overrides the aircraft record)
2. **Aircraft registration** from your fleet
3. **Flight number** on the leg (if no valid registration)

Invalid or placeholder values (e.g. `TBA`, `SAMPLE`) are ignored. Individual aircraft can opt out via **FlightRadar24 Tracking** on the aircraft record.

The booking **Details** tab shows a readiness badge per aircraft: tracking on, off (account/aircraft), invalid format, or no recent FR24 history.

***

## Data sources (and who wins)

Every milestone records **where the time came from**:

| Source            | Typical origin                                                                                                              |
| ----------------- | --------------------------------------------------------------------------------------------------------------------------- |
| **App (Manual)**  | Crew confirmed in the mobile app                                                                                            |
| **FlightRadar24** | Automatic ADS-B detection                                                                                                   |
| **App (GPS)**     | Mobile geofence / speed detection                                                                                           |
| **Inferred**      | System filled a gap on a stalled rotation (schedule-based, only when FR24 or crew evidence exists elsewhere on the booking) |
| **Auto run**      | Scheduled-flight auto-run on published departures (timetable-driven; crew and FR24 take precedence)                         |

**Precedence:** crew manual → FlightRadar24 → GPS → inferred → auto run. Higher-trust sources are never overwritten by lower-trust ones.

Positions on the map may be labelled **(estimated)** when they come from **simulation** (scheduled auto-run gap-fill) or when milestone times use **inferred** / **auto run**.

***

## Guides in this section

{% content-ref url="enabling-and-configuration.md" %}
[enabling-and-configuration.md](enabling-and-configuration.md)
{% endcontent-ref %}

{% content-ref url="automatic-detection.md" %}
[automatic-detection.md](automatic-detection.md)
{% endcontent-ref %}

{% content-ref url="multi-leg-rotations.md" %}
[multi-leg-rotations.md](multi-leg-rotations.md)
{% endcontent-ref %}

***

## Related guides

* [Booking Status](../booking-status.md) — Status tab timeline
* [Bookings Dashboard](../bookings-dashboard.md) — Ops-room live map
* [Flight Status (Mobile)](../../mobile-app/flight-status.md) — Crew confirmations and manual entry
* [Integrations](../../settings/integrations.md) — Enable the Flight Tracking toggle
