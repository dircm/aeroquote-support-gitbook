---
description: Create a tour product — details, scenic route, weight limits, add-ons, waiver, cancellation policy, photos, and the shareable deep link.
---

# Building a Tour

Create the tour product customers will see on your storefront, from the name and seat price through weight limits, add-ons, and photos.

## Prerequisites

* The Tour Packages module enabled (see the [overview](README.md))
* Your departure airport in the operator airport list
* Optional: a scenic route in your [route library](../custom-items/custom-routes-and-route-library.md) for the storefront map

## Step 1: Create the tour shell

1. Click **Tour Packages → Tours** in the left sidebar
2. Click **+ New Tour**
3. Enter a name, default duration, opening price, and maximum passenger count
4. You're redirected to the tour's edit page, where every other field lives

## Step 2: Fill in the tour details

The edit page is one long form, top to bottom:

1. **Tour Status** — the toggle card at the top controls storefront visibility. New tours start **Disabled** (hidden), so you can stage photos, slots, and pricing in private. Existing bookings remain valid if you disable a live tour.
2. **Tour details** — the name customers see, **Duration (minutes)** including any briefing, **Max passengers** (pick the lower of certified seats and what you're comfortable selling — 3 for an R44), **Price per person**, **Sort order** (controls storefront ordering when you sell multiple tours), and a markdown-friendly **Description** — this is your sales pitch on the detail page.
3. **Scenic route & departure** — pick a **Scenic route** from your route library (renders the storefront route map with your points-of-interest), the **Departure airport** (home base — only airports in your operator list appear), the **Aircraft type** the copy describes, and an optional **Public aircraft label** to override the type name with something more marketable.

## Step 3: Set weight limits

1. **Max per person** — enforced per passenger at checkout (typically 300 lbs for an R44)
2. **Max total** — refuses bookings whose combined declared weight exceeds the aircraft's payload, even when each passenger is under the per-person cap

A customer whose declared weights break either limit gets an error **before** their card is charged. Leave both blank if your aircraft has no constraint.

{% hint style="warning" %}
Customers under-declare weight — build a calibrated scale into your check-in routine and say so in your cancellation policy. The storefront enforces declared weights only; the on-the-day check is yours.
{% endhint %}

## Step 4: Add optional extras

In the **Add-ons** card:

1. Choose **Per person** (attaches to individual seats, multiplied by participant count — e.g. a doors-off photography seat) or **Per booking** (charged once per party — e.g. a champagne celebration)
2. Each add-on has its own active toggle, so you can trial what sells without deleting anything
3. Drag the handles to reorder how add-ons appear at checkout
4. Tick **Tax-exempt** on any add-on that shouldn't attract your tax lines (e.g. a tangible-goods add-on when your fare tax doesn't apply to it) — see [Payments, Tax & Payouts](payments-tax-and-payouts.md)

## Step 5: Waiver and cancellation policy

1. Toggle the waiver on for any tour where customers must accept liability, and type the waiver copy directly into the field — it becomes a checkbox every participant must tick at checkout
2. Write your **Cancellation policy** in plain text — customers see it on the detail page and confirmation. Be specific about weather rebooking ("we'll rebook to the next available slot at no charge if we cancel for weather") — it cuts refund disputes drastically

## Step 6: Upload photos

In the **Tour media** card:

1. Upload one **banner** image — it drives the storefront hero (1600×900 crop) and the card thumbnail. Uploading a new banner replaces the old one on save; tick *Remove on save* to clear it without replacing
2. Upload as many **gallery** images as you like (jpg/png/webp/gif, ≤ 10 MB each) — they appear below the description on the detail page. Click the × on a thumbnail to mark it for removal; an undo strip appears before you save

{% hint style="info" %}
The banner carries most of your storefront conversion — photograph the aircraft on a clear day and save the action shots for the gallery.
{% endhint %}

## Step 7: Enable the tour

When everything is staged, flip the **Tour Status** card to enabled. Until then the tour is invisible on your storefront.

## Linking to the tour from your own website

Above Tour details on the edit page, the **Share this tour** card holds the public deep link to this tour's detail page (`/tour/<your-slug>/<tour-slug>`). **Copy link** writes it to the clipboard; **Open** previews it in a new tab. Use it on your marketing site, campaigns, or a QR code on a flyer.

* Renaming the tour doesn't rewrite the slug — existing links keep working
* While the tour is disabled, the link is copyable (handy for staff preview) but 404s for customers — a yellow strip reminds you

## Next steps

* [Departures & Slots](departures-and-slots.md) — publish the times customers can book
* [Storefront & Branding](storefront-and-branding.md) — how the tour appears to customers
