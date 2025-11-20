---
description: >-
  AeroQuote integrates with leading accounting platforms to streamline your
  invoicing workflow. This guide will help you connect QuickBooks or Xero to
  generate invoices.
---

# Accounting Integrationmak

The accounting integration allows you to:

* **Generate invoices directly from accepted quotes** - No need to manually re-enter quote details
* **Sync customer information** - AeroQuote automatically finds or creates customers in your accounting system
* **Customize invoice details** - Edit invoice line items, dates, and other details before sending
* **Maintain control** - Invoices are only created when you explicitly choose to generate them

AeroQuote currently integrates with:

* **QuickBooks Online** - Popular accounting software for small to medium businesses
* **Xero** - Cloud-based accounting platform used worldwide

{% hint style="info" %}
Only one accounting integration can be active at a time. If you need to switch between QuickBooks and Xero, you'll need to disconnect the current integration first.
{% endhint %}

## How It Works <a href="#using-facilities" id="using-facilities"></a>

### 1. Connect Your Accounting Platform

Navigate to **Settings → Integrations** and connect your QuickBooks or Xero account. This establishes a secure connection between AeroQuote and your accounting system. Follow the setup guides below for your prefered accounting package.

{% content-ref url="xero-integration-setup.md" %}
[xero-integration-setup.md](xero-integration-setup.md)
{% endcontent-ref %}

{% content-ref url="quickbooks-integration-setup.md" %}
[quickbooks-integration-setup.md](quickbooks-integration-setup.md)
{% endcontent-ref %}

### 2. Accept a Quote (Optional)

When you or your customer accepts a quote in AeroQuote, the quote status changes to "Accepted". This generally indicates it is time to request payment from the customer. <img src="../../.gitbook/assets/image (17).png" alt="" data-size="line">

### 3. Generate Invoice (When You're Ready)

On the Quote Details page, click the **"Generate Invoice"** button. This creates a **draft invoice** in AeroQuote's database (not yet sent to your accounting system).

<div align="left"><figure><img src="../../.gitbook/assets/image (18).png" alt="" width="375"><figcaption></figcaption></figure></div>

The draft invoice is pre-populated with:

* Customer information from your quote contacts
* Line items from your selected quote options
* Smart descriptions including quote code, aircraft, route, and dates
* Invoice and due dates

<figure><img src="../../.gitbook/assets/image (19).png" alt="" width="563"><figcaption></figcaption></figure>

#### 4. Send to Accounting System

When you're satisfied with the invoice details, click **"Send to QuickBooks"** or **"Send to Xero"**. This creates the draft invoice in your accounting platform.

Once sent:

* Invoice status changes to "Sent"
* External invoice ID and number are stored
* You can view the invoice directly in your accounting system
* A "View in QuickBooks/Xero" button appears with a direct link
