---
description: >-
  Run Out Report, due items, pending hours confirmation, and the Crew app
  views that come with the Maintenance Tracker add-on.
---

# Maintenance Tracker

The Maintenance Tracker is an add-on module. It builds on [Maintenance Limits](maintenance-limits.md): confirmed flight hours, landings and engine cycles flow into a live due list (the **Run Out Report**), with program items, components, sign-offs and an audit trail.

{% hint style="info" %}
The Maintenance Tracker is enabled per operator by AeroQuote. Contact [support@aeroquote.com](mailto:support@aeroquote.com) to switch it on. There is no self-serve toggle for it on **Settings → Modules** yet.

**Aircraft Maintenance** (running totals and baselines) is a separate feature and should also be on, otherwise hours will not roll into the report. See [Maintenance Limits](maintenance-limits.md).
{% endhint %}

When the module is off, **Maintenance → Run Out Report** is hidden in the web app. In the AeroQuote Crew app, operators without the module do not see maintenance features — only the profile avatar and the **Aircraft** tab (and the dashboard **Fleet** / **View Fleet** entry) are shown to everyone. See [In the Crew app](#in-the-crew-app).

***

## Open the Run Out Report

1. Click **Maintenance → Run Out Report** in the sidebar, or open an aircraft and click **Run Out Report**
2. Use the **Aircraft** selector to see one aircraft or **All aircraft**

| Column | Meaning |
| ------ | ------- |
| Status | Green, amber or red for the item as a whole (the worst of its limits) |
| Aircraft | Registration |
| Item | Item title, reference and any component it applies to |
| **Hours remaining** | Hours to the next due point, in tenths |
| **Days remaining** | Days to the calendar due date (Days or Months limits) |
| **Cycles remaining** | Cycles to the next due point |
| Limits (whichever first) | Each limit with its own colour and due point. The limit driving the forecast is in bold. Tolerance is shown, and “using tolerance” appears when an item is past due but still inside its + tolerance |
| **Forecast due** | The date the item is expected to fall due |
| View | Opens the item page for sign-off, editing and history |

The report is sorted red first, then amber, then green, then by forecast date.

If Aircraft Maintenance is off, the report shows: *Aircraft hours capture is off for this operator, so flight hours, cycles and landings will not roll into the run out report.*

### Traffic lights

| Status | Meaning |
| ------ | ------- |
| 🟢 Green | Not yet within the amber threshold |
| 🟠 Amber | Within the amber threshold, or past due but still inside the + tolerance |
| 🔴 Red | Past due plus tolerance |

The default amber thresholds are 10 hours, 10 cycles, 10 landings and 30 days. A limit can override its own threshold.

### How the forecast works

* Calendar limits use their due date.
* Hours, cycles and landings: AeroQuote divides what remains by the aircraft's average daily use, calculated from confirmed flights over a recent window (90 days by default).
* If the baseline is newer than the window, the average uses the days since the baseline, but never fewer than 30 days.
* If an aircraft has no recent confirmed flying, no forecast is shown for its usage-based limits.
* When one aircraft is selected, its utilisation (hours per day and landings per day over the window) is shown beside the selector.

***

## Confirmed and pending hours

Only **confirmed** hours count towards the totals and the Run Out Report.

* **Counted automatically:** an **On Block** time that crew record in the Crew app for their booking leg. That marks the flight's hours as confirmed, so the office does not need to confirm it again.
* **Pending until confirmed on the web:** hours that come from flight tracking (FlightAware or Flightradar24) or from [Flight Logs](../bookings-operators/flight-tracking/flight-logs.md) entries. These show **Hours pending confirmation** until someone with aircraft edit permission confirms them in Flight Logs.

On the Run Out Report, an amber link shows **N flights pending hours confirmation — review in Flight Logs**. Click it to open Flight Logs with those flights selected.

In **Flight Logs**:

* A count of **N flights pending hours confirmation** is shown at the top, and each such flight has an **Hours pending confirmation** badge.
* Open a flight, review the times, check **Landings** and **Cycles** under **Confirm hours**, then click **Confirm hours**.
* Or tick several pending flights (Flight Logs entries that are not on a booking) and click **Confirm N selected**.

Confirming does not change the flight times. It records you as the reviewer, posts the hours to the aircraft totals once, and writes an audit entry. Newly confirmed flights are credited in tenths of an hour (see [Aircraft time in tenths](maintenance-limits.md#aircraft-time-in-tenths)). Flights confirmed before this rule was introduced are not changed.

Flights with on-block times before the aircraft's baseline are covered by the baseline and never appear as pending.

If flight tracking later revises the block times on a confirmed Flight Logs entry that is not on a booking, the flight goes back to pending and its hours are taken out of the totals until it is confirmed again.

{% hint style="info" %}
There is no Confirm hours or Pending hours screen in the Crew app. Confirm tracked or logged hours on the web in Flight Logs. See [How hours work](../bookings-operators/flight-tracking/flight-logs.md#how-hours-work).
{% endhint %}

***

## Add components

Register engines, propellers and other components.

1. Select the aircraft, then click **Add component**
2. Choose the type (engine, propeller or component) and enter the name, part number, serial number and position (for example #1 / LH)
3. Enter current **TSN** (hours), **CSN**, and if known **TSO** / **CSO**
4. Choose where it is installed: directly on the aircraft, or on a parent component (for example a starter generator on an engine)
5. Click **Add component**

From then on, component times grow with the aircraft. Component cycles are the aircraft's engine cycles divided by its engine count.

### Remove, install and overhaul

* **Remove** closes the installation record and stops counters accumulating. Child components stay with their parent.
* **Install** fits the component to an aircraft or parent component; install history is kept.
* **Overhauled** resets TSO and CSO to zero.

To track a program item against a component (for example an engine's overhaul life), choose the component when you add the item.

***

## Add program items

1. On the **Run Out Report**, select the aircraft in the **Aircraft** selector (the form asks you to choose an aircraft first)
2. In **Add program item**, enter the **Title** (for example “100 hourly inspection”) and an optional **Reference**
3. Choose whether it applies to the aircraft or to an installed component
4. Leave **Recurring** ticked for repeating items; untick it for a one-off
5. Add one or more limits: **Hours**, **Cycles**, **Landings**, **Days** or **Months**. For each limit, enter **Every** (the interval), optional **+ tol** and **− tol**, and **Last done at**
6. Click **Add another limit** for a second limit (for example 100 hours or 12 months, whichever first). Each limit type can be used once per item
7. Click **Add item**

The item is due at **whichever limit comes first**.

For Hours, Cycles and Landings, **Last done at** is the aircraft or component figure when it was last done. For Days and Months, it is the date. Leave it blank to start counting from now. Intervals must be greater than zero, and Cycles and Landings intervals must be whole numbers.

The amber threshold is set per limit when you [edit an item](#edit-an-item-and-its-limits). If you leave it blank, the operator default is used.

***

## Record a sign-off

When the maintenance has been done and certified:

1. On the Run Out Report, click **View** on the item, then **Sign off**
2. Enter the **Completed date** (today or earlier)
3. Check **Aircraft hours at completion**. It is pre-filled with the current figure; change it to the hours recorded at completion. **Cycles at completion** and **Landings at completion** also appear when the item has those limits
4. Enter **Signed off by (name / licence)**. Your own AeroQuote name is also recorded as the user who entered it
5. Add the **Work order / reference** (optional) and **Notes**
6. Click **Record sign-off**. The message **Sign-off recorded. Next due has been rolled forward.** confirms it

### How next due rolls forward

* Every limit on the item rolls forward from the completion values you entered.
* If the work was done inside the tolerance window (from due minus − tolerance to due plus + tolerance), the next due is counted from the **scheduled** due point, so using tolerance does not shift the schedule.
* If it was done outside the window, the next due is counted from the actual completion.
* A one-off (non-recurring) item becomes inactive once signed off.

### Void a sign-off

If a sign-off was recorded in error, open the item page, find it in **Sign-off history**, and click **Void sign-off** (shown to users with aircraft edit permission). Enter the **Reason (required)** and click **Void and recalculate**.

A voided sign-off is never deleted. It stays in the history marked **Voided**, and the item's due state goes back to what it was before that sign-off.

***

## Edit an item and its limits

1. On the Run Out Report, click **View** on the item
2. Click **Edit item** (shown to users with aircraft edit permission)
3. Change the **Description**, **Reference**, **Notes**, **Recurring** or **Active** as needed
4. For each limit you can change the **Limit type**, **Interval**, **Amber threshold**, **Tolerance +** and **Tolerance −**, the **Last done value** (or **Last done date** for calendar limits), and set a **Next due override** if needed
5. Use **Add limit** or **Remove limit** as needed. An item needs at least one limit
6. Click **Save and recalculate**

Next due is recalculated from the existing last-done values. The sign-off history is not changed. Untick **Active** to take an item off the Run Out Report without deleting it.

The item page also has **Maintenance audit history**: an append-only record of item and sign-off changes, each with date and time, user, and expandable before and after values. Entries cannot be edited or deleted.

***

## In the Crew app

In the Crew app, a user sees and can update only the aircraft on their **Fleet list**: the aircraft on bookings where they are rostered as air or ground crew.

### When the Maintenance Tracker is on

On the **Aircraft** tab, each aircraft card can show:

* TTIS, landings and cycles pills (or **No maintenance baseline set**), when Aircraft Maintenance is also on
* A **Due Items** button with a count and a colour dot for the worst status (green **OK**, amber **Due soon**, red **Overdue**)
* A **Maintenance totals** button, when both Aircraft Maintenance and the Maintenance Tracker are on

**Due Items** (titled **Due Items** or **Due Items · {registration}**) lists the aircraft's active items, worst first, with what remains on the limit that will come first and the status. Tap an item to see each limit, whether it is **in tolerance**, the **Forecast** due date, and the **Last sign-off**. Sign-off and void are done on the web only.

**Maintenance totals** shows **Current totals**, the **Entered baseline** (with **As at**, **Reason**, who entered it and when) and **Since baseline**. Users with the **Aircraft - Maintenance Totals** permission (or aircraft edit permission) can tap **Update** to enter a new dated baseline, using **Decimal hours** or **hh:mm**. This needs a connection and is never queued offline. See [Updating a baseline](maintenance-limits.md#update-a-baseline).

### Recording flight times

On a live booking leg, crew can set and edit **Off Block**, **Departure**, **ETD** (until the flight has departed), **ETA** (while airborne), **Arrival** and **On Block**. Those crew-entered times override FlightAware and Flightradar24 for that flight, and can be corrected later on the same live leg.

Recording **On Block** counts towards the aircraft totals (if the aircraft has a baseline) and marks the hours as confirmed.

Crew cannot edit older **Flight Log** entries (recorded flights) in the app. Managers correct those on the web with aircraft edit permission. See [Flight Status](../mobile-app/flight-status.md) and [Flight Logs](../bookings-operators/flight-tracking/flight-logs.md).

### When the module is off

Users whose operator does not have the Maintenance Tracker (and does not have Aircraft Maintenance) still see:

* The profile avatar (the first letter of their name)
* The **Aircraft** tab and list, titled **Aircraft Fleet**, with each card showing the image, registration, seats, name, and **Year**, **Max MTOW** and **Range**
* An optional **Show {n} Booking(s)** row when that aircraft appears on synced bookings
* The dashboard **Fleet** / **View Fleet** entry

They do not see TTIS pills, **Due Items**, **Maintenance totals**, or pending hours.

***

## Who can do what

| Action | Who | Where |
| ------ | --- | ----- |
| View the Run Out Report and Due Items | Users with access to the maintenance features (crew: Fleet list aircraft only) | Web and app |
| Set or update a dated baseline | Users with the **Aircraft - Maintenance Totals** permission or aircraft edit permission. By default: account administrator, manager, chief pilot and crew roles | Web (whole fleet) and app (Fleet list only) |
| Confirm tracked or logged flight hours | Users with aircraft edit permission | Web only |
| Create program items and record sign-offs | Users with access to the Run Out Report | Web only |
| Edit items and limits, void sign-offs | Users with aircraft edit permission | Web only |
| Edit live booking flight times | Crew in the app (and operations on the booking). Crew times override FlightAware / Flightradar24 | Crew app and web |
| Edit older Flight Log (recorded flight) times | Office users with aircraft edit permission on the web. Crew cannot edit these in the app | Web only |

An account administrator can remove the **Aircraft - Maintenance Totals** permission from any role at **Settings → Permissions**.

{% hint style="warning" %}
Airworthiness directives, service bulletins, life-limited part alerts, defects and exports are not yet part of the tracker.
{% endhint %}

See also [Maintenance Limits](maintenance-limits.md) for baselines, tenths and the aircraft **Maintenance** tab, and [Flight Logs](../bookings-operators/flight-tracking/flight-logs.md) for **Confirm hours**.
