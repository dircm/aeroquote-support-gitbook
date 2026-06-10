---
description: Save and reuse common quote configurations.
---

# 📋 Templates

Templates let you save quote configurations that you use frequently. Instead of setting up the same options repeatedly, create a template and apply it with one click.

***

## Accessing Templates

From the sidebar, click **Templates** to open the Templates list. The page has two sections:

* **Email Templates** — reusable wording for the email that delivers a quote (see below).
* **Booking Templates** — saved booking layouts you can reuse.

***

## Quote Email Templates

Email templates are the saved wording for the email that sends a quote to your customer. Pick one in the **Send** step of a quote — or set a default that's chosen for you automatically.

<figure><img src="../../.gitbook/assets/Screenshot 2026-06-09 at 8.10.48 pm.png" alt=""><figcaption></figcaption></figure>

### What you write vs. what's added for you

You only write the **message in the middle**. Aeroquote wraps it automatically every time a quote is sent:

| Added for you                                         | Detail                                                                                                                                                                                                            |
| ----------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Open button — above&#x20;**_**and**_**&#x20;below** | A button labelled **Open&#x20;**_**\<your quote name>**_ (for example _Open Charter Estimate_) that links to the online quote. Because it's added automatically, a quote can never go out without a working link. |
| **Your branding**                                     | Operator name in the header                                                                                                                                                                                       |
| **Subject line**                                      | Generated per quote as _\<your quote name> \<quote code> from \<your operator name>_ (e.g. _Charter Estimate ACG-7 from Acme Air_). It's shown in the Send step and you can edit it before sending.               |

{% hint style="success" %}
There are **no merge codes to manage** (no more `{{ quoteUrl }}` or `{{ customerName }}`). Just write your message with normal formatting — bold, links, and lists.
{% endhint %}

### Changing the button & quote-title wording

The _**\<your quote name>**_ that appears on the **Open** button, in the email subject line, and as the title on the customer's online quote all come from one setting: your **Default Quote Title**.

* Set it in **Settings → Quote Defaults → Default Quote Title** (e.g. _Charter Estimate_, _Flight Proposal_, _Travel Quote_).
* **If you leave it blank, it defaults to&#x20;**_**Charter Estimate**_ — so the button reads _Open Charter Estimate_ and the subject reads _Charter Estimate \<code> from \<your company>_.
* Change it once and it updates everywhere: the **Open** button, the subject line, and the quote web view.
* You can also **override it on an individual quote** if a particular quote should use a different title.

<figure><img src="../../.gitbook/assets/quote title.png" alt=""><figcaption></figcaption></figure>

### Creating an email template

1. On the Templates page, in **Email Templates**, click **Add Email Template**.
2. Give it a **Name** (your team sees this when picking a template).
3. Write the **Email body** using the formatting toolbar.
4. Optionally tick **Use as the default template**.
5. Click **Create**.

### Editing, default, and deleting

* **Edit** — change the name, body, or default flag at any time. Changes apply to future sends.
* **Set default** — the default template is pre-selected in the Send step for new quotes. Only one template can be the default.
* **Delete** — remove a template you no longer need. You'll always keep at least one.

### Using a template when sending

In a quote's **Send** step:

1. Choose a template from the **Email Template** list (your default is pre-selected).
2. Edit the **Subject** or message for this quote if you want — your edits apply to this quote only and don't change the saved template.
3. Use **Preview** to see the finished email, then send.

{% hint style="info" %}
To save the message you've just edited as a new reusable template, use **Save as New Template** in the Send step.
{% endhint %}

<figure><img src="../../.gitbook/assets/select email template.png" alt=""><figcaption></figcaption></figure>

***

## Booking Templates

### What Templates Save

A template can include:

| Setting                | Description                         |
| ---------------------- | ----------------------------------- |
| **Aircraft Selection** | Which aircraft to include in quotes |
| **Pricing Rules**      | Margin percentages, minimum charges |
| **Default Documents**  | Documents to attach automatically   |
| **Terms & Conditions** | Which T\&Cs to require              |
| **Email Templates**    | Default email content               |
| **Quote Validity**     | Default expiry period               |

***

## Creating a Template

### Step 1: Start a New Template

Click **Add Template** from the Templates list.

### Step 2: Name Your Template

Give it a descriptive name, e.g.:

* "Standard Charter Quote"
* "VIP Service Package"
* "Cargo Flight Template"

### Step 3: Configure Settings

Set up the defaults you want this template to apply:

1. **Aircraft** — Select which aircraft to include by default
2. **Pricing** — Set margin or hourly rate preferences
3. **Documents** — Choose documents to auto-attach
4. **T\&Cs** — Select terms document
5. **Validity** — Set default quote expiry (e.g., 7 days)

### Step 4: Save

Click **Save Template**.

***

## Using a Template

When creating a new quote:

1. Start a new quote as normal
2. Look for the **Apply Template** option
3. Select your template
4. Settings are pre-filled automatically
5. Adjust as needed for this specific quote

***

## Managing Templates

### Editing a Template

1. Find the template in the list
2. Click **Edit**
3. Update settings
4. Save changes

{% hint style="info" %}
Editing a template doesn't affect quotes already created from it.
{% endhint %}

### Duplicating a Template

To create a variation:

1. Find the template to copy
2. Click **Duplicate**
3. Rename and modify as needed
4. Save the new template

### Deleting a Template

1. Find the template
2. Click **Delete**
3. Confirm removal

***

## Template Tips

{% hint style="success" %}
**Start with your most common scenario** — Create a template for your bread-and-butter quote type first, then add variations.
{% endhint %}

* Name templates clearly so the whole team knows when to use them
* Review templates quarterly to keep them current
* Create separate templates for different customer segments (corporate, leisure, cargo)
* Use templates to enforce consistency across your team

***

## Next Steps

* [Creating a Quote](../quotes/) — Use templates when quoting
* [Documents](../documents/) — Set up documents to include in templates
* [Terms & Conditions](../settings/terms-and-conditions.md) — Create T\&Cs for templates
