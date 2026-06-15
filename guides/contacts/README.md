---
description: >-
  Contacts serve as your main CRM entries for quotes and bookings, while
  Passengers are a distinct "passenger" type used for flight manifests and
  assignments.
cover: >-
  https://images.unsplash.com/photo-1454923634634-bd1614719a7b?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHw0fHxjcm93ZHxlbnwwfHx8fDE2OTI3MDUyOTJ8MA&ixlib=rb-4.0.3&q=85
coverY: 0
---

# Contacts

AeroQuote distinguishes between two types of contacts:

- **Main Contacts** (type: `contact`): Your primary customer relationship management (CRM) database. These are used as the main point of contact for quotes and bookings, quote history, CSV imports, quick search, and customer communications.
- **Passengers** (type: `passenger`): Special-purpose contacts used for passenger manifests, flight leg assignments, weights for payload calculations, check-in, and crew views. 

New passengers added via the **Passengers & Cargo** step in a booking (when not linking to an existing contact) are automatically created as passenger-type contacts. These appear in the Contacts list when you filter by **Passengers**. You can also use existing main contacts as passengers on bookings.

{% hint style="info" %}
If you use a contact (main or passenger) as a passenger, edit the contact's weight for accurate payload calculations. Passenger-type contacts are ideal for one-off or manifest-specific entries to avoid cluttering your main CRM list.
{% endhint %}

## Listing and Filtering Contacts

Click the <img src="../../.gitbook/assets/contacts menu item.png" alt="" data-size="line"> Contacts menu item to open the list of contacts.

![](<../../.gitbook/assets/contacts page.png>)

From this page, you can:

* **Add new Contact** - Click this button to add a new *main* contact. [See how](add-a-new-contact.md)
* **Import CSV** - Bulk import main contacts from spreadsheets. [See how](import-contacts.md)
* **Filter by type** — Use the **Show:** filter buttons (All / Contacts / Passengers) to view main contacts, passenger-type contacts, or both.
* **Search** - search for contacts by name, email, company name, phone, or notes.
* Edit a Contact - click the <img src="../../.gitbook/assets/contact edit button.png" alt="" data-size="line">button to open the edit contact window.

{% content-ref url="add-a-new-contact.md" %}
[add-a-new-contact.md](add-a-new-contact.md)
{% endcontent-ref %}

{% content-ref url="import-contacts.md" %}
[import-contacts.md](import-contacts.md)
{% endcontent-ref %}
