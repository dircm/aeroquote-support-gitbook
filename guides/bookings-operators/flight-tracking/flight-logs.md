---
description: >-
  Add and edit flights, how hours work, hours flown over the last 7, 30 and 90
  days, flights that are on a booking, deleting, and what each tracking badge means.
---

# Flight Logs

Flight Logs lists the flights FlightAware saw for your aircraft, plus any flights you add yourself.

## Add a flight

Use **Add flight** for a flight FlightAware missed.

1. Select **Add flight** at the top of Flight Logs.
2. Choose the **Aircraft**. Only aircraft in your fleet are listed.
3. Enter **From** and **To** as ICAO or IATA codes, for example **YSSY** or **SYD**.
4. Enter **Off-block** and **On-block**, **Takeoff** and **Landing**, or all four. Times are in the **departure airport's local time**.
5. Optionally enter **Passengers** and **Circuits**.
6. Select **Save flight**.

AeroQuote checks that:

- on-block is after off-block
- landing is after takeoff
- at least one pair of times is entered
- no time is in the future

{% hint style="info" %}
Saving a flight doesn't add any hours. Check the times, then use **Confirm hours** (see [How hours work](#how-hours-work)).
{% endhint %}

## Edit a flight

Select **Edit** on a row to change it.

- For a flight that **isn't on a booking**, you can change everything: aircraft, airports, times, passengers and circuits.
- If you change the airports, AeroQuote keeps your airports even if FlightAware sends an update for that flight later.
- If the flight's hours are already confirmed, they're updated for you. See [How hours work](#how-hours-work).

For a flight that **is on a booking**, see [Flights on a booking](#flights-on-a-booking).

## How hours work

**Confirm hours** posts a flight's hours to your records:

- **Aircraft hours, landings and engine cycles** are posted when aircraft maintenance is on and the aircraft has a maintenance baseline. Aircraft **TTIS** is credited from **Departure** to **Arrival** (not Off Block to On Block), in tenths of an hour, and only once both departure and arrival times exist. If either time is missing, the TTIS credit is held; if an earlier credit had been posted, it is reversed until both times are present again. Landings are the number of circuits, or 1 if none is entered. You can change **Landings** and **Cycles** (whole numbers from 1 to 999) before confirming.
- **Crew flight time** is posted when flight and duty time is on.

**Confirm hours** is offered when either of those is on. Confirming does not change the flight times. It records you as the reviewer and posts the hours once.

Hours that come from flight tracking (FlightAware or Flightradar24), or from flights you add on Flight Logs, stay pending until someone with aircraft edit permission confirms them. They do not count towards aircraft totals or the [Run Out Report](../../aircraft/maintenance-tracker.md) until then.

- A count of **N flights pending hours confirmation** is shown at the top of Flight Logs, and each such flight has an **Hours pending confirmation** badge.
- Open a flight, review the times under **Confirm hours**, then click **Confirm hours**.
- Or tick several pending flights that are not on a booking, and click **Confirm N selected**. Booking flights are confirmed one at a time.
- The [Run Out Report](../../aircraft/maintenance-tracker.md) also has an amber link, **N flights pending hours confirmation — review in Flight Logs**.

An **On Block** time that crew record in the Crew app for their booking leg is confirmed automatically. The office does not need to confirm it again.

When aircraft maintenance is on, newly confirmed flights are credited to TTIS from departure to arrival, in tenths of an hour, using the 6-minute table (0–3 minutes is .0, 4–9 is .1, and so on; 58–60 rounds up to the next hour). See [Aircraft time in tenths](../../aircraft/maintenance-limits.md#aircraft-time-in-tenths). Flights confirmed before the tenths rule was introduced are not changed. The hours ledger is append-only: editing times writes a reversal of the previous credit and a new capture, and does not overwrite earlier rows.

Flights with on-block times before the aircraft's baseline never appear as pending — they are already covered by the baseline.

If flight tracking later revises the block times on a confirmed Flight Logs entry that is not on a booking, the flight goes back to pending and its hours are taken out of the totals until it is confirmed again.

Once a flight's hours are confirmed:

- If you edit its departure, arrival or block times, circuits or aircraft, the hours are adjusted by a reversal of the previous credit and a new capture where needed. You're never counted twice, and earlier ledger rows are not overwritten.
- If you change the aircraft, the hours move from the old aircraft to the new one.
- If you clear the on-block time, or clear departure or arrival so TTIS cannot be calculated, the hours are taken back and the flight shows as not confirmed when the on-block time is cleared.

There is no Confirm hours screen in the Crew app. Crew cannot edit older Flight Log entries in the app; change those on the web with aircraft edit permission, or edit a booking flight's times on the booking.

## Hours flown

Three **Hours flown** cards sit at the top of the page:

| Card | Covers |
| --- | --- |
| **Last 7 days, all aircraft** | Flights that finished in the last 7 days |
| **Last 30 days, all aircraft** | Flights that finished in the last 30 days |
| **Last 90 days, all aircraft** | Flights that finished in the last 90 days |

- The totals include every aircraft on your account, whatever fleet or date filter you have set.
- Each flight counts its **block time** (off blocks to on blocks). If there's no block time, the flight counts its airborne time instead. For a [circuit session](circuit-sessions.md), that's the sum of the airborne time on each hop.
- A flight counts once it has landed. Flights still in the air don't count yet.
- Totals are shown in hours to one decimal place, for example **12.5 h**. They update when a flight lands, when you add or edit a flight, or when a flight is deleted.

## Flights on a booking

When you turn a flight into a booking, it **stays on Flight Logs**. The row shows:

- a **Booked** badge
- the booking's type, for example **Charter**, **Scheduled**, **Tour** or **Repositioning**
- a **View booking** link with the booking code, which opens the booking

When you open the flight, the panel shows **Linked to** with the booking code and type.

{% hint style="info" %}
On Flight Logs you can only change the **airports** of a flight that's on a booking, and only on the flight log itself. Its times and aircraft belong to the booking. **Mark as landed** and **Not flown** aren't offered. If you try to change the times, you'll see *"This flight is on a booking. Edit its times on the booking."*

**Edit** shows a link to the booking. Change the times, the aircraft and the leg's airports on the booking. Flight Logs never changes the booking.
{% endhint %}

The times from Flight Logs are still copied onto the booking's leg when you convert the flight. After that, the leg's hours belong to the booking.

## Delete a flight

Select **Delete** on a row, or tick several rows and delete them together.

- **Flight not on a booking, hours confirmed:** the aircraft hours, landings, engine cycles and crew flight time posted from it are taken back. You'll see a warning first.
- **Flight on a booking:** only the flight log is deleted. The booking, its leg and the hours on that leg are kept. The warning says so.

## Tracking badges

Sometimes AeroQuote closes a flight because FlightAware never reported a landing. The row then gets one of these badges:

| Badge | What it means | What you can do |
| --- | --- | --- |
| **Arrival estimated** | The flight departed and its estimated landing time has passed, but no landing was reported. AeroQuote keeps watching for a real landing for a while. | Nothing needed. A reported landing replaces the estimate. |
| **Arrival unconfirmed** | FlightAware stopped tracking the flight before it reported a landing. | **Mark as landed** and enter the landing time. |
| **Expired** | The flight is long overdue and no landing was reported. | **Mark as landed** and enter the landing time. |
| **Not flown** | The flight never departed, or you marked it **Not flown**. | **Mark as landed** if it did fly. |

## Flights to and from custom airports

FlightAware has no airport code for a private strip or other custom airport. For those flights it sends no destination, or sends a position instead of a code. AeroQuote now matches the flight to your booking when that position is within about 10 nm of the custom airport you booked. Departures from a custom airport are matched the same way.

The aircraft (by registration, flight number or alert) and the date still have to match. If FlightAware reports a different real airport from the one you booked, the flight isn't matched to the booking. It appears on Flight Logs instead.

## Link to existing booking

Sometimes a flight that was already booked still appears on Flight Logs as unmatched. To fix that, select the flight and choose **Link to existing booking**. Then pick the booked leg and click **Link**. Only legs on the same aircraft within two days of the flight are listed.

When you link a flight:

* its times are copied onto the leg, and the booking is updated as if FlightAware had matched the flight;
* any hours you already confirmed move to the leg, so they are not counted twice;
* no new booking is created;
* the Flight Logs row becomes read-only, because the booking now holds its times.
