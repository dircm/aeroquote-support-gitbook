---
description: Send booking confirmations and updates to customers.
---

# 📧 Sending Confirmations

The Send section lets you communicate with customers about their booking. Send confirmations, updates, and itineraries directly from AeroQuote.

---

## Accessing Send Options

1. Go to **Bookings** from the sidebar
2. Click on a booking
3. Select the **Send** tab

---

## What You Can Send

| Document Type | Purpose |
|---------------|---------|
| **Booking Confirmation** | Confirms the booking details |
| **Itinerary** | Flight schedule and details |
| **Invoice** | Payment request |
| **Manifest** | Passenger/cargo list |
| **Updates** | Changes or notifications |

---

## Sending a Confirmation

### Step 1: Select Document Type

Choose what you want to send (e.g., Booking Confirmation).

### Step 2: Choose Recipients

Select who should receive it:
- Primary customer contact
- Additional contacts on the booking
- Custom email addresses

### Step 3: Preview

Review what will be sent:
- Check the content is correct
- Verify recipient details
- Review any attachments

### Step 4: Send

Click **Send** to deliver the communication.

---

## Email Templates

AeroQuote uses templates for communications:

- **Subject line** — Includes booking reference
- **Body** — Professional template with your branding
- **Attachments** — PDFs of relevant documents

Templates can be customized in Settings → Communications.

---

## Online Booking View

Instead of (or in addition to) email, customers can view bookings online:

1. Send includes a link to the online booking view
2. Customer clicks link
3. Sees real-time booking details
4. Can view itinerary, status updates

{% hint style="info" %}
Online booking view keeps customers informed without you sending constant updates.
{% endhint %}

---

## Resending Communications

Need to send again?

1. Go to Send tab
2. Select the document type
3. Choose recipients
4. Send again

Previous sends are logged in the booking history.

---

## Communication History

Track what's been sent:

| Column | Description |
|--------|-------------|
| **Date** | When it was sent |
| **Type** | Confirmation, invoice, etc. |
| **Recipients** | Who received it |
| **Status** | Sent, delivered, opened (if tracked) |

---

## Sending Updates After Changes

When you make changes to a booking:

1. Update the booking details
2. Go to Send tab
3. Send an updated confirmation
4. Customer receives current information

{% hint style="success" %}
**Communicate changes proactively** — Customers appreciate being informed before they have to ask.
{% endhint %}

---

## Crew Communications

You can send booking details to crew:
- Flight brief
- Passenger manifest
- Route information
- Special requirements

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

This helps operators identify flights that consistently run over or under estimated durations, informing future quoting accuracy.

{% hint style="info" %}
The completion email is fully automatic — no manual action is required. It fires after the system confirms all block times are recorded, either from flight tracking or from the 2-hour fallback timer.
{% endhint %}

---

## Tips

- Send confirmation immediately after booking creation
- Include clear next steps for the customer
- Attach relevant documents (itinerary PDF, etc.)
- Follow up closer to departure with reminders
- The completion email handles post-flight communication automatically

---

## Next Steps

- [Booking Status](booking-status.md) — Keep status updated
- [Passengers & Cargo](passengers-and-cargo.md) — Complete the manifest
