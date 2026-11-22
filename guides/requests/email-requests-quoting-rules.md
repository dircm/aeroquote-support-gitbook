---
description: >-
  How automated quotes from emailed charter requests are grouped, and the
  quoting rules for the maximum time an aircraft waits on the ground away
  from base, the minimum time it must have at base if it flies home,
  which aircraft are quoted automatically, how a requested aircraft
  (for example "can you quote the Conquest") is always included, and how
  option prices can be rounded.
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

A **plain-language summary** under the controls explains the rules as you have them, and updates as you change the boxes, before you save. For example: "Aircraft away longer than 2 days fly home in between, unless they'd have less than 2 days at base."

The draft explains what happened, for example:

> Ground stay at Darwin (4 d 2 h) exceeds the 1 d 0 h limit; aircraft returns to base between legs (already at base, no ferry needed).

One limit applies to all your aircraft. The longest limit you can set is 30 d 23 h.

### When the limit is exceeded

* **Follow the limit**: always return to base when the wait is longer than the limit.
* **Use the cheaper price**: price each aircraft both ways (returning to base and staying away) and keep whichever is cheaper. The draft says which was used, for example "VH-ABC: returning to base is cheaper (returning to base A$4,200.00, staying away A$5,000.00 ex tax)."

### Minimum time at base

A return to base can be a short turnaround when the destination is far from base: the aircraft flies home only to turn around and fly back out soon after.

Enter the shortest time the aircraft should spend on the ground at base, in **days and hours**. The default is **2 days**. Leave both boxes blank for no minimum.

When a return to base is triggered, AeroQuote works out the time at base from the wait between legs minus the flights home and back (using the durations already calculated for the quote; it does not make an extra iFlightPlanner call). If that would be less than the minimum, the aircraft **stays away** instead, and the draft says why, for example:

> VH-ABC: returning to base from Katherine would leave only 1 h at base (minimum 2 h; ferries home and back take 2 h); quoted staying away.

This check does not apply when the aircraft is **already at base** (no ferry is added). Daily charges still count only the days the aircraft is away when it does fly home, and the full stay when it stays away.

### Price rounding

Off by default. When you turn it on, each option's **quoted price is rounded** after the aircraft have been chosen, so rounding never changes which options appear.

Choose **Save quoting rules** to apply it. A live example under the controls, starting from A$12,343.25 and a smaller trip of A$2,849.60, shows what your choice would do.

* **Round to the nearest**: choose **Don't round**, or an increment of A$1, A$5, A$10, A$50, A$100, A$500 or A$1,000.
* **Round up** (the usual choice): the price is never below the calculated amount, for example A$12,343.25 becomes A$12,400.00 when rounding up to the nearest A$100.
* **Round to nearest**: halfway cases round up. A price can go slightly below the calculated amount.
* **Round down**: can put a small trip below cost. The price is never taken below the aircraft's **minimum price to customer**. If rounding down would go below that minimum, the price is kept at the minimum and the draft says so.

Rounding is applied to the **stored sell price** of each option (the figure after any margin or hourly rates, and after the aircraft's minimum price to customer). **Cost is not rounded.** Tax is worked out from the rounded amount: when tax is added on top, the price you edit is before tax; when tax is included in the price, the rounded figure is the customer total. This applies only to **quotes created from email requests**, not to quotes you build by hand.

The draft shows a line for each option that was changed, for example:

> Rounded up to the nearest A$100 (was A$12,343.25).

> VH-ABC: price kept at the minimum of A$12,350.00 (rounding down to the nearest A$100 would have been A$12,300.00).

The same lines go into the draft quote's operator notes. The heading of **Quoting rules** shows whether rounding is on, for example "prices rounded up to the nearest A$100".

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

## When the email asks for a particular aircraft

Requesters sometimes ask for an aircraft by name, for example "Can you quote the Conquest?". AeroQuote reads that from the email and makes sure a matching aircraft is in the draft, even when it's dearer than the other options. This works for ACS table emails (the text above the table) and for emails the AI reads.

**What it understands**

* A **type or model**, as people write it: a common name ("Conquest", "King Air", "Caravan", "Navajo"), the full model ("Cessna 441 Conquest II"), or an ICAO type code ("C441", "BE20", "B200").
* A **category**, for example "Turboprop".
* A **registration**, for example "VH-JFO". The 3-letter callsign ("JFO") works too.

AeroQuote matches these against each aircraft's ICAO type code, name, manufacturer, category and registration, and knows common names. "Conquest" matches a Cessna 441 Conquest II (C441), and "King Air" or "B200" matches a Beechcraft King Air (BE20).

**How the options are chosen**

* **"Can you quote the Conquest?"** (a preference): the draft keeps the normal options, cheapest first, and the best matching aircraft takes the place of the dearest option that wasn't asked for. The number of options stays within **Options per quote**. The aircraft it replaces is listed with the options over the limit.
* **"Only the Conquest"** or **"Must be a Conquest"** (exclusive): only matching aircraft are quoted. Other aircraft are listed as "left out: the email asked for only Conquest."
* **A registration**: that aircraft is quoted instead of a cheaper aircraft of the same type.

The requested aircraft still has to pass the normal checks: it must be in the automated quote fleet, available on the trip days (when **Skip unavailable aircraft** is on), and able to fly the trip (seats, strip length, range and the positioning cap). It's priced the same way as the other options. When ranking with AeroQuote estimates is on, it's added to the shortlist that's priced through iFlightPlanner.

**What the reviewer sees**

The draft shows a line starting with ✈, and the option is marked **requested**. For example:

> Requested Conquest: Cessna 441 Conquest II VH-JFO is in the options, ahead of cheaper aircraft (see the options over the limit).

If no matching aircraft can be quoted, the draft has the normal best options and a line in red saying why:

> Requested Conquest: all booked or unavailable on these dates (VH-JFO is not available: …); quoted the best options without it.

> Requested King Air: no matching aircraft in the fleet; quoted the best options without it.

Other reasons are "no matching aircraft can be quoted for this trip", with each aircraft's reason (for example the strip is too short, or it isn't in the automated quote fleet), and "no matching aircraft could be priced". An exclusive request falls back to the normal best options in the same way. The same lines go into the draft quote's operator notes.

The wording from the email is still kept in the request's instructions for the reviewer.

## Daily charges when the aircraft goes home

When the aircraft returns to base between legs, **daily charges count only the days it is away from base**. In the example above, two flying days are charged, not the five calendar days from Friday to Tuesday. See [Cost types](../aircraft/cost-types.md#daily-charge).
