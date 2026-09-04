---
description: >-
  Walk through the Quote Details step — status actions, contacts, validity,
  print/PDF, and how it fits with Options, Documents, and Send.
---

# Quote Details Page

The **Quote Details** step is the first tab you see when you open a quote from **Quotes** or the **Dashboard**. The page title shows **Quote** plus the quote reference code.

<figure><img src="../../../.gitbook/assets/Quote Details Page.png" alt="Quote Details step on an open quote"><figcaption></figcaption></figure>

***

## Quote steps (tabs)

Use the tabs at the top of the quote to move between builder steps:

| Tab (label) | What you do there |
| --- | --- |
| **Quote Details** | Status, contacts, validity, T&Cs, job notes, generate booking / invoice |
| **Options** (or **Flight** when there is only one option) | Edit itinerary, costs, and pricing; **Add Option** (top-left, Admin View); toggle **Admin View** / **Customer View**. See [Add a Quote Option](../add-a-quote-option.md) |
| **Documents** | Build the customer-facing PDF package and preview / download it |
| **Summary** | Review the cost breakdown per option (including per-passenger charges) before you send |
| **Send** | Email the quote and attachments to the customer |
| **Status** | Comments, questions, and status history |

{% hint style="info" %}
**Looking for a printable full itinerary?** See [View or print the full quote itinerary](../view-or-print-quote-itinerary.md).
{% endhint %}

***

## Header actions

These buttons appear near the top of **Quote Details** (permission and status dependent):

| Control | What it does |
| --- | --- |
| **Copy to new Quote** | Copies flights and aircraft options into a new quote (contacts are **not** copied). You choose a start date for the new quote. |
| **Save as Template** | Converts this quote into a reusable template for similar jobs. |
| **Delete Quote** | Permanently deletes this quote (confirmation required). |

***

## Status actions

Available actions depend on the current quote status (shown as **Quote Status …**):

| Control | Typical when | What it does |
| --- | --- | --- |
| **Accept Quote** | Created / In progress | Marks the quote as accepted |
| **Cancel Accept** | Accepted / partial payment / paid | Returns the quote toward in-progress so you can keep editing |
| **Mark as Paid** | Created through partial payment | Marks the quote paid (accounting can also set this when an invoice is paid) |
| **Generate a Booking** | Bookings module enabled | Opens **Create Booking from Quote** — pick the first charter date and option(s). After success, status becomes **Booking Generated**. [Learn more](../../bookings-operators/create-a-booking-from-a-quote.md). |
| **Generate another new Booking** | Already booking-generated | Creates an additional booking from the same quote |

{% hint style="warning" %}
**Accept Quote** does **not** by itself create an accounting invoice. If QuickBooks or Xero is connected, use the **Invoice** card on this page (**Generate Invoice**, then **Edit & Send** as needed).
{% endhint %}

***

## Job details and Download PDF

When the quote is **Accepted**, has **Partial payment**, is **Paid**, or has a **Booking generated**, a collapsible **Job details** section appears. It lists main contacts, selected aircraft options, and each leg (departing, duration, arriving, pax).

1. Open the quote on the **Quote Details** step
2. Expand **Job details** if it is collapsed (**View**)
3. Click **Download PDF**

This downloads an **internal job-details PDF** (totals, contacts, flight table per option). It is **not** the same as the branded customer document package from the **Documents** step.

***

## Quote date and validity

* **First flight departs** — Shows the first departure. Use **Set quote date** or **Change quote date** when needed (including after a TBC quote).
* **Valid till Date** — Set how many days the quote is valid, or reset an existing date. See [Edit Quote valid till date](edit-quote-valid-till-date.md).

***

## Contacts and notes

### Main Contacts

* Search **Add main contact (search name or email)** to attach customers who can receive the quote
* **Make Primary** / **Primary Contact** — one primary contact
* **Edit** or **Remove** (primary cannot be removed until another is primary)
* Contacts without email are flagged and skipped when sending

### Additional Recipients (view only)

People who can view the quote but are not main contacts. Add via **Add additional recipient (search name or email)**.

### Internal notes

**Internal notes (not visible to customer)** — operator-only notes for your team.

***

## Terms and Conditions

* Toggle **Customer required to accept.** so the online quote requires T&C acceptance
* **Load from Template** replaces the current T&C content with a saved template
* Edit the rich text body as needed

See also [Require T&Cs to be accepted online](../require-t-and-cs-to-be-accepted-online.md).

***

## Invoice (accounting)

Shown when QuickBooks or Xero is connected and the quote is in a billable status:

1. Click **Generate Invoice** to create a draft in your accounting system
2. Use **Edit & Send**, **View Details**, or **View in QuickBooks/Xero** as the draft progresses

See [Accounting Integration](../../accounting-integration/).

***

## Related guides

* [View or print the full quote itinerary](../view-or-print-quote-itinerary.md)
* [Add a Quote Option](../add-a-quote-option.md)
* [Creating a Quote from scratch](../creating-a-quote.md)
* [Cost Management](../cost-management.md)
* [Using Documents in a Quote](../../documents/using-documents-in-a-quote.md)
* [Create a Booking from a Quote](../../bookings-operators/create-a-booking-from-a-quote.md)
