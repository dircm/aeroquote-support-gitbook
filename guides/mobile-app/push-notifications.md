# Push Notifications

The AeroQuote Crew app supports push notifications to keep your team informed of booking updates and flight events in real time.

## Setup

Push notifications are enabled automatically when you sign in. The app will request notification permission on first launch:

* **iOS** — A system prompt asks to allow notifications. Tap **Allow**.
* **Android** — Notifications are enabled by default on most versions. Android 13+ will show a permission prompt.

{% hint style="warning" %}
If you denied notification permission, you can re-enable it in your device's **Settings → AeroQuote Crew → Notifications**.
{% endhint %}

## What You'll Receive

Notifications are sent for key booking events, such as:

* **Flight departure detected** — When FlightAware detects your aircraft has departed
* **Flight arrival detected** — When FlightAware detects your aircraft has arrived
* Booking status changes
* New passenger or crew assignments
* Flight schedule updates

<!-- 📸 PLACEHOLDER: Screenshot of an iOS rich notification with the route map image expanded -->
<!-- Suggested filename: .gitbook/assets/mobile-push-notification-ios.png -->

### Flight Status Notifications

When a flight departs or arrives, all crew assigned to that flight leg receive a push notification containing:

* The flight route (e.g. YBBN → YSSY)
* Aircraft registration
* The detected time from FlightAware
* A static map image of the route

Tapping the notification opens a **confirmation sheet** where you can accept the detected time or adjust it before confirming. See [Flight Status](flight-status.md) for details.

### Rich Notifications (iOS)

On iOS, notifications include a **route map image** showing the flight path — giving you instant visual context without opening the app.

## Tapping a Notification

Tapping a notification opens the app and navigates directly to the relevant booking or flight detail screen. For flight status notifications, a confirmation sheet appears automatically.

## Troubleshooting

| Issue | Solution |
|-------|----------|
| Not receiving notifications | Check device Settings → AeroQuote Crew → Notifications is enabled |
| Notifications delayed | Ensure the app has background refresh enabled; check Do Not Disturb is off |
| No map image on notification (iOS) | Ensure you're running the latest app version |
