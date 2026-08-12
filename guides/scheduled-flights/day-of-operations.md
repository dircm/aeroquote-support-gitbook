---
description: Run your scheduled operation — the Flight Board, aircraft & crew assignment, manual bookings, reschedules, cancellations, refunds, manifests, and freight.
---

# Day-of Operations

Once routes are selling, day-to-day work happens on the **Flight Board**, the **Departures** list, and each departure's detail page. This guide covers the operational playbook.

## Prerequisites

* Published departures (see [Schedules & Publishing](schedules-and-publishing.md))

## The Flight Board

**Scheduled Flights → Flight Board** is your FIDS-style morning scan — all upcoming departures grouped by date, auto-refreshing every 30 seconds:

* **Day range** — Today / 3 days / 7 days (remembered between visits), plus a **route filter**
* **Status pills** — show/hide by status; the default view shows Published, Sold Out, and In Progress
* **Alert strip** — clickable badges for **Unassigned aircraft**, **Unassigned crew**, **Low load** (under 30% sold within 48 hours), and **In progress** flights; click a badge to filter to just those rows
* **Per-row data** — status, route with ICAO codes, local departure/arrival times, aircraft and crew, and a colour-coded load-factor bar
* **Live tracking** — airborne flights show the FlightRadar24 ETA, altitude, and speed (see [Flight Tracking](../bookings-operators/flight-tracking/README.md))

For sales KPIs (gross sales, load factor, busiest routes) use **Scheduled Flights → Sales**; for payment-provider payout reconciliation use **Scheduled Flights → Payouts**.

## Assign aircraft and crew

**Scheduled Flights → Assign Aircraft & Crew** assigns tails and crew across many departures at once:

1. Pick a route or cherry-pick departures on the left
2. Pick a fleet aircraft or crew member on the right
3. Click **Assign**

A caution engine flags problems — red for overlapping assignments or insufficient rest, amber for approaching rolling block-hour limits or an aircraft-type mismatch. Cautions warn rather than block; overrides are recorded in the audit trail.

On the **Crew** tab, selecting a crew member pre-ticks their existing roster and shows an **Assigned** badge on rows they already operate, so the button always reflects the genuine delta (e.g. *"Assign … to 5 new departures"*). A secondary button removes the selected crew from ticked departures they're already on.

## Issue a manual booking

For phone bookings, walk-ups, Community Fares, comp tickets, or voucher redemptions — any seat you issue directly instead of sending the customer to the storefront.

Open the modal from the **Flight Board** or **Departures** row menu (**… → Add passenger…**), or the **+ Add passenger** link on the departure detail page. Then:

1. **Receipt email** — where the confirmation lands; no customer account needed
2. **Segment** — on multi-stop routes pick the actual origin and destination (defaults to the full route)
3. **Fare class** — any active class, including operator-only ones tagged "(operator-only)"
4. **Passengers** — at least one; add more with **+ Add another passenger** (or use **Add many** on private routes — see below)
5. **Payment notes** — free-text audit trail visible only to staff (e.g. "Cash on board, $80 — receipt #4421", "NSW Govt voucher VR-7788")
6. Click to issue the booking

The purchase is marked **Paid** immediately — your payment provider is never charged; payment is handled offline and the notes field is your audit trail. The customer receives the standard confirmation email with wallet passes, the booking counts against seat inventory straight away, and it's stamped as an operator-manual booking so you can separate it from public sales in reporting.

### Bulk add passengers (private routes)

On **private** routes, the add-passenger modal can open in **Add many** table mode (you can switch back to the detailed single-passenger form anytime):

1. Open **Add passenger…** on a private departure
2. Choose **Add many** if it isn’t already selected
3. Fill a row per person — **name**, optional **passenger weight**, optional **bag weight**
4. Start typing a name to search prior contacts; picking a match can prefill known weight
5. Watch the **running seat count** (hard-capped by remaining seats) and **total weight** as you go
6. Issue the tickets — same manual/paid flow as a single add; you land back on the departure page with seats and tickets refreshed

{% hint style="info" %}
**Add many** is for private (non-storefront) routes only. Public routes keep the detailed passenger form so checkout field requirements (passport, DOB, etc.) stay enforced.
{% endhint %}

## Reschedule a departure

1. On the **Flight Board** or **Departures** list, open the row's **…** menu and choose **Reschedule…**
2. Pick the new departure time (in the airport's local timezone) and an optional reason
3. Tick **Email affected passengers** to queue a "Your flight has been rescheduled" email to every paid ticket holder — or leave it unticked for a silent one-minute tidy-up
4. Confirm

Arrival times, the linked booking's flight item, and every paid ticket's wallet pass update automatically (iPhone passengers get a lock-screen notification). For deeper changes — different aircraft, different route — use the underlying booking's itinerary editor instead.

## Cancel a departure

From the same **…** row menu, choose **Cancel flight…** (or **Cancel departure** in the departure page header), add an optional reason shown to passengers, and confirm. Automatically:

* The departure flips to **Cancelled**
* Every paid ticket is refunded through your connected payment provider in the background, and every passenger receives a cancellation email
* Wallet passes are voided, with a "Flight cancelled" lock-screen notification on iPhone
* The linked booking's flight item is marked cancelled (the booking remains as the financial record)

**Bulk cancel:** on the **Departures** list, filter to the route and status, tick the affected rows (or the header checkbox for all visible), click **Cancel selected**, enter a reason like "Airport closed", and confirm.

## Refunds

On the departure detail page, find the ticket row and click **Refund**. For non-refundable fare classes the button reads **Goodwill refund** — it waives the fare rules and logs the override in the Activity trail. Manual bookings refund normally even though no card was charged (a $0 comp refunds as $0, and the cancellation is still recorded).

## Customer contact fixes

* **Lost confirmation email** — point them at the **Find my booking** page, or click **Resend confirmation** next to the purchase row on the departure
* **Mistyped email** — click **Edit email** on the purchase row, correct it, save, then **Resend confirmation**
* **Wrong passenger name or passport** — edit the ticket row inline in the **Tickets & passengers** table; every change lands in the audit trail

## The manifest, weights, and freight

The departure page doubles as the flight's operational manifest — every passenger (grouped by segment on multi-leg routes) with the fields you collect, and payload totals for weight & balance:

* **Passenger weight is per ticket**, so a repeat traveller's new booking never overwrites the weight on a historical manifest. You can correct weights on the day directly on the departure page.
* **Luggage** over the route's included allowance is flagged as **excess**, and each passenger's luggage is projected onto the manifest as a baggage item on exactly the legs they fly.
* **Freight:** the departure's **Freight** card takes a consignment description, optional weight and notes, and — on multi-leg routes — **From**/**To** stop pickers so the consignment counts against only the legs it rides. Each consignment gets a printable **Con-note** label PDF with a QR code that uniquely identifies it.

## The Activity card

Every action above — publishes, refunds, reschedules, cancellations, edits — is logged on the departure's **Activity** card with who did it and what changed. Use it when a colleague asks who refunded a ticket, or an auditor wants the record of a data correction.

## Next steps

* [Travel Agents](travel-agents.md) — agent bookings, commission, and statements
* [Flight Tracking](../bookings-operators/flight-tracking/README.md) — how departures are tracked in the air
