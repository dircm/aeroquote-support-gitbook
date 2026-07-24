---
description: Configure basic aircraft information.
---

# Aircraft Details

The Details section contains basic information about your aircraft that identifies it and determines how it's used in quotes.

---

## Accessing Details

1. Go to **Aircraft** from the sidebar
2. Click on an aircraft (or Add Aircraft)
3. The **Details** tab is typically the first section

---

## Required Information

| Field | Description | Example |
|-------|-------------|---------|
| **Registration** | Aircraft tail number / registration | N123AB, VH-XYZ |
| **Aircraft Type** | Model of aircraft | King Air 350, Citation XLS |
| **Homebase** | Default airport location | YBBN, KJFK |

---

## Registration type lookup (Add Aircraft)

When you **Add Aircraft** and enter a **Registration**, AeroQuote can guess the type for you:

1. Enter the tail number in the builder (e.g. `VH-ABC`)
2. A progress panel appears while AeroQuote checks available flight data, then AI if needed
3. **Cancel lookup** anytime if you prefer to choose the type yourself
4. On a solid match, the type is applied and a short “Guessed …” banner is shown — you can still change the type
5. If nothing reliable is found, the panel closes with no banner (no empty “null” suggestions)

{% hint style="info" %}
Lookup lookup is optional. You can always search and select the aircraft type manually.
{% endhint %}

---

## Auto-save

On the **Details** step, edits save automatically shortly after you change a field (same pattern on **Flight Performance**). There is no separate Save button. A short success toast confirms each save.

---

## Optional Information

| Field | Description |
|-------|-------------|
| **Serial Number** | Aircraft serial/MSN |
| **Year of Manufacture** | Build year |
| **Configuration** | Seating layout description |
| **Maximum Passengers** | Passenger capacity |
| **Notes** | Internal notes about the aircraft |

---

## Homebase

The homebase is important for quote calculations:

- **Positioning flights** — If a trip doesn't start at homebase, AeroQuote calculates ferry flight costs
- **Return positioning** — After a one-way trip, the aircraft needs to return home
- **Availability** — Fleet timeline assumes aircraft are at homebase when not scheduled

{% hint style="info" %}
Set the homebase to where the aircraft is normally parked overnight. This ensures accurate positioning cost calculations.
{% endhint %}

---

## Aircraft Type

Selecting the correct aircraft type is crucial because it:

- Determines available performance data templates
- Affects fuel burn calculations
- Influences landing fee estimates
- Sets passenger expectations

---

## Active vs Inactive

Toggle an aircraft to **Inactive** when:

- It's undergoing maintenance
- It's been sold or retired
- You temporarily don't want it included in quotes

Inactive aircraft don't appear in quote options but their historical data is preserved.

---

## Next Steps

- [Flight Performance](flight-performance.md) — Configure speed and fuel data
- [Costings](costings.md) — Set up pricing
