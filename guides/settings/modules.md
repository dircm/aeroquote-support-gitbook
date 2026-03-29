---
description: Enable, disable, and manage AeroQuote module subscriptions.
---

# 🧩 Modules

The Modules tab lets you customize which features are active in your AeroQuote account. Some modules are included free with your plan, while others are available as paid add-ons.

---

## Accessing Modules

1. Go to **Settings** from the sidebar
2. Click the **Modules** tab

---

## Available Modules

| Module | Type | Description |
|--------|------|-------------|
| **Bookings & Flight Tracking** | Paid | Manage bookings, track flights, assign crew and passengers, and access analytics |
| **Request for Quote (RFQ)** | Free | Enable broker-style RFQ workflows to source aircraft from external operators |

---

## Free vs Paid Modules

Modules are labelled with a **Free** or **Paid** badge on the module card.

- **Free modules** can be toggled on or off instantly with no billing impact
- **Paid modules** show pricing on the card and require a subscription confirmation before enabling

---

## Subscribing to a Paid Module

1. Find the module you want to enable (e.g. **Bookings & Flight Tracking**)
2. Click **Enable**
3. A confirmation modal will appear showing the pricing and your billing period
4. Click **Subscribe** to add the module to your subscription
5. The module becomes immediately available

Your Stripe subscription is updated automatically. The module cost will appear on your next invoice.

---

## Unsubscribing from a Paid Module

1. Find the module you want to disable
2. Click **Disable**
3. A confirmation modal will warn you about losing access
4. Click **Unsubscribe** to remove the module from your subscription

{% hint style="warning" %}
Unsubscribing removes access to bookings, flight tracking, and analytics features. Your existing booking data is preserved and will be accessible if you re-subscribe later.
{% endhint %}

---

## Enabling / Disabling Free Modules

1. Find the module you want to toggle
2. Click **Enable** or **Disable**
3. The change takes effect immediately across your account

{% hint style="info" %}
Disabling a free module hides it from the interface but doesn't delete any data. Re-enable anytime to access your data again.
{% endhint %}

---

## Grace Period

If you had access to the Bookings module during the free evaluation period, you will see a banner on your dashboard prompting you to subscribe before the grace period ends.

- The banner shows pricing in your billing currency
- Click **Subscribe** to go directly to the Modules page
- Once you subscribe, the banner disappears
- If you don't subscribe before the grace period ends, the module will be disabled

---

## Who Can Manage Modules

Module subscription changes require the **billing.manage** permission, which is assigned to the **Account Administrator** role by default. Users without this permission can still see the Modules page but cannot subscribe or unsubscribe from paid modules.

---

## Tips

{% hint style="success" %}
**Start minimal** — Enable only what you need. You can always turn on more modules later as your needs grow.
{% endhint %}

- Fewer active modules = cleaner interface for your team
- The grace period banner only appears for users with billing access
- If you think a module was disabled in error, contact [support@aeroquote.com](mailto:support@aeroquote.com)
