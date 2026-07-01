---
description: Account, subscription, and integration emails sent to operators.
---

# Admin Emails

These emails relate to your AeroQuote account, subscription, and third-party integrations.

---

## Subscription & Account

### Trial Ending Warning

| | |
|---|---|
| **Trigger** | Scheduled — runs hourly, sent 3 days before your trial expires |
| **Sent to** | Operator |
| **Content** | Warning that your trial ends in 3 days, with a prompt to subscribe. |

### Trial Expired

| | |
|---|---|
| **Trigger** | Scheduled — runs hourly, sent within 1 hour after your trial ends |
| **Sent to** | Operator |
| **Content** | Notification that your trial has ended, with a prompt to upgrade. |

### Subscription Cancelled

| | |
|---|---|
| **Trigger** | Automatic — sent when a subscription is cancelled (either by the operator or via Stripe) |
| **Sent to** | Operator |
| **Content** | Cancellation confirmation, cancellation date, and who initiated the cancellation. |

### Bookings Module Deactivated

| | |
|---|---|
| **Trigger** | Automatic — sent when the Bookings & Flight Tracking module is deactivated for non-payment after the grace period ends |
| **Sent to** | Operator |
| **Content** | Notification that the Bookings module has been deactivated. |

---

## Accounting Integrations

### Xero Invoice Created

| | |
|---|---|
| **Trigger** | Automatic — sent after AeroQuote successfully creates an invoice in Xero |
| **Sent to** | Operator |
| **Content** | Quote code, Xero invoice number, and a link to the invoice in Xero. |

### Xero Connection Failed

| | |
|---|---|
| **Trigger** | Automatic — sent when AeroQuote encounters an error creating or syncing an invoice with Xero |
| **Sent to** | Operator |
| **Content** | Error message and troubleshooting information. Common causes include expired tokens, missing connection data, or API errors. |

### Xero Token Expiring

| | |
|---|---|
| **Trigger** | Scheduled — runs weekly, checks for Xero tokens that are about to expire |
| **Sent to** | Operator |
| **Content** | Warning that your Xero connection token is expiring soon, with a prompt to reconnect. |

### QuickBooks Invoice Created

| | |
|---|---|
| **Trigger** | Automatic — sent after AeroQuote successfully creates an invoice in QuickBooks |
| **Sent to** | Operator |
| **Content** | Quote code, QuickBooks invoice number, and a link to the invoice in QuickBooks. |

### QuickBooks Connection Failed

| | |
|---|---|
| **Trigger** | Automatic — sent when AeroQuote encounters an error creating or syncing an invoice with QuickBooks |
| **Sent to** | Operator |
| **Content** | Error message and troubleshooting information. Common causes include missing connection data, unconfigured line items, or API errors. |

---

## Website Widget

### New Enquiry from Widget

| | |
|---|---|
| **Trigger** | Automatic — a website visitor submits a quote request via the AeroQuote widget embedded on your website |
| **Sent to** | Operator |
| **Content** | Flight itinerary with route map, passenger count, customer contact details (name, email, phone), and a link to open the request in AeroQuote. |

{% hint style="info" %}
Widget enquiries are automatically created as requests in AeroQuote. The email is a notification that a new request is waiting for your review. See [Widgets](../widgets/README.md) for setup instructions.
{% endhint %}
