# Tidey Remote Privacy Policy

Last updated: 2026-04-29

## Overview

Tidey Remote lets an iPhone connect to the user's own Mac running Tidey and Tidey Remote Bridge. The app is designed for remote control of the user's own terminal and agent sessions, not for advertising, tracking, or selling user data.

Tidey Remote does not include third-party analytics SDKs or advertising SDKs. It does not sell personal data.

## Data the app handles

### Pairing and connection data

Tidey Remote stores paired Mac records on the iPhone, including:

- Mac display name.
- Host identifier.
- LAN, tunnel, and resolver endpoints.
- Connection state metadata.
- Device credentials used to authenticate with the user's Mac.

Device credentials and pairing identity values are stored in the iOS Keychain where appropriate. Host records and local preferences are stored on the device.

### Terminal, chat, and control data

When connected to a Mac, Tidey Remote sends user actions and messages to Tidey Remote Bridge on that Mac. This can include chat messages, selected workspace or panel identifiers, and commands needed to operate the user's own sessions.

These messages are sent to the user's paired Mac. Tidey Remote does not use them for advertising or analytics.

### Images and attachments

When the user selects or captures an image attachment:

- The image is processed locally on the iPhone.
- HEIC and other input formats are converted to JPEG for upload.
- The image is resized and compressed before upload.
- The processed image is uploaded to the user's Mac-side Tidey Remote Bridge.
- The Mac stores uploaded images under `~/Library/Application Support/Tidey Remote Bridge/uploads/`.

If the user takes a new photo from the camera flow, Tidey Remote may save that photo to the user's Photos library when the user grants the related permission.

### Local preferences

Tidey Remote stores local settings such as paired hosts, editor settings, notification prompt state, and UI preferences. These values stay on the user's device unless needed for pairing or connection to the user's Mac.

### Notifications

Tidey Remote can show local notifications for replies or session updates. Notification permission is optional and controlled by iOS Settings.

### Pasteboard

Tidey Remote uses the system pasteboard only when the user explicitly chooses a copy action in the app.

### Demo mode

Try Demo uses local sample data. It does not connect to a live Bridge and does not send network requests.

## Network services

### Local network

On the same network, Tidey Remote connects directly to Tidey Remote Bridge on the user's Mac. This uses local network access and the Mac-side Bridge authentication token or device credential.

### Cloudflare tunnel and resolver

For remote access outside the local network, Tidey can use Cloudflare Quick Tunnel and a resolver service.

The resolver stores host-to-tunnel metadata needed to recover from changing tunnel URLs. This metadata can include:

- Host identifier.
- Current tunnel endpoint.
- Timestamps such as update and expiry time.

The resolver does not need chat messages, image contents, transcript contents, or terminal output.

Cloudflare tunnel traffic and resolver requests transit Cloudflare infrastructure. Cloudflare may process network metadata as part of providing the tunnel or resolver hosting service.

## Permissions

Tidey Remote may request these permissions:

- Camera: scan a Mac pairing QR code and capture photo attachments.
- Photos add-only access: save photos captured from the camera flow to the user's library.
- Local network: connect to the user's Mac on the same network.
- Notifications: show local reply or session update notifications.

The app should still work with reduced functionality if optional permissions are denied.

## Retention and deletion

On iPhone:

- Removing a paired Mac deletes the app's saved host record and associated credential reference.
- Uninstalling the app removes app-local data. Keychain behavior may depend on iOS system behavior and existing credential cleanup paths.

On Mac:

- Uploaded image attachments are stored under `~/Library/Application Support/Tidey Remote Bridge/uploads/`.
- Tidey Remote Bridge includes storage cleanup for uploaded files, including age-based cleanup and a storage size cap.
- Users can reveal or clean the upload folder from Tidey Mac's Remote settings.
- Users can revoke paired devices from Tidey Mac's Remote settings.

## Children's privacy

Tidey Remote is not directed to children.

## Changes to this policy

This policy may be updated as Tidey Remote adds features or changes its network architecture. The public policy includes the effective date of the latest version.

## Contact

Privacy contact: fsjforever26@gmail.com
