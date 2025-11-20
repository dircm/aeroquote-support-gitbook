---
description: >-
  This guide walks you through connecting QuickBooks Online to AeroQuote and
  configuring the required invoice settings.
icon: sack-dollar
---

# Quickbooks Integration Setup

Before you begin, ensure you have:

* ✅ An active **QuickBooks Online** subscription (QuickBooks Desktop is not supported)
* ✅ Admin access to your QuickBooks Online account
* ✅ Admin access to your AeroQuote operator account
* ✅ **At least one Service** item created in QuickBooks - [learn how to create a Service Item here](https://quickbooks.intuit.com/au/learn-and-support/quickbooks-online/add-products-services/).

{% hint style="info" %}
This integration requires QuickBooks **Online** - the cloud-based version. QuickBooks Desktop is not supported.
{% endhint %}

### Step 1: Navigate to Integrations Settings

1. Log into your AeroQuote account
2. Click **Settings** in the navigation menu
3. Select **Integrations** from the settings menu
4. Scroll to the **Accounting Integrations** section

You'll see two integration options: QuickBooks Online and Xero.

### Step 2: Connect to QuickBooks

1. Locate the **QuickBooks Online** card
2. Click the green **"Connect to QuickBooks"** button

**What happens next:**

* A new window opens with the official Intuit/QuickBooks login page
* You'll be asked to sign in to your QuickBooks account
* QuickBooks will ask you to authorize AeroQuote to access your account

#### Authorization Flow

1. **Sign in to QuickBooks**: Enter your QuickBooks username and password on the Intuit login page
2. **Select your company**: If you have multiple QuickBooks companies, select the one you want to connect
3. **Review permissions**: QuickBooks shows what AeroQuote will be able to access:
   * Create and read invoices
   * Create and read customers
   * Read items (products and services)
   * Read payment terms, classes, and departments
4. **Click "Connect"**: Authorize the connection

#### After Authorization

Close the Authorized page or tab and go back to the **Integrations** page. ⏲ Wait for the connection status to automatically update to show:

* ✅ Green "Connected" badge
* ✅ Green "Active" pill (if this is your only integration)
* 📅 Token expiration countdown (refreshes automatically)

<div data-full-width="false"><figure><img src="../../.gitbook/assets/Screenshot 2025-10-16 at 5.08.08 pm.png" alt="" width="563"><figcaption></figcaption></figure></div>

### Step 3: Configure Default Service Item (<mark style="color:$danger;">Required</mark>)

{% hint style="warning" %}
**This step is mandatory for QuickBooks integration.** Without a default invoice line item configured, invoice generation will fail.
{% endhint %}

#### What is a Default Invoice Service Item?

When AeroQuote creates an invoice in QuickBooks, every line item must be associated with a Service item from your QuickBooks Products and Services list. The "Default Invoice Line Item" is the item that will be used for all invoice line items generated from quotes. [learn how to create a Service Item here](https://quickbooks.intuit.com/au/learn-and-support/quickbooks-online/add-products-services/).

#### Selecting Your Default Line Item

Once connected, you'll see an **Invoice Configuration** section appear below the QuickBooks card:

1. Locate the **"Default Invoice Line Item"** dropdown
2. Click the dropdown to see all Products and Services from your QuickBooks account
3. Type to search and select the item you want to use (e.g., "Charter Flight Services", "Aviation Services", "Flight Booking")
4. The selection saves automatically

**Tip**: The dropdown loads items from QuickBooks in real-time, so you'll see exactly what's in your QuickBooks Products and Services list.

#### Don't have a suitable item yet?

If you don't have an appropriate Product or Service item in QuickBooks, you'll need to create one first. [learn how to create a Service Item here](https://quickbooks.intuit.com/au/learn-and-support/quickbooks-online/add-products-services/)

Common options for aviation charter operators:

* "Charter Flight Services"
* "Aircraft Charter"
* "Flight Services"
* "Aviation Services"
* "Private Charter"

### Step 5: Test the Connection

To verify everything is working:

1. Navigate to a quote with "**Accepted**" status
2. Look for the **Invoice** section on the Quote Details page
3. Click **"Generate Invoice"**
4. Verify the invoice modal opens with prepopulated data
5. Review the invoice and click **"Send to QuickBooks"**
6. Check that the invoice appears in your QuickBooks account

