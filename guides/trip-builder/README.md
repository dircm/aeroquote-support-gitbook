---
description: >-
  Plan multi-leg trips with fuel range, payload, optional comfort endurance,
  fuel stops, create a Request or Quote, or save a Custom Trip — Trip Builder
  is in BETA for operators with Preview features.
---

# Trip Builder (BETA)

**Trip Builder** plans a full multi-leg trip with **fuel range**, **payload**, **max ramp fuel**, and **fuel-stop uplifts** when the aircraft has a linked **performance model** — then creates a **Request** or **Quote**, or saves a reusable **Custom Trip**. Aircraft without a performance model still plan **times** from AeroQuote performance; fuel calculations are unavailable.

{% hint style="warning" %}
**BETA** — Trip Builder is available when your operator has **Preview features** enabled (Account Settings). Behaviour may change as we refine fuel-stop suggestions, comfort rules, and cost preview.
{% endhint %}

***

## Who can use it

| Requirement | Detail |
| --- | --- |
| **Preview features** | Operator setting **Preview features** must be **on** (Account Settings). Without it, the Trip Builder promo card does not appear. |
| **Aircraft** | **Active** aircraft appear if they have a linked **performance model**, or AeroQuote **cruise TAS / quoting speed**. A usable **fuel tank** on the performance model is best (full fuel-stop and uplift estimates). If the model has **no tank data**, Trip Builder still plans times and uses the aircraft **maximum range** (or cruise range) as the hop limit. Native tails show **AeroQuote times** — fuel calculations are unavailable. |
| **Permissions** | No separate Trip Builder permission — you need access to **Requests**, **Quotes**, or **Custom Items**. |

See [Advanced performance models](../aircraft/advanced-performance.md) if an aircraft is missing from the list.

***

## Opening Trip Builder

Trip Builder is **not** a sidebar menu item. It opens as a full-screen wizard from:

| Page | What you create |
| --- | --- |
| **Requests** list | A **Request** with the planned flights and the selected aircraft |
| **Quotes** list | A **Quote** (or open **Quote Builder** with the plan preloaded) |
| **Custom Items → Custom Trips** | A reusable **Custom Trip**, or a **Quote** from a saved trip |

On Requests and Quotes, look for the amber promo card:

* Title: **Trip Builder** + **BETA**
* Copy: *Create accurate trips with full fuel planning and uplift costs, now in BETA.*
* Button: **Open Trip Builder**

On **Custom Items**, the **Custom Trips** section (BETA pill) is only shown when Preview features is on. See [Custom Trips (BETA)](../custom-items/custom-trips.md).

***

## Wizard overview

| Step | Name | Purpose |
| --- | --- | --- |
| **1** | **Setup** — Aircraft & payload | Choose aircraft, passengers, crew, cargo, optional comfort endurance |
| **2** | **Route** — Flights | Origins, destinations, times (or TBC), parking gap, optional homebase ferries |
| **3** | **Plan & stops** | Run fuel/range plan, insert fuel or range stops, review and edit the schedule |
| **4** | **Review** | Costs preview, fuel uplifts, create Request or Quote, or save a Custom Trip |

Use **Next** / **Back** / **Close**. Create and save actions appear only on **Review** when the plan is complete.

***

## Step 1: Setup (Aircraft & payload)

1. Search **Aircraft** by registration or name. Each result shows **Advanced times** (linked performance model) or **AeroQuote times** (native performance)
2. Set **Passengers** and **Avg passenger weight** (uses your operator weight unit)
3. Set **Crew** and **Avg crew weight** — crew count is remembered as a default for that aircraft
4. Optional **Cargo weight**
5. Optional **Limit hop length (comfort endurance)** — hours between **1** and **18** (off by default)
6. Review **Payload total** — calculated from pax + crew + cargo; edit if needed, or **Revert to calculated**

