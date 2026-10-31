---
description: >-
  Hours flown over the last 7, 30 and 90 days, flights that are on a booking,
  and what each tracking badge means.
---

# Flight Logs

Flight Logs lists the flights FlightAware saw for your aircraft.

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
- Totals are shown in hours to one decimal place, for example **12.5 h**. They update when a flight lands, when times change, or when a flight is deleted.

## Flights on a booking

When you turn a flight into a booking, it **stays on Flight Logs**. The row shows:

- a **Booked** badge
- the booking's type, for example **Charter**, **Scheduled**, **Tour** or **Repositioning**
- a **View booking** link with the booking code, which opens the booking

When you open the flight, the panel shows **Linked to** with the booking code and type.

{% hint style="info" %}
A flight on a booking is read-only on Flight Logs. Its times are shown but can't be edited here, and **Mark as landed** and **Not flown** aren't offered. If you try to change them, you'll see *"This flight is on a booking. Edit its times on the booking."* Change the times on the booking instead.
{% endhint %}

The times from Flight Logs are still copied onto the booking's leg when you convert the flight.

## Tracking badges

Sometimes AeroQuote closes a flight because FlightAware never reported a landing. The row then gets one of these badges:

| Badge | What it means | What you can do |
| --- | --- | --- |
| **Arrival estimated** | The flight departed and its estimated landing time has passed, but no landing was reported. AeroQuote keeps watching for a real landing for a while. | Nothing needed. A reported landing replaces the estimate. |
| **Arrival unconfirmed** | FlightAware stopped tracking the flight before it reported a landing. | **Mark as landed** and enter the landing time. |
| **Expired** | The flight is long overdue and no landing was reported. | **Mark as landed** and enter the landing time. |
| **Not flown** | The flight never departed, or you marked it **Not flown**. | **Mark as landed** if it did fly. |
