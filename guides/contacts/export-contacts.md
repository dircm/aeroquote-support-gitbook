# Export contacts

Download the contacts for the operator you are signed in to as an Excel spreadsheet.

Open **Contacts** and click **Export**. The file is named `contacts-YYYY-MM-DD.xlsx`.

{% hint style="warning" %}
The export is a full copy of your contact list, including passport numbers and dates of birth. Keep the file somewhere private.
{% endhint %}

## Columns

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

{% hint style="info" %}
This file is not the import template. **Import CSV** still needs the [sample CSV](https://cdn.aeroquote.com/sample-assets/aeroquote_contact_import_example.csv). Uploading an export file is rejected because it has extra columns.
{% endhint %}
