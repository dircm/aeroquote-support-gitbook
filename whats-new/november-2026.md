---
description: >-
  Maintenance Tracker, dated baselines, aircraft time in tenths, Confirm hours,
  crew live flight times, add and edit flights on Flight Logs, and the CASA
  audit trail now live on production.
---

# November 2026


## CASA audit trail now live

The Maintenance Tracker on production now keeps a CASA-oriented audit trail of maintenance records. In short:

- Audit rows include a reason, the actor's ARN, source and device context.
- Aircraft TTIS is credited from **Departure** to **Arrival**, and held until both times exist.
- The hours ledger is append-only: a later change writes a reversal plus a new capture, and does not overwrite earlier rows.
- Sign-off needs the **Maintenance - Sign Off** permission, a confirmation of the name and ARN (pre-filled from the user profile), and a reason on corrections and voids. Sign-offs cannot be hard-deleted.
- Life-limit and component writes are audited; life-limit items are soft-deleted rather than removed outright. Installed component snapshots are re-anchored when you update a baseline or adjust totals.
- **Record history** (per aircraft or all aircraft) is a read-only view behind **Maintenance - View Records**, with **Export CSV** and **Export PDF**.

Dates these went live (Australia/Brisbane, AEST) are listed in [CASA audit trail — what is live](../guides/aircraft/maintenance-tracker.md#casa-audit-trail--what-is-live).

See [Maintenance Tracker](../guides/aircraft/maintenance-tracker.md) and [Permissions](../guides/settings/permissions.md).

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
