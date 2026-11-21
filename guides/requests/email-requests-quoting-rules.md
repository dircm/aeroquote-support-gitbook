---
description: >-
  How automated quotes from emailed charter requests are grouped, and the
  quoting rules for the maximum time an aircraft waits on the ground away
  from base, and which aircraft are quoted automatically.
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

### Automated quote fleet

For a large fleet, these settings decide which aircraft are priced and how many options a quote shows. Choose **Save automated quote fleet** to apply them.

* **Options per quote**: how many aircraft options a draft offers, from 1 to 6. The default is **4**. Options are always listed **cheapest first**, one per aircraft type.
* **Positioning cap**: the most positioning (base to first pickup, plus last drop-off back to base) an aircraft can need and still be quoted, from 100 to 2,000 NM. The default is **500 NM**. Raise it if aircraft at another base, for example Alice Springs on Top End requests, should be considered. If no aircraft is within the cap, the nearest aircraft is quoted and the draft says the cap was relaxed.
* **Types to quote**: tick the aircraft types that can be quoted automatically. Only aircraft that can be priced are quoted, following each aircraft's pricing setting:
  * **Use fixed hourly rates**: the aircraft needs a **charter rate**.
  * **Margin percentage over total costs**: the aircraft needs a **margin** and at least one **cost item**. The charter rate can be empty or zero.

  Types with no aircraft that can be priced are greyed out ("no charter rate or margin costs, not quoted") and are never priced, and the draft tells the reviewer which aircraft were left out and what's missing. When every type is ticked, types that can be priced later are included automatically.
* **Skip unavailable aircraft**: on by default. An aircraft that is **booked, booked out, or not released from maintenance** on the trip days is left out, and the draft tells the reviewer which aircraft were skipped and why. Turn it off to keep those aircraft with a warning instead. Cautions such as deferred defects or maintenance coming due are always shown on the draft but don't stop the aircraft being quoted.

To leave one aircraft out of automated quotes, open the aircraft, tick **Exclude from automated quotes** on the details step and save. Excluded aircraft are listed in the panel under **Left out of automated quotes**, with **Include again**.

To keep pricing quick, AeroQuote prices only the **3 nearest aircraft of each type** (by positioning distance) and keeps the cheapest of each type.

All quoting rule changes apply to new email requests. To update a draft that already exists, use **Re-run** on that request.

## Daily charges when the aircraft goes home

When the aircraft returns to base between legs, **daily charges count only the days it is away from base**. In the example above, two flying days are charged, not the five calendar days from Friday to Tuesday. See [Cost types](../aircraft/cost-types.md#daily-charge).
