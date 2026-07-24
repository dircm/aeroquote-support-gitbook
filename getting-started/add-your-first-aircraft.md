# ✈️ Add Your First Aircraft

Before you can create quotes, you need at least one aircraft in your fleet. This guide walks you through adding and configuring your first aircraft.

## Step 1: Open the Aircraft Page

Click **Aircraft** in the left sidebar to see your fleet list.

## Step 2: Add a New Aircraft

Click the **Add Aircraft** button at the top of the page. This opens the aircraft setup wizard.

## Step 3: Enter Basic Details

Fill in the required information:

| Field             | What to enter                                    | Example             |
| ----------------- | ------------------------------------------------ | ------------------- |
| **Registration**  | Your aircraft tail number (optional but recommended) | VH-XYZ, N123AB  |
| **Aircraft Type** | Select from the dropdown, or let AeroQuote guess from registration | King Air 350, AS350 |
| **Homebase**      | The airport where the aircraft is normally based | YBBN, KJFK          |

### Type from registration

When you enter a **Registration**, AeroQuote can look up the aircraft type for you. A short progress panel shows while the lookup runs (you can **Cancel lookup** anytime). If a confident match is found, the type is applied automatically; if not, choose the type yourself as usual.

The **homebase** is important — AeroQuote uses it to calculate positioning (ferry) flights when a trip doesn't start or end at home.

**Tip:** Set the homebase to where the aircraft parks overnight. This ensures accurate positioning cost calculations.

## Step 4: Configure Flight Performance

Navigate to the **Flight Performance** tab and enter:

* **Cruise Speed** — Normal cruising speed
* **Fuel Burn Rate** — Fuel consumption per hour
* **Range** — Maximum distance on a full tank

If your aircraft type is in the AeroQuote database, some values may be pre-filled. Review and adjust them to match your specific aircraft.

## Step 5: Set Up Costings

Navigate to the **Costings** tab. This determines how quotes are priced:

* **Hourly Rate** — The per-hour charge to customers
* **Minimum Flight Time** — Minimum chargeable hours per flight
* **Positioning Rate** — Rate for ferry (empty) flights (can differ from the passenger rate)

You can use either **hourly rate** pricing or **margin-based** pricing depending on your business model.

**Tip:** On an existing aircraft’s Costings step you can click **Suggest costs for me** to review AI-suggested rates and operating costs, then apply or skip. See [Costings](../guides/aircraft/costings.md).

## Step 6: Add Aircraft Images (Optional)

Navigate to the **Images** tab to upload photos of your aircraft (or add a photo from a public image URL). These appear in quote documents sent to customers and help make a professional first impression.

## Step 7: Finish the wizard

Use **Next** through the remaining steps and complete the builder to add the aircraft to your fleet. When you later edit Details or Performance, changes **auto-save** as you leave each field — there is no separate Save button on those steps.

The aircraft will appear in quote options when you create requests.

## What's Next?

Now that you have an aircraft, you're ready to create your first quote:

* [Create Your First Quote](create-your-first-quote.md) — The complete quote workflow
* [Cost Simulator](../guides/aircraft/cost-simulator.md) — Test your pricing before quoting live
