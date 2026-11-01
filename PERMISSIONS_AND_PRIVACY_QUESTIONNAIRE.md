# Permissions & Privacy Practices Questionnaire

Use these exact responses when filling out the **Privacy Practices** tab in the Chrome Web Store Developer Dashboard and the **Submission Options / Notes for Certification** in Microsoft Edge Partner Center.

---

## 1. Single Purpose Description
> **Question:** *An extension must have a single purpose that is narrow and easy-to-understand. Describe your extension's single purpose.*

```text
This extension has a single purpose: to automatically locate, convert to PDF, and bulk-download host VAT invoices from the user's Airbnb Host Reservations page into a local ZIP archive.
```

---

## 2. Permission Justifications

### `debugger`
```text
Required solely to invoke the Chrome DevTools Protocol command "Page.printToPDF" on background tabs displaying the user's Airbnb VAT invoice HTML page. Chrome's standard extensions API does not provide a non-debugger method for service workers to programmatically render a tab to a PDF binary buffer for inclusion in a ZIP archive. The debugger is attached momentarily only during PDF generation and detached immediately afterward.
```

### `downloads`
```text
Required to save the generated ZIP archive containing the user's VAT invoice PDFs to the user's local Downloads folder (or user-configured subfolder) via chrome.downloads.download.
```

### `scripting`
```text
Required to dynamically execute the content script (content.js) on the active Airbnb Hosting Reservations tab when the user clicks "Download Invoices", ensuring reliable extraction even after Single-Page Application (SPA) navigation on Airbnb.
```

### `activeTab`
```text
Required to interact with the currently open Airbnb Host Reservations tab when the user explicitly initiates a bulk invoice download from the extension popup.
```

### `tabs`
```text
Required to query the active reservation tab, open each discovered VAT invoice URL in a temporary background tab for PDF rendering, and automatically close those temporary background tabs once the PDF buffer has been captured.
```

### `storage`
```text
Required to store the user's preferred download subfolder path, temporary download progress/log state across popup openings, and the user's Lemon Squeezy license activation key and cached validation metadata locally in the browser.
```

### `host_permissions` (`*://*.airbnb.*/*` and `https://api.lemonsqueezy.com/*`)
```text
Access to regional Airbnb domains (*://*.airbnb.com/*, .pt, .es, .fr, .it, .co.uk, .de, .ca, .com.au, .com.br, .co.in, .mx, .nl, .ch, .at, .be, .dk, .se, .no, .fi) is required so the content script and PDF generator can read reservation rows and render VAT invoice pages regardless of which regional Airbnb domain the host uses. Access to https://api.lemonsqueezy.com/* is required solely to activate, validate, and deactivate the user's subscription license key.
```

---

## 3. Remote Code Declaration
> **Question:** *Are you using remote code?*

* **Selection:** `No, I am not using remote code`
* **Explanation (if prompted):** All JavaScript logic (`background.js`, `content.js`, `popup.js`, `options.js`, `license.js`, and `jszip.min.js`) is bundled locally inside the extension package. The only external network request is a standard JSON/form POST request to `https://api.lemonsqueezy.com/v1/licenses/*` for license key verification.

---

## 4. Data Usage Disclosures (Chrome Web Store Checkboxes)

> **Question:** *What user data do you plan to collect from users now or in the future?*

Check **only** the following box:
- [x] **Authentication information** *(specifically: the user-entered Lemon Squeezy License Key and basic browser OS identifier used as the license instance name during activation with Lemon Squeezy)*

Leave **all other boxes unchecked**:
- [ ] Personally identifiable information *( Note: Lemon Squeezy returns the customer's own email/name associated with their license key to display in the extension popup, which is stored only in `chrome.storage.sync` on the user's browser and never sent to any third party )*
- [ ] Health information
- [ ] Financial and payment information *(Handled externally on Lemon Squeezy's checkout website; the extension never collects payment details, nor does it transmit Airbnb invoice data externally)*
- [ ] Personal communications
- [ ] Location
- [ ] Web history
- [ ] User activity
- [ ] Website content *(Airbnb reservation codes and VAT invoices are processed strictly locally in memory to create the user's local ZIP download and are never transmitted off the device)*

### Required Certification Checkboxes (Check All 3):
- [x] *I certify that myインパ/extension does not sell user data to third parties, outside of the approved use cases.*
- [x] *I certify that my extension does not use or transfer user data for purposes that are unrelated to my item's single purpose.*
- [x] *I certify that my extension does not use or transfer user data to determine creditworthiness or for lending purposes.*

