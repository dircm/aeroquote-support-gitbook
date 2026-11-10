---
description: >-
  Maintenance Tracker, dated baselines, aircraft time in tenths, Confirm hours,
  crew live flight times, plus add and edit flights on Flight Logs.
---

# November 2026

## Add and edit flights on Flight Logs

You can now **add a flight** on Flight Logs. Use it for a flight FlightAware didn't see:

- choose the aircraft and the From and To airports
- enter block or air times in the departure airport's local time
- optionally add passengers and circuits

Select **Edit** on a flight to fix it.

- For a flight that isn't on a booking, you can change everything.
- For a flight on a booking, you can change its airports. Times and aircraft are changed on the booking.

**Confirm hours** is now offered when aircraft maintenance is on, even if flight and duty time is off.

If a flight's hours are already confirmed and you edit it, the hours are adjusted by the difference. If you change its aircraft, the hours move to the new aircraft.

## Deleting a flight takes back its hours

Deleting a flight whose hours you confirmed now takes those aircraft and crew hours back. Before this change, they stayed on the aircraft.

Deleting a flight that's on a booking keeps the booking and its hours.

See [Flight Logs](../guides/bookings-operators/flight-tracking/flight-logs.md).

## Maintenance Tracker, baselines and tenths

The **Maintenance Tracker** add-on is now documented for operators who have it switched on:

- The **Run Out Report** lists due items with hours, days and cycles remaining, a forecast date and traffic lights. Crew see the same items under **Due Items** in the app.
- Hours from FlightAware or Flightradar24 stay pending until you **Confirm hours** in Flight Logs. An **On Block** that crew record in the app is confirmed automatically.
- Aircraft time is shown and credited in tenths of an hour, using a 6-minute table (0–3 minutes is .0, 4–9 is .1, up to 58–60 which is the next hour). New confirmations are snapped to that table; existing confirmed flights and baselines are not rewritten.
- **Update baseline** sets absolute TTIS, landings and engine cycles as at a date and time. Older flights do not contribute. You can enter TTIS as **Decimal** or **hh:mm** (1209.6 is 1209:36). This needs the **Aircraft - Maintenance Totals** permission or aircraft edit permission, and is available on the web and in the Crew app.
- Crew can set and edit live flight times in the app — **Off Block**, **Departure**, **ETD** (until departed), **ETA** (while airborne), **Arrival** and **On Block**. Those times override FlightAware and Flightradar24. Crew cannot edit older Flight Log entries in the app.

See [Maintenance Tracker](../guides/aircraft/maintenance-tracker.md), [Maintenance Limits](../guides/aircraft/maintenance-limits.md) and [Flight Status](../guides/mobile-app/flight-status.md).
