---
icon: sack-dollar
---

# Payment Status Tracking

When your customers pay invoices in QuickBooks or Xero, AeroQuote automatically updates your quote status and notifies you—instantly. No manual updates, no checking back and forth between systems. You'll know the moment a payment is received, whether it's partial payment or paid in full.

This guide shows you what happens when your customers make payments and how AeroQuote keeps you informed every step of the way.

### What Happens When a Customer Pays

Once you've connected [QuickBooks](quickbooks-integration-setup.md) or [Xero](xero-integration-setup.md) and [sent an invoice from AeroQuote](./#id-4.-send-to-accounting-system), the payment tracking begins automatically. Here's what you can expect:

#### The Moment Payment is Received

As soon as your customer makes a payment in your accounting system:

1. **You receive an email** with payment details
2. **The quote status updates automatically** in AeroQuote
3. **A status badge appears** on the quote details page
4. **The activity log records** the payment for your records

All of this happens within seconds—no action required from you.

### Understanding Partial Payments

#### What You'll See

Sometimes customers pay part of an invoice upfront, with the rest to follow. AeroQuote recognizes these partial payments and tracks them separately.

**Example Scenario:** Your quote for $10,000 is invoiced. The customer pays $4,000 as a deposit, with the remaining $6,000 due later.

#### Email Notification

You'll receive an email like this:

**Subject:** Quote AQ-2024-1234 partial payment received via QuickBooks invoice INV-5678

```
Quote AQ-2024-1234 - Partial Payment Received
via QuickBooks invoice INV-5678

A partial payment has been received for this quote.

Amount Paid: $4,000.00
Amount Remaining: $6,000.00

[View Quote]
```

Click the **View Quote** button to see the updated quote details in AeroQuote.

#### What Changes in AeroQuote

**On the Quote Details Page:**

* The quote status changes to **"Partial Payment Received"**
* A blue **"Partial Payment"** badge appears in the Invoice panel with a currency icon
* The activity log shows a new entry: "Quote partial payment received"

**Finding Your Quotes:**

* Quotes with partial payments are easy to identify in your quote list
* Use the status filter to find all quotes awaiting final payment
* The blue status badge makes them stand out at a glance

#### Multiple Partial Payments

If your customer makes several partial payments, AeroQuote tracks each one:

* You receive a new email notification for each payment
* The email shows the cumulative amount paid and remaining balance
* The quote stays in "Partial Payment Received" status until fully paid
* All payment events are recorded in the activity log

**Example:**

* Payment 1: $4,000 paid → Email shows $4,000 paid, $6,000 remaining
* Payment 2: $3,000 paid → Email shows $7,000 paid, $3,000 remaining
* Payment 3: $3,000 paid → Quote marked as "Paid" (see next section)

### Understanding Full Payment

#### What You'll See

When your customer pays the full invoice amount (or the final installment), AeroQuote marks the quote as fully paid.

**Example Scenario:** Your $10,000 invoice is paid in full, or the final $3,000 installment completes the payment.

#### Email Notification

You'll receive a confirmation email like this:

**Subject:** Quote AQ-2024-1234 paid via Xero invoice INV-5678

```
Quote AQ-2024-1234 has been paid
via Xero invoice INV-5678

[View Quote]
```

#### What Changes in AeroQuote

**On the Quote Details Page:**

* The quote status changes to **"Paid"**
* A green **"Paid"** badge appears in the Invoice panel with a checkmark icon
* The activity log shows: "Quote paid in full"

**Your Next Steps:** Once a quote is fully paid, you can:

* **Convert it to a booking** to begin flight operations
* **Generate additional invoices** if amendments or extra services are needed
* **View the complete payment history** in the activity log
* **Export the data** for your records or reporting

### What You Need to Know

#### It Just Works

Once you've connected QuickBooks or Xero and sent an invoice from AeroQuote, payment tracking is automatic. There's no setup, no configuration, and no manual steps to take.

#### Only Tracks AeroQuote Invoices

{% hint style="warning" %}
If you create an invoice directly in QuickBooks or Xero without using AeroQuote, it won't be tracked.
{% endhint %}

Payment tracking works for invoices you've generated and sent from AeroQuote using the **"Send to QuickBooks"** or **"Send to Xero"** buttons.

#### Works with Any Payment Method

It doesn't matter how your customer pays—credit card, bank transfer, check, or cash. As long as the payment is recorded in QuickBooks or Xero and applied to the invoice, AeroQuote will track it.

#### Real-Time Updates

Changes appear in AeroQuote within seconds of payment being recorded in your accounting system. You don't need to refresh the page—the status updates automatically.

#### Everyone Sees the Same Thing

When a payment is received, all team members viewing that quote will see the updated status. The change is instant and system-wide.

#### Complete Payment History

Every payment event is recorded in the quote's activity log with timestamps. You can always review:

* When payments were received
* How much was paid each time
* The running balance
* The complete payment timeline

### Common Questions

#### "What if I don't receive the email notification?"

First, check your spam or junk folder—sometimes automated emails end up there. If you still don't see it, the payment status will still be updated in AeroQuote. You can verify by checking the quote details page and viewing the status badge and activity log.

To ensure you receive future notifications:

* Add AeroQuote to your email contacts or safe senders list
* Verify your email address is correct in Settings
* Contact support if the issue persists



#### "Can I manually change the quote status to Paid?"

Yes! If you need to mark a quote as paid manually (for example, if payment was received outside your accounting system), you can use the **"Mark as Paid"** button on the quote details page. This gives you flexibility for special situations.

#### "What if a customer pays in my accounting system before I send the invoice from AeroQuote?"

The payment tracking starts when you send the invoice from AeroQuote. If payment was recorded earlier in QuickBooks or Xero, AeroQuote will check the invoice status when it's sent and immediately reflect the correct payment status.

#### "Can I disable payment tracking?"

Payment tracking is automatic and cannot be disabled as long as your accounting integration is active. It's designed to keep your quote statuses accurate without any effort on your part. If you disconnect QuickBooks or Xero, payment tracking will stop.

### Tips for Success

#### Send Invoices from AeroQuote

Always use the **"Generate Invoice"** and **"Send to QuickBooks/Xero"** features in AeroQuote. This ensures payment tracking works correctly and your quote stays synchronized with your accounting records.

#### Review the Activity Log

The activity log on each quote shows you the complete payment timeline. Use it to:

* Verify when payments were received
* Track payment progression over time
* Provide payment history to customers if needed
* Audit your payment records

#### Use Status Filters

In your quote list, use the status filter to quickly find:

* All quotes awaiting payment (Status: Accepted or Sent)
* Quotes with partial payments (Status: Partial Payment Received)
* Fully paid quotes (Status: Paid)

This helps you stay on top of your outstanding invoices and follow up on payments.

#### Convert Paid Quotes to Bookings Promptly

Once a quote shows "Paid" status, you can proceed with confidence. [Convert it to a booking](../bookings-operators/create-a-booking-from-a-quote.md) so your operations team can begin planning the flight. The payment status confirmation eliminates uncertainty.

### Getting Help

If you have questions or encounter issues with payment tracking:

1. **Check the Activity Log** on the quote details page to see if payment events were recorded
2. **Verify the invoice was sent** via AeroQuote's "Send to QuickBooks/Xero" feature
3. **Confirm your integration is active** in Settings → Integrations
4. **Review your accounting system** to ensure the payment was applied to the correct invoice
5. **Contact support** if you need assistance—include the quote code and invoice number

Payment tracking is designed to work automatically and reliably. Most issues are resolved quickly by checking these common areas.

