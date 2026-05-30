---
description: >-
  Configure GST, VAT, sales tax and other charges so they appear correctly on
  your customer-facing quotes, bookings, receipts and tax invoices.
---

# 🧾 Tax Setup

AeroQuote's tax engine handles GST (Australia / New Zealand), VAT (Europe / UK / Africa), sales tax (US / Canada) and any other operator-level tax line you need to itemise — in the operator's local currency and using the operator's preferred terminology. Once configured, the breakdown flows automatically onto your customer-facing quote pages, booking pages, PDFs, confirmation emails and downloadable tax invoices.

{% hint style="info" %}
If you have not configured any tax items, your customer-facing pricing is unchanged — totals show exactly the amount you entered into AeroQuote, with no breakdown or "Includes GST" subtext. Tax setup is **opt-in**.
{% endhint %}

---

## What you can configure

There are two parts to tax setup, and they live in different places:

| Setting | Where to find it | What it does |
|---------|------------------|--------------|
| **Tax invoice details** | Settings → [Account Settings](account-settings.md) | Legal business name, address, registration label (ABN / VAT / EIN), registration number — these appear on the tax invoice header |
| **Tax rates & items** | Settings → **Tax** | Per-rate name, percentage, inclusive flag, scope (fare / surcharge / add-ons) — drives the itemised lines on the customer page and receipts |

Both pages are available to every operator regardless of which modules you have enabled. Tax rates are operator-wide — the same configuration drives charter quotes / bookings, scheduled-flight ticket purchases, and tour-package bookings.

---

## Step 1 — Set your tax invoice details

These four fields appear at the top of every tax invoice / receipt PDF and are jurisdiction-agnostic — pick the registration label that matches your country (ABN for Australia, VAT for the EU/UK, GST for New Zealand, EIN for the US, etc.).

1. Go to **Settings** from the sidebar
2. Open the **Account Settings** step
3. Fill in the four tax invoice fields:
   - **Legal business name** — falls back to your trading name when blank
   - **Business address** — multi-line, prints in the document header
   - **Tax registration label** — e.g. `ABN`, `VAT`, `EIN`, `USt-IdNr.`
   - **Tax registration number** — e.g. `12 345 678 901`, `EE100123456`
4. Click **Save**

{% hint style="success" %}
Setting a registration number flips the customer-facing PDF title from "Receipt" to "Tax invoice" automatically. If you leave the registration number blank, customers see a plain "Receipt" with the same totals breakdown.
{% endhint %}

### Preview before you save

On **Settings → Tax**, the Tax invoice details panel has a **Preview** button. It opens a mock invoice built from your current details and a sample fare run through your tax items — so you can see exactly how the header flips between "Tax invoice" and "Receipt" and how the breakdown itemises, before saving. The preview reflects unsaved edits, so tweak a field and re-open it to check the result.

---

## Step 2 — Set your tax rates

Tax rates are configured under **Settings → Tax**. The same rates power your charter quotes / bookings, scheduled-flight ticket purchases, and tour-package bookings — there is one tax configuration per operator.

### Pick a jurisdiction preset

AeroQuote ships with presets for 23 countries spanning Australia / New Zealand / UK / EU / US / Canada and the SADC + East Africa region. Selecting a preset replaces your tax items with sensible defaults you can then tweak.

| Region | Preset code | Defaults |
|--------|-------------|----------|
| Australia | AU | 10% GST, inclusive |
| New Zealand | NZ | 15% GST, inclusive |
| United Kingdom | GB | 20% VAT, inclusive |
| European Union | EU | 22% VAT (placeholder), inclusive — adjust to your local rate |
| United States | US | 7.5% Federal Excise + state sales tax (set your state rate), exclusive |
| Canada | CA | 5% GST + provincial tax (set your provincial rate), exclusive — toggle compound for Quebec |
| Africa / Indian Ocean | AO, BW, CD, KE, KM, LS, MG, MU, MW, MZ, NA, SC, SZ, TZ, ZA, ZM, ZW | Single-line standard-rate VAT / TVA / IVA, inclusive |
| Custom | Custom | Start from scratch — useful for non-listed jurisdictions |

