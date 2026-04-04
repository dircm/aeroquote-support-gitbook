---
description: Send booking confirmations and updates to customers, crew, and external operators.
---

# Sending Confirmations

The **Send** tab lets you communicate booking details to customers, crew members, and external operators directly from AeroQuote.

---

## Accessing the Send Tab

1. Go to **Bookings** from the sidebar
2. Click on a booking
3. Select the **Send** tab

You will see three send buttons at the top of the page:

| Action | Recipients | When to use |
|--------|-----------|-------------|
| **Send to Customer** | Main contacts and additional recipients on the booking | After creating or updating a booking |
| **Send to Crew** | All crew members assigned to the booking | After assigning crew and finalising the itinerary |
| **Send to External Operators** | External operators whose aircraft are assigned | When using aircraft from another operator |

{% hint style="info" %}
The **Send to External Operators** button is disabled if no external aircraft are assigned to the booking.
{% endhint %}

---

## Sending to Customers

### Step 1: Review Recipients

The Send tab shows two recipient groups pulled from the booking's contact list:

- **Main Contacts** — contacts marked as main contacts on the booking. The designated **Primary Contact** is shown with a badge.
- **Additional Recipients** — other contacts attached to the booking.

{% hint style="warning" %}
Recipients are the contacts assigned to the booking. You cannot enter custom email addresses — to add a recipient, first add them as a contact on the booking's **Contacts** tab.
{% endhint %}

### Step 2: Choose Basic or Detailed View

For each contact group, toggle **Send with Detailed View** to control what the customer sees when they click the link in their email:

- **Basic View** — booking summary with flight itinerary
- **Detailed View** — includes the passenger list and any amendments marked as visible

You can also copy the booking link to your clipboard to share it manually.

### Step 3: Preview and Add Notes

Click **Send to Customer** to open the preview modal. Here you can:

- **Preview** the customer booking view exactly as the recipient will see it
- **Edit Customer Booking Notes** — add or update notes that appear in the customer's email (e.g. special instructions, payment details, or a personal message)
- **Include QR code boarding passes** — toggle this on to attach scannable boarding passes for each passenger in the email (requires [Bookings V2](../../whats-new/april-2026.md))

### Step 4: Send

Click **Send Now** to deliver the email. The system records when the email was last sent — this timestamp is shown beneath the Send to Customer button.

---

## Sending to Crew

Click **Send to Crew** to open a preview of the crew booking view. This shows the itinerary grouped by aircraft with crew-specific flight assignments.

Crew emails are sent to all crew members assigned to the booking who have an email address on file.

---

## Sending to External Operators

Click **Send to External Operators** to preview the external operator view. This shows only the flights relevant to each external operator's aircraft.

Emails are sent to external operators who have an email address on file.

---

## Customer Booking Notes

You can add custom notes to the customer email. These appear in the email body above the booking link.

- **Per-booking notes** — edit in the send confirmation modal before each send
- **Default notes** — set a default message for all new bookings in **Settings → Default Units** under the "Default Booking Customer Notes" field

---

## Online Booking View

Every customer email includes a secure link to an online booking view. Customers can:

- View the full itinerary and booking details in their browser
- See real-time status updates without you needing to resend
- Download the itinerary PDF

The link is cryptographically signed — no login is required, but only people with the link can access it.

{% hint style="info" %}
The online booking view keeps customers informed without you needing to send constant updates. Share the link once and they can check back any time.
{% endhint %}

---

## Resending After Changes

When you make changes to a booking:

1. Update the booking details
2. Go to the **Send** tab
3. Click the relevant send button (Customer, Crew, or External Operators)
4. Review the preview and click **Send Now**

The "Last sent" timestamp beneath each button shows when that communication was most recently sent.

{% hint style="success" %}
**Communicate changes proactively** — Customers appreciate being informed before they have to ask.
{% endhint %}

---

## Automatic Booking Completion Email

When a booking is fully completed and all block times have been recorded, AeroQuote **automatically sends a completion summary email** to:

* The **operator** — full flight summary with planned vs actual duration analysis
* All **assigned crew members** — flight summary without cost analysis

This email is sent approximately **2 hours after the final flight arrives** (allowing time for block times and flight track data to be finalised).

### What's included

Each flight in the booking shows:

| Detail | Description |
|--------|-------------|
| **Block Off** | Time the aircraft left the gate/parking |
| **Departed** | Takeoff time |
| **Arrived** | Landing time |
| **Block On** | Time the aircraft reached the gate/parking |
| **Actual Duration** | Total flight time (departed to arrived) |
| **Flight Track Map** | Static map showing the actual path flown (when flight tracking data is available) |

### Operator-only: Duration Variance

The operator version includes a **planned vs actual duration** comparison for each flight:

* **Green** — Actual duration was shorter than planned
* **Red** — Actual duration was longer than planned

This helps identify flights that consistently run over or under estimated durations, informing future quoting accuracy.

{% hint style="info" %}
The completion email is fully automatic — no manual action is required. It fires after the system confirms all block times are recorded, either from flight tracking or from the 2-hour fallback timer.
{% endhint %}

---

## Tips

- Send the customer confirmation as soon as the booking is created
- Use **Customer Booking Notes** for payment terms, meeting points, or any message specific to this booking
- Toggle **Detailed View** on when you want customers to see their passenger list and any amendments
- The completion email handles post-flight communication automatically — no action needed

---

## Next Steps

- [Booking Status](booking-status.md) — Track and update flight status
- [Passengers & Cargo](passengers-and-cargo.md) — Manage the passenger and cargo manifest
- [Crew Assignment](crew-assignment.md) — Assign crew to flights
