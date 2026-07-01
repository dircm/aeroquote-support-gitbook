---
description: Emails sent in relation to bookings — confirmations, crew notifications, completion summaries, and expiry warnings.
---

# Booking Emails

These emails are sent during the booking lifecycle — from confirmation through to flight completion.

---

## Customer Emails

### Booking Confirmation

| | |
|---|---|
| **Trigger** | User-initiated — operator clicks **Send to Customer** on the booking's Send tab |
| **Sent to** | Main contacts and/or additional contacts on the booking |
| **Content** | Booking code, route map, customer booking notes, and a secure link to the online booking view. Optionally includes **QR code boarding passes** for each passenger on charter flights. |

{% hint style="info" %}
The booking link can be sent as a **Basic View** (itinerary only) or **Detailed View** (includes passenger list and visible amendments). This is controlled per-contact group via toggles on the Send tab. See [Sending Confirmations](../bookings-operators/sending-confirmations.md) for details.
{% endhint %}

### Booking Comment Reply to Customer

| | |
|---|---|
| **Trigger** | Automatic — sent approximately 2 minutes after an operator replies to a customer's question on a booking |
| **Sent to** | Primary contact on the booking |
| **Content** | Booking code and notification of a new reply, with a signed link to the online booking view. |

---

## Crew Emails

### Crew Booking Itinerary

| | |
|---|---|
| **Trigger** | User-initiated — operator clicks **Send to Crew** on the booking's Send tab |
| **Sent to** | All crew members assigned to the booking who have an email address |
| **Content** | Booking code, flight assignments grouped by aircraft, and a secure link to the crew booking view. |

### Booking Completion Summary (Crew)

| | |
|---|---|
| **Trigger** | Automatic — sent approximately 2 hours after the final flight in a booking arrives |
| **Sent to** | All crew members assigned to the booking |
| **Content** | Booking code, flight summary for each leg (block off, departed, arrived, block on, actual duration), flight track maps where available, and a link to the crew booking view. Does **not** include cost or variance analysis. |

---

## External Operator Emails

### External Operator Booking Details

| | |
|---|---|
| **Trigger** | User-initiated — operator clicks **Send to External Operators** on the booking's Send tab |
| **Sent to** | External operators whose aircraft are assigned to the booking (must have an email address) |
| **Content** | Booking code, flight assignments for that external operator's aircraft only, and a secure link to the external operator booking view. |

---

## Operator Emails

### Customer Question on Booking

| | |
|---|---|
| **Trigger** | Automatic — customer submits a question on the online booking view |
| **Sent to** | Operator |
| **Content** | Booking code and question text. |

### Booking Comment from Customer

| | |
|---|---|
| **Trigger** | Automatic — sent approximately 2 minutes after a customer adds a follow-up comment to a booking question |
| **Sent to** | Operator |
| **Content** | Booking code and notification of unread comments. |

### Booking Completion Summary (Operator)

| | |
|---|---|
| **Trigger** | Automatic — sent approximately 2 hours after the final flight in a booking arrives |
| **Sent to** | Operator |
| **Content** | Booking code, flight summary for each leg (block off, departed, arrived, block on, actual duration), flight track maps where available, and a **planned vs actual variance analysis** for departure times and flight durations. Includes a link to view the booking. |

The variance analysis uses colour coding:

- **Green** — variance is within 15% of planned
- **Red** — variance exceeds 15% of planned

{% hint style="info" %}
The completion email is fully automatic. It is sent after the system confirms all block times are recorded — either from flight tracking data or from the 2-hour fallback timer. No manual action is required. See [Sending Confirmations](../bookings-operators/sending-confirmations.md#automatic-booking-completion-email) for more details.
{% endhint %}

### Booking Expiry Warning

| | |
|---|---|
| **Trigger** | Scheduled — runs every 10 minutes, checks for bookings that ended approximately 12 hours ago |
| **Sent to** | Operator |
| **Content** | Booking code and warning that the booking will auto-complete in 12 hours if not updated. Link to view the booking. |
| **Conditions** | Only sent for bookings in Confirmed or GroundTime status. Operator must have an active subscription. |

### Booking Auto-Completed

| | |
|---|---|
| **Trigger** | Scheduled — runs hourly, marks old bookings as Completed |
| **Sent to** | Operator |
| **Content** | Booking code and completion notice. |
| **Conditions** | Sent when a booking's end date is more than 7 days ago (or the operator's configured expiry period). Operator must have an active subscription. |
