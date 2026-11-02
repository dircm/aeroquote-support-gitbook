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

**Confirm hours** posts a flight's block time to your records:

- **Aircraft hours, landings and engine cycles** are posted when aircraft maintenance is on and the aircraft has a maintenance baseline. Landings are the number of circuits, or 1 if none is entered.
- **Crew flight time** is posted when flight and duty time is on.

**Confirm hours** is offered when either of those is on.

Once a flight's hours are confirmed:

- If you edit its block times, circuits or aircraft, the hours are adjusted by the difference. You're never counted twice.
- If you change the aircraft, the hours move from the old aircraft to the new one.
- If you clear the on-block time, the hours are taken back and the flight shows as not confirmed.

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
