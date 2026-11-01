# Privacy Policy — Bulk VAT Invoice Downloader for Airbnb Hosts

**Effective Date:** November 1, 2026  
**Last Updated:** November 1, 2026

This Privacy Policy explains how **Bulk VAT Invoice Downloader for Airbnb Hosts** ("the Extension", "we", "us", or "our") handles information when you install and use our browser extension.

---

## 1. Summary of Our Privacy Commitment

* **Zero Airbnb Data Transmission:** All Airbnb reservation details, confirmation codes, and VAT invoice documents are processed **100% locally** within your browser and saved directly to your device. We never transmit, collect, store, or view your Airbnb data on any external server.
* **Minimal License Data:** The only external network communication performed by the Extension is with **Lemon Squeezy** (`https://api.lemonsqueezy.com`) to activate, validate, or deactivate your subscription license key.
* **No Tracking or Ads:** The Extension contains no analytics scripts, telemetry, advertising SDKs, or third-party trackers.

---

## 2. Information Processed Locally on Your Device

When you use the Extension on an Airbnb Host Reservations page, the Extension accesses:
1. **Airbnb Reservation & Invoice Pages:** Used locally within your browser tab to identify VAT invoice links, open the invoice view, convert the invoice into a PDF document using the browser's built-in PDF renderer, and bundle the resulting PDFs into a ZIP file in your local `Downloads` folder.
2. **Extension Settings & Logs (`chrome.storage.local` & `chrome.storage.sync`):**
   * Your custom download subfolder preference (`downloadPath`).
   * Temporary activity logs and status indicators for the current download session (`appState`).
   * Your Lemon Squeezy license key, activation instance ID, last check timestamp, and license metadata (`licenseKey`, `instanceId`, `licenseMeta`, `lastLicenseCheck`).

None of your Airbnb reservation data, guest names, payout amounts, or VAT invoices ever leave your browser.

---

## 3. Information Shared with Third-Party Services (Lemon Squeezy)

To verify your subscription or free trial status, the Extension communicates directly with the **Lemon Squeezy License API** (`https://api.lemonsqueezy.com/v1/licenses`):
* **Data Sent:** Your entered License Key, an activation instance identifier, and a generic browser/OS label (e.g., `Chrome Extension - Windows NT 10.0`) to identify your activation slot.
* **Data Received & Cached Locally:** License validity status, expiration/renewal date, and the customer name/email associated with the purchase so you can view your account status in the Extension popup.
* **Payment Processing:** All subscription checkouts and billing management occur directly on Lemon Squeezy (`https://bnbvatdownload.lemonsqueezy.com`). The Extension never sees or handles your credit card or billing details. Please refer to [Lemon Squeezy's Privacy Policy](https://www.lemonsqueezy.com/privacy) for details on how they handle checkout and billing data.

---

## 4. Browser Permissions Explained

* **`activeTab` & `scripting`:** Used to scan the active Airbnb Reservations page for VAT invoice links when you click "Download Invoices".
* **`tabs` & `debugger`:** Used to open discovered VAT invoice URLs in temporary background tabs and invoke Chrome's native `Page.printToPDF` command to save them as PDF files.
* **`downloads`:** Used to save the bundled ZIP file of VAT invoices to your computer.
* **`storage`:** Used to save your license status and download subfolder preference in your browser.
* **`host_permissions` (`*.airbnb.*` and `api.lemonsqueezy.com`):** Used to operate across international Airbnb country domains and validate your license key.

---

## 5. Data Sharing, Sale, and Retention

* We **do not** sell, rent, trade, or transfer any user data to third parties.
* We **do not** use user data for advertising, profiling, creditworthiness, or lending purposes.
* Locally stored settings and license keys remain in your browser's storage until you click "Deactivate" / "Remove saved key" or uninstall the Extension.

---

## 6. Changes to This Privacy Policy

We may update this Privacy Policy from time to time to reflect changes in legal requirements or Extension functionality. Any updates will be posted on this page with an updated revision date.

---

## 7. Contact Us

If you have any questions about this Privacy Policy or the Extension's data practices, please contact us through our billing/support portal at `https://bnbvatdownload.lemonsqueezy.com/billing` or via the support email listed on our extension store page.

