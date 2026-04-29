# Tidey Remote Support

Last updated: 2026-04-29

## Contact

For questions, bug reports, or feature requests, email **fsjforever26@gmail.com**.

We aim to respond within a few business days.

## Getting started

Tidey Remote is the iPhone companion for **Tidey**, a developer-friendly terminal app for macOS.

To use Tidey Remote you need:

1. A Mac running macOS Sonoma or later.
2. **Tidey** installed on that Mac.
3. **Tidey Remote Bridge** running on that Mac (a small companion service that exposes Tidey to the iPhone app).

Both Tidey and the Bridge are free.

## Pairing your iPhone

1. Open Tidey on your Mac.
2. In Tidey's settings, open the **Remote** tab.
3. A QR code will appear once the Bridge is available.
4. Open Tidey Remote on your iPhone, tap **Pair a Mac**, and scan the QR code with the camera.

If pairing fails, check that:

- Both devices are on the same Wi-Fi network for the first pairing.
- The Bridge is running on your Mac (it shows a status in Tidey Settings → Remote).
- The Camera permission for Tidey Remote is granted in iOS Settings.

## Connecting from outside your network

When you leave your Wi-Fi, Tidey Remote will reconnect to your Mac through Cloudflare Quick Tunnel and a small resolver service that tracks your Mac's current tunnel endpoint.

If a remote connection fails:

- Check that your Mac is awake and online.
- Check that Tidey is running and the Bridge service is active.
- Reopen Tidey Remote on your iPhone — the app will retry the connection automatically.

## Try Demo mode

If you do not yet have Tidey on a Mac, tap **Try Demo** on the host list to explore the app with sample data. Demo mode does not connect to a live Mac and does not send network requests.

## Permissions

Tidey Remote uses these permissions:

- **Camera** — scan the pairing QR code and capture image attachments.
- **Photos (add only)** — save photos taken from the camera flow to your library.
- **Local network** — discover your Mac on the same Wi-Fi.
- **Notifications** — show local replies and session updates.

All permissions are optional and the app works with reduced functionality if you decline them.

## Privacy

Tidey Remote does not include third-party analytics or advertising SDKs and does not sell user data. See the [Privacy Policy](privacy.html) for details.

## Reporting a bug

When reporting a bug, please include:

- iPhone model and iOS version.
- macOS version on your Mac.
- A short description of what you were doing when the issue happened.
- Whether the issue is repeatable.

Send the report to **fsjforever26@gmail.com**.
