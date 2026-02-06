---
description: Configure speed, range, and fuel consumption data.
---

# Flight Performance

The Flight Performance section contains the technical data AeroQuote uses to calculate flight times and fuel costs. Accurate data here means accurate quotes.

---

## Accessing Flight Performance

1. Go to **Aircraft** from the sidebar
2. Click on an aircraft
3. Select the **Flight Performance** tab

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

When you create a quote, AeroQuote uses this data to:

1. **Calculate flight time** — Distance ÷ cruise speed
2. **Estimate fuel needed** — Flight time × fuel burn rate
3. **Check range** — Can this aircraft make the trip non-stop?
4. **Determine fuel costs** — Fuel needed × fuel price at airport

---

## Performance Templates

When you select an aircraft type, AeroQuote may provide default performance values based on typical specifications. You can:

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

- [Costings](costings.md) — Configure pricing and hourly rates
- [Cost Simulator](cost-simulator.md) — Test your settings
