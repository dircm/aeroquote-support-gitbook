# Flight Status

Record flight departures and arrivals from the mobile app — either by confirming automated FlightAware notifications or by manually entering times.

<!-- 📸 PLACEHOLDER: Screenshot of the Flight Status section showing Departed/Arrived buttons and confirmation bottom sheet -->
<!-- Suggested filename: .gitbook/assets/mobile-flight-status.png -->

## How It Works

AeroQuote uses **FlightAware** to automatically detect when your aircraft departs and arrives. When a flight event is detected:

1. All crew assigned to that flight leg receive a **push notification**
2. Tapping the notification opens a **confirmation sheet** pre-filled with the FlightAware time
3. Crew can accept the time as-is or adjust it before confirming

Once confirmed by crew, the time is locked and cannot be overwritten by subsequent FlightAware updates. This ensures crew-confirmed times always take priority.

{% hint style="info" %}
If a notification arrives while the app is open, the confirmation sheet appears automatically — no need to tap the notification.
{% endhint %}

## Confirming a Departure

1. Receive a **departure notification** from FlightAware
2. Tap the notification (or view the sheet if the app is open)
3. The bottom sheet shows:
   * The flight route (e.g. YBBN → YSSY)
   * A time picker pre-filled with the detected departure time
   * Adjust the time if the actual departure differs
4. Tap **Confirm Departure**
5. The departure button turns green to indicate it has been recorded

## Confirming an Arrival

1. Receive an **arrival notification** when FlightAware detects the landing
2. Follow the same flow — confirm or adjust the arrival time
3. Both buttons now show green, indicating the flight is complete

## Manual Entry

If FlightAware doesn't detect a flight (e.g. remote airstrips, VFR flights without ADS-B coverage), you can record times manually:

1. On the Flight Detail screen, scroll to the **Flight Status** section
2. Tap the **Departed** button
3. Adjust the time in the picker
4. Tap **Confirm Departure**
5. After departure is recorded, the **Arrived** button becomes active — tap and confirm when landed

{% hint style="warning" %}
Manual entries also take priority over FlightAware data. Once you confirm a time, it won't be overwritten.
{% endhint %}

## Offline Support

Flight status updates work offline:

* Status changes are saved locally and queued for sync
* A pending indicator shows until the update reaches the server
* Status syncs automatically when connectivity is restored

## Live Bookings Dashboard

Flight status updates from the mobile app feed directly into the **Bookings Dashboard** — a real-time ops display designed for TV screens and wall monitors. When a departure or arrival is confirmed:

* The flight appears on the **live map** with the actual track from FlightAware
* The **activity feed** shows the departure/arrival event in real time
* Booking cards update with actual times
* Multi-leg bookings transition to **Ground Time** status between legs

See the [Bookings Dashboard](../bookings-operators/bookings-dashboard.md) guide for more information.
