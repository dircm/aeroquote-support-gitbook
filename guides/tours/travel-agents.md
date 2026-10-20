---
description: Let travel agents book tours on customers' behalf — agent logins on the tours storefront, snapshotted commission, and card vs invoice payment terms.
---

# Travel Agents (Tours)

Register travel agencies so they can book tours on customers' behalf, earn a snapshotted commission per booking, and optionally settle by invoice instead of card.

## Prerequisites

* A live tours storefront with published slots (see [Storefront & Branding](storefront-and-branding.md))

{% hint style="info" %}
Agent records are **shared across your storefront** — if you also sell [Scheduled Flights](../scheduled-flights/travel-agents.md), your existing agents work for tours immediately, and vice versa.
{% endhint %}

## Step 1: Register an agent

1. Click **Tour Packages → Travel Agents**, then **+ New Agent**
2. Fill in:
   * **Company name** and **contact person** — shown on the agent's dashboard and booking attribution
   * **Email + password** — the agent's portal login; share the login URL (below) and password securely yourself
   * **Commission %** — snapshotted at booking time, so changing it later never rewrites existing bookings
   * **Payment terms** — **Card on booking** (default: the customer's card is charged at checkout, exactly like a public booking) or **Invoice** (no card charge; the booking records as paid and the agent settles with you later)
3. Create the agent

Suspending an agent (the toggle on their row) blocks logins and new bookings without touching existing ones.

## Step 2: How agents book

1. The agent signs in at `/tour/<your-slug>/agent/login` under your storefront URL
2. Their **Agent Dashboard** shows a 30-day count of bookings, passengers, and commission earned, plus recent bookings — scoped to *their* sales only
3. From the dashboard they click **Book a tour** and book like a public customer; every booking completed while signed in is attributed to them automatically
4. They enter the **customer's** email as the receipt address — the customer (not the agent) receives the confirmation email and tax invoice

For agents on **Invoice** terms, checkout skips the card form entirely — they confirm the booking and the customer gets their confirmation; you reconcile the receivable with the agent later.

## Where attribution shows up

Every agent booking carries a booking source of **agent** (vs **public**), the commission amount and snapshotted rate, and a link back to the agent — visible on the operator [booking detail](bookings-manifests-and-refunds.md), filterable in the bookings list, and counted on the agent's own dashboard.

## Statements and invoicing

Agent statements, marking bookings paid, and raising Xero/QuickBooks invoices work the same way across your storefront — see [Agent statements & raising invoices](../scheduled-flights/travel-agents.md#agent-statements--raising-invoices).

## What agents can't do

* Refund or cancel bookings — operator-only
* Change their own password or commission rate
* See other agents' bookings

## Next steps

* [Bookings, Manifests & Refunds](bookings-manifests-and-refunds.md) — handling agent-booked customers on the day
* [Travel Agents (Scheduled Flights)](../scheduled-flights/travel-agents.md) — the shared statements and invoicing tooling
