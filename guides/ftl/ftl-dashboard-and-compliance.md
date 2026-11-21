---
description: >-
  Monitor crew duty hours and flight time against your FTL profile, set your
  operations manual daily flight-time cap, and download the Flight and Duty
  Time Summary.
---

# FTL Dashboard & Summary

The **FTL** section tracks crew duty periods, flight hours and the limits in your FTL profile when Fleet & Crew Limits is enabled.

{% hint style="warning" %}
**Planning aid only.** AeroQuote's flight and duty time figures and checks help you plan and keep records. They are not a regulatory compliance determination, no regulator has approved them, and not every rule in the regulation is checked. Your operations manual or approved scheme governs, and you (the operator) remain responsible for compliance. The same notice appears on the FTL pages, the summary PDF and the mobile app.
{% endhint %}

## Prerequisites

* **FTL / Crew Limits** enabled in **Settings → Modules**
* Crew assigned via **Staff** and linked to user accounts where required
* FTL profiles configured for your operation

***

## Step 1: Open the FTL Dashboard

1. Click **FTL** (or **Crew Limits**) in the sidebar
2. Open **Dashboard** for a snapshot of current duty status across crew

The dashboard highlights crew approaching amber or red thresholds.

## Step 2: Review the timeline

1. Open **Timeline** from the FTL menu
2. View duty blocks and flight assignments on a calendar timeline
3. Identify overlaps or insufficient rest between duties

## Step 3: Configure profiles

1. Open **FTL Profiles**
2. Pick the regulation template for the profile (for example CAO 48.1 Appendix 4)
3. Use **FDP overrides** for operator-approved values (for example from an FRMS approval)

{% hint style="info" %}
FAR Part 117 is no longer offered for new profiles. It applies to US Part 121 airline operations only. Existing profiles that already use it keep working.
{% endhint %}

## Step 4: Set your daily flight-time cap (Australia)

CAO 48.1 Appendices 1, 4 and 4B don't set a daily flight-time limit. They point to the maximum flight time in **your operations manual**. AeroQuote therefore doesn't assume one.

1. Open **FTL Profiles**
2. In **Operations manual limits**, enter the **Daily flight-time cap** in hours and minutes from your operations manual
3. Click **Save cap**

* Leave it **blank** (the default) and the daily flight-time check shows **"Not configured — not checked"**.
* When set, each duty's flight time is checked against it. Positioning is not counted as flight time.
* An FDP override with its own flight-time value takes precedence.
* Changing the cap needs the **Edit settings** permission and is recorded in the FTL activity log.

## Step 5: Crew FTL view

1. Open **Crew** under FTL
2. Select a crew member to see their rolling counters and upcoming assignments

**What counts:**

* **Leave** is shown on the timeline but is **not duty**. It doesn't add to duty totals and doesn't count as the previous duty for rest.
* **Positioning** counts as **duty** but **not as flight time**.
* When one duty mixes CAO 48.1 appendices (for example App 4 charter and App 4B medical), AeroQuote uses the **lowest** FDP limit of the appendices involved.

## Step 6: Flight and Duty Time Summary and discretion reports

| Report | Purpose |
|---|---|
| **Flight & Duty Summary** (formerly *Compliance Report*) | PDF of each crew member's block and duty totals, rolling-window peaks and over-limit incidents for a period. File name: `Flight-Duty-Time-Summary-<from>-<to>.pdf` |
| **Discretion Reports** | Record and review captain's discretion events |

Open each report from the FTL menu, set the date range, and export or review in the browser.

***

{% hint style="warning" %}
FTL calculations depend on accurate block times and crew assignments on bookings. Ensure [Flight Tracking](../bookings-operators/flight-tracking/README.md) and [Crew Assignment](../bookings-operators/crew-assignment.md) data are up to date.
{% endhint %}
