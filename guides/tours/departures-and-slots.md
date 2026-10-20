---
description: Publish bookable departure times — the Departures hub, recurring schedules with auto-extend, manual bulk creation, and per-slot cancel, reopen, and delete.
---

# Departures & Slots

Publish the departure times customers can book — each slot is one departure with a fixed capacity, and a recurring schedule keeps your calendar topped up automatically.

## Prerequisites

* An enabled tour (see [Building a Tour](building-a-tour.md))

{% hint style="info" %}
Publishing slots creates **storefront availability only** — no operational booking exists until a customer pays. Your Flight Board and dispatch screens only ever show departures someone has actually booked.
{% endhint %}

## The Departures hub

Click **Tour Packages → Departures**. Every active tour appears as a row showing:

* **Publish horizon** — e.g. "Published to 24 Jul · 60 days ahead". Green means healthy, amber means the horizon has dropped below your warning threshold, grey means nothing upcoming is published
* **Auto-extend status** — a blue "auto-extend 60d" pill when it's on, or "manual only"
* **Extend now** — one click publishes that tour's slots out to its horizon immediately
* **Manage** — opens the tour's slot page

## Step 1: Set a recurring schedule with auto-extend (recommended)

On a tour's **Manage** page, the top card is the **Recurring schedule**:

1. Tick the **days of week** you operate
2. Enter **departure times**, comma-separated in 24-hour format: `09:00, 11:00, 13:00, 15:00`
3. Set the **capacity per slot** (usually the tour's max passengers) and the **timezone**
4. Tick **Auto-extend** and set how many days ahead to keep published (e.g. 60), plus a low-horizon warning threshold (e.g. 14)
5. Click **Save schedule**

A nightly job rolls the window forward from then on — the storefront always has bookable slots without you touching this page. Want slots right now instead of waiting for tonight's run? Click **Publish to horizon now** (Manage page) or **Extend now** (hub). Both skip any slot that already exists, so they're safe to run repeatedly — never duplicates.

## Step 2: Manual one-off publishing (optional)

Below the schedule card, the **Bulk create slots** card publishes a specific date range by hand — for an extra date outside your usual pattern, or if you'd rather not use auto-extend:

1. Pick the date range, days, times, capacity, and timezone
2. Click **Create slots**

## Per-slot actions

Each slot card shows its booking progress ("2 / 3 booked") and carries:

* **Cancel** — pulls the slot off the storefront. Existing bookings are preserved; capacity locks at the current booked count
* **Reopen** — un-cancels a slot; it returns to available (or full, if already at capacity)
* **Delete** — only available on slots with zero bookings; the right tool for a slot created by mistake

## Troubleshooting

* **Customers see "No tours available"** — either no tour is enabled, or no future slots exist on any enabled tour. Check the Departures hub for grey/amber horizon badges and click **Extend now**
* **A horizon badge is grey or amber** — open **Manage**, confirm the recurring schedule has at least one day and time saved, then **Publish to horizon now** — or enable auto-extend so it never lapses again

## Next steps

* [Storefront & Branding](storefront-and-branding.md) — what customers see when they book a slot
* [Bookings, Manifests & Refunds](bookings-manifests-and-refunds.md) — what happens after they pay
