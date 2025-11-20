---
description: >-
  This guide walks you through connecting Xero to AeroQuote and configuring
  optional invoice settings.
icon: sack-dollar
---

# Xero Integration Setup

Before you begin, ensure you have:

* ✅ An active **Xero** account (any subscription level)
* ✅ Admin or Adviser access to your Xero organization
* ✅ Admin access to your AeroQuote operator account

### Step 1: Navigate to Integrations Settings

1. Log into your AeroQuote account
2. Click **Settings** in the navigation menu
3. Select **Integrations** from the settings menu

You'll see two integration options: QuickBooks Online and Xero.

### Step 2: Connect to Xero

1. Click the **"Connect to Xero"** button (with Xero logo)

**What happens next:**

* A new window opens with the official Xero login page
* You'll be asked to sign in to your Xero account
* Xero will ask you to authorize AeroQuote to access your organization

#### OAuth Authorization Flow

1. **Sign in to Xero**: Enter your Xero email and password on the Xero login page
2. **Select your organization**: If you have multiple Xero organizations, select the one you want to connect
3. **Review permissions**: Xero shows what AeroQuote will be able to access:
   * Create and read invoices
   * Create and read contacts
   * Read tracking categories
   * Read branding themes
   * Read organization details
4. **Click "Authorize"**: Grant permission for the connection

#### After Authorization

Close the Authorized page or tab and go back to the **Integragtions** page. Wait for the connection status to automatically update to show:

* ✅ Green "Active" pill (if this is your only integration)
* 📅 Token refresh information

**That's it!**

#### Token Refresh Strategy

AeroQuote refreshes Xero tokens in two scenarios:

1. **Before expiration**: Every 30 days automatically
2. **On demand**: When the access token expires before an API call

{% hint style="info" %}
As long as you generate at least one invoice every 60 days, the connection will stay active indefinitely.
{% endhint %}

#### Reconnection (If Needed)

If your connection becomes inactive (e.g., no invoices for 60+ days):

1. Navigate to **Settings → Integrations**
2. Click **"Disconnect"** on the Xero card
3. Click **"Connect to Xero"** again
4. Complete the OAuth authorization flow
5. Start generating invoices again

{% hint style="info" %}
Previously created invoices are not affected by reconnection.
{% endhint %}

