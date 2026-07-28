---
description: >-
  See when customers open your quote and booking emails and when they open the
  quote or booking link.
---

# 🆕 Email Tracking

AeroQuote tracks engagement on the **customer quote emails** and **customer booking emails** you send — so you can see whether a message was sent, opened in the inbox, and whether the customer opened the quote or booking link.

Nothing extra to turn on: tracking starts automatically when you send those emails as usual.

***

## Status meanings

| Status       | What it means                                                                  |
| ------------ | ------------------------------------------------------------------------------ |
| **Not sent** | No customer quote/booking email has been sent yet (or the last send failed)    |
| **Sent**     | The email was accepted for delivery                                            |
| **Opened**   | The email was opened in the customer's inbox (open pixel)                      |
| **Viewed**   | The customer opened the **quote** or **booking** link (loaded the online page) |

Statuses move forward for the **latest** send: **Sent → Opened → Viewed**.

{% hint style="info" %}
**Viewed** is about the link, not the inbox. A customer can open the email without images and never show as Opened, then still become Viewed when they click through to the online quote or booking.
{% endhint %}

***

## Which emails are tracked

| Tracked                                       | Not tracked (this release)                            |
| --------------------------------------------- | ----------------------------------------------------- |
| Quote email to the customer (Send step)       | Operator notification emails (accepted, expiry, etc.) |
| Customer booking email (**Send to Customer**) | Crew booking emails                                   |
|                                               | External operator booking emails                      |
|                                               | Comment / question notification emails                |
|                                               | RFQ and other system emails                           |

***

## Where to see tracking

### Quote and booking lists

The **mail status** column shows **NotSent**, **Sent**, **Opened**, or **Viewed** (with a relative time for recent activity where shown).

Use this to scan which quotes need a follow-up (still only Sent) versus which customers have engaged.

### Quote — Send step

After you send, the Send step shows:

* Last sent time
* Current mail status
* For the latest tracked send: **Opened** and **Link** (with times and counts when available)

### Quote — Status step

An **Email tracking** panel lists recent quote emails for that quote:

* When each was sent and to whom
* Opened time and open count
* Link click time and click count

Quote **events** still log send and “email viewed” activity as before.

### Booking — Send tab

Under **Send to Customer**:

* Last sent time and mail status
* Open / link summary for the latest customer email
* A short **Customer email tracking** history when you have sent more than once

Crew and external-operator sends are unchanged and are not included in this tracking.

### Dashboard

On the home **Dashboard**, three cards summarise quote email engagement over the **last 30 days** (with a comparison to the prior 30 days):

| Card                  | What it counts                                                                     |
| --------------------- | ---------------------------------------------------------------------------------- |
| **Quote Emails Sent** | Number of tracked quote email sends                                                |
| **Email Opens**       | Quote emails that recorded at least one open                                       |
| **Link Clicks**       | Quote emails that recorded at least one link open (customer opened the quote page) |

These cards refresh when you send, open, or click; a normal page refresh is enough to pick up new activity.

***

## How it works (briefly)

1. **Sent** — recorded when AeroQuote successfully sends the customer quote or booking email.
2. **Opened** — a tiny tracking image (pixel) in the email loads when the client displays images.
3. **Viewed** — the customer opens the signed **Open quote** / **View booking** link and loads the online page (not as an operator preview).

Resending creates a new tracked send. List and summary status reflect the **latest** send; older sends remain visible in the tracking history panels.

***

## Limitations and caveats

{% hint style="warning" %}
**Opens are not guaranteed.** Many email apps block images by default. Treat **Opened** as a useful signal when present, not proof that every reader opened the message.
{% endhint %}

* **Sent** means AeroQuote handed the message to the mail system — it is not a full delivery or bounce report.
* **Operator previews** and **preview links** (e.g. additional contacts on a quote) do not mark the quote as Viewed the way a real customer open does.
* Opening the quote/booking while logged in as that operator is treated as preview and does not count as a customer Viewed.
* Only **customer quote** and **customer booking** emails are in scope for this feature.

***

## Tips

* Still **Sent** after a day? Consider a short follow-up call or resend with a clearer subject.
* **Opened** but not **Viewed**? They may have seen the email but not clicked — a phone call often works better than another long email.
* **Viewed**? Good time to prioritise a personal follow-up while the quote is on their mind.
* Use the **dashboard** cards to spot quiet weeks or a drop in opens after template changes.

***

## Related guides

* [Quote Emails](quote-emails.md) — what goes out when you send a quote
* [Booking Emails](booking-emails.md) — customer booking confirmation content
* [Sending Confirmations](../../bookings-operators/sending-confirmations.md) — booking Send tab
* [Dashboard](../../dashboard/) — home metrics
