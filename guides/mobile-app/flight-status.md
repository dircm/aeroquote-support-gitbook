# Flight Status

Mark flights as **Departed** or **Arrived** directly from the mobile app with confirmed timestamps.

## Recording Departure

1. On the Flight Detail screen, scroll to the **Flight Status** section
2. Tap the **Departed** button
3. A bottom sheet appears with:
   * The flight route (e.g. YBBN → YSSY)
   * A time picker pre-filled with the current time
   * Adjust the time if the actual departure differs
4. Tap **Confirm Departure**
5. The button turns green to indicate departure has been recorded

## Recording Arrival

1. After departure is recorded, the **Arrived** button becomes active
2. Tap it and follow the same flow — confirm the arrival time
3. Both buttons now show green, indicating the flight is complete

{% hint style="info" %}
Flight status updates sync to the AeroQuote server automatically. Other team members will see the updated status in the web application.
{% endhint %}

## Offline Support

Like check-ins, flight status updates work offline:

* Status changes are saved locally and queued for sync
* A pending indicator shows until the update reaches the server
* Status syncs automatically when connectivity is restored