The hint under the aircraft field: tails with a linked performance model plan **fuel and range** when tank data exists. Other aircraft use **AeroQuote times**; **fuel calculations are unavailable**.

{% hint style="info" %}
**Comfort endurance** is a **preference**, not a hard fuel or range limit. On the plan step you can continue when a leg is only over comfort; legs that need a **fuel** or **range** stop still require a stop.
{% endhint %}

Click **Next** when an aircraft is selected.

### Changing the aircraft

You can change the tail on **Setup** at any time — use **Back** from Route, Plan & stops, or Review.

When you pick a different aircraft, Trip Builder:

* Drops the current fuel/range plan (you will **Plan trip** again)
* Removes **homebase ferry** legs and asks the Yes/No ferry prompts again (the new tail may have a different homebase)
* Reloads that aircraft’s saved **crew** default
* If you were already on **Review**, you are taken back to **Plan & stops** so you cannot create from a stale plan

Then go through **Route** (confirm ferries) and **Plan trip**. If the new tail has no performance model, expect the amber **Fuel calculations are unavailable for this aircraft** banner — times still use AeroQuote performance.

Trip Builder always plans **one aircraft**. For a multi-option quote, create the trip first, then add more aircraft on the Request estimator or Quote Options.

***

## Step 2: Route (Flights)

Build the charter itinerary Trip Builder will plan.

### How to use this page?

On the Flights header, **How to use this page?** opens a short note: add the intended charter departure (it does not need to be the aircraft homebase) and destination, plus any intermediate stops you already plan to use. The next step checks the legs and suggests fuel (or range) stops if needed.

### No date yet (TBC)

Tick **Customer just wants a price — no travel date yet (TBC)** if the customer only wants a price. Departure times show as TBD until you set real dates later.

### Parking between flights

Set **Parking between flights** (hours and minutes) for the gap after each arrival before the next departure (later charters, fuel stops, and ferries). It seeds from the operator default. After you change it, **Use operator default** appears. This override is **for this trip only** — it does not change Account Settings.

If a later flight already has a time you typed, and the new parking gap would crowd that time, Trip Builder opens **Adjust onward flights?** (same idea as Quote Options). Choose **Apply changes** to move later flights forward, or **Keep current times** to leave the overlap.

### Homebase ferry prompts

If the aircraft has a **homebase** that does not match the first origin and/or last destination, amber banners ask:

* **Yes, add ferry** — insert a **Ferry** leg (homebase → origin, and/or destination → homebase)
* **No** — plan without that positioning leg

Ferry rows show a **Ferry** badge. Origin/destination are locked; ferries carry no passengers, crew, or cargo. Schedule uses arrival plus the parking gap above.

### Flights

* **+ Add flight** — add another sector (origin prefilled from the previous destination)
* Set **origin** and **destination** (search by name or ICAO/IATA)
* **Departing at** on the first charter leg (required unless TBC), in origin local time. If you go to Plan & stops and come back, that time is still shown
* Later legs can use an **optional** departing-at time. Leave it empty to auto-chain from previous arrival + parking. If you set a time that sits inside the parking gap, **Adjust onward flights?** asks before moving later flights
* You can remove non-ferry flights (keep at least one charter sector)

Click **Next** when every charter leg has origin and destination, and the first departure is set (or TBC is on).

***

## Changing departure times

You can set and change times on **Route** and again on **Plan & stops → Schedule**. Times are **schedule only** — they do not recalculate fuel or range until you change the aircraft, route, payload, or click **Re-plan trip**.

### On Route

* **First charter** — **Departing at** is required unless TBC is on. Time is in **origin local time**. If you go to Plan & stops and come **Back**, that time is still shown
* **Later charters** — optional departing-at. Leave it empty to auto-chain from previous **arrival + parking**. Type a time only when you want a specific later departure
* **TBC** — clears departing-at on every flight and drops the current plan (you must plan again)
* **Custom Trip author** mode — departing-at is not used (dates are not saved)

