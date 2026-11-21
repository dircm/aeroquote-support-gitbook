---
description: >-
  How automated quotes from emailed charter requests are grouped, and the
  quoting rules for the maximum time an aircraft waits on the ground away
  from base.
---

# Email requests: quoting rules

AeroQuote can read charter requests that arrive by email and prepare draft quotes for you to review on the **Email requests** page. This page explains how those drafts are built and the **Quoting rules** you control.

## One request, one quote

A request with several sectors becomes **one trip, one draft and one quote with every leg**, even when the sectors are on different days. For example, Jabiru → Darwin on Friday and Darwin → Jabiru the next Tuesday is one quote.

A request is still split into separate drafts when:

* the sectors carry **different request references**
* a sector has **no date**
* a sector **doesn't connect** to the rest of the trip (it starts somewhere the aircraft hasn't been), for example a separate group of passengers
* **no single aircraft can fly every leg**. The draft then says "No single aircraft could fly every leg of this request, so each date is quoted separately."

The review page shows each trip's date range, the date of every sector, and how long the aircraft waits on the ground between legs.

## Quoting rules

Open **Quoting rules** at the top of the **Email requests** page. You need the **edit settings** permission to change them. Everyone else can see them.

### Maximum ground stay

Enter the longest time the aircraft should wait away from base between legs, in **days and hours** (for example 1 d 0 h).

* **Leave both boxes blank for no limit.** The aircraft stays away between legs, and overnight and daily charges apply for the whole trip.
* When a wait is longer than the limit, the aircraft **returns to base** after the earlier leg and comes back for the next one. Overnight and ground-time charges for the gap are not charged.
* If that leg already finishes at the aircraft's base, **no extra ferry is added**. The aircraft is already home.

The draft explains what happened, for example:

> Ground stay at Darwin (4 d 2 h) exceeds the 1 d 0 h limit; aircraft returns to base between legs (already at base, no ferry needed).

One limit applies to all your aircraft. The longest limit you can set is 30 d 23 h.

### When the limit is exceeded

* **Follow the limit**: always return to base when the wait is longer than the limit.
* **Use the cheaper price**: price each aircraft both ways (returning to base and staying away) and keep whichever is cheaper. The draft says which was used, for example "VH-ABC: returning to base is cheaper (returning to base A$4,200.00, staying away A$5,000.00 ex tax)."

Changes apply to new email requests. To update a draft that already exists, use **Re-run** on that request.

{% hint style="info" %}
The positioning limit is shown in the same panel. A draft isn't prepared for an aircraft that would need more than 500 NM of positioning.
{% endhint %}

## Daily charges when the aircraft goes home

When the aircraft returns to base between legs, **daily charges count only the days it is away from base**. In the example above, two flying days are charged, not the five calendar days from Friday to Tuesday. See [Cost types](../aircraft/cost-types.md#daily-charge).
