# NOWPayments Payment Gateway Configuration in WHMCS

### NOWPayments Payment Gateway **[WHMCS](https://puqcloud.com/link.php?id=77)** 

#####  [Order now](https://puqcloud.com/index.php?rp=/store/whmcs-module-nowpayments-payment-gateway) | [Download](https://download.puqcloud.com/WHMCS/gateways/PUQ_WHMCS_PG-nowpayments/) | [FAQ](https://faq.puqcloud.com/)

##### Configure Payment Gateway in WHMCS

```
Setup → Payment Gateways → NOWPayments
```

In the **Gateway settings** section, configure the following parameters for the **"PUQ NOWPayments"** module

[![image-1758534275052.png](https://doc.puq.info/uploads/images/gallery/2025-09/scaled-1680-/image-1758534275052.png)](https://doc.puq.info/uploads/images/gallery/2025-09/image-1758534275052.png)

- **Show on Order Form:** Check this box to display NOWPayments as a payment option during checkout. When enabled, customers will see NOWPayments in the list of available payment methods.
- **Display Name:** The name that will be shown to customers on the order form. Default is "NOWPayments" but can be customized to match your branding.
- **License Key:** A pre-purchased license key for the **"PUQ NOWPayments"** module. The module will verify this key and display the status (success/expiration date). The key must be active for the module to function correctly.
- **Mode of Operation:** Choose between "Production - live payments" or "Sandbox - test environment". In sandbox mode, all transactions are test transactions and no real money is processed. Always test in sandbox first before switching to production.
- **API Key (Production):** Your production API key from NOWPayments account. This key is used to authenticate API requests in the live environment. You can find it in your [NOWPayments production account settings](https://account.nowpayments.io/store-settings#keys?link_id=4222128310).
- **IPN Secret Key (Production):** Secret key for securing Instant Payment Notifications (IPN) callbacks in production. This key is used to verify that webhook notifications are coming from NOWPayments. Configure this in your [NOWPayments production notifications settings](https://account.nowpayments.io/store-settings#notifications?link_id=4222128310).
- **API Key (Sandbox):** Your sandbox API key for testing purposes. This key is used for test transactions in the sandbox environment. Obtain it from your [NOWPayments sandbox account settings](https://account-sandbox.nowpayments.io/store-settings#keys?link_id=4222128310).
- **IPN Secret Key (Sandbox):** Secret key for sandbox IPN callbacks. This ensures secure webhook notifications during testing. Configure this in your [NOWPayments sandbox notifications settings](https://account-sandbox.nowpayments.io/store-settings#notifications?link_id=4222128310).
- **IPN Callback URL:** This URL is automatically generated and shows where NOWPayments will send payment status notifications. Copy this URL and paste it into your NOWPayments account webhook settings. The format is: `https://yourdomain.com/modules/gateways/callback/puq_nowpayments.php`
- **Module Version:** Displays the current version of the installed NOWPayments module (e.g., "1.0"). This field is read-only and helps with troubleshooting and support.
- **Convert To For Processing:** Select the currency that incoming payments will be converted to for processing. This is typically your primary business currency (e.g., USD, EUR). The module will automatically convert cryptocurrency payments to this currency using current exchange rates.

#####  

##### Payment Flow Configuration  
  
  


The module automatically handles the following payment flow:

1. **Customer Selection:** Customer selects NOWPayments as payment method during checkout
2. **Currency Selection:** Customer chooses from 200+ supported cryptocurrencies
3. **Rate Calculation:** Module fetches real-time exchange rates from NOWPayments API
4. **Payment Creation:** Creates payment invoice in NOWPayments system
5. **Payment Processing:** Customer completes payment using their chosen cryptocurrency
6. **Webhook Notification:** NOWPayments sends payment status via secure webhook
7. **Invoice Update:** WHMCS automatically marks invoice as paid upon successful payment

<p class="callout warning">Important Notes:</p>

- Always test the payment gateway in sandbox mode before going live
- Ensure the IPN Callback URL is correctly configured in your NOWPayments account
- The webhook URL must be accessible from the internet for NOWPayments to send notifications
- Keep your API keys and IPN secret keys secure and never share them publicly
- Monitor the WHMCS gateway logs for any payment processing issues

<div id="bkmrk--0"><div></div></div>