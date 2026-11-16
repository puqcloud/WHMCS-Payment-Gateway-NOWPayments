# Changelog

### NOWPayments Payment Gateway module **[WHMCS](https://puqcloud.com/link.php?id=77)**
#####  [Order now](https://puqcloud.com/whmcs-payment-gateways.php) | [Download](https://download.puqcloud.com/WHMCS/gateways/PUQ_WHMCS_PG-nowpayments/) | [Community](https://community.puqcloud.com/)

## v4.0.0 — 2026-11-16

- **PUQ Series 4 Architecture Upgrade:** Refactored module structure to full PUQ v4 standards.
- **Embedded Licensing System:** License class is embedded directly into the primary gateway file, removing external dependency files. Non-blocking license check maintains warning-only status in WHMCS admin.
- **Modern Guzzle HTTP Client:** Migrated all API calls to `GuzzleHttp\Client` with strict timeouts, error handling, and masked logging in WHMCS Module Log.
- **Searchable Select2 Currency Selector:** Integrated Select2 with coin logos, instant keyboard search, smart default cryptocurrency selection, and real-time rate updates for over 200 cryptocurrencies.
- **Comprehensive 27-Language Internationalization (i18n):** Complete translation dictionary for 27 languages supported by WHMCS, including invoice selectors, advisories, error templates, and admin alerts with typographic apostrophe safety.
- **Minimum Invoice Amount & Micro-Payment Handling:** Resolved micro-invoice rendering issues under $7–$8 with real-time coin minimum advisories, low-fee cryptocurrency recommendations (LTC, TRX, DOGE, USDT-TRC20), and open hosted checkout fallback without a locked currency.
- **Configurable Payment Flow:** Added choice between "Embedded Currency Selector" and "Direct Hosted Checkout".
- **Configurable Minimum Invoice Amount & Blocking Mode:** Added admin settings to display an advisory or strictly block payment processing for invoices below the micro-payment threshold.
- **Atomic IPN Concurrency Lock & Fee Conversion:** Added exclusive transaction locking (`flock`) in the IPN webhook handler to prevent duplicate credits from concurrent webhook deliveries, along with automatic conversion of cryptocurrency network/service fees into the client's WHMCS currency.
- **WHMCS Gateway Log & Module Log Integration:** Full transaction audit trail with masked API keys and HMAC verification details.
- **Directory Protection:** Added directory index protection across all subdirectories.
- **Full PHP 7.4 - 8.4 Support:** Universal ionCube 15 compatibility across PHP 7.4, 8.1, 8.2, 8.3, and 8.4 for WHMCS 8.x/9.x.

---

## v1.1 — 2025-10-22

- Option in module settings to show or hide currency codes in the dropdown list.
- Ability to enable a feature where the buyer pays the commission (`is_fee_paid_by_user`).
- Currency icons added in the client area during currency selection.
- Option to sort currencies in the dropdown list (Ascending, Descending, None).

---

## v1.0 — 2025-09-22

- First official release of the PUQ NOWPayments gateway module for WHMCS.
- Support for production and sandbox environments.
- Real-time IPN webhook callbacks with HMAC-SHA512 verification.
- Dynamic currency selector on the invoice view screen.
