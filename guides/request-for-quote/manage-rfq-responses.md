---
description: >-
  RFQ responses contain information from the External Operator but this also
  effect your Quote in multiple ways.
---

# Manage RFQ Responses

Read below to understand how responses are handled for:

[#receiving-a-question](manage-rfq-responses.md#receiving-a-question "mention")

[#receiving-a-price-response](manage-rfq-responses.md#receiving-a-price-response "mention")

[#automatic-price-updates](manage-rfq-responses.md#automatic-price-updates "mention")

[#receive-a-rejection](manage-rfq-responses.md#receive-a-rejection "mention")



### Receiving a Question

When you receive a Question type response, you may read the question text in the automated email and reply directly to that email.

{% hint style="info" %}
replying to the email in your email client will automatically use the External Operator email address
{% endhint %}

You will also see the question text when viewing the RFQ from the **Request for Quotes** page.



### Receiving a Price response

Once the External Operator provides a price to you using their online RFQ page, a number of changes will be made directly to your Quote.

#### Automatic Price Updates:

* External operator's total price is immediately applied to the corresponding quote option **cost**

<figure><img src="../../.gitbook/assets/image (8) (1).png" alt=""><figcaption></figcaption></figure>

* Currency conversion happens automatically if the response is in a different currency.
* Any original cost estimates are overridden but preserved for reference
* You should review the new cost and adjust your price to customer accordingly

#### Flight Segment Synchronization

External operators can make flight segment modifications via the online RFQ view including Adding stops, Adding repositioning flights and adjusting flight times. When the External Operator add extra stops or modify the flight plan in any way, these changes are automatically synchronized back to your Quote Option flights **once they send a response to you.**

What Gets Synchronized?

New Flight Segments: If an external operator adds stops between airports, new flight segments are created in your quote option

Updated Timings and durations: Departure and arrival times for all flight segments are synchronized

Facility / FBO Changes: Any facility selections made by the external operator.



#### Receive a rejection

Sometimes the External Operator will choose to respond with "Aircraft Unavailable".  This will be emailled to you and also update the banner attached to the Option.  A handy **Delete Option** button is available to allow you to remove this Option before sending to the customer.

<figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

From the [Request for Quotes menu](track-responses-to-a-rfq.md#method-2-view-all-the-rfqs-in-the-request-for-quotes-menu.-the-status-is-shown-in-the-list) you can perform actions on multiple RFQs within the same quote group:

<figure><img src="../../.gitbook/assets/image (22).png" alt="" width="375"><figcaption></figcaption></figure>

#### Available Bulk Actions

1. **Send** - Send selected RFQs to external operators
   * Option to include external notes with the email
   * RFQs are grouped by operator to minimize emails sent
2. **Cancel RFQ** - Cancel selected RFQs
   * Marks RFQs as cancelled
   * Requires confirmation before proceeding
   * Cannot be undone
3. **Delete** - Permanently delete selected RFQs
   * Removes RFQ and associated flight data
   * Requires confirmation before proceeding
   * Cannot be undone

#### Using Bulk Actions

1. Select one or more RFQs using the checkboxes
2. Click the "Bulk actions" button that appears
3. Choose your desired action from the dropdown
4. Complete any required fields (e.g., external notes for Send)
5. Confirm the action
