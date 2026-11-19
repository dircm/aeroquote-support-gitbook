---
description: Include library documents and placeholder itinerary PDFs on a quote.
---

# Using Documents in a Quote

Documents from your library are attached to quotes on the **Documents** step. That is also where you preview and download the **customer-facing itinerary / quote PDF**.

***

## Outcome

Build the PDF package the customer sees (and that you can print), then optionally attach it when you send the quote.

***

## Prerequisites

* At least one document in your library (including a **placeholder** type for live quote content) — see [Uploading a new Document](uploading-a-new-document.md)
* An open quote

***

## Step 1: Open Documents on the quote

1. Open the quote from **Quotes**
2. Click the **Documents** tab

***

## Step 2: Add documents from the library

1. In the sidebar library list, find the document you want
2. Click **Add** (or the add control) on that document so it appears under **Selected Documents (email attachments)**
3. For a **placeholder** document, choose a style if prompted (**Pick a style**) — this drives the live quote itinerary layout
4. Remove a document with **Remove** if it should not be included

***

## Step 3: Preview and download / print

1. On desktop, open **Quote Placeholder Preview** below the selected list
2. Click **Download PDF** to save a printable file
3. On mobile / narrow screens, use **Preview Document** to open the PDF in a new tab, then print from the browser

{% hint style="info" %}
Need the full path comparison (internal job PDF vs customer package vs booking)? See [View or print the full quote itinerary](../quotes/view-or-print-quote-itinerary.md).
{% endhint %}

***

## Step 4: Templates (optional)

* **Load Template** — apply a saved document set to this quote
* **Save as New Template** — store the current selection for reuse

***

## Step 5: Send with the quote

1. Open the **Send** step
2. Ensure attachments are included as needed
3. Send the quote so the customer receives the document package

***

## Customers can download the selected documents

Every document under **Selected Documents** can also be downloaded from the customer's online quote. They don't need the email attachments.

* When a customer opens the quote link, a **Documents** section below the quote options lists each selected document with its name, file type and size, plus a **Download** button
* The placeholder document downloads as the quote PDF in the style you picked
* Anyone with the quote link can download the documents. No customer login is needed, the same as viewing the quote
* If you remove a document from **Selected Documents**, it disappears from the online quote straight away, and old download links stop working
* Once the quote expires (its valid-until date passes or it's marked **Expired**), the **Documents** section is hidden and downloads are no longer available. Old download links stop working too. An **accepted** quote doesn't expire this way, so the customer keeps access to its documents
* Each download is recorded in **Quote Events** on the quote's **Status** step, for example *Quote document downloaded by customer*. You don't get a notification
* If no documents are selected, the **Documents** section doesn't appear

{% hint style="warning" %}
Only add documents you're happy for the customer to have. Anything in **Selected Documents** can be downloaded by anyone who has the quote link.
{% endhint %}

***

## Watch the walkthrough (optional)

**Watch the walkthrough:** [Arcade demo](https://app.arcade.software/share/nS4AOa0tzXgqwqpUNw0Y)

{% @arcade/embed flowId="nS4AOa0tzXgqwqpUNw0Y" url="https://app.arcade.software/share/nS4AOa0tzXgqwqpUNw0Y" %}

***

## Related

* [View or print the full quote itinerary](../quotes/view-or-print-quote-itinerary.md)
* [Creating PDFs for Aeroquote.com Upload](creating-pdfs-for-aeroquote.com-upload.md)
* [Quote Details Page](../quotes/quote-details-page/)
