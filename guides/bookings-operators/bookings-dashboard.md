# Bookings Dashboard

The Bookings Dashboard is a **real-time operations display** designed to give your team a live overview of all flight activity. It's purpose-built for wall-mounted TVs, dedicated monitors, or a second screen — leave it open and watch your bookings progress through their lifecycle.

<!-- 📸 PLACEHOLDER: Full-width screenshot of the Bookings Dashboard with active flights, map, and activity feed visible -->
<!-- Suggested filename: .gitbook/assets/bookings-dashboard-hero.png -->
<!-- Dimensions: 1400x900, captured from a wide browser window in dark mode -->

## Opening the Dashboard

1. Navigate to **Bookings** from the main menu
2. Click the **Bookings Dashboard** button (top-right of the bookings list)
3. The dashboard opens in a **new browser tab** — full-screen, no navigation

{% hint style="info" %}
The dashboard uses a dark theme optimised for large displays and low-light environments like ops rooms.
{% endhint %}

## Layout

The dashboard uses a **split-screen layout**:

* **Left half** — Interactive flight map (live tracking or upcoming routes)
* **Right half** — Scrollable list of all booking cards, grouped by status

When there are no active or upcoming bookings, the map is hidden and booking cards take the full width.

### Header

* **AeroQuote logo** and "Bookings Dashboard" title
* **LIVE indicator** — green pulsing dot confirms the page is actively polling
* **Date and live clock** — updates every second, no manual refresh needed

<!-- 📸 PLACEHOLDER: Cropped screenshot of the 4 summary cards (In Progress, Upcoming, Active Legs, Ground Time) -->
<!-- Suggested filename: .gitbook/assets/bookings-dashboard-summary-cards.png -->

### Summary Cards

Four cards across the top provide an at-a-glance snapshot:

| Card | Description |
| --- | --- |
| **In Progress** | Number of bookings with active flights (boarding, airborne) |
| **Upcoming** | Number of confirmed bookings that haven't started yet |
| **Active Legs** | Currently airborne flight legs vs total legs across all bookings |
| **Ground Time** | Bookings waiting between flight legs (e.g. overnight stops) |

<!-- 📸 PLACEHOLDER: Cropped screenshot of the activity feed showing check-in, departure, and arrival events -->
<!-- Suggested filename: .gitbook/assets/bookings-dashboard-activity-feed.png -->

### Activity Feed

A live feed strip below the summary cards shows the **last 6 events** across all bookings:

* 👤 **Passenger check-ins** — Name, flight route, booking code
* 🚪 **Boarding commenced** — Route, aircraft registration
* ✈️ **Departed** — Route, aircraft, booking code (auto-detected or confirmed by crew)
* ✅ **Arrived** — Route, aircraft, booking code (auto-detected or confirmed by crew)

Events appear automatically as they happen — no page refresh required. Departure and arrival events are auto-detected via **FlightRadar24** position tracking, or when crew confirm times via the [mobile app](../mobile-app/flight-status.md). The source (e.g. FlightRadar24, Crew confirmed) is shown alongside each event.

When a flight arrives, AeroQuote automatically saves the complete flight track. This track is displayed as a route map on the booking's itinerary card — no manual action required.

<!-- 📸 PLACEHOLDER: Screenshot of the live flight map showing dark theme, position trail, airport markers, and aircraft arrow -->
<!-- Suggested filename: .gitbook/assets/bookings-dashboard-live-map.png -->

### Flight Map

The map occupies the **left half of the screen** and adapts based on flight status:

#### When flights are airborne ("Live Flight Map")

* **Blue markers** — Departure airports
* **Green markers** — Arrival airports
* **Orange arrow** — Current aircraft position and heading, with registration label
* **Blue trail line** — Actual flight path from position tracking data
* **Dashed grey line** — Planned route (shown for flights without position data yet)

#### When no flights are airborne ("Upcoming Routes")

* **Muted airport markers** — All departure and arrival airports for upcoming bookings
* **Dashed amber lines** — Planned routes for all upcoming flights, giving a visual overview of what's ahead

The map automatically transitions between these modes as flights depart and arrive.

Position data is sourced from **FlightRadar24** via ADS-B tracking. The map uses a dark theme to match the dashboard.

{% hint style="info" %}
Flight tracking must be enabled in **Settings → Integrations** for position data to appear. See the [Integrations](../settings/integrations.md) guide for setup.
{% endhint %}

