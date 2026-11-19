# Export contacts

Download the contacts on the Contacts page, with their quote and flight metrics, as an Excel workbook.

{% hint style="info" %}
Only roles with the **Contacts - Export** permission see **Export metrics**. Account administrators have it by default. Other roles can be given it under [Permissions](../settings/permissions.md).
{% endhint %}

Open **Contacts** and click **Export metrics**.

The export follows what the table is showing: your search, filters and sort order. The file is named `contacts-metrics-YYYY-MM-DD.xlsx`, or `contacts-metrics-YYYY-MM-DD-filtered.xlsx` when a search or filter is applied.

{% hint style="warning" %}
The export includes passport numbers, dates of birth and booking values. Keep the file somewhere private.
{% endhint %}

The workbook has three sheets.

## Contacts sheet

The first 15 columns are the contact details:

| Column | Contents |
| --- | --- |
| contact_name | Name |
| gender | Gender, when it is set |
| contact_email | Email |
| contact_phone | Phone |
| contact_notes | Notes saved on the contact |
| weight | Weight value |
| weight_unit | `kg`, `lb`, or `t` |
| passport_number | Passport number |
| passport_expiry | Passport expiry, as `YYYY-MM-DD` |
| date_of_birth | Date of birth, as `YYYY-MM-DD` |
| additional_emails | Extra email addresses. Each one is `address (label)`, separated by a semicolon |
| company_name | Company name |
| company_email | Company email |
| company_phone | Company phone |
| created_at | When the contact was added |

Then the metrics:

| Column | Contents |
| --- | --- |
| type | Passenger, Contact or Both |
| quotes_included, quotes_included_to, quotes_included_cc | Quotes the contact is on, and how many as main (To) or Cc |
| quotes_sent, quotes_accepted | Quotes sent to / accepted by the contact as main (To) contact |
| quotes_sent_inferred | Sends from before per-contact tracking, worked out from the quote's email history |
| conversion_pct | quotes_accepted ÷ quotes_sent |
| flights_flown | Revenue legs flown, including estimated legs |
| flights_estimated | Past legs on confirmed bookings that were never closed off |
| flights_upcoming | Future legs on confirmed bookings |
| hours_flown | Hours (airborne, else block, else planned time) |
| hours_planned_share_pct | Share of hours that came from planned times |
| distance_m | Distance in **metres** |
| flights_charter, hours_charter, distance_m_charter (and the same for scheduled and tour) | Split by flight type |
| first_flown, last_flown | Dates, as `YYYY-MM-DD` |
| checked_in_legs | Legs where the passenger checked in |
| ff_tier, ff_score | Suggested frequent-flyer tier and score |
| value, value_currency | Ticket fares, tour price per passenger, and charter booking price credited to the primary booking contact. Bookings in another currency are skipped |
| value_mixed_currency_skipped | Yes when some value was skipped for being in another currency |
| baseline_flights, baseline_hours, baseline_distance_m, baseline_value, baseline_as_at | The contact's [baseline](contact-baselines.md) |
| total_flights, total_hours, total_distance_m, total_value | AeroQuote history plus baseline (all time) |

The **value** columns are only in the export. They are not shown on the Contacts page.

When **Flight type** or **Flown between** is set, the flight, hours, distance and first/last flown columns cover the filtered flights only. The baseline and total columns are always all time.

## Flights sheet

One row per flown, estimated or upcoming leg for the exported contacts: contact name and email, date, booking reference, type, state, from, to, hours and where they came from, distance in metres and where it came from, and whether the passenger checked in.

## About sheet

When the file was made, how many contacts and flight rows it has, the filters that were applied, and what each figure means.

{% hint style="info" %}
This file is not the import template. **Import CSV** still needs the [sample CSV](https://cdn.aeroquote.com/sample-assets/aeroquote_contact_import_example.csv). To load opening figures, use [Import baselines](contact-baselines.md#import-baselines-from-a-csv).
{% endhint %}
