---
description: >-
  Add opening flights, hours, distance and value for travel a contact did
  before AeroQuote or in another system, one at a time or from a CSV.
---

# Contact baselines

A **baseline** is a set of opening figures for a contact: flights, hours, distance and (optionally) value from before you used AeroQuote or from another system.

Baselines are added to the all-time **Flights**, **Hours** and **Distance** columns and to the `total_*` columns in the export. They are **not** added to:

* totals filtered by **Flight type** or **Flown between**
* the **Frequent flyer** tier or score
* the flight history list

Your bookings are never changed. Each contact has at most one baseline. Every change is written to the activity log with who made it and the old and new figures.

{% hint style="info" %}
You need the **Contacts - Edit** permission to add, change, remove or import baselines.
{% endhint %}

## Set one contact's baseline

1. Open **Contacts**.
2. Click **Baseline** on the contact's row.
3. Enter **Flights**, **Hours** and **Distance (km)**. **Value** (in your currency, shown in the export only), **Figures as at** and **Notes** are optional.
4. Click **Submit**.

To remove a baseline, set flights, hours, distance and value to 0 and click **Submit**.

## Import baselines from a CSV

1. Open **Contacts** and click **Import baselines**.
2. Click **Download template** if you want a starting file.
3. Upload your CSV or Excel (.xlsx) file and click **Preview**.
4. Check the preview. Nothing is saved yet. Rows with problems are listed first, in red, with the reason.
5. Click **Apply N valid rows** to save the valid rows, or **Cancel**.

Rows with problems are skipped; fix them and upload the file again. A row replaces any baseline the contact already has. The preview expires after 30 minutes.

### CSV format

The first row must be a header row. Columns can be in any order and headers are not case-sensitive.

| Column | Required | Format |
| --- | --- | --- |
| `contact_email` | One of these two columns | The contact's email address (not case-sensitive) |
| `contact_name` | | The contact's name exactly as it appears in AeroQuote |
| `flights` | At least one figure | Whole number |
| `hours` | | Decimal hours, e.g. `12.5` |
| `distance_km` | | Kilometres. Use this **or** `distance_m`, not both |
| `distance_m` | | Metres, whole number |
| `value` | No | Amount in your currency, e.g. `4500.00` |
| `as_at` | No | Date the figures are up to, as `YYYY-MM-DD`. Can't be in the future |
| `notes` | No | Up to 500 characters |

Blank figures count as 0. Up to 5,000 rows per file.

Example:

```csv
contact_email,contact_name,flights,hours,distance_km,value,as_at,notes
jane@example.com,Jane Citizen,14,22.5,6400,18500.00,2026-06-30,Flights before AeroQuote
,Sam Example,3,4,950,,,Matched by name when there is no email
```

### How rows are matched

* If `contact_email` is filled in, the row matches the contact with that email. If two contacts share the email, add the exact `contact_name` too.
* Otherwise the row matches the contact with exactly that `contact_name`. If two contacts share the name, add their email.
* Only your own operator's contacts are matched.

### Row problems

| Message | Fix |
| --- | --- |
| No contact with email … / No contact named … | Check the spelling, or add the contact first |
| More than one contact … | Add the email (or exact name) so only one contact matches |
| … must be a number / must be a whole number | Remove letters and units from the figure |
| … can't be negative | Use 0 or a positive number |
| as_at must be a date like 2026-06-30 / can't be in the future | Use `YYYY-MM-DD` and a date up to today |
| Same contact as line N | Keep one row per contact |
| All figures are zero or blank | Add at least one figure, or remove the row |
