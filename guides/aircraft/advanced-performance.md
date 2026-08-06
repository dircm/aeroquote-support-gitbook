---
description: >-
  Link, change, or revert advanced performance models; type search when adding
  aircraft; when standard AeroQuote performance is used instead.
---

# Advanced performance models

Advanced performance models improve how AeroQuote plans **flight time** and **distance** for estimates on Requests, Quotes, and Bookings. They use climb and descent profiles and route winds rather than only simple still-air assumptions.

{% hint style="info" %}
In the product you may also see **iFlightPlanner** on search labels and help text. Customer-facing quotes and PDFs do not depend on that name — they show your usual prices and itinerary.
{% endhint %}

---

## Who this applies to

* **All operators** can search models when adding aircraft and can link or change models on **Details**
* Estimates use advanced planning **per aircraft** when that aircraft is linked to a model and advanced planning is active for it
* Other aircraft can stay on **standard AeroQuote performance data** (manual Flight Performance fields)

You can mix both modes in one fleet.

---

## Adding an aircraft (type search)

1. Go to **Aircraft** → **Add Aircraft**
2. Enter **Registration** if you want (optional type lookup still runs as before)
3. In **Search aircraft database (iFlightPlanner)**, type make, model, or ICAO (minimum 2 characters)
4. Select a model from the list — advanced performance data is used when the catalogue has profiles for that model
5. If no models match, use **Select AeroQuote aircraft type (fallback)** and continue with native performance fields

{% hint style="warning" %}
Some catalogue models may appear in search but still lack usable performance profiles. If estimates fail or look empty after linking, try **Change model** to a close sibling type, or contact support with the registration and the model name you tried.
{% endhint %}

---

## Aircraft Details — link, change, revert

1. Open **Aircraft** from the sidebar  
2. Click the aircraft  
3. Stay on **Details**

### Already on advanced performance

A green banner shows **Using advanced performance model** (an internal model ID may appear next to it).

| Action | What it does |
| ------ | ------------ |
| **Change model** | Opens a slide-over titled **Change advanced model**. Search, select a model, click **Update model**. The aircraft keeps its registration and identity; the next estimate uses the new model. |
| **Revert** | Confirm **Revert?**. That aircraft goes back to **standard AeroQuote performance data**. Other aircraft are unchanged. A toast confirms the revert. |

### Not linked yet

A blue banner prompts you to link a model for advanced performance data.

1. Click **Link model** (slide-over: **Link advanced model**)  
2. Search and select a model  
3. Click **Link model** to save  

---

## Flight Performance tab

| Mode | What you see |
| ---- | ------------ |
| **Advanced model linked** | Performance from the linked model (read-oriented advanced data) |
| **Standard AeroQuote** | Manual climb, cruise, and related fields you edit yourself (auto-save as usual) |

After **Revert**, use the manual fields again so native estimates stay accurate.

See [Flight Performance](flight-performance.md).

---

## Estimates and fuel burn

### Live estimates (before you save a quote)

On **Requests**, **Quote Builder**, and **Booking Builder**, after you add aircraft:

* Times and distances for advanced-model aircraft use the new planning engine  
* A **Fuel** column may show planned burn for those aircraft  

### Saved quotes and bookings (planned burn)

When you **create a quote or booking** from that estimate, planned burn is stored on each flight leg with duration. Your team can see it later without re-running estimates:

| Where | Display |
| ----- | ------- |
| Quote **Options** | Per leg next to duration; option header **Charter** / **Ferry** / **Fuel** totals (left of the option title) |
| Quote **Details** | Per leg next to duration; **Total fuel** under the option flight table when data exists |
| Booking **Itinerary** | Per leg next to duration |
| Crew itinerary link | Per leg next to duration |
| **Flight manifest** PDF | Planned fuel under duration |

**Fuel burn is internal only** — not on customer quote/booking views or customer PDFs. Unit comes from **Settings → Localization** (default fuel unit). Blank cells or **est.** are explained in [Using the Estimator](../requests/using-the-estimator.md).

Pricing and margins still follow your **Costings** and quote rules.

{% hint style="info" %}
Quotes and bookings created **before** planned burn was stored will not show fuel until you re-estimate or create them again from a new plan. Editing only duration on a leg keeps the last planned burn figure (it is not recalculated automatically).
{% endhint %}

---

## If something does not look right

1. **Change model** to a better catalogue match for that type  
2. **Revert** that registration to standard performance if you need the previous behaviour immediately  
3. Contact support with **registration**, **route**, **date**, and expected vs shown times  

---

## Related guides

* [Aircraft Details](aircraft-details.md)  
* [Flight Performance](flight-performance.md)  
* [Add Your First Aircraft](../../getting-started/add-your-first-aircraft.md)  
* [Using the Estimator](../requests/using-the-estimator.md)  
* [Creating a Quote from scratch](../quotes/creating-a-quote.md)  
* [Booking Manifests](../bookings-operators/booking-manifests.md)  
* [August 2026 What's New](../../whats-new/august-2026.md)  
