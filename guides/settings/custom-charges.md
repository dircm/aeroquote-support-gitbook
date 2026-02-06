---
description: Override default pricing with custom sector and landing charges.
---

# 💰 Custom Charges

Custom Charges let you override AeroQuote's default pricing calculations with your own rates. Use these when you have specific pricing agreements or need to adjust costs for particular routes or airports.

---

## Types of Custom Charges

### 1. Custom Sector Charges

Override costs for specific routes (origin → destination pairs).

**Use cases:**
- Special pricing on your most common routes
- Competitive rates for specific markets
- Promotional pricing

### 2. Custom Landing Charges

Override landing fees at specific airports.

**Use cases:**
- Negotiated rates at home base
- Discounted landing fees at partner airports
- Correcting outdated database pricing

### 3. Custom Sector Durations

Override calculated flight times for specific routes.

**Use cases:**
- Account for known airspace restrictions
- Adjust for typical routing in busy areas
- Correct for wind patterns on common routes

---

## Adding Custom Sector Charges

1. Navigate to the Custom Charges section
2. Click **Add Sector Charge**
3. Enter:
   - **Origin Airport** — Departure point
   - **Destination Airport** — Arrival point
   - **Aircraft Type** — Which aircraft this applies to (or all)
   - **Charge Amount** — Your custom price
4. Click **Save**

{% hint style="info" %}
Sector charges can be one-way or round-trip. Specify the direction or create two entries for different rates in each direction.
{% endhint %}

---

## Adding Custom Landing Charges

1. Click **Add Landing Charge**
2. Enter:
   - **Airport** — The airport code
   - **Aircraft Type** — Which aircraft (or all)
   - **Charge Amount** — Your negotiated landing fee
3. Click **Save**

---

## Adding Custom Sector Durations

1. Click **Add Sector Duration**
2. Enter:
   - **Origin Airport**
   - **Destination Airport**
   - **Aircraft Type**
   - **Duration** — Flight time in minutes
3. Click **Save**

---

## How Custom Charges Apply

When AeroQuote calculates a quote:

1. Checks for custom charges matching the route/airport
2. If found, uses your custom values
3. If not found, uses database defaults

Custom charges **override** defaults completely — they don't add or subtract.

---

## Managing Custom Charges

### Viewing All Charges

The Custom Charges page lists all your overrides with:
- Route or airport
- Aircraft type
- Custom amount
- Date added

### Editing

1. Find the charge in the list
2. Click **Edit**
3. Update values
4. Save

### Deleting

1. Find the charge
2. Click **Delete**
3. Confirm — defaults will apply again

---

## Tips

{% hint style="success" %}
**Audit regularly** — Custom charges can become outdated. Review quarterly to ensure your pricing stays competitive and accurate.
{% endhint %}

- Start with your most frequent routes
- Document why each custom charge exists
- Check quote results after adding charges
- Remove custom charges when underlying rates change
