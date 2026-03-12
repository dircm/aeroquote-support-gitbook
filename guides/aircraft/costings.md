---
description: Set up pricing and hourly rates for your aircraft.
---

# Costings

The Costings section defines how AeroQuote calculates prices for this aircraft. Configure hourly rates, minimum charges, and pricing rules here.

---

## Accessing Costings

1. Go to **Aircraft** from the sidebar
2. Click on an aircraft
3. Select the **Costings** tab

---

## Pricing Models

AeroQuote supports different pricing approaches:

### Hourly Rate Pricing

Charge based on flight time:

| Field | Description |
|-------|-------------|
| **Hourly Rate** | Base rate per flight hour |
| **Positioning Rate** | Rate for empty/ferry flights (often lower) |

### Cost-Plus (Margin) Pricing

Calculate costs and add a margin:

| Field | Description |
|-------|-------------|
| **Operating Costs** | Your actual hourly operating cost |
| **Margin Percentage** | Profit margin to add |

---

## Rate Configuration

### Flight Hour Rates

| Rate Type | When Applied |
|-----------|--------------|
| **Standard Rate** | Normal passenger flights |
| **Positioning Rate** | Empty legs / ferry flights |
| **Minimum Flight Time** | Minimum billable time per leg |

### Example

If your standard rate is $2,500/hour and minimum is 1 hour:
- A 30-minute flight bills as 1 hour = $2,500
- A 2-hour flight bills as 2 hours = $5,000

---

## Minimum Charges

Protect your margins with minimums:

| Minimum Type | Description |
|--------------|-------------|
| **Minimum Flight Time** | Shortest billable leg (e.g., 1 hour) |
| **Daily Minimum** | Minimum charge per day |
| **Trip Minimum** | Minimum charge per trip |

---

## Sector Charges (Cost Types)

Add recurring costs that are automatically calculated on every quote for this aircraft. These are configured in the **Aircraft costs that you will pay** section.

Each cost has a **type** that determines how it's calculated (per hour, per sector, per passenger, per distance, daily, overnight, or ground time) and a **rule** that controls which flights it applies to (all sectors, charter only, or ferry only).

{% hint style="info" %}
See [Cost Types](cost-types.md) for a detailed explanation of each cost type, how it's calculated, and when to use it.
{% endhint %}

---

## Currency

Set the currency for this aircraft's pricing:

- Prices are quoted in this currency
- AeroQuote can convert for international quotes if configured

---

## How Costs Calculate

For a typical quote, AeroQuote calculates:

1. **Flight time** × Hourly rate
2. **+ Positioning costs** (if needed)
3. **+ Fuel costs** (based on performance data)
4. **+ Landing/handling fees** (from airport database)
5. **+ Additional charges** (overnight, etc.)
6. **= Total quote price**

---

## Tips

{% hint style="success" %}
**Know your costs** — Understanding your true operating costs ensures you set profitable rates.
{% endhint %}

- Review competitor pricing in your market
- Consider different rates for different trip types
- Update rates when fuel costs change significantly
- Use the Cost Simulator to verify your pricing

---

## Next Steps

- [Cost Types](cost-types.md) — Detailed guide to each cost type and when to use it
- [Cost Simulator](cost-simulator.md) — Test your pricing configuration
- [Flight Performance](flight-performance.md) — Verify performance data
