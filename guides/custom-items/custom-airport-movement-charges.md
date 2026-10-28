---
description: Set your own landing, departure, parking and passenger charges at a specific airport.
---

# Custom Airport Movement Charges

A **Custom Airport Movement Charge** (previously called a *custom landing charge*) lets you set your own airport charges at a specific airport, for one aircraft or for all of your aircraft. Use it for negotiated rates at your home base, partner airports, or anywhere our published charges don't match what you actually pay.

Custom airport movement charges are **private to your operator** — no one else sees or uses them.

***

## Adding a Custom Airport Movement Charge

1. Go to **Custom Items** from the sidebar
2. In the **Custom Airport Movement Charges** section, click **Add Custom Airport Movement Charge**
3. Choose the **Aircraft**, or turn on **Apply to all aircraft.**
4. Choose the **Airport**
5. Fill in any of the charges below (all optional)
6. Click **Save**

<!-- TODO: add screenshot of the Custom Airport Movement Charge form -->

***

## Charge fields

Every field is optional. Fill in only the charges you want to override.

| Field                              | How it's charged                                                     |
| ---------------------------------- | -------------------------------------------------------------------- |
| **Landing (arrival) charge**       | Flat charge when the aircraft arrives at this airport               |
| **Departure charge**               | Flat charge when the aircraft departs this airport                  |
| **Parking charge per 24 hours**    | Charged per 24 hours on the ground at this airport                  |
| **Arrival charge per passenger**   | Charged per passenger arriving at this airport                      |
| **Departure charge per passenger** | Charged per passenger departing this airport                        |

### How parking is counted

Parking is charged in 24-hour blocks. Exactly 24 hours on the ground counts as **1 day**; any part of a further 24 hours counts as another day. For example, 24 hours = 1 day, 25 hours = 2 days.

***

## How custom charges work with automatic charges

* **Each filled field overrides only its matching automatic charge** at that airport. For example, entering a Landing (arrival) charge replaces the published landing charge, but published passenger and parking charges still apply.
* **A blank field** falls back to the automatic airport charges, and then to the aircraft's [default airport arrival/departure charges](../aircraft/costings.md#default-airport-arrival-and-departure-charges).
* **0 means deliberately free** — nothing is charged for that field, and no automatic or default charge is used in its place.
* **Custom charges apply even when "Automatically calculate airport charges" is turned off** on the aircraft.
* **Aircraft-specific charges beat all-aircraft charges** for the same field at the same airport.

Custom charges show as their own explanation lines in the quote, e.g. *Custom airport arrival charge per passenger*.

{% hint style="info" %}
The app is renaming *landing charges* to **movement charges**. You may still see both terms while the change rolls out — they mean the same thing.
{% endhint %}

***

## Tips

{% hint style="success" %}
**Review regularly** — Negotiated rates change. Check your custom charges when agreements are renewed so your quotes stay accurate.
{% endhint %}

* Use **Apply to all aircraft.** for airport-wide agreements, then add aircraft-specific charges only where a type is priced differently
* Enter 0 to waive a charge you never pay, such as parking at your home base
* Check a test quote after adding charges to confirm the explanation lines look right

***

## Related

* [Costings](../aircraft/costings.md) — Automatic airport charges and aircraft defaults
* [Custom Airports](custom-airports.md)
* [Custom Charges](../settings/custom-charges.md)
