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
| **Aircraft type / model** | Search the advanced model catalogue, or use native type if search is empty; registration can also guess a type | Citation CJ4, C25C, King Air 350 |
| **Homebase**      | The airport where the aircraft is normally based | YBBN, KJFK          |

### Type from registration

When you enter a **Registration**, AeroQuote looks up the type, then **searches the aircraft database** for that ICAO (or model name). A short progress panel shows while the lookup runs (you can **Cancel lookup** anytime).

* **One** database model — that performance model is selected
* **Several** models — pick one from the list (**Next** stays off until you do)
* **No** database match — a unique native AeroQuote type may be applied, or you pick one

### Search aircraft database

Type search uses **Search aircraft database** first:

1. Enter at least **2 characters** (make, model, or ICAO code)
2. Pick a model from the list when results appear — this links advanced performance data when available
3. If **no models are found**, use **Select AeroQuote aircraft type (fallback)** and continue with standard performance fields

You can later **Change model** or **Link model** from **Aircraft → Details**. See [Advanced performance models](../guides/aircraft/advanced-performance.md).

The **homebase** is important — AeroQuote uses it to calculate positioning (ferry) flights when a trip doesn't start or end at home.

**Tip:** Set the homebase to where the aircraft parks overnight. This ensures accurate positioning cost calculations.

## Step 4: Configure Flight Performance

Navigate to the **Flight Performance** tab.

* If you selected an **advanced model**, performance may come from that model (see the green status on **Details**).
* If you used a **native AeroQuote type**, enter or review:

  * **Cruise Speed** — Normal cruising speed  
  * **Fuel Burn Rate** — Fuel consumption per hour  
  * **Range** — Maximum distance on a full tank  

If defaults were pre-filled from a type template, review and adjust them to match your specific aircraft.

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
* [Advanced performance models](../guides/aircraft/advanced-performance.md) — Link, change, or revert the planning model
* [Cost Simulator](../guides/aircraft/cost-simulator.md) — Test your pricing before quoting live
