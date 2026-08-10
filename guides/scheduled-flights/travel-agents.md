---
description: Register travel agents on your storefront — agent logins, commission tracking, card vs invoice payment terms, statements, and raising accounting invoices.
---

# Travel Agents

If agents book flights on behalf of their customers, register them here. Agents get their own login on your public storefront, earn commission on each booking, and see their sales on a dedicated dashboard — while refunds and cancellations stay operator-only.

## Prerequisites

* A live storefront with published departures (see [Storefront & Custom Domain](storefront-and-custom-domain.md))

## Step 1: Register an agent

1. Click **Scheduled Flights → Travel Agents**, then the new-agent button
2. Fill in:
   * **Company name** and **Contact person**
   * **Email** — the agent's login username (unique per operator)
   * **Commission rate (%)** — of the ticket subtotal, before surcharge and tax (10% on a $270 fare = $27)
   * **Payment terms** — **Card on booking** (default: the agent enters the customer's card and it's charged immediately) or **Invoice** (no card charge; you bill the agent later)
   * **Password** — the agent's initial password; share it securely (agents can't reset it themselves)
3. Create the agent

**Edit** on an agent's row reopens the same form; leave the password blank to keep the current one. **Suspend** blocks the agent's login (and **Activate** re-enables it).

## How agents book

1. The agent opens your storefront and uses the **Agent login** link (`/agent/login` under your storefront URL)
2. Once signed in, their company name appears in the header and they book exactly like a public customer
3. After each booking they return to their **Dashboard**: bookings, commission earned, and passengers over the last 30 days, plus a table of recent bookings

You receive an internal **"New booking from <Agent>"** email for every agent sale — reference, route, passengers, totals, commission, and **net to you**, with Reply-To set to the agent. Public and operator-manual bookings don't trigger it.

## Commission

Commission is calculated at booking time (`subtotal × rate`), and the rate is **snapshotted** per purchase — changing an agent's rate later never rewrites existing bookings. Totals show on the Travel Agents list, and each purchase records the agent as its source.

## Card vs invoice payment terms

Each agent's **Payment terms** pill on the list toggles between:

* **Card on booking** — charged at checkout; tickets land fully Paid, nothing more to do
* **Invoice** — the ticket is issued normally (customer gets their ticket and wallet pass), but the seat lands **Unpaid** in money terms until the agent settles. Typical for councils administering subsidised fares on a grant cycle, or Net-30 agencies.

Track money state on the **Sales** dashboard's *Paid* column — per-row toggles, or checkboxes with **Mark paid** / **Mark unpaid** for batches. The Paid flag is money-received state only; it's independent of the ticket's lifecycle.

## Agent statements & raising invoices

For invoice-terms agents, bill on your own schedule from the **Agent statement** page (open it from the Travel Agents list):

1. Pick the **agent** and a **from/to date range** (defaults to the current month); leave **Outstanding bookings only** ticked for the invoice view
2. Review the rows — date, reference, **PO number**, route, seats, fares, outstanding amount, commission, and paid status, with totals at the foot
3. **Download statement (PDF)** for a branded statement, or **Export CSV** for your spreadsheet
4. Once the agent settles, **Mark all paid** clears every outstanding booking in the view

**With Xero or QuickBooks connected** (see [Accounting Integration](../accounting-integration/README.md)), tick the bookings to bill and click **Raise invoice in Xero/QuickBooks**. AeroQuote finds or creates the agent's contact, builds one line per ticket, and creates the invoice; invoiced bookings get an **Invoiced** badge linking to the invoice and are excluded from re-invoicing, so the same seat can't be billed twice.

## What agents can't do

* Refund or cancel bookings — operator-only
* Change their own password or commission rate
* See other agents' bookings

## Next steps

* [Day-of Operations](day-of-operations.md) — handling changes on agent-booked seats
* [Accounting Integration](../accounting-integration/README.md) — connect Xero or QuickBooks for invoice raising