1. Go to **Settings → Tax** from the sidebar
2. Click the **Jurisdiction** dropdown and pick your country
3. Click **Apply preset**
4. Review and adjust the rates, names and inclusive flags to match your situation
5. Click **Save**

### Tax item fields

Each tax item has the following fields:

| Field | What it does |
|-------|--------------|
| **Name** | The label customers see (e.g. `GST`, `VAT`, `Federal Excise`, `Provincial`) |
| **Rate** | The percentage — supports three decimal places, so Quebec's 9.975% TVQ rounds correctly |
| **Is inclusive** | Whether the rate is already baked into the fares you enter (inclusive) or added on top (exclusive) — see [Inclusive vs exclusive](#inclusive-vs-exclusive) below |
| **Applies to** | Whether the rate is applied to the fare, add-ons, surcharge, or some combination |
| **Compound on** | (Optional) Layers this rate on top of another rate's amount — used for Quebec TVQ on top of GST |
| **Active** | Toggle off to retire a rate without deleting it |

---

## Inclusive vs exclusive

The **pricing mode** dropdown at the top of the Tax page is a master switch — choosing inclusive or exclusive re-flags every tax item to match, and the live preview on the right updates instantly. The per-item inclusive toggle is what's authoritative at calculation time, so once you've set the mode you can still fine-tune individual items (see mixed mode below).

### Inclusive (Australia, New Zealand, UK, EU, most of Africa)

Your fare prices already include tax. The customer pays exactly the amount you entered, and the breakdown shows what portion is tax.

- You enter `$1,100` into AeroQuote
- The customer sees `$1,100` with an `Includes $100 GST` subtext below the total
- The breakdown on the receipt shows `GST (10%) — $100`

### Exclusive (US, Canada, most pre-tax pricing setups)

Your fare prices are pre-tax. Tax is added on top.

- You enter `$1,000` into AeroQuote
- The customer sees a `Subtotal $1,000` line, a `Federal Excise (7.5%) $75` line, and a final `$1,075` total
- The breakdown on the receipt shows the same itemisation

{% hint style="info" %}
**Mixed mode is supported.** You can run one inclusive item (e.g. GST baked into the fare) alongside one exclusive item (e.g. airport fees added on top) — AeroQuote will render each correctly.
{% endhint %}

When tax is configured, the price input on the quote builder and the booking total field show a small helper line below — `"Fares are entered including GST — this is what the customer pays"` or `"Fares are entered pre-tax — Federal Excise will be added at checkout"` — so there's no surprise about how the number is interpreted.

---

## Cost items and tax

AeroQuote computes tax from the **option price** (or booking price), not from the sum of individual cost items. Cost items are display-only — they show the customer how the price is composed, but they do not feed the tax calculation.

{% hint style="warning" %}
**Enter all cost items pre-tax.** Whether you're operating inclusive or exclusive, your cost items should reflect amounts **before** AeroQuote applies the tax breakdown. Tax is calculated once, on the final option price, and shown on its own line. If you put a manual "GST" or "VAT" row in your cost items, customers will see tax twice — once in your cost line and once in the system breakdown.
{% endhint %}

If you've been adding a manual `Tax` / `GST` / `VAT` cost item on your quotes historically as a workaround, remove those rows once you configure your tax rates — AeroQuote will itemise the tax automatically.

Likewise, if you used the free-text **price suffix** (e.g. "Excluding Taxes" or "+ GST") to disclaim tax, you don't need to clear it. AeroQuote automatically hides the suffix on customer pages and PDFs once you configure tax rates, so customers never see a stale disclaimer next to a computed breakdown. The suffix reappears on its own if you later remove all your tax items.

---

## What customers see

Once tax is configured, the breakdown appears in four places — all read from a per-document **snapshot** taken when the quote or booking was generated, so changing your tax rates later does not retroactively rewrite historical documents.

### On the customer quote page

- Inclusive operators: the headline total + an `Includes $X GST` subtext below
- Exclusive operators: a `Subtotal / Tax (rate%)` two-row block above the headline grand total

### On the customer booking page

Same breakdown as the quote page, rendered as a "Booking total" card. Two download buttons appear: **Download Itinerary** and either **Tax invoice** (when you have a registration number set) or **Receipt** (when you don't). The receipt download can be hidden per-operator — see [Hiding the receipt download](#hiding-the-receipt-download) below.

### On quote PDFs

Every quote variant template includes the breakdown alongside each option's price — inclusive operators see the `Includes …` subtext below, exclusive operators see the itemised tax lines above the total.

### On the downloadable receipt / tax invoice

This is a customer-filed proof of purchase, separate from the operational itinerary PDF. Operators with a tax registration get a properly headed **Tax invoice** PDF showing the legal business name, address, registration line and the itemised tax breakdown. Operators without a registration get a simpler **Receipt** PDF without the registration line.

### On confirmation emails

The customer booking confirmation email includes a totals panel mirroring the customer page, plus an optional download link to the receipt / tax invoice labelled correctly for your registration state.

Whether that link is included is controlled per send. When you email a booking, the send dialog shows an **Include tax invoice in email** (or **Include receipt in email**) toggle alongside **Include QR code boarding passes**. It defaults to your Customer Pages Branding download setting (see [Hiding the receipt download](#hiding-the-receipt-download)) — so if the download is enabled, the link is included by default, and you can untick it for a one-off send. The toggle only appears when the booking has a price and the download is enabled.

---

## Hiding the receipt download

If you issue formal invoices through Xero, QuickBooks or your own accounting system and don't want AeroQuote serving a competing artifact, you can hide the downloadable receipt / tax invoice per-operator.

1. Go to **Settings → Customer Pages Branding**
2. Find the **Tax invoice / receipt download (bookings only)** checkbox
3. Uncheck it and click **Save branding**

When the toggle is off:

- The **Tax invoice** / **Receipt** button no longer appears on the customer booking page
- The **Include tax invoice in email** toggle is hidden from the booking send dialog, and confirmation emails never carry the download link
- The PDF download URL itself returns a 404, so any link a customer has previously bookmarked or forwarded also stops working

When it's on, the email link defaults to included but you can still untick **Include tax invoice in email** per send.

{% hint style="info" %}
**The inline totals breakdown stays on either way.** Hiding the download only gates the standalone PDF artifact — customers still see the "Booking total" card on the booking page with the same inclusive / exclusive breakdown. If you want to hide the price entirely from the customer booking page, leave the booking's stored price at `0`.
{% endhint %}

---

## Snapshot rule

Tax is captured onto each quote and booking at the moment it's generated. After that:

- The customer always sees the **as-of-generation** breakdown, even if you later change your tax rates
- Historical PDFs render with the original rate, not a recomputed one
- Re-issuing a quote regenerates the snapshot at the new rate

{% hint style="warning" %}
This is intentional. If you bumped GST from 10% to 15%, you don't want your customer who accepted a quote last week to suddenly see a different number on their booking. Snapshot the past, apply new rates to future quotes.
{% endhint %}

---

## Tips

{% hint style="success" %}
**Run a test quote after configuring tax** — Create a $100 test quote and check that the customer page, PDF, and confirmation email all render the breakdown you expect. The customer page is the fastest preview while you're tuning rates.
{% endhint %}

- Set your tax invoice details before you set rates — that way the first quote you issue carries the proper "Tax invoice" header.
- Use the **Custom** preset when your country isn't in the list, or when you need to add a non-standard rate (e.g. airport fees that the host airport collects on your behalf).
- For Quebec operators: use the CA preset, then toggle **Compound on GST** on the provincial line — the TVQ is calculated on top of fare + GST, not on the bare fare.
- Operators who only need a tax invoice header (and no itemised GST / VAT line) can leave the rates table empty — set just the tax invoice details on Account Settings and AeroQuote will issue tax-invoice-headed receipts without any tax breakdown.
- If Xero or QuickBooks is already producing your formal invoices, hide the AeroQuote receipt download in Customer Pages Branding so customers aren't offered two competing documents — see [Hiding the receipt download](#hiding-the-receipt-download).
