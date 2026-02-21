# Bookings Dashboard

The Bookings Dashboard is a **real-time operations display** designed to give your team a live overview of all flight activity. It's purpose-built for wall-mounted TVs, dedicated monitors, or a second screen — leave it open and watch your bookings progress through their lifecycle.

## Opening the Dashboard

1. Navigate to **Bookings** from the main menu
2. Click the **Bookings Dashboard** button (top-right of the bookings list)
3. The dashboard opens in a **new browser tab** — full-screen, no navigation

{% hint style="info" %}
The dashboard uses a dark theme optimised for large displays and low-light environments like ops rooms.
{% endhint %}

## Layout

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

### Activity Feed

A live feed strip below the summary cards shows the **last 6 events** across all bookings:

* 👤 **Passenger check-ins** — Name, flight route, booking code
* 🚪 **Boarding commenced** — Route, aircraft registration
* ✈️ **Departed** — Route, aircraft, booking code
* ✅ **Arrived** — Route, aircraft, booking code

Events appear automatically as they happen — no page refresh required.

### Live Flight Map

When any flight is airborne, an interactive map appears showing:

* **Blue markers** — Departure airports
* **Green markers** — Arrival airports
* **Orange arrow** — Current aircraft position and heading
* **Blue trail line** — Flight path so far (position history)

The map uses a dark theme to match the dashboard and updates every 10 seconds.

{% hint style="warning" %}
The map requires a valid Google Maps API key. If the map appears as a grey box, check your API key configuration in Settings.
{% endhint %}

### Booking Sections

Bookings are organised into four sections, each with colour-coded cards:

#### 🔵 In Progress

Bookings with at least one flight currently boarding or airborne. Each card shows:

* **Booking code** (links to the individual booking)
* **Route string** (e.g. YBBN → YSSY)
* **Crew assigned** and **aircraft registration**
* **Check-in progress** (e.g. 3/4 passengers)
* **Departure time** and **ETA** (based on actual departure + flight duration, in the arrival airport's timezone)
* **Live telemetry** — altitude and speed for airborne flights
* **Status badges** per flight leg (Boarding, InProgress, Completed)

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

## Auto-Refresh

The dashboard automatically refreshes every **10 seconds**. There is no need to manually reload the page. All sections — summary cards, activity feed, map, and booking cards — update together.

## Permissions

The dashboard respects existing booking permissions:

* **bookings.view** — Can see bookings they are assigned to as crew
* **bookings.view-all** — Can see all bookings for the operator

## Tips for Ops Rooms

* **Full-screen mode** — Press `F11` (Windows) or `⌘ Ctrl F` (Mac) for a true full-screen experience
* **Prevent sleep** — Configure your display to stay awake, or use a "keep awake" browser extension
* **Multiple monitors** — Open the dashboard on a dedicated screen while using the main AeroQuote app on another
* **Session timeout** — The page includes an auto-refresh meta tag to keep the session alive during the configured session lifetime
