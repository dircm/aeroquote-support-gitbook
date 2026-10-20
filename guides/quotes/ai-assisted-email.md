---
description: >-
  Optionally draft the quote email subject and body with Grok on the Send step —
  tones, option text, snippets, and editable output before you send.
---

# AI-assisted quote email

On the quote **Send** step you can optionally use **Generate** to draft the email **subject** and **HTML body** with Grok. Generate does **not** run when you click Send — it only fills the editors so you can review and edit before sending.

{% hint style="info" %}
Sending still works if Generate fails or you skip it. AeroQuote continues to wrap your message with the usual **Open** quote buttons and operator branding. See [Quote Emails](../settings/emails/quote-emails.md#quote-sent-to-customer).
{% endhint %}

***

## Where to find it

1. Open a quote and go to the **Send** step
2. Prepare recipients and attachments as usual
3. Use **Generate** when you want an AI draft of the subject and body
4. Edit the result, then send when you’re ready

{% hint style="warning" %}
Generate is optional. It does **not** auto-run on Send, and it does **not** learn from your later edits or fine-tune on your messages.
{% endhint %}

***

## Tone

Before you generate, pick a tone chip:

| Tone                 | Typical feel                                      |
| -------------------- | ------------------------------------------------- |
| **Friendly / familiar** | Warm and conversational                         |
| **To the point**     | Short and direct                                  |
| **Formal**           | More polished / business-like                     |

Your last chosen tone is remembered **per user** (same idea as other AeroQuote per-user preferences — nothing to configure under Settings).

***

## Include options as text

Optionally turn on **include options as text**. When enabled, the app builds a factual block of options and legs for the model to use:

* Town / airport **names** and aircraft **descriptions**
* A single option is **not** labelled “Option 1”
* Hidden legs are **not** included
* **No ICAO codes** are injected into that block

{% hint style="success" %}
The AI must not invent prices. Pricing belongs on the online quote (and your Open-quote buttons), not as fabricated figures in the email body.
{% endhint %}

***

## Snippets

**Snippets** are operator-scoped rich-text blocks you can reuse across quote emails.

### Using snippets on Generate

1. Tick the snippet checkboxes you want included for this generate
2. Click **Generate**
3. Review the subject and body — snippets are placed according to each snippet’s placement setting

Selected snippet IDs are remembered **per user** along with tone and the include-options preference.

### Add, edit, and delete

* **Add / edit** snippets in the rich-editor modal from the Send step
* **Delete** requires confirmation

### Placement

Each snippet has a placement:

| Placement           | What it does                                                                 |
| ------------------- | ---------------------------------------------------------------------------- |
| **Before content**  | Inserts the snippet before the generated message body                       |
| **After content**   | Inserts the snippet after the generated message body                        |
| **Replace closing** | The snippet owns the ending; the default CTA closing is turned off          |

***

## Default call to action

When you are **not** using a **Replace closing** snippet, the draft should guide the customer to:

* Open the quote link to **approve** or **ask questions**, or
* **Reply** to the email

AeroQuote still adds the **Open** quote buttons around your message when the email is sent.

***

## After Generate

* The subject and body are **always editable** after Generate
* You can regenerate with a different tone, options toggle, or snippet selection
* If Generate fails, you can still write or paste wording (including from [email templates](../templates/)) and **Send** as normal

***

## Related

* [Quote Emails — Quote Sent to Customer](../settings/emails/quote-emails.md#quote-sent-to-customer)
* [Templates — Quote Email Templates](../templates/)
* [AI-assisted customer email (bookings)](../bookings-operators/ai-assisted-customer-email.md)
