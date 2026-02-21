# Push Notifications

The AeroQuote Crew app supports push notifications to keep your team informed of booking updates in real time.

## Setup

Push notifications are enabled automatically when you sign in. The app will request notification permission on first launch:

* **iOS** — A system prompt asks to allow notifications. Tap **Allow**.
* **Android** — Notifications are enabled by default on most versions. Android 13+ will show a permission prompt.

{% hint style="warning" %}
If you denied notification permission, you can re-enable it in your device's **Settings → AeroQuote Crew → Notifications**.
{% endhint %}

## What You'll Receive

Notifications are sent for key booking events, such as:

* Booking status changes
* New passenger or crew assignments
* Flight schedule updates

<!-- 📸 PLACEHOLDER: Screenshot of an iOS rich notification with the route map image expanded -->
<!-- Suggested filename: .gitbook/assets/mobile-push-notification-ios.png -->

### Rich Notifications (iOS)

On iOS, notifications may include a **route map image** showing the flight path — giving you instant visual context without opening the app.

## Tapping a Notification

Tapping a notification opens the app and navigates directly to the relevant booking or flight detail screen.

## Troubleshooting

| Issue | Solution |
|-------|----------|
| Not receiving notifications | Check device Settings → AeroQuote Crew → Notifications is enabled |
| Notifications delayed | Ensure the app has background refresh enabled; check Do Not Disturb is off |
| No map image on notification (iOS) | Ensure you're running the latest app version |
