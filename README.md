# Store Submission Kit — Bulk VAT Invoice Downloader for Airbnb Hosts (v1.0)

This folder contains every package, document, privacy disclosure, and graphic asset required to publish **Bulk VAT Invoice Downloader for Airbnb Hosts** to the **Chrome Web Store**, **Microsoft Edge Add-ons**, and **Opera Add-ons**.

---

## Folder Contents

### 1. Extension Upload Package
* [`airbnb-vat-invoice-downloader-v1.0.zip`](./airbnb-vat-invoice-downloader-v1.0.zip) — Clean, production-ready Manifest V3 archive with `manifest.json` at the root and forward-slash relative paths. Upload this exact `.zip` file to Chrome Web Store, Edge Add-ons, and Opera Add-ons.

### 2. Copy-Paste Store Listing & Compliance Docs
* [`STORE_LISTING.md`](./STORE_LISTING.md) — Title options, Short Summary (≤132 chars), Detailed Description, Category, Language, and official URLs.
* [`PERMISSIONS_AND_PRIVACY_QUESTIONNAIRE.md`](./PERMISSIONS_AND_PRIVACY_QUESTIONNAIRE.md) — Exact copy-paste answers for the Single Purpose declaration, Remote Code question, Data Usage checkboxes, and individual justifications for `debugger`, `downloads`, `scripting`, `activeTab`, `tabs`, `storage`, and `host_permissions`.
* [`PRIVACY_POLICY.html`](./PRIVACY_POLICY.html) & [`PRIVACY_POLICY.md`](./PRIVACY_POLICY.md) — Ready-to-host Privacy Policy in both standalone styled HTML and Markdown formats.
* [`REVIEWER_INSTRUCTIONS.md`](./REVIEWER_INSTRUCTIONS.md) — Template for the store certification team explaining how to activate a complimentary Lemon Squeezy test key and verify the extension.

### 3. Visual & Graphic Assets (`./assets/`)
| File | Dimensions | Format | Target Store Use |
| :--- | :--- | :--- | :--- |
| [`assets/icon-128x128.png`](./assets/icon-128x128.png) | `128 × 128 px` | PNG | Chrome Web Store & Opera Store Icon |
| [`assets/icon-300x300-edge.png`](./assets/icon-300x300-edge.png) | `300 × 300 px` | PNG | Microsoft Edge Add-ons Store Logo (Required by Edge) |
| [`assets/promo-small-440x280.png`](./assets/promo-small-440x280.png) | `440 × 280 px` | 24-bit PNG (no alpha) | Small Promotional Tile (Chrome & Edge) |
| [`assets/promo-marquee-1400x560.png`](./assets/promo-marquee-1400x560.png) | `1400 × 560 px` | 24-bit PNG (no alpha) | Marquee Promotional Tile (Chrome & Edge) |
| [`assets/screenshot-0-how-to-use-1280x800.png`](./assets/screenshot-0-how-to-use-1280x800.png) | `1280 × 800 px` | 24-bit PNG (no alpha) | **How-To-Use Instructions Guide** (`airbnb.com/hosting/completed`, Date Filters & Next Page Limiter) |
| [`assets/screenshot-1-bulk-download-1280x800.png`](./assets/screenshot-1-bulk-download-1280x800.png) | `1280 × 800 px` | 24-bit PNG (no alpha) | Store Screenshot #1: 1-Click Bulk Download on `airbnb.com/hosting/completed` |
| [`assets/screenshot-2-zip-archive-1280x800.png`](./assets/screenshot-2-zip-archive-1280x800.png) | `1280 × 800 px` | 24-bit PNG (no alpha) | Store Screenshot #2: Clean PDF Naming & Single ZIP Output |
| [`assets/screenshot-3-license-and-options-1280x800.png`](./assets/screenshot-3-license-and-options-1280x800.png) | `1280 × 800 px` | 24-bit PNG (no alpha) | Store Screenshot #3: 3-Day Free Trial, License & Pagination/Folder Options |

---

## Quick Submission Checklist

1. **Host Your Privacy Policy:** Upload [`PRIVACY_POLICY.html`](./PRIVACY_POLICY.html) to your website, GitHub Pages, or Notion and copy the public URL.
2. **Generate a Reviewer License Key:** Create a test license key (or 100% discount code) in your Lemon Squeezy dashboard and paste it into [`REVIEWER_INSTRUCTIONS.md`](./REVIEWER_INSTRUCTIONS.md).
3. **Upload to Chrome Web Store:**
   * Dashboard: https://chrome.google.com/webstore/devconsole
   * Click **New Item** → Upload `airbnb-vat-invoice-downloader-v1.0.zip`.
   * Fill in **Store Listing** from `STORE_LISTING.md` and upload the images from `assets/`.
   * Fill in **Privacy Practices** from `PERMISSIONS_AND_PRIVACY_QUESTIONNAIRE.md` and paste your Reviewer Instructions.
4. **Upload to Microsoft Edge Add-ons:**
   * Dashboard: https://partner.microsoft.com/dashboard/microsoftedge/overview
   * Click **Create new extension** → Upload `airbnb-vat-invoice-downloader-v1.0.zip`.
   * Upload `assets/icon-300x300-edge.png` along with the screenshots and promo tiles, and paste the certification notes from `REVIEWER_INSTRUCTIONS.md` and `PERMISSIONS_AND_PRIVACY_QUESTIONNAIRE.md`.

