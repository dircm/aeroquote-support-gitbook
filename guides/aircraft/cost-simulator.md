---
description: Test your aircraft pricing before going live.
---

# Cost Simulator

The Cost Simulator lets you test your aircraft configuration by simulating quotes. Verify that your performance data and pricing produce accurate results before using the aircraft in real quotes.

---

## Accessing the Cost Simulator

1. Go to **Aircraft** from the sidebar
2. Click on an aircraft
3. Select the **Cost Simulator** tab

---

## How It Works

The Cost Simulator creates a test quote without saving anything:

1. **Enter a route** — Origin and destination airports
2. **Set parameters** — Date, passengers, options
3. **Run simulation** — See calculated costs
4. **Review breakdown** — Check each cost component
5. **Adjust if needed** — Go back and tweak settings

---

## Simulation Inputs

| Input | Description |
|-------|-------------|
| **From** | Departure airport |
| **To** | Arrival airport |
| **Date** | Flight date (affects fuel prices) |
| **Passengers** | Number of passengers |
| **Return Trip** | One-way or round-trip |

---

## Understanding Results

The simulator shows a detailed breakdown:

### Flight Costs
- Flight time calculation
- Hourly rate applied
- Subtotal for flight time

### Fuel Costs
- Estimated fuel consumption
- Fuel price at airports
- Fuel discounts applied (if any)

### Airport Costs
- Landing fees
- Parking fees (if applicable)
- Handling charges

### Additional Costs
- Positioning (if not starting at homebase)
- Overnight fees
- Other charges

### Total
- Grand total for the simulated trip

---

## Testing Scenarios

Use the simulator to verify:

| Scenario | What to Check |
|----------|---------------|
| **Short hop** | Minimum charges apply correctly |
| **Long haul** | Fuel calculations are realistic |
| **Round trip** | Both legs priced correctly |
| **From homebase** | No unnecessary positioning |
| **Away from homebase** | Positioning costs included |

---

## Comparing to Real Quotes

{% hint style="info" %}
The simulator uses the same calculation engine as real quotes. If it looks right here, it'll be right in quotes.
{% endhint %}

After simulating:
1. Check if the total seems reasonable
2. Verify fuel costs match current prices
3. Confirm positioning logic is correct
4. Compare to your mental estimate

---

## Making Adjustments

If the simulation shows unexpected results:

1. **Flight time wrong?** → Check [Flight Performance](flight-performance.md)
2. **Fuel cost off?** → Verify fuel burn rate
3. **Price too high/low?** → Adjust [Costings](costings.md)
4. **Landing fees wrong?** → Check airport data or custom charges

---

## Tips

{% hint style="success" %}
**Test before launch** — Always run a few simulations when setting up a new aircraft or changing rates.
{% endhint %}

- Simulate your most common routes
- Test edge cases (very short and very long trips)
- Compare to previous quotes for sanity check
- Run simulations when fuel prices change significantly

---

## Next Steps

- [Costings](costings.md) — Adjust pricing if needed
- [Flight Performance](flight-performance.md) — Update performance data
