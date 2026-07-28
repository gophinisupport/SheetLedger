# SheetLedger

[ Auf Deutsch anzeigen 🇩🇪 ](README-de) | [ Privacy Policy 🛡️ ](privacy) | [ Terms of Service 📄 ](service) | [ Help ❓ ](help)

---

## Application Purpose Statement

**SheetLedger** is a personal finance, expense tracking, and budget management application. The primary purpose of **SheetLedger** is to allow users to track, organize, and analyze their daily financial transactions, accounts, and budgets in a secure, local-first environment.

To provide cloud backup, cross-device synchronization, and multi-user collaboration without relying on central third-party servers, **SheetLedger** integrates directly with Google Drive, Google Sheets, and Google User Account APIs. This enables users to store, manage, and back up their personal financial records entirely within their own private Google accounts.

---

## Google OAuth Permissions & Data Usage Disclosure

**SheetLedger** requests specific Google OAuth scopes strictly to fulfill core app functions. Here is how each permission is used:

* **`email` (User Identification & Audit Trail):** Used exclusively to identify the creator or editor of transaction entries in shared ledgers. This ensures multi-user collaborative ledgers can correctly attribute entries and audit histories to individual contributors.
* **`https://www.googleapis.com/auth/drive.file` (Personal Sheet Access):** Used to create, read, update, and manage Google Spreadsheet database files explicitly created by or opened with **SheetLedger** inside the user's personal Google Drive.
* **`https://www.googleapis.com/auth/spreadsheets` (Collaborative Shared Sheet Access):** Requested on-demand only when a user opts to link and co-edit shared ledgers created by third parties. This allows **SheetLedger** to read and sync transaction entries across shared spreadsheets where `drive.file` sandbox boundaries apply.

### Absolute Privacy Guarantee
* **Zero Third-Party Backend:** **SheetLedger** operates entirely serverless. All Google user data and ledger entries are processed locally on your device and transmitted directly to Google's official APIs. We do not store, collect, sell, or transfer your data to any external servers.
* **Limited Use Compliance:** **SheetLedger**'s use and transfer of information received from Google APIs to any other app will adhere to the [Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy), including the Limited Use requirements.

---

## Key Features & Architecture

* **Absolute Data Sovereignty:** Serverless personal finance utility designed for users who demand total control over their data.
* **Local-First Performance:** Local transactions, account configurations, and categories are saved instantly within the device's secure application sandbox.
* **Multi-User Collaboration:** Native support for shared ledgers with automatic contributor attribution via user email identifiers.
* **Automated Data Protection:** Encryption metadata, database structures, and system configurations are automatically managed within spreadsheet App Properties without requiring complex user passphrases.

---

## Download & Availability

Available on the [Google Play Store](https://play.google.com/store/apps/details?id=com.king011.apps.sheetledger).

---

© 2026 gophini (`The Powerpuff Penguin`). Built with meticulous care.  
Support & Inquiries: [gophini.support@gmail.com](mailto:gophini.support@gmail.com)
