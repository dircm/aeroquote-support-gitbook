---
description: >-
  Running totals (TTIS, landings and engine cycles), dated baselines, tenths
  of an hour, and tracked items on each aircraft.
---

# Maintenance Limits

Aircraft Maintenance keeps a running total of each aircraft's time in service (TTIS), landings and engine cycles, built from a dated baseline plus confirmed flights. It also supports simpler **Tracked items** on the aircraft **Maintenance** tab.

The [Maintenance Tracker](maintenance-tracker.md) add-on builds on these totals with the **Run Out Report**, program items, sign-offs and **Due Items** in the Crew app.

{% hint style="info" %}
Aircraft Maintenance is enabled per operator by AeroQuote. Once it is on, an **Aircraft Maintenance** card (labelled **Free**) appears under **Settings → Modules**, so you can disable or re-enable it. Contact [support@aeroquote.com](mailto:support@aeroquote.com) if you do not see the card.

The **Maintenance** tab appears on each aircraft when the feature is on. **Limits → Aircraft Maintenance** in the sidebar opens the fleet status view.
{% endhint %}

***

## Open the Maintenance tab

1. Click **Aircraft** in the sidebar
2. Open an aircraft
3. Select the **Maintenance** tab

An aircraft with no baseline shows **Maintenance tracking not set up**. Until a baseline is set, AeroQuote does not count its hours.

***

## Aircraft time in tenths

TTIS, maintenance intervals and hours remaining are always shown in tenths of an hour (for example 1209.6 h), using this 6-minute table:

| Minutes | Tenth | Minutes | Tenth |
| ------- | ----- | ------- | ----- |
| 0–3 | .0 | 34–39 | .6 |
| 4–9 | .1 | 40–45 | .7 |
| 10–15 | .2 | 46–51 | .8 |
| 16–21 | .3 | 52–57 | .9 |
| 22–27 | .4 | 58–60 | 1.0 (next hour) |
| 28–33 | .5 |  |  |

When a newly confirmed flight is added to the totals, it is credited using the same table. A 9-minute flight credits 0.1 h; a 1 h 32 min flight credits 1.5 h.

Flights confirmed before this rule was introduced, and baselines already entered, are not changed unless you edit them. Crew flight and duty time (FTL) is not affected by this rounding.

### Decimal or hh:mm

When you enter TTIS, choose **Decimal** (default) or **hh:mm** under **TTIS format**. Switching between the two does not change the value.

| Entered | Format | Saved as |
| ------- | ------ | -------- |
| 1209.6 | Decimal | 1209.6 h (1209:36) |
| 1209:36 | hh:mm | 1209.6 h (1209:36) |
| 1209:40 | hh:mm | 1209.7 h (1209:42) — snapped to the 6-minute grid when saved |
| 1209.65 | Decimal | Not accepted — use 1209.6 or 1209.7, or switch to hh:mm |

Decimal allows at most one decimal place. A value you don't change is never altered, even if it is off the grid.

***

## Set the first baseline

Do this once per aircraft, using the figures from the logbook or current maintenance release.

1. On the **Maintenance** tab, click **Set baseline**
2. Choose the **TTIS format**: **Decimal** or **hh:mm**
3. Enter **Total Time In Service**. In Decimal, use at most one decimal place (for example 1234.5). In hh:mm, enter hours and two-digit minutes (for example 1234:30)
4. Enter **Total landings** and **Total engine cycles**. Cycles are per engine; the form reminds you how many engines the aircraft has
5. Set the **As at date** (today or earlier) and add notes if you want, for example the logbook reference
6. Click **Set baseline**. The message **Maintenance baseline saved.** is shown, and the **Maintenance running totals** card shows your figures

A baseline is the aircraft's absolute TTIS, landings and engine cycles **as at** a specific date and time. Every baseline records who entered it, when it was entered, the effective (as at) time and the reason.

* Flights whose on-block time is **before** the as-at time never change the totals. They are already included in the baseline figures.
* Confirmed flights whose on-block time is **at or after** the as-at time are added on top.
* The as-at time cannot be in the future, and cannot be earlier than the aircraft's latest baseline.

***

## Update a baseline

Use **Update baseline** whenever the AeroQuote totals need to be brought back into line with the logbook: after a maintenance release, an engine change, a missed flight, or a periodic reconciliation. You enter absolute values as at a date and time, not a difference.

This needs the **Aircraft - Maintenance Totals** permission or aircraft edit permission. By default it is granted to the account administrator, manager, chief pilot and crew roles. An account administrator can change that at **Settings → Permissions**.

