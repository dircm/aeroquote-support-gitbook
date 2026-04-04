---
description: Emails sent in relation to quotes — customer quotes, acceptance notifications, expiry warnings, and RFQ communications.
---

# Quote Emails

These emails are sent during the quoting process — from sending a quote to a customer through to acceptance, payment, expiry, and archival.

---

## Customer Emails

### Quote Sent to Customer

| | |
|---|---|
| **Trigger** | User-initiated — operator sends quote from the Send step |
| **Sent to** | Primary contact and/or additional contacts |
| **Content** | Quote details with a link to the online quote view. Uses a customisable email template (editable in Settings → Templates) with merge fields for quote number, customer name, operator branding, and contact details. |

{% hint style="info" %}
The quote email template is fully customisable per operator. You can edit the subject line, body text, and merge fields in **Settings → Templates**. Additional contacts receive a preview-only link without accept/decline actions.
{% endhint %}

### Quote Comment Reply to Customer

| | |
|---|---|
| **Trigger** | Automatic — sent approximately 2 minutes after an operator replies to a customer's question on a quote |
| **Sent to** | Primary contact on the quote |
| **Content** | Notification that a new reply has been added to their question, with the quote reference. |

---

## Operator Emails

### Quote Accepted

| | |
|---|---|
| **Trigger** | Automatic — customer accepts the quote online |
| **Sent to** | Operator |
| **Content** | Quote code, selected aircraft options with full itinerary (departure, duration, arrival, passengers), customer contact details (name, phone, email), and a link to view the quote. |

### Quote Paid

| | |
|---|---|
| **Trigger** | Automatic — webhook from Xero or QuickBooks when the linked invoice is fully paid |
| **Sent to** | Operator |
| **Content** | Quote code, payment confirmation message, and invoice details. |

### Quote Partial Payment

| | |
|---|---|
| **Trigger** | Automatic — webhook from Xero or QuickBooks when a partial payment is received |
| **Sent to** | Operator |
| **Content** | Quote code, amount paid, amount remaining. |

### Customer Question on Quote

| | |
|---|---|
| **Trigger** | Automatic — customer submits a question on the online quote view |
| **Sent to** | Operator |
| **Content** | Quote code, question text, and customer contact details. |

### Quote Comment from Customer

| | |
|---|---|
| **Trigger** | Automatic — sent approximately 2 minutes after a customer adds a follow-up comment to a quote question |
| **Sent to** | Operator |
| **Content** | Quote code and notification of unread comments. |

### Quote Expiry Warning

| | |
|---|---|
| **Trigger** | Scheduled — runs every 10 minutes, checks for quotes expiring within approximately 24 hours |
| **Sent to** | Operator |
| **Content** | Quote code, expiry time, and customer details. Link to view the quote. |
| **Conditions** | Only sent for quotes in an active status (Created, In Progress, Sent, Changes Requested, or Mail Opened). Operator must have an active subscription. |

### Quote Has Expired

| | |
|---|---|
| **Trigger** | Scheduled — runs every 10 minutes, sent when a quote's valid-until date has passed |
| **Sent to** | Operator |
| **Content** | Quote code and expiry notice. |
| **Conditions** | Operator must have an active subscription. |

### Quotes Archived

| | |
|---|---|
| **Trigger** | Scheduled — runs twice monthly (1st and 16th) for quotes older than 9 months |
| **Sent to** | Operator |
| **Content** | List of quotes that have been automatically archived. |
| **Conditions** | Operator must have an active subscription. |

---

## Request for Quote (RFQ) Emails

These emails are exchanged between operators and external operators during the RFQ process.

### RFQ Sent to External Operator

| | |
|---|---|
| **Trigger** | User-initiated — operator sends an RFQ from the Request page or Quote Builder |
| **Sent to** | External operator |
| **Content** | Flight details, aircraft requirements, passenger count, job notes, and operator contact information. |

### Grouped RFQ Sent to External Operator

| | |
|---|---|
| **Trigger** | User-initiated — operator sends multiple RFQs to the same external operator at once |
| **Sent to** | External operator |
| **Content** | Multiple RFQ requests grouped into a single email. |

### RFQ Response Received

| | |
|---|---|
| **Trigger** | Automatic — external operator submits their response to an RFQ |
| **Sent to** | Operator |
| **Content** | Quoted price, response message from the external operator, and a link to the quote options. |

### RFQ Approved

| | |
|---|---|
| **Trigger** | Automatic — operator approves/accepts an external operator's RFQ response |
| **Sent to** | External operator |
| **Content** | Notification that their quote has been accepted. |

### RFQ Question

| | |
|---|---|
| **Trigger** | User-initiated — operator asks a question on an RFQ |
| **Sent to** | External operator |
| **Content** | RFQ reference and question text. |

### RFQ Comment Reply to Operator

| | |
|---|---|
| **Trigger** | Automatic — external operator replies to an RFQ comment |
| **Sent to** | Operator |
| **Content** | RFQ/quote reference and notification of unread comments. |

### RFQ Comment Reply to External Operator

| | |
|---|---|
| **Trigger** | Automatic — operator replies to an RFQ comment |
| **Sent to** | External operator |
| **Content** | RFQ/quote reference and notification of unread comments. |

### RFQ Attachment Added

| | |
|---|---|
| **Trigger** | User-initiated — operator adds an attachment to an RFQ |
| **Sent to** | External operator |
| **Content** | Attachment name and RFQ reference. |
