# Bookings Dashboard

The Bookings Dashboard is a **real-time operations display** designed to give your team a live overview of all flight activity. It's purpose-built for wall-mounted TVs, dedicated monitors, or a second screen — leave it open and watch your bookings progress through their lifecycle.

## Opening the Dashboard

The Bookings Dashboard is accessed from the **Bookings card** on the operator Home page:

1. Log in to AeroQuote
2. On the Home page, find the **Bookings** summary card (shows total bookings, in-progress count, and upcoming count)
3. Click the **Dashboard** link (with TV icon) on the right side of the card footer — it opens in a **new browser tab**

The Dashboard link is only visible to users with **Manager**, **Account Administrator**, or **Chief Pilot** roles (users with the `bookings.view-all` permission). Crew members with basic `bookings.view` can see the Bookings card but not the Dashboard link.

{% hint style="info" %}
The dashboard uses a dark theme optimised for large displays and low-light environments like ops rooms.
{% endhint %}

## Layout

The dashboard layout consists of:

1. **Header** — Logo, live clock, LIVE indicator
2. **Summary Cards** — Four at-a-glance stats
3. **Highlighted Booking** — Featured in-progress booking card (above the map)
4. **Flight Map** — Full-width interactive map
5. **Booking Cards** — Ground Time, Upcoming, and Recently Completed in a 3-column grid below the map

### Header

* **AeroQuote logo** and "Bookings Dashboard" title
* **LIVE indicator** — green pulsing dot confirms the page is actively polling
* **Date and live clock** — updates every second, no manual refresh needed

### Summary Cards

Four cards across the top provide an at-a-glance snapshot:

| Card | Description |
| --- | --- |
| **In Progress** | Number of bookings with active flights (boarding, airborne) |
| **Upcoming** | Number of confirmed bookings that haven't started yet |
| **Active Legs** | Currently airborne flight legs vs total legs across all bookings |
| **Ground Time** | Bookings waiting between flight legs (e.g. overnight stops) |

## Booking Rotation

When **multiple bookings are in progress** simultaneously, the dashboard automatically cycles through them every **10 seconds**:

* A **highlighted booking card** appears above the map showing full flight details
* The **map zooms** to show only that booking's airports and flight trail
* A **progress bar** at the top of the card shows the rotation countdown
* **Dot indicators** below the card let you manually jump to a specific booking
* All other bookings' markers remain visible on the map but don't affect the zoom

When only **one booking** is in progress, the highlighted card is shown without rotation.

## Activity Feed

Recent activity is displayed as a **popup modal** that appears automatically when the page loads:

* Shows the **last 6 events** across all bookings
* **Auto-dismisses after 10 seconds** with a progress bar countdown
* Can be dismissed early with the **X button** or by clicking outside
* Shows only once per page load

Activity events include:

* **Passenger check-ins** — Name, flight route, booking code
* **Boarding commenced** — Route, aircraft registration
* **Departed** — Route, aircraft, booking code (auto-detected or confirmed by crew)
* **Arrived** — Route, aircraft, booking code (auto-detected or confirmed by crew)

When an **Arrived** event is shown for a recently completed booking with saved flight track data, the **actual flight track map** is displayed below the event list — showing the real path flown as captured by FlightRadar24.

Events from **recently completed bookings** (within the last 2 hours) are included in the feed, so "Arrived" events don't disappear immediately when a booking transitions to Completed status.

## Flight Map

The map is **full-width** and adapts based on flight status:

### When flights are airborne ("Live Flight Map")

* **Blue markers** — Departure airports
* **Green markers** — Arrival airports
* **Orange arrow** — Current aircraft position and heading, with registration label
* **Blue trail line** — Actual flight path from position tracking data
* **Dashed grey line** — Planned route (shown for flights without position data yet)

### When aircraft are on the ground between legs ("Ground Time")

For multi-leg bookings in ground time, the map shows the full journey context:

