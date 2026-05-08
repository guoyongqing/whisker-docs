# Privacy Policy

**Effective Date:** May 7, 2026

Whisker ("we", "us", "the app") is a local-first pet health record for iOS. This Privacy Policy explains, in plain language, what data Whisker handles, where it lives, and what we do — and do not — do with it.

**Short version:** We do not collect any personal data. We do not have a server. We cannot read your records, because they never leave your device unencrypted.

## 1. Data Whisker stores on your device

When you use Whisker, you may enter information about your pets, including:
- Pet name, species, breed, birth date, microchip ID, allergies, medical conditions, photos
- Vaccine, deworming, medication, weight, vet-visit records and dates
- Scanned documents (lab reports, prescriptions, invoices) and the OCR text extracted from them
- Veterinarian contact details you choose to save

All of the above is stored inside the iOS application sandbox in a database encrypted with 256-bit AES (SQLCipher). The encryption key is generated on first launch and stored in the iOS Keychain on your device. The key never leaves your device.

## 2. Data we collect

None.

We do not have user accounts. We do not have a server. We do not run analytics SDKs (no Firebase Analytics, no Mixpanel, no Sentry, no Crashlytics, no advertising IDs). We do not track app opens, feature usage, errors, or any other behavior.

## 3. Permissions Whisker requests

Whisker may ask for the following iOS permissions. Each one is used locally and never transmitted off your device:

- **Camera** — to scan paper documents like lab reports and prescriptions. Image processing (Vision OCR) runs entirely on your iPhone.
- **Photo Library** — only when you pick an existing image to attach to a pet record.
- **Face ID / Touch ID** — to lock the app, if you enable biometric unlock in Settings. Whisker uses Apple's `LocalAuthentication` API; no biometric data is ever read or stored by us.
- **Apple Health** — read-only access to your step count and outdoor walking time, used to plot exercise correlations next to your dog's weight curve. We never write to HealthKit. The data stays in HealthKit; we read it on demand.
- **Local Network** — only if you enable Family Sharing. Used to discover other Whisker devices on your Wi-Fi via Apple's MultipeerConnectivity framework. Records sync peer-to-peer between paired devices and never traverse a server we control.

## 4. In-App Purchases

Whisker offers optional Premium subscriptions and a one-time lifetime purchase. All purchases are processed by Apple via the App Store. Whisker never sees, transmits, or stores your payment details. Purchase receipts are validated locally on your device.

## 5. On-device AI

Whisker uses Apple's on-device machine learning for two features:
- **Vision OCR** to convert scanned paper into text.
- **Apple Foundation Models** (iOS 26+, on Apple Intelligence-capable devices) to extract structured lab values from messy OCR text.

Both run entirely on your iPhone. No image, no text, and no extracted value is ever sent to a remote server by Whisker.

## 6. Backups

If you create a backup using the in-app feature, the resulting file:
- Is encrypted with AES-256-GCM using a key derived from your passphrase or 12-word recovery phrase
- Is saved to whatever destination you choose (Files app, AirDrop, etc.)
- Is never sent to us or to any third party

We have no ability to recover your backup if you lose your passphrase or recovery phrase.

## 7. Children's privacy

Whisker is not directed at children under 13. We do not knowingly collect any personal information from children — and indeed we do not knowingly collect personal information from anyone.

## 8. Your rights

Because we hold no personal data, requests to access, correct, export or delete data should be directed to your own device. You can:
- Export your records via the in-app backup feature
- Delete all records by uninstalling the app (the encrypted database is removed with the app sandbox)
- Reset onboarding state by deleting and reinstalling

If you are in the EU/UK (GDPR) or California (CCPA), please note: we are not a "data controller" or "business" handling your personal information, because we do not collect or process your data on any system we operate.

## 9. Changes to this policy

If we ever change Whisker's architecture in a way that involves collecting or transmitting your data — for example by adding a sync server — we will update this Privacy Policy and present the change in the app before the new behavior takes effect.

## 10. Contact

Questions about this policy: shadeless@126.com