### Booking Cards

All booking cards are displayed on the **right half of the screen** in a scrollable list, ordered by status:

<!-- 📸 PLACEHOLDER: Screenshot of an In Progress booking card showing route, crew, check-in count, ETA, altitude/speed, and status badge -->
<!-- Suggested filename: .gitbook/assets/bookings-dashboard-card-inprogress.png -->

#### 🔵 In Progress

Bookings with at least one flight currently boarding or airborne. Each card shows:

* **Booking code** and **route string** (e.g. YBBN → YSSY)
* **Crew assigned** and **aircraft registration**
* **Check-in progress** (e.g. 3/4 passengers)
* **Departure time** and **ETA** — When FlightRadar24 provides an estimated arrival time, the source is shown (e.g. "ETA FlightRadar24"). Otherwise, a calculated ETA based on departure time + flight duration is shown as "ETA (calc)". Times are displayed in the arrival airport's timezone.
* **Live telemetry** — altitude and speed for airborne flights
* **Status badges** per flight leg (Boarding, InProgress, Completed)

<!-- 📸 PLACEHOLDER: Screenshot of a Ground Time booking card showing completed outbound leg and upcoming return leg -->
<!-- Suggested filename: .gitbook/assets/bookings-dashboard-card-groundtime.png -->

#### 🟠 Ground Time

Multi-leg bookings where all current flights have landed but future legs are scheduled. For example, a return flight departing the next day. The card shows:

* "Next leg in X hours" — countdown to the next scheduled departure
* Completed legs with actual arrival times
* Upcoming legs with scheduled departure times

{% hint style="info" %}
**Ground Time** is an automatic status. When a flight leg completes and the booking has future legs, the booking transitions to Ground Time. When the next leg's boarding begins, it returns to In Progress.
{% endhint %}

#### 🟡 Upcoming

Confirmed bookings that haven't started yet, ordered by departure time. Shows:

* Scheduled departure time and "Departs in X" countdown
* Route, crew, aircraft, and passenger count

#### ✅ Recently Completed

Bookings that finished within the **last 2 hours**, then automatically removed. Provides a brief record of today's completed operations.

## Automatic Flight Tracking

When flight tracking is enabled, AeroQuote automatically detects key flight events via **FlightRadar24**:

* **Block off** — Detected when the aircraft begins taxiing (ground movement detected)
* **Departure** — Detected when the aircraft becomes airborne
* **Arrival** — Detected when the aircraft lands near the destination airport
* **Block on** — Estimated after arrival

Crew can always override auto-detected times via the mobile app — **crew-confirmed times always take precedence** over automated tracking.

## Booking Expiry

Bookings that are still in **Confirmed** or **Ground Time** status 24 hours after their last flight has ended are automatically marked as **Expired**. This keeps the dashboard and mobile app uncluttered by clearing out bookings the operator forgot to close.

{% hint style="info" %}
Expired bookings are **not deleted** — they can be reverted to Confirmed at any time from the booking details page using the **Revert to Confirmed** button. Expired bookings are hidden from the mobile app and the Bookings Dashboard.
{% endhint %}

## Auto-Refresh

The dashboard automatically refreshes every **60 seconds**. There is no need to manually reload the page. All sections — summary cards, activity feed, map, and booking cards — update together.

## Permissions

The dashboard respects existing booking permissions:

* **bookings.view** — Can see bookings they are assigned to as crew
* **bookings.view-all** — Can see all bookings for the operator

<!-- 📸 PLACEHOLDER: Photo or mockup of the Bookings Dashboard displayed on a wall-mounted TV in an ops room setting -->
<!-- Suggested filename: .gitbook/assets/bookings-dashboard-tv-mockup.png -->
<!-- This could be a real photo or a device-frame mockup showing the dashboard on a large screen -->

## Tips for Ops Rooms

* **Full-screen mode** — Press `F11` (Windows) or `⌘ Ctrl F` (Mac) for a true full-screen experience
* **Prevent sleep** — Configure your display to stay awake, or use a "keep awake" browser extension
* **Multiple monitors** — Open the dashboard on a dedicated screen while using the main AeroQuote app on another
* **Session timeout** — The page includes an auto-refresh meta tag to keep the session alive during the configured session lifetime
