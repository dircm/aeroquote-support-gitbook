---
description: Connect AeroQuote to your accounting software and other services.
---

# 🔌 Integrations

The Integrations tab lets you connect AeroQuote to external services like accounting software. Once connected, data flows automatically between systems.

---

## Accessing Integrations

1. Go to **Settings** from the sidebar
2. Click the **Integrations** tab

---

## Available Integrations

### Accounting Software

| Integration | Description |
|-------------|-------------|
| **Xero** | Automatic invoice creation and sync |
| **QuickBooks** | Invoice sync with QuickBooks Online |

### Other Integrations

| Integration | Description |
|-------------|-------------|
| **iFlightPlanner** | Route planning and facility data |
| **Firestore** | Real-time mobile app sync |

---

## Setting Up Accounting Integration

For detailed setup instructions, see:

{% content-ref url="../accounting-integration/xero-integration-setup.md" %}
[xero-integration-setup.md](../accounting-integration/xero-integration-setup.md)
{% endcontent-ref %}

{% content-ref url="../accounting-integration/quickbooks-integration-setup.md" %}
[quickbooks-integration-setup.md](../accounting-integration/quickbooks-integration-setup.md)
{% endcontent-ref %}

### Quick Overview

1. Click **Connect** next to your accounting software
2. Sign in to your accounting account
3. Authorize AeroQuote access
4. Configure sync settings

---

## Integration Status

Once connected, you'll see:

- **Connected** indicator with account details
- **Last Sync** timestamp
- **Disconnect** option

---

## Troubleshooting

### Connection Issues

If an integration shows as disconnected:

1. Click **Reconnect**
2. Re-authorize access
3. Check your accounting software for any required approvals

### Sync Errors

If invoices aren't syncing:

1. Check the integration status
2. Verify the booking/quote has all required fields
3. Review error messages in the sync log

{% hint style="info" %}
For persistent issues, contact support@aeroquote.com with details about the error.
{% endhint %}

---

## Disconnecting an Integration

1. Find the integration you want to remove
2. Click **Disconnect**
3. Confirm the disconnection

{% hint style="warning" %}
Disconnecting stops all data sync. Existing synced data remains in both systems.
{% endhint %}
