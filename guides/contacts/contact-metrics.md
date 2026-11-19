---
description: >-
  See how often each contact has been quoted and how much they have flown with
  you: flights, hours, distance, last flown and a suggested frequent-flyer tier.
---

# Contact and passenger metrics

The **Contacts** page shows each contact's quote history and the revenue flying they have done with you as a passenger.

{% hint style="info" %}
You need the **Contacts - View** or **Contacts - View All** permission to open the Contacts page. Roles without either permission do not see **Contacts** in the menu.
{% endhint %}

## Columns

| Column | What it shows |
| --- | --- |
| **Type** | **Passenger** (has flown), **Contact** (on quotes or bookings, never flown), or **Both** |
| **Quotes inc · sent · acc** | Quotes the contact is on (To or Cc) · quotes sent to them · quotes accepted. Sent and accepted count the main (To) contact only. Hover for the To / Cc split |
| **Flights** | Revenue legs flown. Click the number to open the contact's flight history |
| **Hours** | Hours flown. `≈` means more than 20% of the hours come from planned times because no airborne or block times were recorded |
| **Distance km** | Kilometres flown |
| **Last flown** | Date of the most recent flown leg |
| **Frequent flyer** | Suggested tier (Bronze, Silver or Gold). Hover for the score and the rule |

Hidden columns you can turn on from the column menu: **First flown**, and **Charter / Scheduled / Tour flights**.

The **Quotes**, **Bookings** and **Training** badges still show upcoming quotes, upcoming bookings and training flights.

### What counts as a flight

* **Revenue flights only.** Charter, scheduled and tour bookings count. Training, private, repositioning and maintenance flights do not.
* **Completed legs** count, and so do **past legs on confirmed bookings that were never closed off**. These are marked as estimated (hover the Flights number).
* Cancelled, expired and deleted bookings are never counted.
* **Hours** use the airborne time, then the block time, then the planned time.
* **Distance** uses the saved route, then the straight line between the airports. A tour with no saved route and the same start and end airport counts as 0 km.

Figures refresh automatically a minute or so after a booking, leg, passenger list or quote changes.

## Filters

| Filter | Use it to |
| --- | --- |
| **Type** | Show passengers, contacts who have never flown, or both |
| **Flight type** | Count only charter, scheduled or tour flights |
| **Flown between** | Count only flights between two dates |
| **Minimums** | Contacts with at least N flights or N hours (all time) |
| **Recency** | Contacts who flew in the last N days, or who have not flown for N days |
| **Frequent flyer tier** | Contacts in one or more tiers |
| **Has been sent a quote** / **Has an accepted quote** | Contacts with quote activity |

When **Flight type** or **Flown between** is set, the Flights, Hours and Distance columns say **(filtered)**, show only the matching flights, and the list only shows contacts with matching flights. Filtered totals never include [baselines](contact-baselines.md).

## Flight history

Click a contact's **Flights** number to see each leg: date, booking, type, route, hours and where the hours came from, distance, and whether the passenger checked in. Estimated and upcoming legs are labelled.

## Frequent flyer tiers

Tiers are a suggestion for your team. Customers never see them.

A contact gets the highest tier whose **flights OR hours** threshold they meet in the **last 12 months**, and who flew within the tier's recency window:

| Tier | Flights (12 months) | Or hours (12 months) | Flown within |
| --- | --- | --- | --- |
| Bronze | 3 | 3 | any time |
| Silver | 6 | 8 | 180 days |
| Gold | 12 | 20 | 90 days |

The **score** (0–100) weights frequency 40%, recency 30% and hours 30%, each capped at the Gold threshold.

Users with **Settings - Edit** see **Frequent flyer settings** on the Contacts page. Change the thresholds or weights and click **Submit**, or click **Reset to defaults**. Every contact is re-scored straight away and the change is written to the activity log.

Baselines do not count towards tiers.

## Export

Admins can download these figures with **Export metrics**. See [Export contacts](export-contacts.md).
