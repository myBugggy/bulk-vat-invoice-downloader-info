# Reviewer & Certification Testing Instructions

Paste the text below into the **"Instructions for Reviewers"** (Chrome Web Store) and **"Notes for Certification"** (Microsoft Edge Add-ons) box before clicking Submit for Review.

> **Important:** Before pasting, replace `[INSERT_LEMON_SQUEEZY_TEST_LICENSE_KEY]` with a real active license key generated in your Lemon Squeezy dashboard, and optionally replace `[INSERT_UNLISTED_DEMO_VIDEO_URL]` if you record a short screen capture.

---

## Copy-Paste Template for Store Reviewers

```text
TESTING & REVIEW INSTRUCTIONS FOR CERTIFICATION TEAM:

1. LICENSE ACTIVATION (COMPLIMENTARY REVIEWER KEY)
This extension requires an active Lemon Squeezy license key (or 3-day trial key) to unlock the main interface. Please use the following complimentary license key for testing:

License Key: [INSERT_LEMON_SQUEEZY_TEST_LICENSE_KEY]

Steps to activate:
- Click the extension icon in the toolbar.
- Paste the License Key above into the input field and click "Activate".
- The main "VAT Downloader" interface will immediately unlock.

2. HOW THE EXTENSION WORKS ON AIRBNB HOST ACCOUNTS
This extension is designed specifically for Airbnb Hosts who have completed reservations with EU VAT invoices located at:
https://www.airbnb.com/hosting/completed (or https://www.airbnb.com/hosting/reservations/completed on any regional Airbnb domain such as airbnb.pt, airbnb.es, airbnb.fr, etc.)

Host workflow:
- The host navigates to `airbnb.com/hosting/completed` and uses Airbnb's "Filters" button to select their desired date range.
- In the extension popup, the host sets "Max 'Next' page clicks" (defaults to 2) and clicks "Download Invoices".
- `content.js` clicks the action menu ("..." / "More" button) on each reservation row on the page to locate the "VAT invoice" link (`/invoice/...` or `host_vat_invoice`), then clicks the pagination "Next / Próximo" button up to the configured limit (default 2 times) to collect invoices across pages.
- `background.js` opens each discovered VAT invoice URL in a temporary background tab, attaches `chrome.debugger` momentarily to invoke `Page.printToPDF`, detaches the debugger, and closes the temporary tab.
- `background.js` packages all generated PDF buffers into a single timestamped ZIP archive using bundled `jszip.min.js` and saves it via `chrome.downloads.download`.

3. TESTING WITHOUT AN ACTIVE AIRBNB HOST ACCOUNT
Because testing live invoice extraction requires an authenticated Airbnb Host account with completed financial reservations (which contains real guest PII and tax records), you can verify functionality in two ways:
- Live UI & License Verification: Activate the license key above in the popup, inspect the "Manage License" panel, open the "Options" page to configure a custom download subfolder, and trigger "Download Invoices" on any page to observe the real-time activity log and status handling.
- Video Walkthrough of Live Host Account Extraction: [INSERT_UNLISTED_DEMO_VIDEO_URL]
```

