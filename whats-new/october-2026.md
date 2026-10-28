---
description: >-
  Bookings is now Flights, and circuit hops within 10 minutes are stored as one
  recorded flight with no track.  Download your full contact list as an Excel
  spreadsheet.
---

# October 2026

## Bookings is now Flights

The **Bookings** module is now **Flights**.

Charter work is still there. The new name makes room for other flying you already do — training, maintenance, private, and other flights — alongside charter, in the same list and the same tracker.

### What you will see

* The sidebar says **Flights** rather than **Bookings**
* Quotes use **Generate a Charter Flight - just like before**
* The operations screen is the **Flights Dashboard**
* See your Flightaware flights in the new **Flight Logs**

Settings → Modules still labels the card **Bookings Module**. The grace-period banner still says **Bookings & Flight Tracking**.

When you create a flight, the first step is **Type**. The choices are Charter, Repositioning, Maintenance, and Private. Charter still asks for the customer contact and customer notes. The other three do not ask for a contact. Private is for owner or personal flying.

Existing charter flights, crew, passengers, tracking, and customer pages keep working. Customer confirmations still go out as they do today.

See [Flights](../guides/bookings-operators/) and [Creating a Flight](../guides/bookings-operators/booking-builder.md).

### Settings order and charter defaults

**Localization** now sits before **Billing**. **Default Currency** is on Localization, with the date format, timezone, and fuel unit.

The step that was **Booking defaults** is labelled **Charter Flight defaults**. Charter departure reminders are written there.

### Departure reminders

You can turn on two reminders for charter flights and two for scheduled flights. Each one has days and hours before departure, a subject, and a message. Nothing is sent until **Send this reminder** is on and you save.

* Charter reminders: **Settings → Charter Flight defaults**. They go to the primary contact. The link to their booking page is added at the end.
* Scheduled reminders: **Scheduled Flights → Branding → Booking email**. They go to each paid passenger. The link to that passenger's ticket is added at the end.

Type `{operator}` where you want your operator name. See [Booking Emails](../guides/settings/emails/booking-emails.md).

## Circuit training is one recorded flight

When the same aircraft lands and takes off again **within 10 minutes**, at the same airport, AeroQuote stores the hops as one recorded flight. The type is **No track recorded**. A gap of 10 minutes or more starts a new flight.

A Hayward helicopter detail that flew 02:34–02:45 and then 02:54–03:05 is one flight. If the second takeoff is 02:59, that is a separate flight.

The session runs from the first takeoff to the last landing. The minutes are the airborne time added up, without the pauses on the ground. There is no map. You can still open the row on **Flight Logs** and choose **Training**. Training asks for the student. Hops that stayed separate can be ticked together and converted the same way.

See [Circuit sessions](../guides/bookings-operators/flight-tracking/circuit-sessions.md).

## Export contacts to Excel

**Contacts** has an **Export** button next to **Import CSV**.

The download is an Excel file of the contacts for the operator you are signed in to. It includes name, email, phone, notes, company, weight, gender, passport, date of birth, and extra email addresses.

This file is a copy for your own records. It is not the import template. Uploading it with **Import CSV** is rejected.

See [Export contacts](../guides/contacts/export-contacts.md).
