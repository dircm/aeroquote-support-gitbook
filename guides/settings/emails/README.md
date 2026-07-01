---
description: All system-generated emails sent by AeroQuote.
---

# 📬 System Emails

AeroQuote sends emails automatically in response to events, on a schedule, or when triggered by a user action. This section documents every system email, who receives it, what triggers it, and what it contains.

***

## Email Categories

| Category                                | Description                                                                             |
| --------------------------------------- | --------------------------------------------------------------------------------------- |
| [**Quote Emails**](quote-emails.md)     | Emails related to quotes — sent to customers, operators, and external operators         |
| [**Booking Emails**](booking-emails.md) | Emails related to bookings — sent to customers, crew, operators, and external operators |
| [**Admin Emails**](admin-emails.md)     | Account, subscription, and integration emails — sent to operators                       |

***

## Trigger Types

Each email is classified by how it is triggered:

| Trigger            | Meaning                                                                                                          |
| ------------------ | ---------------------------------------------------------------------------------------------------------------- |
| **User-initiated** | An operator clicks a button to send the email (e.g. sending a quote or booking confirmation)                     |
| **Automatic**      | The system sends the email in response to an event (e.g. a customer accepts a quote)                             |
| **Scheduled**      | A background job checks for conditions on a regular interval and sends the email when met (e.g. expiry warnings) |

***

## Who Receives Emails

| Recipient             | Examples                                                            |
| --------------------- | ------------------------------------------------------------------- |
| **Customer**          | Primary contact, additional contacts on a quote or booking          |
| **Operator**          | The operator team — typically the operator's main email address     |
| **Crew**              | Staff members assigned to booking flights                           |
| **External Operator** | Third-party operators whose aircraft are used in a quote or booking |
