---
description: >-
  Quote an aircraft type (for example "Cessna Citation CJ2") instead of a
  specific tail, and pick the real aircraft when you create the flight.
---

# Generic aircraft types

A **generic aircraft** is an aircraft *type* you can quote. Examples are "Cessna Citation CJ2" and "King Air 350". You quote the type when you have several aircraft of that type and don't yet know which one will fly. When the customer accepts and you create the flight, you pick the real aircraft.

{% hint style="info" %}
If you only have **one** aircraft of a type, you don't need a generic. Quote that aircraft directly.
{% endhint %}

***

## What a generic is (and isn't)

* It is set up like any other aircraft: type, performance, speed and **Costings**.
* It has **no registration**. Quotes, the calendar and PDFs show its name.
* It **doesn't count** towards your plan's aircraft total.
* It is never flown. Book-outs, maintenance, hours, flight tracking and availability cautions don't apply to it, so those tabs and buttons are hidden.
* Only your own fleet aircraft can be linked to it. External or partner aircraft can't.

***

## Create a generic

**New:** in **Add Aircraft**, tick **Generic aircraft type**, choose the aircraft type, and finish the wizard as usual. There is no registration step.

**At your plan's aircraft limit:** the Aircraft list shows **Add generic aircraft type** instead of **Add new Aircraft**. Generics don't count towards the limit, so you can still add them. A real aircraft can't be added until you're below the limit, and a generic can't be switched back to a real aircraft while you're at it.

**Existing aircraft:** open the aircraft, go to the **Details** tab, and switch on **Generic aircraft type**. To switch it off again, unlink its aircraft first; it also needs a registration.

***

## Link your aircraft to the generic

Each aircraft can be linked to **one** generic.

1. Open the real aircraft and go to the **Details** tab.
2. Under **Linked generic type**, pick the generic. If a generic of the same type exists, AeroQuote suggests it. When you add a new aircraft, the suggestion is pre-selected.
3. Choose whether to **Use the generic type's rates**:
   * **Ticked:** the aircraft's Costings are copied from the generic, and they update whenever the generic's Costings change. The aircraft's Costings tab becomes read-only.
   * **Not ticked:** the aircraft keeps its own rates.

You can link an aircraft of a different type. AeroQuote warns you, so check its rates and performance.

The generic's page lists every linked aircraft. Each one shows whether it uses the generic's rates or its own.

### What is copied from the generic

* Charter rate and ferry rate
* Price margin, and whether hourly rates are used
* Minimum customer price
* Auto airport charges, and the default arrival and departure airport charges
* Route (sector) charges

Performance is **not** copied (speed, seats, MTOW, fuel type, photos). Each aircraft keeps its own.

If you unlink an aircraft, it keeps the last rates it had. Changing a generic's rates doesn't reprice quotes you've already made.

***

## Quoting

Choose the generic as the aircraft for an option, the same way you would choose a real aircraft. The quote uses the generic's speed and Costings.

***

## Create the flight: pick the real aircraft

A flight can't use a generic. When you select **Create Flight** on an accepted quote, the modal asks you to **Pick the aircraft that will fly** for each option quoted on a generic. For each linked, active aircraft it shows:

* its **status dot** for the flight dates;
* the **cost** recalculated for that aircraft;
* the **margin** in $ and %, in red when it is a loss and amber when it is below that aircraft's price margin;
* any change in **flight time**, and a warning if the aircraft is a different type.

**Create Flight** is disabled until every option has an aircraft picked.

When the flight is created:

* the picked aircraft is put on each leg;
* **costs** are recalculated for that aircraft, but the **price stays as quoted**;
* if the aircraft is faster or slower, the leg flight times change. Departures stay as quoted and arrival times move. This also changes the itinerary the customer sees.

The cost change appears on the booking like a reprice, with the original quoted cost kept. You can revert it or turn it into an amendment as usual.

***

## Calendar

Accepted quotes on a generic show the generic's name.

If more accepted quotes on the same generic overlap than you have linked aircraft free at that time, the quotes show an amber ⚠ note with the counts. Linked aircraft already booked or booked out at that time aren't counted as free. The note is information only. It doesn't stop you quoting or accepting.
