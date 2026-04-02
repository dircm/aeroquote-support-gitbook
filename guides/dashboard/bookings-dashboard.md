---
description: >-
  The Bookings Dashboard is a real-time operations display designed to give your
  team a live overview of all flight activity. It's purpose-built for
  wall-mounted TVs, dedicated monitors, or a second scr
---

# Bookings Dashboard

## Opening the Dashboard

The Bookings Dashboard is accessed from the **Bookings card** on the operator Home page:

1. Log in to AeroQuote
2. From the Home dashboard, find the **Bookings** summary card (shows total bookings, in-progress count, and upcoming count)
3. Click the **Dashboard** link (with TV icon) on the right side of the card footer — it opens in a **new browser tab**

The Dashboard link is only visible to users with **Manager**, **Account Administrator**, or **Chief Pilot** roles .

{% hint style="info" %}
The dashboard uses a dark theme optimised for large displays and low-light environments like ops rooms. This cannot be changed.
{% endhint %}

## Layout

<figure><img src="../../.gitbook/assets/Screenshot 2026-03-31 at 1.20.02 pm.png" alt=""><figcaption></figcaption></figure>

The dashboard layout consists of:

1. **In-progress Bookings** — in-progress booking card&#x20;
2. **Flight Map** — Auto adjusting Non-interactive map
3. **Other Booking Cards** — Ground Time, Upcoming, and Recently Completed in that order below any in-progress bookings

### Activity Feed

<figure><img src="../../.gitbook/assets/Activity Feed.png" alt=""><figcaption></figcaption></figure>

Recent activity is displayed as a **popup modal** that appears automatically when activity is recorded:

* Shows the **last 6 events** across all bookings
* **Auto-dismisses after 10 seconds** with a progress bar countdown
* Can be dismissed early with the **X button** or by clicking outside

Activity events include:

* **Passenger check-ins** — Name, flight route, booking code
* **Boarding commenced** — Route, aircraft registration
* **Departed** — Route, aircraft, booking code (auto-detected or confirmed by crew)
* **Arrived** — Route, aircraft, booking code (auto-detected or confirmed by crew)

{% hint style="info" %}
Events from **recently completed bookings** (within the last 2 hours) are included in the feed, so "Arrived" events don't disappear immediately when a booking transitions to Completed status.
{% endhint %}

### Flight Map

<figure><img src="../../.gitbook/assets/Bookings Dashboard map.png" alt=""><figcaption></figcaption></figure>

The map auto-adapts and zooms to tracks based on flight status:

#### When flights are airborne ("Live Flight Map")

* **Blue markers** — Departure airports
* **Green markers** — Arrival airports
* **Orange arrow** — Current aircraft position and heading, with registration label
* **Blue trail line** — Actual flight path from position tracking data
* **Dashed grey line** — Planned route (shown for flights without position data yet)

#### When aircraft are on the ground between legs ("Ground Time")

For multi-leg bookings in ground time, the map shows the full journey context:

* **Dimmed grey trail** — Completed leg's flight path (faded to show it's finished)
* **Orange aircraft marker** — Aircraft position at the current airport, with registration label
* **Dashed green line** — Route to the next destination
* **Green destination marker** — Next arrival airport (slightly larger to draw attention)

#### When no flights are airborne or on ground ("Upcoming Routes")

* **Muted airport markers** — All departure and arrival airports for upcoming bookings
* **Dashed amber lines** — Planned routes for all upcoming flights

The map automatically transitions between these three modes as flights depart, land, and enter ground time.

{% hint style="info" %}
Flight tracking must be enabled in **Settings > Integrations** for position data to appear.
{% endhint %}

### Booking Cards

<figure><img src="../../.gitbook/assets/Booking Cards.png" alt=""><figcaption></figcaption></figure>

To the right of the map, booking cards are displayed grouped by status:

#### In-progress

Bookings that have starting boarding, taxiing, in-flight ordered by departure time. Shows:

* Actual departure time and also in hours and minutes ago
* Passenger checked-in count
* ETA of next arrival
* Flight telemetry data
* Route

#### Ground Time

Multi-leg bookings where all current flights have landed but future legs are scheduled. Shows:

* "Next leg in X hours" — countdown to the next scheduled departure
* Completed legs with actual arrival times
* Upcoming legs with scheduled departure times

#### Upcoming

Confirmed bookings that haven't started yet, ordered by departure time. Shows:

* Scheduled departure time and "Departs in X" countdown
* Route, crew, aircraft, and passenger count

#### Recently Completed

Bookings that finished within the **last 2 hours**, then automatically removed. When a completed booking has saved flight track data, the **actual flight track** is shown as a map thumbnail on the card — displaying the real path flown rather than a straight-line route.

### Actual Flight Tracks

When a flight completes, AeroQuote automatically fetches the complete flight track from FlightRadar24. This track data is used to:

* Show the **real path flown** on recently completed booking cards (as a static map thumbnail)
* Replace the simple departure-to-arrival line in the **bookings list** with the actual route
* Display in the **activity modal** when an "Arrived" event is present

### Automatic Flight Tracking

When flight tracking is enabled, AeroQuote automatically detects key flight events via **FlightRadar24**:

* **Off Block** — Detected when the aircraft begins taxiing (ground movement detected)
* **Departure** — Detected when the aircraft becomes airborne
* **ETA updates** — In-flight estimated arrival time updated at key milestones
* **Arrival** — Detected when the aircraft lands near the destination airport
* **On Block** — Estimated after arrival

{% hint style="success" %}
Crew can always override auto-detected times via the mobile app — **crew-confirmed times always take precedence** over automated tracking.
{% endhint %}

#### Disabling tracking per aircraft

FlightRadar24 tracking can be disabled for individual aircraft from the **Aircraft Details** page using the **FlightRadar24 Tracking** toggle. Sample aircraft created during operator signup have tracking disabled by default.

### Auto-Refresh

The dashboard automatically refreshes every **60 seconds**. The page also performs a full reload every **4 hours** for long-running stability.

### Tips for Ops Rooms



* **Full-screen mode** — Press `F11` (Windows) or `Cmd Ctrl F` (Mac) for a true full-screen experience
* **Prevent sleep** — Configure your display to stay awake, or use a "keep awake" browser extension
* **Multiple monitors** — Open the dashboard on a dedicated screen while using the main AeroQuote app on another
* **Session timeout** — The page includes an auto-refresh meta tag to keep the session alive, no need to refresh.
