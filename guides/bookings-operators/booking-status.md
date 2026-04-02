---
description: Track flight progress through status updates and automatic flight tracking.
---

# 📊 Booking Status

The Status tab tracks each flight through its lifecycle — from block off to block on. Status updates can come from crew via the mobile app, or automatically from FlightRadar24 integration.

***

## Accessing Status

1. Go to **Bookings** from the sidebar
2. Click on a booking
3. Select the **Status** tab

***

## Flight Status Timeline

Each flight leg tracks four key events in sequence:

| Event         | Description                                         |
| ------------- | --------------------------------------------------- |
| **Block Off** | Aircraft leaves the gate or parking position        |
| **Departed**  | Aircraft takes off                                  |
| **Arrived**   | Aircraft lands                                      |
| **Block On**  | Aircraft reaches the gate or parking at destination |

Each event records:

* **Timestamp** — When it occurred
* **Source** — How it was recorded (see Sources below)

***

## Flight Status Values

Each flight leg has a status that updates as events are recorded:

| Status          | Meaning                                 |
| --------------- | --------------------------------------- |
| **Boarding**    | Passengers are boarding the aircraft    |
| **In Progress** | Aircraft has departed and is airborne   |
| **Completed**   | Aircraft has arrived at its destination |
| **Cancelled**   | Flight has been cancelled               |

***

## Status Sources

Every status event is tagged with its source, so you always know how it was recorded:

| Source            | Description                               |
| ----------------- | ----------------------------------------- |
| **FlightRadar24** | Automatically detected by flight tracking |
| **App (Manual)**  | Crew confirmed via the mobile app         |
| **App (GPS)**     | Detected by GPS on the crew's device      |

{% hint style="info" %}
**Crew input always takes priority.** If a crew member confirms a departure or arrival time via the mobile app, that time takes precedence over any automatic tracking data.
{% endhint %}

***

## Automatic Flight Tracking

When Flight Tracking is enabled in **Settings → Integrations**, AeroQuote automatically detects flight events using FlightRadar24:

### Departure Detection

* Detects ground movement (block off) when the aircraft begins taxiing
* Records departure when the aircraft becomes airborne
* Monitoring begins 5 minutes before the scheduled departure

### In-Flight Tracking

* Live position updates with altitude, speed, and heading
* ETA updates as the flight progresses
* Position trail visible on the Bookings Dashboard map

### Arrival Detection

* Detects arrival when the aircraft lands at the destination airport
* Records the full flight track for your records after landing

{% hint style="success" %}
**No crew input needed.** Flight tracking works automatically using the aircraft registration or flight number — your crew can focus on the flight while AeroQuote handles the status updates.
{% endhint %}

***

## Manual Status Updates

Crew can also update flight status manually via the mobile app:

1. Open the booking in the AeroQuote mobile app
2. Tap the flight leg
3. Tap to confirm departure or arrival
4. Timestamp is recorded immediately

Manual updates from the app are also available for ETA changes when conditions change in flight.

***

## Status on the Dashboard

The **Bookings Dashboard** provides a real-time operations view:

* **Live flight map** — Aircraft positions with registration labels and position trails
* **Booking cards** — Altitude, speed, ETA, and check-in progress for active flights
* **Activity feed** — Status changes stream in as they happen with their source
* **Summary cards** — Count of in-progress, upcoming, and ground time bookings

The dashboard auto-refreshes and is designed for wall-mounted displays or ops room screens.

***

## Status History

Every status change is recorded with:

* What changed
* When it changed
* The source (FlightRadar24, crew app, etc.)
* The timestamp of the event

View the full audit trail in the [Amendments](amendments.md) section.

***

## Tips

{% hint style="success" %}
**Enable Flight Tracking** — Automatic status updates via FlightRadar24 mean less manual work and more accurate records. Enable it in Settings → Integrations.
{% endhint %}

* Assign aircraft registrations or flight numbers on bookings so flight tracking can identify your flights
* Crew can override any automatic tracking data from the mobile app
* The completion email with variance analysis is sent automatically after all flights finish — see [Sending Confirmations](sending-confirmations.md)

***

## Next Steps

* [Amendments](amendments.md) — View full change history
* [Sending Confirmations](sending-confirmations.md) — Customer communications and completion emails
