---
description: Start a quote's repositioning leg from where the aircraft is likely to be, instead of its home base.
---

# Start the ferry from the calculated airport

**Start the ferry from the calculated airport** is off for every aircraft until you turn it on. While it is off, a repositioning leg still starts at the aircraft home base.

## Why you would use this

A floating fleet is rarely sitting at one home base. The next charter often starts from wherever the aircraft finished its last job. If every quote still ferries from home base, the price includes an empty leg the aircraft may not fly.

This switch projects the airport the aircraft is most likely to be at when you build a quote with automatic ferry legs. The repositioning cost is then calculated from that airport. You can compare aircraft on the trip they would actually fly, not on a return to base that is not going to happen. A shorter ferry usually means a lower price for the customer, and an aircraft that would have looked too expensive from home base can win the job. That is how the same fleet stays busier.

## How to turn it on

The switch is on the aircraft record, and on the type and operations steps when you add an aircraft.

Turning it on clears the home base and greys that field out. Turning the switch off does not put the old home base back. Choose a home base again yourself.

## How a quote chooses the airport

With the switch on, a quote looks for where that aircraft already is before the new trip:

1. It uses the latest flight already in AeroQuote that finishes before the trip starts. Finished means on-blocks, otherwise arrival, otherwise departure plus the leg duration. Cancelled, expired, and template flights are skipped. Charter, training, maintenance, repositioning, and private flights all count.
2. That arrival airport is used only when the aircraft will have been free there for at least the operator’s **Projected airport ground time**. That setting is on **Settings → Charter Flight defaults**. Example: the ground time is 4 hours, the aircraft arrived 10 hours before the new trip, so the ferry starts at that arrival airport. If it arrived only 30 minutes before, that arrival is not used.
3. If no flight qualifies, AeroQuote uses the last airport FlightAware placed the aircraft at. There is no separate screen for that airport. A later tracking event replaces it.
4. If neither a flight nor a last known airport is available, the estimate has no ferry starting point.

The settings line under **Projected airport ground time** says leaving it empty always uses home base. With the aircraft switch on, an empty value is treated as one minute, and home base is already cleared, so the estimate uses a recent arrival or the last known airport instead.
