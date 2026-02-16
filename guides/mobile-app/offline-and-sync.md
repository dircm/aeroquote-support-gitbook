# Offline Mode & Data Sync

The AeroQuote Crew app is designed to work reliably in areas with limited or no internet connectivity — a common reality at remote airfields and during flights.

## How It Works

All data is stored locally on your device in a dedicated database. The app never reads directly from the server during normal use — it reads from the local copy and syncs in the background.

### Automatic Sync

The app syncs data from the server in three ways:

1. **On login** — A full sync runs immediately when you sign in
2. **Every 5 minutes** — While the app is open, data refreshes automatically
3. **On app resume** — When you switch back to the app after using other apps, a sync runs immediately

### Manual Sync

Pull down on the **Bookings list** to trigger an immediate sync.

### Offline Queue (Outbox)

Actions you take while offline are queued locally:

* Passenger and cargo check-ins
* Flight departure and arrival status updates

These are stored in an outbox and automatically sent to the server when connectivity returns. You'll see a **sync pending** indicator next to any queued action.

## Connectivity Indicator

* **Green dot + "Online — System Synced"** on the Dashboard means you're connected
* **"Offline" indicator** appears when the device loses connectivity
* An **offline banner** may appear at the top of certain screens

## Tips

* **Don't worry about signal** — Complete your check-ins and flight status updates as normal. Everything queues safely.
* **Force a sync** — If you need the latest data right now, pull to refresh on the Bookings screen.
* **Restarting the app** — All local data and pending actions survive app restarts. Nothing is lost.

{% hint style="success" %}
The app is designed so that boarding and flight operations are **never blocked** by connectivity issues. Check-in passengers, mark departures, and record arrivals — the data will sync when it can.
{% endhint %}
