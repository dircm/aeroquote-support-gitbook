---
description: >-
  Optionally draft customer booking notes with Grok when sending to the
  customer — same tones and snippets idea as quote email, notes only.
---

# AI-assisted customer email (bookings)

On **Send to Customer**, you can optionally use **Generate** to draft the **customer notes** that appear in the booking email. The overall email layout stays fixed — Generate only fills the notes field.

{% hint style="info" %}
Generate does **not** run automatically on Send. If it fails or you skip it, you can still edit notes and send. Recipient selection, basic/detailed view, QR boarding passes, and default notes behaviour are unchanged. See [Sending Confirmations](sending-confirmations.md).
{% endhint %}

***

## Where to find it

1. Open a booking → **Send** tab
2. Click **Send to Customer** to open the preview modal
3. Use **Generate** when you want an AI draft of the **customer notes**
4. Edit the notes if needed, then **Send Now**

{% hint style="warning" %}
Generate does **not** auto-learn from your edits and is **not** fine-tuned on your messages. It drafts notes for you to review.
{% endhint %}

***

## Tone

Pick a tone chip before generating:

| Tone                 | Typical feel                    |
| -------------------- | ------------------------------- |
| **Friendly / familiar** | Warm and conversational      |
| **To the point**     | Short and direct                |
| **Formal**           | More polished / business-like   |

Your last tone is remembered **per user** (not a Settings screen).

***

## Snippets (booking context)

Snippets work the same way as on quotes, but in the **booking** context: operator-scoped rich-text blocks you can tick to include on Generate.

### Placement

| Placement           | What it does                                                        |
| ------------------- | ------------------------------------------------------------------- |
| **Before content**  | Snippet before the generated notes                                  |
| **After content**   | Snippet after the generated notes                                   |
| **Replace closing** | Snippet owns the ending (default closing CTA for notes is turned off) |

Add and edit snippets in the rich-editor modal; delete asks for confirmation. Selected snippet IDs are remembered **per user** with your tone preference.

***

## What stays the same

After Generate (or without it), you still:

* Choose **Main Contacts** / **Additional Recipients** on the Send tab
* Toggle **Send with Detailed View** per contact group
* Edit **Customer Booking Notes** before send
* Optionally include **QR code boarding passes**
* Use **default notes** from **Settings → Default Units** when you have not overridden them for this booking

***

## Related

* [Sending Confirmations](sending-confirmations.md)
* [Booking Emails — Booking Confirmation](../settings/emails/booking-emails.md#booking-confirmation)
* [AI-assisted quote email](../quotes/ai-assisted-email.md)