### On Plan & stops → Schedule

When dates are set, **Schedule** lists every planned leg (charters, fuel/via stops, and ferries):

* **Departs** — first charter uses your Route time; later charters can **override** the auto time
* **Arrives** — departure plus planned flight time, in **destination local time**
* Fuel-stop and ferry times stay **auto** (not editable)
* **Use auto** on a later charter clears your override so the parking chain is used again

### Adjust onward flights?

If a later typed time (or a wider **Parking between flights**) would sit inside the parking gap, Trip Builder opens **Adjust onward flights?** — the same idea as Quote Options:

* **Apply changes** — move later flights forward
* **Keep current times** — leave the overlap

### When you must re-plan

Change **aircraft**, **origins/destinations**, **payload**, **comfort endurance**, or **TBC**, then use **Plan trip** / **Re-plan trip**. Changing only a departure time does **not** throw away the fuel plan.

***

## Step 3: Plan & stops

### Auto-plan

The **first time** you open this step (with no plan yet), Trip Builder **plans automatically**. After that, use **Plan trip** or **Re-plan trip** when you change the route or payload. Changing a departure time on this step does **not** throw away the plan.

While recalculating you may see **Adjusting plan…** / *Recalculating route and fuel range…*

### Status banners

| Status | Meaning |
| --- | --- |
| **Trip is within range** | Fuel (or published-range) plan is complete for all legs |
| **Trip is within fuel range** (amber) | Fuel is OK, but a leg is **over comfort preference** — you may continue or **Add stop** |
| **Fuel stop needed** | At least one leg exceeds practical fuel range — pick a stop before **Next** |
| **Fuel calculations are unavailable for this aircraft** (amber) | Native / AeroQuote times — hop times use cruise TAS or quoting speed; fuel uplifts are not estimated |
| **Range stop needed** | The performance model has **no tank data**, and a hop is longer than the aircraft **maximum range** — pick a stop before **Next** |
| **No tank data in the performance model** (blue) | Hop limits use this aircraft’s published maximum range. **Fuel uplifts are not estimated** |
| **Times and costs only** (amber) | No tank and no published range — times/costs still plan; range and fuel stops are off |

### Schedule