1. Open the aircraft's **Maintenance** tab and click **Update baseline**
2. Set **As at** to the date and time the logbook figures apply. The time is in the operator's time zone, which is shown in the form
3. Choose the **TTIS format** and check or enter the **TTIS**. The form is pre-filled with the current totals
4. Check or enter **Total landings** and **Engine cycles**
5. Enter a **Reason** (required), for example “Logbook reconciliation after maintenance release”
6. Click **Save baseline**. The message **Maintenance baseline updated.** is shown

What happens when you save:

* The totals become the values you entered plus every confirmed flight with on-blocks at or after the as-at time.
* Flights before the as-at time stay in the history but no longer change the totals, even if they are later edited or re-confirmed.
* Any earlier [Adjust totals](#adjust-totals) corrections are superseded by the new absolute values.
* No flight times, crew FTL records or tracking data are changed.
* Who entered it, when, the as-at time and the reason are recorded.

If somebody else changed the totals while you had the form open (for example a flight was confirmed), AeroQuote will not save. It shows **The aircraft totals changed. Review the current values and try again.**

You can also update a baseline from the Crew app: on an aircraft in your Fleet list, tap **Maintenance totals**, then **Update**. Choose **Decimal hours** or **hh:mm**, enter **Landings**, **Engine cycles**, **As at** and a **Reason**, then **Review** and **Confirm**. If you are offline, the app shows **Connect to the internet to update totals.** Nothing is queued offline. On success it shows **Maintenance totals updated.** If the totals changed, it shows **Totals changed since you opened this**.

***

## Adjust totals

**Adjust totals** applies a signed correction (plus or minus) to the current totals, with a required **Reason for adjustment**. It suits a small known correction, for example two landings missed from a training flight.

1. On the **Maintenance** tab, click **Adjust totals**
2. Choose the **TTIS format** and enter a **TTIS adjustment** if needed (for example 0.5 or −1.0 in Decimal, or 0:30 in hh:mm). Leave blank if TTIS isn't changing
3. Enter a **Landings adjustment** and/or **Engine cycles adjustment** if needed
4. Enter the **Reason for adjustment** and click **Save adjustment**. The message **Maintenance totals adjusted.** is shown

For reconciling against the logbook, prefer **Update baseline**. It records the absolute logbook figure and the date it applies, which is easier to audit.

***

## Tracked items

The aircraft **Maintenance** tab also has a simpler list of **Tracked items** with progress bars. These are separate from [Run Out Report](maintenance-tracker.md) program items. They drive the fleet status view, the aircraft badges on booking screens, and daily email alerts.

1. Click **+ Add item**. The form is titled **Add maintenance item**
2. Enter the name, category, **Every** and **Unit** (flight hours, landings, engine cycles, calendar days or calendar months), last completed, **Warn at (% of interval used)** (default 90) and **Recurring**
3. Click **Add item**

Items turn amber at the warn-at percentage and red at 100%. **Sign off** records the completed date and time, **Signed off by**, and notes. The aircraft's totals at that moment are stamped on the record and the next due rolls forward by the interval.

The pencil icon edits the item. The unit cannot be changed; archive and add a new item instead. **Archive item** removes it from the active list but keeps its sign-offs in the **Audit log**.

{% hint style="info" %}
Use the Run Out Report for the maintenance program when the [Maintenance Tracker](maintenance-tracker.md) is on (multiple limits, tolerance, forecasting, void and the full audit history; this is what crew see under **Due Items**). Use tracked items if you also want the fleet status tiles, booking-screen badges and email alerts for a particular check.
{% endhint %}

***

## Fleet status, badges and email alerts

**Limits → Aircraft Maintenance** opens **Aircraft Maintenance — Fleet Status**. It lists every aircraft with TTIS, landings and cycles, filterable by **Baseline set** and **No baseline**, with a colour dot and the most imminent tracked item.

When you choose an aircraft while building a booking, viewing booking details or assigning scheduled departures, a maintenance badge shows the totals and the most imminent tracked item.

A daily check at 06:00 sends an email when a tracked item first passes its warning level and again when it becomes overdue. Recipients and on/off settings are under the **Fleet & Crew Limits** notification settings (**Maintenance item approaching its limit** and **Maintenance item overdue**).

{% hint style="warning" %}
All maintenance indicators are advisory. A red item does not stop you assigning an aircraft; airworthiness decisions remain with the operator and maintenance personnel.
{% endhint %}

See also [Maintenance Tracker](maintenance-tracker.md) and [Flight Logs](../bookings-operators/flight-tracking/flight-logs.md) for confirming pending hours.
