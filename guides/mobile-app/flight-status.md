# Flight Status

Record flight departures and arrivals from the mobile app — either by confirming automated flight tracking notifications or by manually entering times.

<!-- 📸 PLACEHOLDER: Screenshot of the Flight Status section showing Block Off/Departed/Arrived/Block On buttons and confirmation bottom sheet -->
<!-- Suggested filename: .gitbook/assets/mobile-flight-status.png -->

## How It Works

AeroQuote integrates with flight tracking providers (FlightRadar24 and FlightAware) to automatically detect when your aircraft departs and arrives. When a flight event is detected:

1. All crew assigned to that flight leg receive a **push notification**
2. Tapping the notification opens a **confirmation sheet** pre-filled with the detected time
3. Crew can accept the time as-is or adjust it before confirming

Once confirmed by crew, the time is locked and cannot be overwritten by subsequent tracking updates. This ensures crew-confirmed times always take priority.

{% hint style="info" %}
If a notification arrives while the app is open, the confirmation sheet appears automatically — no need to tap the notification.
{% endhint %}

## Flight Timeline

The Flight Detail screen shows four time events in sequence:

1. **Block Off** — When the aircraft leaves the gate/parking position
2. **Departed** — When the aircraft takes off
3. **Arrived** — When the aircraft lands
4. **Block On** — When the aircraft reaches the gate/parking position

Each event has a button that shows the recorded time once confirmed. Tap any button to record or edit the time.

## Confirming a Departure

1. Receive a **departure notification** from the flight tracking provider
2. Tap the notification (or view the sheet if the app is open)
3. The bottom sheet shows:
   * The flight route (e.g. YBBN → YSSY)
   * A **UTC/Local toggle** — switch between Zulu time and the airport's local timezone
   * A time picker pre-filled with the detected departure time
   * Adjust the time if the actual departure differs
4. Tap **Confirm Departure**
5. The departure button turns green to indicate it has been recorded

## Confirming an Arrival

1. Receive an **arrival notification** when the tracking provider detects the landing
2. Follow the same flow — confirm or adjust the arrival time
3. Both buttons now show green, indicating the flight is complete

## Manual Entry

If flight tracking doesn't detect a flight (e.g. remote airstrips, VFR flights without ADS-B coverage), you can record times manually:

1. On the Flight Detail screen, scroll to the **Flight Status** section
2. Tap the **Block Off** button to record gate departure (optional)
3. Tap the **Departed** button and confirm the takeoff time
4. After departure is recorded, the **Arrived** button becomes active — tap and confirm when landed
5. Tap the **Block On** button to record gate arrival (optional)

{% hint style="warning" %}
Manual entries take priority over tracking data. Once you confirm a time, it won't be overwritten.
{% endhint %}

## Adjust ETD

Before a flight begins, crew can adjust the estimated departure time (ETD):

1. On the Flight Detail screen, scroll to the **Flight Status** section
2. Tap the **Adjust ETD** button
3. A time picker appears pre-filled with the current scheduled departure time
4. Adjust the time and tap **Confirm ETD**

The new departure time updates the flight schedule — the arrival time shifts accordingly based on the planned flight duration. The booking's start and end times are also recalculated.

{% hint style="info" %}
The Adjust ETD button disappears once the flight enters an in-progress state (block off recorded, departed, etc.). ETD can only be changed before the flight begins.
{% endhint %}

## Live Time Remaining

While a flight is in progress, the app shows a **live countdown** to the estimated arrival:

* On the **Booking Detail** screen, each in-flight leg card replaces the planned duration with a live "Xh Ym remaining" countdown and the current ETA
* On the **Flight Detail** screen, the route card and Flight Status section both display the time remaining and ETA with source label (Crew/FA)
* The countdown updates every minute automatically
* If the current time passes the ETA, the display clamps to **"Arriving soon"** rather than showing negative time

The ETA used for the countdown follows this priority: **Crew ETA** > **FlightAware ETA** > **Scheduled arrival time**.

## Log Position

While a flight is in progress, crew can report their current GPS position:

1. Tap the **Log Position** button on the Flight Detail screen
2. The app reads the device's GPS coordinates
3. The position is queued and sent to the server

This is useful for flights without ADS-B coverage where the operator needs to track progress. Positions appear on the booking's live map in the web application.

{% hint style="info" %}
The Log Position and Update ETA buttons are hidden once a flight is marked as arrived — they are only available during active flights.
{% endhint %}

## Update ETA

Crew can manually update the estimated arrival time during a flight:

1. Tap the **Update ETA** button on the Flight Detail screen
2. A time picker appears pre-filled with the current ETA
3. Adjust the time and confirm

The ETA source is shown on the dashboard hero card:

* **FR24 ETA** — Estimated by FlightRadar24
* **FA ETA** — Estimated by FlightAware
* **Crew ETA** — Manually set by crew via the app

Crew-set ETAs take priority over automated tracking ETAs.

## Offline Support

All flight status operations work offline:

* **Block off/on**, **departure/arrival**, **ETA updates**, **ETD adjustments**, and **position logs** are all saved locally and queued for sync
* A pending indicator shows until the update reaches the server
* Updates sync automatically when connectivity is restored
* Failed syncs are retried with exponential backoff

{% hint style="success" %}
You never need to wait for a network connection to record flight events. All operations update the UI instantly and sync in the background.
{% endhint %}

## Live Bookings Dashboard

Flight status updates from the mobile app feed directly into the **Bookings Dashboard** — a real-time ops display designed for TV screens and wall monitors. When a departure or arrival is confirmed:

* The flight appears on the **live map** with the actual track
* The **activity feed** shows the departure/arrival event in real time
* Booking cards update with actual times
* Multi-leg bookings transition to **Ground Time** status between legs

See the [Bookings Dashboard](../bookings-operators/bookings-dashboard.md) guide for more information.
