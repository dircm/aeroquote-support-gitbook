---
description: Turn on flight tracking, configure aircraft identifiers, and understand per-aircraft opt-out.
---

# Enabling & Configuration

---

## Prerequisites

1. **Bookings access** — Subscribe to the Bookings module, or use Scheduled Flights / Tour Packages (these include bookings functionality).
2. **Flight Tracking toggle** — **Settings → Integrations → Flight Tracking** → ON.

The toggle is turned on automatically when you subscribe to Bookings in many cases. Operators on older accounts can ask support to verify `flight_tracking_enabled` if the toggle is missing.

{% hint style="warning" %}
Without a valid aircraft identifier (registration or flight number), AeroQuote cannot match your leg to FlightRadar24. Check the **Details** tab on each booking before departure day.
{% endhint %}

---

## Per-booking identifiers

Open a booking → **Details** tab → expand each aircraft group:

| Field | Purpose |
| --- | --- |
| **Assigned registration** | Overrides the fleet registration for this booking only — use when the flying tail differs from the default aircraft record (e.g. dry lease, sub-charter). |
| **Flight number** | Fallback lookup when registration is unavailable or not tracked. |

These fields feed the same lookup order described in the [Flight Tracking overview](README.md).

---

## Per-aircraft opt-out

On **Aircraft → Details**, the **FlightRadar24 Tracking** toggle disables automatic polling for that airframe. Sample aircraft created at signup often have this off by default.

Use opt-out for:

* Aircraft never on ADS-B
* Test / placeholder fleet rows
* When you rely entirely on crew mobile updates for that type

Crew mobile updates still work when FR24 tracking is disabled on the aircraft.

---

## Operator-level checklist

| Step | Action |
| --- | --- |
| 1 | Confirm Bookings module is active (**Settings → Modules**) |
| 2 | Enable **Flight Tracking** (**Settings → Integrations**) |
| 3 | Ensure each active aircraft has a valid **registration** |
| 4 | Assign crew to legs that should receive push notifications |
| 5 | For multi-leg charters, verify **occurring_at** and **duration** on each leg — used for ETA, inference, and expiry logic |

---

## What crew need

Crew assigned to a leg receive:

* **Visible** push notifications for FR24-detected **departure** and **arrival** (confirm or adjust in the app)
* **Silent** background sync when block off or ETA updates from FR24 (app refreshes without a banner)

See [Flight Status (Mobile)](../../mobile-app/flight-status.md) for the full crew workflow.

---

## Troubleshooting badges (Details tab)

| Badge | Meaning |
| --- | --- |
| **FR24 tracking on** | Identifier valid and tracking enabled |
| **Tracking off (account)** | Flight Tracking toggle disabled in Integrations |
| **Tracking off (aircraft)** | `FlightRadar24 Tracking` disabled on the aircraft |
| **Tracking off (invalid format)** | Registration or flight number fails validation |
| **No FR24 history** | Identifier looks valid but FR24 has no recent flights for that tail — common for new registrations or remote operations |

{% hint style="success" %}
**Remote strips?** Pair FR24 where coverage exists with crew **Log Position** and manual departure/arrival on the mobile app. See [Automatic Detection](automatic-detection.md) for how AeroQuote recovers mid-leg coverage gaps.
{% endhint %}

---

## Next steps

* [Automatic Detection](automatic-detection.md) — What happens from taxi to landing
* [Multi-leg Rotations](multi-leg-rotations.md) — Ground time, inference, booking completion vs expiry