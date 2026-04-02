---
description: Manage passenger manifests and cargo for each flight.
---

# 👥 Passengers & Cargo

The Passengers & Cargo section lets you build complete manifests for each flight leg. Track who and what is on each flight.

---

## Accessing Passengers & Cargo

1. Go to **Bookings** from the sidebar
2. Click on a booking
3. Select the **Passengers & Cargo** tab

---

## Adding Passengers

### Step 1: Click Add Passenger

Click **Add Passenger** to open the passenger form.

### Step 2: Enter Details

| Field | Required | Description |
|-------|----------|-------------|
| **Name** | Yes | Passenger's full name |
| **Weight** | Yes | Passenger weight (for W&B calculations) |
| **Contact** | No | Link to existing contact |
| **Email** | No | Passenger email |
| **Phone** | No | Contact number |
| **Notes** | No | Special requirements, preferences |

### Step 3: Assign to Flights

Select which flight legs this passenger is on:
- Check each leg they're traveling on
- A round-trip passenger would be on both outbound and return

### Step 4: Save

Click **Save** to add the passenger.

---

## Passenger Weights

Accurate passenger weights are important for:
- Weight and balance calculations
- Fuel planning
- Safety compliance

{% hint style="info" %}
See [Passenger Weights](passenger-weights.md) for more details on weight configuration.
{% endhint %}

---

## Adding Cargo

### Step 1: Click Add Cargo

Click **Add Cargo** to open the cargo form.

### Step 2: Enter Details

| Field | Required | Description |
|-------|----------|-------------|
| **Description** | Yes | What the cargo is |
| **Weight** | Yes | Cargo weight |
| **Dimensions** | No | Size (L × W × H) |
| **Handling** | No | Special handling notes |

### Step 3: Assign to Flights

Select which legs the cargo travels on.

### Step 4: Save

Click **Save** to add the cargo item.

---

## Viewing the Manifest

The Passengers & Cargo tab shows:

### Passengers Table
- Name
- Weight
- Flight legs assigned
- Contact info

### Cargo Table
- Description
- Weight
- Dimensions
- Flight legs

### Weight Summary
- Total passenger weight
- Total cargo weight
- Combined payload

---

## Editing Entries

1. Click on a passenger or cargo item
2. Update the details
3. Save changes

---

## Removing Entries

1. Find the passenger or cargo item
2. Click **Delete** or the remove icon
3. Confirm removal

---

## QR Code Boarding Passes

Generate QR code boarding passes for passengers and include them in customer emails and flight manifests.

### Enabling QR Boarding Passes

1. Open the booking
2. Go to the **Send** tab
3. Toggle on **Include QR code boarding passes**
4. Send the booking confirmation — each passenger receives a unique QR code

### Scanning at the Aircraft

Crew use the AeroQuote mobile app to scan boarding passes:
1. Open the flight in the mobile app
2. Tap the QR scanner
3. Scan the passenger's boarding pass
4. The passenger is automatically checked in

The scanner handles duplicate scans gracefully and works across flights in the same booking.

---

## Passenger Check-In

Passengers can be checked in for their flights, either by scanning QR boarding passes or manually via the mobile app.

### Manual Check-In (Mobile App)

1. Open the flight in the AeroQuote mobile app
2. View the passenger list
3. Tap each passenger to toggle their check-in status

### Check-In Tracking

Check-in progress is visible on:
- The **Bookings Dashboard** — each booking card shows a check-in progress bar
- The **mobile app** — passenger list with check-in status
- The **activity feed** — check-in events stream in real time

{% hint style="info" %}
All check-in activity is audited — who checked in each passenger and when.
{% endhint %}

---

## Per-Leg Management

For multi-leg trips, you can have different passengers/cargo on each leg:

**Example: Business trip with pickup**
- Leg 1 (BNE → SYD): 2 passengers
- Leg 2 (SYD → MEL): 4 passengers (picked up 2 more)
- Leg 3 (MEL → BNE): 4 passengers

---

## Tips

{% hint style="success" %}
**Collect early** — Request passenger details when the booking is confirmed to avoid last-minute scrambles.
{% endhint %}

- Use consistent weight units across all entries
- Note any mobility requirements or special needs
- Mark dangerous goods appropriately
- Keep manifests updated until departure

---

## Next Steps

- [Crew Assignment](crew-assignment.md) — Assign pilots and crew
- [Booking Status](booking-status.md) — Track flight progress
