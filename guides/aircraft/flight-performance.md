---
description: Configure speed, range, and fuel consumption data.
---

# Flight Performance

The Flight Performance section holds the technical data used for **standard AeroQuote** flight times and fuel cost inputs. Accurate data here means accurate quotes for aircraft that are not on an advanced performance model.

{% hint style="info" %}
If **Details** shows **Using advanced performance model**, estimates use the linked advanced model for planning. The Performance tab then reflects that advanced data rather than the manual fields below. See [Advanced performance models](advanced-performance.md).
{% endhint %}

---

## Accessing Flight Performance

1. Go to **Aircraft** from the sidebar
2. Click on an aircraft
3. Select the **Flight Performance** tab

---

## Auto-save

On the **manual** performance form, changes save automatically after you finish editing a field. There is no separate Save button. A short confirmation toast appears when a save succeeds.

---

## Key Performance Fields

### Speed

| Field | Description | Units |
|-------|-------------|-------|
| **Cruise Speed** | Normal cruising speed | Knots (kts) |
| **Max Speed** | Maximum cruise speed | Knots (kts) |

{% hint style="info" %}
Use realistic cruise speeds for your typical operations. Published max speeds are rarely used in practice.
{% endhint %}

### Range

| Field | Description | Units |
|-------|-------------|-------|
| **Maximum Range** | How far the aircraft can fly | Nautical miles (nm) |
| **Range with Reserves** | Practical range with fuel reserves | Nautical miles (nm) |

### Fuel Consumption

| Field | Description | Units |
|-------|-------------|-------|
| **Fuel Burn Rate** | Fuel consumption per hour | Gallons or liters per hour |
| **Fuel Type** | Jet-A, Avgas, etc. | — |
| **Fuel Capacity** | Maximum fuel load | Gallons or liters |

---

## How Performance Data is Used

### Standard AeroQuote performance

When the aircraft is **not** on an advanced model (or after **Revert**), estimates use these fields to:

1. **Calculate flight time** — Distance and your cruise / climb inputs  
2. **Estimate fuel needed** — Flight time × fuel burn rate  
3. **Check range** — Can this aircraft make the trip non-stop?  
4. **Determine fuel costs** — Fuel needed × fuel price at airport  

### Advanced performance model

When **Details** shows **Using advanced performance model**, sector times and distances are planned with the linked model (winds, climb, and descent). Internal estimate screens may also show a **Fuel** column. Customer quotes and PDFs do not show that fuel burn column.

See [Advanced performance models](advanced-performance.md) and [Using the Estimator](../requests/using-the-estimator.md).

---

## Performance Templates

When you select a **native AeroQuote aircraft type** (including the fallback after an empty advanced catalogue search), AeroQuote may provide default performance values based on typical specifications. You can:

- **Accept defaults** — Use the template values  
- **Customize** — Adjust for your specific aircraft's performance  

{% hint style="warning" %}
Templates are starting points. Your aircraft's actual performance may differ based on age, configuration, and modifications.
{% endhint %}

---

## Altitude and Conditions

Some advanced configurations include:

- **Typical cruise altitude** — Affects fuel burn
- **ISA deviation adjustments** — Temperature corrections
- **Payload vs range tradeoffs** — Performance at different weights

---

## Tips for Accuracy

{% hint style="success" %}
**Consult your pilot** — Your chief pilot or flight crew can provide realistic performance figures based on actual operations.
{% endhint %}

- Use flight logs to verify real-world fuel burn
- Consider seasonal variations (winter vs summer performance)
- Update data after any modifications to the aircraft
- Be conservative — it's better to slightly overestimate costs

---

## Next Steps

- [Advanced performance models](advanced-performance.md) — Link or change the planning model
- [Costings](costings.md) — Configure pricing and hourly rates
- [Cost Simulator](cost-simulator.md) — Test your settings