See [Changing departure times](#changing-departure-times). TBC and Custom Trip author mode show no travel dates here.

### Legs table

Each leg shows distance/time, required fuel, and status such as:

* **OK**
* **Fuel stop required**
* **Range stop required** — over aircraft maximum range (no-tank models)
* **Over comfort preference**

Per leg:

| Action | When to use |
| --- | --- |
| **Find fuel stop** | Fuel or range failed — pick a stop that keeps the hop within tank or published range |
| **Add stop** | Voluntary intermediate airport (e.g. comfort or customer via) |
| **Remove stop** | Remove an intermediate stop you added (endpoints stay fixed) |

### Stop picker

* **Airport type filters** (large / medium / small / heliport / custom)
* **Search range** slider on fuel-only search (−25% … +25% of the practical hop)
* **Suggested airports** (fuel) or **Suggested near midpoint** (voluntary add stop)
* **Or search for an airport**
* **Endurance risk** (amber) marks farther fuel candidates that may be tight on range

{% hint style="success" %}
**Fuel stop vs Add stop:** **Find fuel stop** is for range. **Add stop** is for splitting a leg near the midpoint (similar idea to [Add a stop between two airports](../quotes/add-a-stop-between-two-airports.md) on a quote option).
{% endhint %}

### Route map

The map shows the planned route with airport markers:

| Colour | Meaning |
| --- | --- |
| **Blue** | Leg within fuel (and comfort, if set) |
| **Amber** | Over comfort preference |
| **Red** | Fuel stop required |

Hover suggestions in the stop picker to preview a stop on the map.

**Next** is blocked while any leg still needs a fuel or range stop. Comfort-only issues do **not** block **Next**.

***

## Step 4: Review

When the plan is complete you see **Ready to create**.

### Estimated commercial costs

* Labelled as a **preview** from your AeroQuote rates — **not a final quote**
* Uses the **planned legs only** (including ferries you accepted on the Route step)
* Does **not** re-inject extra homebase ferries you declined

### Fuel detail

* Per-leg figures such as required fuel, ramp max, route burn, arrive-with, TOW, LW, payload (as shown in product)
* **Suggested fuel uplift at each airport** — origin typically no uplift; intermediate stops show uplift and approximate cost
* **Show fuel providers and prices** opens a modal with providers/prices and an uplift calculator
* Without **tank** data on the performance model (or on native AeroQuote tails), uplifts are **not** estimated (the plan still has times and, if published range is set, hop limits)

### Create

| Opened from | Actions |
| --- | --- |
| **Requests** list | **Create a Request** — new request with planned flights and **this aircraft only**, then the Request / estimator |
| **Quotes** list | **Create Quote** (primary) — estimate, save, open the quote; or **Open Quote Builder** — preload flights and aircraft for edit before save |
| **Custom Items → Add Custom Trip** | **Save as Custom Trip** only — no dates, no Create Quote |
| Any of the above (Preview on) | **Save as Custom Trip** — unique title; you stay in the wizard (except author mode, which closes after save) |

{% hint style="info" %}
Trip Builder always materialises **one aircraft** — the tail you selected on Setup. For multi-option quotes, add more aircraft after creation on the Request estimator or Quote Options.
{% endhint %}

***

## Custom Trips (BETA)

Save a flyable plan as a reusable route under **Custom Items**.

### Save from Requests or Quotes

On **Review**, with Preview features on, click **Save as Custom Trip**. Enter a **unique title** (unique for your operator). The route thumbnail is the planned map. You can still create the Request or Quote afterwards.

### Add from Custom Items

**Custom Items → Custom Trips → Add Custom Trip** opens Trip Builder in **author** mode: dates are not used, and Review only offers **Save as Custom Trip**. Finish the wizard and save. Trip Builder then closes.

### Create a quote from a saved trip

On the Custom Trips list, **Create quote from this trip** opens Trip Builder as from the Quotes list, with **all saved stops preloaded** and the trip’s **parking gap** if you overrode it. Adjust payload, confirm the route, re-plan if needed, then **Create Quote** or **Open Quote Builder**.

Full detail: [Custom Trips (BETA)](../custom-items/custom-trips.md).

***

## Tips

* Link and confirm a **performance model** on each tail you want fuel/range for — see [Advanced performance models](../aircraft/advanced-performance.md). Native tails still appear as **AeroQuote times**
* If a model has **no tank**, set **maximum range** (or cruise range) on the aircraft so Plan & stops can still flag hops that are too long
* Set aircraft **homebase** so ferry prompts are meaningful
* Use **Parking between flights** on Route when the operator default is not right for this trip
* Use **comfort endurance** for passenger-friendly hop lengths; ignore the amber comfort banner when fuel is already OK
* Prefer **Find fuel stop** when the plan says fuel or range is short; use **Add stop** for voluntary vias
* To change the tail after you have started planning, go **Back** to Setup — that drops the plan and ferry answers
* Change later departures on **Plan & stops → Schedule** when you want a specific time; Trip Builder asks before moving onward flights
* Treat **Review** commercial totals as indicative — refine pricing on the Request or Quote after create
* Planning can take a few seconds on long multi-stop routes

***

## Related guides

* [Creating a Request (Operators)](../requests/creating-a-request-operators.md)
* [Using the Estimator](../requests/using-the-estimator.md)
* [Creating a Quote from scratch](../quotes/creating-a-quote.md)
* [Add a stop between two airports](../quotes/add-a-stop-between-two-airports.md)
* [Advanced performance models](../aircraft/advanced-performance.md)
* [Custom Trips (BETA)](../custom-items/custom-trips.md)
