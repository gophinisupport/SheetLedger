# SheetLedger – User Guide & Help

[ Auf Deutsch anzeigen 🇩🇪 ](help-de)

---

### ⚡ 1. App Startup & Connection Resilience
* **Startup Synchronization:** SheetLedger syncs your local state with your cloud ledger upon initialization.
* **Google API Quota Limitations:** Google Sheets APIs enforce strict per-minute usage limits worldwide. If your local ledger experiences high-volume batched operations, sync requests might be queued and slightly delayed.
* **Connection Failures:** If a sync or Google Drive authorization fails due to transient network congestion or API rate-limiting, **do not panic**. Your local data is completely safe. Simply wait a few moments and try again.

### 💎 2. Subscription Tiers & Google Sheets Quotas
To prevent a single user from exhausting our global API traffic allocation and to guarantee service stability for everyone, **the maximum number of concurrently linked Google Sheets is restricted based on your subscription tier (Free vs. Premium)**. Please check the in-app **Subscription panel** to view your current linked sheet limits.

### ✈️ 3. True Offline Capability (Local-First)
* **Zero Network Dependency:** SheetLedger is built as a pure local-first application. You can view, add, or edit your financial records anywhere—even on a plane or deep underground with zero connectivity.
* **Auto-Resumption:** Once your device re-establishes a network connection, our internal state machine will automatically resume in the background and safely upload your cached modifications to the cloud.

### ⚠️ 4. Crucial: Do Not Manually Edit the Google Sheets Document
* **Cryptographic & Structural Integrity:** The linked Google Sheets document acts as an encrypted storage backend. SheetLedger enforces strict cryptographic validation and relational schema checks.
* **Data Corruption Risk:** **Never manually insert, delete, or modify rows, cells, or columns directly inside the Google Sheets web/mobile interface.** Manual interference will break the data consistency verification hash, causing the app to flag the ledger as corrupted to protect your financial security. All operations must be performed via the SheetLedger app runtime.

### 👥 5. Multi-Device Synchronization
You can securely log in with your personal Google Account on multiple devices (e.g., your Android phone and tablet) simultaneously. The local-first architecture ensures all devices safely converge on the same ledger state via the cloud.

### 🤝 6. Secure Multi-User Collaboration (Shared Ledgers)
SheetLedger natively supports distributed multiplayer bookkeeping with industry-grade access control:
1. **How to Share:** Simply use the official Google Drive/Sheets interface to share your spreadsheet document with your partners, family members, or business associates via their Google Accounts.
2. **Linking the App:** Have them open SheetLedger on their devices and link to that exact same shared Google Sheet.
3. **Identity-Based Security:** To prevent unauthorized tampering, **all transaction logs are tied to the creator's unique Google Account ID**. While multiple users can view and collaborate within the same shared ledger, our state machine strictly verifies identities—records created by one Google ID cannot be modified or forged by another, ensuring mathematical tamper-proofing.

---

### ❓ Frequently Asked Questions (FAQ)

#### Q1: Why is my transaction not showing up in Google Sheets immediately?

SheetLedger works local-first. Your changes are saved instantly to your device so you never lose data. Syncing to Google Sheets happens in the background, but may occasionally be queued or delayed due to Google API rate limits or weak internet connection. Rest assured, your data is completely safe locally.


#### Q2: What happens if I accidentally edit or delete a row directly inside Google Sheets?

Direct manual edits can corrupt the structural integrity and security validation hashes of your ledger. If SheetLedger detects invalid manual changes, sync for that sheet may pause to protect your data. If this happens, please first delete the ledger inside SheetLedger to prevent pushing further updates. Next, restore the spreadsheet to a previous working version via Google Sheets -> File -> Version history (or contact support). Finally, create a new ledger in SheetLedger and reconnect your cloud data.

#### Q3: Can I modify the same ledger across multiple devices?

Yes! Simply sign in with the same Google Account on your different devices, then link SheetLedger to the exact same cloud Sheet. This is one of the biggest features of this app: a seamless cloud-data experience, while keeping full control of your data inside your own Google Drive. No one else can access it—even though the data is stored on Google's servers, without the decryption key, even Google cannot decrypt your data.

#### Q4: Can my spouse/partner and I track expenses together in one ledger?

Yes! Simply share the linked Google Sheet with your partner's Google Account via Google Drive (grant them Editor access). Next, have them open SheetLedger on their device and link to that shared sheet. Both of you can log expenses—our identity verification ensures all records remain tamper-proof. In the app, you can also easily filter data by specific users; for example, while default charts analyze everyone's entries, you can filter by email address if you only want to view your partner's records.

#### Q5: Why do I need to log in again when selecting a shared sheet?

To protect your privacy and data security, SheetLedger only requests the minimum necessary scope (drive.file), which limits the app to accessing spreadsheets you explicitly authorize. Selecting a sheet shared by someone else relies on the official Google Picker API, which requires browser-based authentication. As a result, SheetLedger embeds an in-app WebView to let you securely log in and pick the shared spreadsheet.

#### Q6: Why can't I find a Google Sheet that I created manually?
For privacy and security reasons, SheetLedger requests only the minimum necessary scope (drive.file), which grants access strictly to sheets created directly within this app. If you want to link a sheet that you created manually in Google Drive (or one that was shared with you by someone else), please select the "Link Shared Sheet" option instead.

#### Q7: What are the limits of the Free tier vs. Premium subscription?

Cloud functionality is only available with an active subscription. Because Google API calls are not free, we enforce cloud usage limits to manage operational costs and keep the project sustainable. For non-cloud local features, all versions are completely identical—there are no functional limits and zero annoying ads. If you don't need cloud synchronization, no subscription is required. For most users who want cloud capabilities, we recommend the Basic plan, which covers all essential cloud features and meets the needs of majority of users.

#### Q8: Can I use SheetLedger while traveling or without internet access?

Yes, absolutely! SheetLedger is fully functional offline. You can add, edit, or search transactions anytime without a network connection. Once you are back online, SheetLedger will automatically sync all pending offline changes to your Google Sheets.

#### Q9: How do I transfer my ledgers to a new phone or tablet?

- For cloud-linked data: Simply download SheetLedger on your new device, sign in with the same Google Account, and link to your existing Google Sheet ledger. All your financial data will be seamlessly retrieved and synchronized.

- For local-only data (unlinked): If your ledger is strictly stored locally without a Google Sheet connection, you can use our built-in Backup & Restore feature to export and migrate your data to the new device.

#### Q10: Why is there no restore function for cloud-linked data?

Cloud data utilizes distributed writing. Offering a direct restore mechanism could trigger write conflicts and cause data corruption, which is why a built-in restore feature is omitted for cloud ledgers. If you wish to backup or restore cloud data, you can simply create a copy of your Google Sheet directly inside Google Drive as a backup. When you need to restore, create a new ledger in SheetLedger and link it to that backup copy.

---

© 2026 gophini. Built for ultimate financial sovereignty.  
Need technical assistance? Reach out to: **gophini.support@gmail.com**


