---
description: >-
  Brand the customer-facing quote and booking pages with your colours, font and
  contact details, and choose which sections customers can see.
---

# 🎨 Customer Pages Branding

The pages your customers see when you share a quote or booking link with them — the ones at `/quotes/{id}` and `/bookings/{id}` — can be styled to match your website and trimmed to show only the sections you want them to see. All settings are per-operator and apply to every customer-facing page automatically.

---

## Accessing Customer Pages Branding

1. Go to **Settings** from the sidebar
2. Click the **Customer Pages** tab

---

## What You Can Change

### Colours

| Field | Where it appears |
|---|---|
| **Primary accent colour** | Hero gradient, accept-quote button, section accents, timeline dots |
| **Hero text colour** | Text drawn on top of the hero gradient |
| **Button background** | The Accept Quote and Download Itinerary buttons (defaults to the accent) |
| **Button text** | Text on those buttons |
| **Header background and text** | The sticky bar at the top of every customer page |
| **Footer background and text** | The footer block at the bottom of every customer page |

### Typography

| Field | What it does |
|---|---|
| **Font family** | A CSS font-family value, e.g. `Open Sans, Arial, sans-serif` — quote characters are stripped automatically |
| **Font stylesheet URL** | A Google Fonts or self-hosted stylesheet URL to load the font on the customer pages |

### Element visibility

Eleven toggles let you hide sections customers don't need:

* Route map
* Aircraft images
* Cost breakdown (quotes only)
* Questions and comments
* Operator contact details (bookings only)
* Passenger list (bookings only)
* Cargo section (bookings only)
* Amendments table (bookings only)
* Itinerary download button (bookings only)
* Onboarding hints (quotes only)
* Customer-downloadable PDFs (quotes only)

All toggles default to **on** — your customer pages look complete out of the box. Switch any of them off if you'd rather customers contact you directly for that information.

---

## Setting Your Brand Colours

### Step 1: Pick an Accent Colour

1. Click the colour swatch next to **Primary accent colour**
2. Choose a colour, or paste a hex value into the text field

The live preview on the right updates as you change it.

### Step 2: Adjust Hero Text if Needed

If your accent is a light colour, change **Hero text colour** to a dark value so the hero text stays readable on the gradient.

### Step 3: Match Header and Footer to Your Website

If your website has a dark header, set the customer-page header background to match — it makes the hand-off between your website and the customer page feel seamless.

{% hint style="success" %}
**Match your existing site exactly** — Use your browser's dev tools on your website to copy the body's `font-family` and the header / footer background colours. Paste them into the matching fields here.
{% endhint %}

---

## Using a Custom Font

### Step 1: Find Your Font's Stylesheet URL

If your website uses Google Fonts, copy the `<link>` URL from your Google Fonts embed. For example:

```
https://fonts.googleapis.com/css2?family=Open+Sans&display=swap
```

### Step 2: Paste It Into the Settings

1. Paste the URL into **Font stylesheet URL**
2. Type the corresponding CSS value into **Font family**, e.g. `Open Sans, Arial, sans-serif`

The customer pages load the stylesheet and apply the font.

{% hint style="info" %}
Don't include quote characters around font names. AeroQuote strips them automatically — they don't render correctly inside the embedded styles, so we keep them out.
{% endhint %}

---

## Hiding Sections

Each visibility toggle is a checkbox under **Element visibility**.

To hide a section:

1. Untick the checkbox for that section
2. Click **Save branding**
3. Refresh the customer page — the section is gone

Hidden sections are removed entirely; they're not just visually hidden. The HTML isn't there, so the section doesn't appear at all.

{% hint style="warning" %}
Some sections only render when there's data to show. Hiding **Travellers** has no visible effect until a booking has passengers; hiding **Amendments** has no visible effect until amendments exist.
{% endhint %}

---

## Previewing on Real Quotes and Bookings

The settings page has a **View live on real Quotes and Bookings** card that lists your two most-recent quotes and bookings. Each is a signed link that opens in a new tab.

1. Adjust your branding
2. Click **Save branding**
3. Click one of the quote or booking links
4. The customer page opens in a new tab with your changes applied

Use this to confirm the live result on a real customer page rather than just the miniature preview.

---

## How Branding Reaches Existing Quotes and Bookings

Customer page branding is **read live** — there's no archival snapshot. Any quote or booking you've already sent picks up your new colours the moment a customer next refreshes the link. You don't need to resend or regenerate anything.

This applies to every customer-facing page: ShowQuotePage, ShowBookingPage, the crew booking view, the external operator booking view, and the customer-side Request For Quote page.

---

## Tips

{% hint style="success" %}
**Start with the accent colour** — Most operators get 80% of the look right by setting just the primary accent. The defaults for everything else (white header, dark text, neutral footer) work well alongside almost any accent.
{% endhint %}

* Keep your accent strong enough to read white text on it. The hero gradient darkens your accent toward the bottom-right corner.
* Status badges (In Progress, Completed, Cancelled) keep their semantic colours — amber, green, red — regardless of your accent. Brand drives chrome, not the meaning of state.
* The mobile app is unaffected by these settings. They only style the customer-facing web pages.

---

## Related

* [Banner Images](banner-images.md) — Images for quote PDFs and document layouts
* [Account Settings](account-settings.md) — Operator name, phone, email and website (these feed the customer-page header and footer when **Operator contact details** is enabled)
