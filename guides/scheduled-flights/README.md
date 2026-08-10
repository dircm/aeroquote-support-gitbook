---
description: Sell seats on recurring routes through your own branded storefront — routes, fares, schedules, published departures, and day-of operations.
---

# 🛫 Scheduled Flights

The Scheduled Flights module turns AeroQuote into a seat-selling airline system for regional and commuter operators. You define **routes** (the city-pairs or multi-stop runs you fly), attach **fare classes** and **recurring schedules**, and AeroQuote **publishes departures** customers can book on a public storefront branded to your company — with tickets, QR boarding passes, Apple/Google Wallet passes, and refunds handled for you.

## Who it's for

* Regional and remote-area operators selling seats on fixed runs (mail runs, community services, coastal shuttles)
* Operators running subsidised community routes with resident fares
* FIFO and contract operators who want recurring departures on the Flight Board without any public sales (see [private routes](creating-a-route.md#public-vs-private-routes))

## How it differs from charter quotes and bookings

| | Charter (Quotes → Bookings) | Scheduled Flights |
| --- | --- | --- |
| Customer buys | The whole aircraft | Individual seats |
| Pricing | Quoted per trip | Fare classes on published fares |
| Sales channel | Quote emails, customer pages | Public storefront + operator manual bookings |
| Created by | You, per enquiry | Materialised automatically from a schedule |

Behind the scenes every published departure gets a regular **Booking** and flight item — so crew assignment, manifests, [flight tracking](../bookings-operators/flight-tracking/README.md), and the mobile app all work exactly as they do for charter.

## Prerequisites

* The **Bookings** module and the **Scheduled Flights** module both enabled — check **Settings → Modules**.
* Airports in your directory for every stop you fly.
* A payment provider is **optional to start**: without one the storefront runs in **test mode** (an amber **TEST MODE** banner shows, and checkout uses a one-click **Complete test booking** button — tickets, emails, manifests, and refunds all work, no money moves).

## Where everything lives

The **Scheduled Flights** section in the left sidebar contains: **Flight Board**, **Routes**, **Departures**, **Assign Aircraft & Crew**, **Sales**, **Payouts**, **Travel Agents**, **Branding**, **Custom Domain**, **Payment Provider**, and **Tax**.

## Setup checklist

Work through these guides in order the first time; after go-live most day-to-day work happens on the Flight Board and Departures pages.

1. [Tax Setup](tax-setup.md) — configure your jurisdiction before entering fares
2. [Creating a Route](creating-a-route.md) — stops, visibility, flight numbers, documents
3. [Fares & Pricing](fares-and-pricing.md) — per-leg or flat fares, fare classes, seat caps
4. [Schedules & Publishing](schedules-and-publishing.md) — recurrences, publish departures, auto-extend
5. [Storefront & Custom Domain](storefront-and-custom-domain.md) — branding, your own URL, test booking
6. [Day-of Operations](day-of-operations.md) — Flight Board, manual bookings, reschedules, cancellations, freight
7. [Travel Agents](travel-agents.md) — agent logins, commission, statements and invoicing

{% hint style="success" %}
The happy path — tax, one route, fares, a schedule, 30 days of departures, and a branded storefront with a completed test booking — takes about **30–45 minutes**.
{% endhint %}
