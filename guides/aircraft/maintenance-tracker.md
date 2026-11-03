---
description: >-
  Track engines, propellers and components, program items with multiple
  limits, and a live due list with forecast dates.
---

# Maintenance Tracker

The Maintenance Tracker is an add-on module. It builds on [Maintenance Limits](maintenance-limits.md): flight hours, cycles and landings captured from block times and Flight Logs flow into the tracker automatically.

{% hint style="info" %}
The Maintenance Tracker is enabled per operator. Contact AeroQuote support to switch it on. **Maintenance tracking** must also be enabled in **Settings → Modules** and each aircraft needs a baseline, otherwise flown hours will not roll into the due list.
{% endhint %}

***

## Open the tracker

1. Click **Maintenance → Maintenance Tracker** in the sidebar, or open an aircraft and click **Maintenance Tracker**
2. Pick an aircraft from the selector

## Step 1: Add components

Register engines, propellers and other components.

1. Click **Add component**
2. Choose the type (engine, propeller or component) and enter the name, part number, serial number and position
3. Enter current **TSN** (hours), **CSN**, and if known **TSO**/**CSO**
4. Choose where it is installed: directly on the aircraft, or on a parent component (for example a starter generator on an engine)
5. Save

From then on, component times grow with the aircraft. Component cycles are the aircraft's engine cycles divided by its engine count.

### Remove, install and overhaul

* **Remove** closes the installation record and stops counters accumulating. Child components stay with their parent.
* **Install** fits the component to an aircraft or parent component; install history is kept.
* **Overhauled** resets TSO and CSO to zero.

## Step 2: Add program items

1. Click **Add program item**
2. Enter the title and reference (for example the maintenance program task number)
3. Attach it to the aircraft or to a component
4. Add one or more limits: hours, cycles, landings, calendar days or calendar months
5. For each limit, enter the interval, optional **+/- tolerance**, optional amber threshold, and when it was last done
6. Save

The item is due at **whichever limit comes first**.

## Step 3: Read the due list

| Status | Meaning |
| ------ | ------- |
| 🟢 Green | Not yet within the amber threshold |
| 🟠 Amber | Within the amber threshold, or past due but still inside the + tolerance |
| 🔴 Red | Past due plus tolerance |

Each item shows the remaining amount for every limit and a **forecast date**, calculated from the aircraft's average daily utilisation (up to the last 90 days). Calendar limits use their due date.

The default amber thresholds are 10 hours, 10 cycles, 10 landings and 30 days. A limit can override its own threshold.

## Step 4: Record completion

When an item is done:

* If completed inside the tolerance window, the next due is counted from the scheduled due point, so the schedule doesn't drift.
* Otherwise the next due is counted from when it was actually done.
* One-off (non-recurring) items close once completed.

{% hint style="warning" %}
Airworthiness directives, service bulletins, life-limited part alerts, defects and exports are not yet part of the tracker.
{% endhint %}
