# 📝 Create Your First Quote

This guide walks you through the complete process of creating and sending a quote to a customer. In AeroQuote, quotes start as **Requests** — a request captures the customer's flight needs, and AeroQuote generates cost estimates automatically.

## Prerequisites

Before creating a quote, ensure you have:

* At least one [aircraft configured](add-your-first-aircraft.md) with performance data and costings
* A customer contact (you can also create one during this process)

***

## Step 1: Create a New Request

1. Click **Requests** in the left sidebar
2. Click **Add New Request**

## Step 2: Add Customer Details

* **Contact** — Search for an existing contact or click **Add New Contact** to create one
* **Passengers** — Enter the expected passenger count
* **Notes** — Add any relevant details (special requirements, luggage, etc.)

## Step 3: Add Flight Legs

Click **Add Flight** to add your first flight leg:

1. **From** — Type the departure airport name or code (e.g., YBBN or Brisbane)
2. **To** — Type the arrival airport
3. **Date & Time** — Select the departure date and time

Repeat for additional legs if the trip has multiple flights (e.g., a return journey).

**Tip:** By default, **Automatically add repositioning (ferry) flights for Aircraft with a homebase** is **on**, so estimates include positioning when the trip does not start or end at homebase. Turn the toggle **off** for charter-only legs.

## Step 4: Add Aircraft and Review Estimates

AeroQuote does not estimate every aircraft until you choose them.

1. Click **+ Add Aircraft to see estimates**
2. Pick one or more aircraft from the modal (thumbnails and details)
3. With flights entered, estimates appear for those aircraft only:

* **Flight time** — Based on aircraft speed and route distance
* **Fuel costs** — Calculated from fuel burn rate and current fuel prices
* **Landing fees** — Based on airport and aircraft weight
* **Positioning costs** — Ferry flight costs to/from homebase when ferry auto-add is on

Add more with **+ Add Aircraft** or **+ Add more Aircraft** if you want extra options. Changing the route recalculates only the aircraft on the list.

## Step 5: Generate Quote

AeroQuote can show **multiple aircraft prices on the same quote**. Each aircraft you added becomes an **option** the customer can compare. See [Options](concepts.md#options) for the full concept.

1. Keep the aircraft you want on the estimates list — **one** for a single price, or **several** for side-by-side options
2. Click **Generate Quote**

AeroQuote creates one quote with a separate **option** for each added aircraft, including flight details, costs, and your pricing.

## Step 6: Review the Quote

The quote opens with several sections:

* **Quote Details** — Customer info, validity date, quote reference
* **Itinerary & Costs** — Flight legs, itemised costs, margins, and the final price
* **Document Builder** — Drag-and-drop builder to customise what the customer sees

### Adjusting the Price

If you need to adjust the price:

* Edit individual cost items
* Change the margin percentage
* Add or remove line items
* Override the total price directly

### Adding another aircraft option

On the **Options** step, use **Add Option** (top-left) to add a second aircraft. If charter legs already exist on another option, you can **auto-generate** a full estimated itinerary for the new aircraft. See [Add a Quote Option](../guides/quotes/add-a-quote-option.md).

## Step 7: Build the Quote Document

The **Document Builder** lets you control exactly what the customer sees:

* Drag sections to reorder them
* Toggle sections on/off
* Add your terms and conditions
* Include aircraft images
* Preview the PDF before sending

## Step 8: Send to Customer

1. Navigate to the **Send** step
2. Review the email that will be sent
3. Customise the message if needed
4. Click **Send Quote**

The customer receives an email with a link to view the quote online, where they can accept, ask questions, or request changes.

***

## What Happens Next?

* **Customer accepts** — You'll be notified and can convert the quote to a booking
* **Customer has questions** — They can respond through the online quote page
* **Quote expires** — If the validity date passes, the quote is marked as expired

***

## Quick Reference

| Action             | Where                                |
| ------------------ | ------------------------------------ |
| Create a request   | Requests > Add New Request           |
| View all quotes    | Quotes in sidebar                    |
| Edit a sent quote  | Open quote > Edit                    |
| Resend a quote     | Open quote > Send > Resend           |
| Convert to booking | Open accepted quote > Create Booking |

***

## Tips for Better Quotes

* **Set a validity date** — Give customers a deadline to encourage timely responses
* **Include aircraft images** — Visual appeal increases acceptance rates
* **Use the Cost Simulator first** — Test your pricing on the aircraft page before creating live quotes
* **Add terms and conditions** — Protect your business with clear terms (configure in Settings > Terms & Conditions)
