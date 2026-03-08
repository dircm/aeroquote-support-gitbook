# Calendar Sync

Sync your flight schedules to your device calendar so upcoming flights appear alongside your personal events.

## Setup

1. Open the app and go to **Profile** → **Calendar Sync**
2. Toggle calendar sync **ON**
3. Grant calendar permission when prompted
4. Select which device calendar to sync to (e.g. "AeroQuote", "Personal", or any writable calendar)

## How It Works

* Each flight leg becomes a separate calendar event
* Events include the route (e.g. "YBBN → YSSY"), booking code, departure location, and a deep link back to the booking in the app
* Events are created in UTC and display in your device's local timezone
* When flight times change in AeroQuote, calendar events update automatically on the next sync

### Sync Triggers

Calendar events are synced:

* When you sign in
* When booking data refreshes (every 5 minutes or on pull-to-refresh)
* When a booking is updated via push notification

### What Gets Synced

* All active bookings with flight legs that have a departure time
* Flight duration is used to calculate the event end time
* Cancelled or deleted bookings have their calendar events automatically removed

## Removing Events

* **Toggle sync off** — All AeroQuote events are removed from your calendar
* **Sign out** — All events are cleaned up automatically

{% hint style="info" %}
Calendar sync only creates events in one direction — from AeroQuote to your device calendar. Editing or deleting events in your device calendar does not affect AeroQuote data.
{% endhint %}
