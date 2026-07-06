---
description: Multi-leg booking tracking — leg sequencing, Ground Time, inferred milestones, and when bookings complete vs expire.
---

# Multi-leg Rotations

Charter rotations and scheduled multi-stop routes fly several legs in one booking. Flight tracking treats each leg separately but shares one aircraft registration across the day.

---

## Leg sequencing rule

**The next leg cannot depart** (automatically or via scheduled auto-run) until the previous leg has **arrived** or recorded **block on**.

This prevents leg 3 from picking up FR24 data while leg 2 is still airborne.

| Booking status | Meaning |
| --- | --- |
| **In Progress** | At least one leg is boarding, taxiing, or airborne |
| **Ground Time** | Current leg(s) finished; a future leg is still scheduled |
| **Completed** | Every leg is completed |

The [Bookings Dashboard](../../dashboard/bookings-dashboard.md) map shows completed legs as a faded trail, the aircraft at the current airport, and a dashed line to the next destination during Ground Time.

---

## When coverage is patchy

Remote rotations often match this pattern:

1. Leg 1 — FR24 sees departure; coverage lost before arrival; arrival inferred or detected late
2. Leg 2 — Never seen on the ground at origin; FR24 resumes **mid-route**
3. Later legs — Mixed partial coverage

AeroQuote handles this in layers:

### 1. Mid-leg FR24 recovery

If FR24 shows the aircraft en route on leg 2's corridor, departure is recorded even when the origin airport was never seen. See [Automatic Detection](automatic-detection.md).

### 2. Inferred milestones (`inferred` source)

If the rotation **stalled** — a leg never got departure/arrival but the booking clearly flew — AeroQuote can fill missing milestones from the **schedule** (each leg's `occurring_at` and `duration`).

Inferred times respect what actually happened: when an earlier leg ran late, the following legs shift to the **real arrival plus a minimum turnaround** — a leg is never shown departing before the aircraft had landed from the previous one.

**Inference only runs when there is real evidence** on the booking:

* FR24 or FlightAware on a milestone, or
* Crew manual / GPS confirmation, or
* At least one FR24 position stored on any leg

**Inference waits when live detection is likely:**

* If the previous leg's arrival was tracked **down to the surface** (good ADS-B coverage at that airport), the next departure is left for FR24 to detect — for up to **six hours** past the expected departure, after which inference proceeds so the booking still resolves
* Nothing is inferred while the aircraft has an FR24 sighting in the last **30 minutes** — live tracking takes over

Inferred times are labelled **(estimated)** in the Status tab. Crew updates always overwrite them, and AeroQuote keeps watching FR24 for estimated legs — if the aircraft is detected, the estimate is replaced with the **real takeoff time** automatically.

A background job checks stalled bookings every **10 minutes** after the booking's end time.

### 3. Completion vs expiry (24-hour rule)

If a booking sits in **Confirmed** or **Ground Time** for more than **24 hours after the last leg's scheduled end** (`ends_at`):

| Situation | Outcome |
| --- | --- |
| **No leg ever departed** | Booking → **Expired** (operator emailed; can revert to Confirmed) |
| **At least one leg departed** | Remaining legs inferred when evidence exists → booking → **Completed** (not expired) |

{% hint style="info" %}
You receive a **warning email** around 12 hours before the 24-hour cutoff if the booking is still open — time to confirm legs manually or verify tracking identifiers.
{% endhint %}

---

## Example: four-leg remote charter

| Leg | Route | Risk |
| --- | --- | --- |
| 1 | Base → remote strip A | Coverage gap before arrival |
| 2 | A → remote strip B | First ADS-B mid-route |
| 3 | B → remote strip C | Departure missed; partial en-route |
| 4 | C → base | Departure missed; arrival seen at base |

With leg 1 confirmed by FR24, AeroQuote can:

* Recover leg 2 via mid-route sighting
* Infer legs 3–4 times from schedule after the rotation ends — shifted to match any delay, and waiting for real detection first where coverage is good
* Mark the booking **Completed** instead of **Expired**

Without any FR24 or crew evidence, inference does not run — operators should record times manually on the mobile app.

---

## Scheduled flights: auto-run

Published scheduled departures can enable **Auto run departures** at route or departure level. When enabled (and crew have not taken manual ownership), AeroQuote progresses boarding, departure, simulated positions, and arrival on the timetable.

**Crew and FR24 always beat auto-run.** Simulated map positions show **(estimated)**.

This is separate from charter **inferred** recovery — auto-run is for timetable-driven scheduled services.

---

## Operator actions when tracking stalls

1. Open the booking **Status** tab — which leg is stuck?
2. Check **Details** — registration, tracking badges, FR24 history warning
3. Ask crew to **confirm departure/arrival** on the mobile app (locks times, unblocks next leg)
4. If the rotation finished but web status lags, wait for the inference job or contact support with booking code and tail number

---

## Next steps

* [Enabling & Configuration](enabling-and-configuration.md)
* [Booking Status](../booking-status.md)
* [Amendments](../amendments.md) — full audit trail of status changes