* **Dimmed grey trail** — Completed leg's flight path (faded to show it's finished)
* **Orange aircraft marker** — Aircraft position at the current airport, with registration label
* **Dashed green line** — Route to the next destination
* **Green destination marker** — Next arrival airport (slightly larger to draw attention)

### When no flights are airborne or on ground ("Upcoming Routes")

* **Muted airport markers** — All departure and arrival airports for upcoming bookings
* **Dashed amber lines** — Planned routes for all upcoming flights

The map automatically transitions between these three modes as flights depart, land, and enter ground time.

{% hint style="info" %}
Flight tracking must be enabled in **Settings > Integrations** for position data to appear.
{% endhint %}

## Booking Cards

Below the map, booking cards are displayed in a **3-column grid** grouped by status:

### Ground Time

Multi-leg bookings where all current flights have landed but future legs are scheduled. Shows:

* "Next leg in X hours" — countdown to the next scheduled departure
* Completed legs with actual arrival times
* Upcoming legs with scheduled departure times

### Upcoming

Confirmed bookings that haven't started yet, ordered by departure time. Shows:

* Scheduled departure time and "Departs in X" countdown
* Route, crew, aircraft, and passenger count

### Recently Completed

Bookings that finished within the **last 2 hours**, then automatically removed. When a completed booking has saved flight track data, the **actual flight track** is shown as a map thumbnail on the card — displaying the real path flown rather than a straight-line route.

## Actual Flight Tracks

When a flight completes, AeroQuote automatically fetches the complete flight track from FlightRadar24. This track data is used to:

* Show the **real path flown** on recently completed booking cards (as a static map thumbnail)
* Replace the simple departure-to-arrival line in the **bookings list** with the actual route
* Display in the **activity modal** when an "Arrived" event is present

## Automatic Flight Tracking

When flight tracking is enabled, AeroQuote automatically detects key flight events via **FlightRadar24**:

* **Block off** — Detected when the aircraft begins taxiing (ground movement detected)
* **Departure** — Detected when the aircraft becomes airborne
* **ETA updates** — In-flight estimated arrival time updated at key milestones
* **Arrival** — Detected when the aircraft lands near the destination airport
* **Block on** — Estimated after arrival

Crew can always override auto-detected times via the mobile app — **crew-confirmed times always take precedence** over automated tracking.

### Disabling tracking per aircraft

FlightRadar24 tracking can be disabled for individual aircraft from the **Aircraft Details** page using the **FlightRadar24 Tracking** toggle. Sample aircraft created during operator signup have tracking disabled by default to prevent unnecessary API calls.

## Booking Completion Email

When a booking is fully completed and all block times have been recorded (approximately 2 hours after the final flight lands), AeroQuote automatically sends a **completion summary email** to:

* The **operator** — includes planned vs actual duration variance analysis per flight
* All **assigned crew members** — flight summary without cost analysis

The email includes per-flight details: block off/on times, departure/arrival times, actual duration, and a static map showing the actual flight track (when available).

## Booking Expiry

Bookings that are still in **Confirmed** or **Ground Time** status 24 hours after their last flight has ended are automatically marked as **Expired**.

{% hint style="info" %}
Expired bookings are **not deleted** — they can be reverted to Confirmed at any time.
{% endhint %}

## Auto-Refresh

The dashboard automatically refreshes every **60 seconds**. The page also performs a full reload every **4 hours** for long-running stability.

## Permissions

The Bookings Dashboard and Analytics page require the **bookings.view-all** permission, which is available to:

* **Account Administrator**
* **Manager**
* **Chief Pilot**

Users with only `bookings.view` (Crew role) can access the bookings list and their assigned bookings, but cannot access the dashboard or analytics.

## Tips for Ops Rooms

* **Full-screen mode** — Press `F11` (Windows) or `Cmd Ctrl F` (Mac) for a true full-screen experience
* **Prevent sleep** — Configure your display to stay awake, or use a "keep awake" browser extension
* **Multiple monitors** — Open the dashboard on a dedicated screen while using the main AeroQuote app on another
* **Session timeout** — The page includes an auto-refresh meta tag to keep the session alive
