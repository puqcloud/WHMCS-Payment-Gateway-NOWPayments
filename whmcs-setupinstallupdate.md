# WHMCS setup(install/update)

### NOWPayments Payment Gateway **[WHMCS](https://puqcloud.com/link.php?id=77)** 

#####  [Order now](https://puqcloud.com/index.php?rp=/store/whmcs-module-nowpayments-payment-gateway) | [Download](https://download.puqcloud.com/WHMCS/gateways/PUQ_WHMCS_PG-nowpayments/) | [FAQ](https://faq.puqcloud.com/)

<p class="callout info">**Module is coded in PHP with ionCube protection**</p>

Supported php version:

- php 7.4 WHMCS 8.0 +
- php 8.1 WHMCS 8.0 +
- php 8.2 WHMCS 8.0 +

<p class="callout info">To install and update a module, you must perform one and the same action.</p>

<span style="font-size: 1.4em; font-weight: 400;">1. Download the latest version of the module.</span>

PHP 8.2

```
wget https://download.puqcloud.com/WHMCS/gateways/PUQ_WHMCS_PG-nowpayments/php82/PUQ_WHMCS_PG-nowpayments-latest.zip
```

PHP 8.1

```Powershell
wget https://download.puqcloud.com/WHMCS/gateways/PUQ_WHMCS_PG-nowpayments/php81/PUQ_WHMCS_PG-nowpayments-latest.zip
```

PHP 7.4

```Powershell
wget https://download.puqcloud.com/WHMCS/gateways/PUQ_WHMCS_PG-nowpayments/php74/PUQ_WHMCS_PG-nowpayments-latest.zip
```

<p class="callout info">All versions are available via link: [https://download.puqcloud.com/WHMCS/gateways/PUQ\_WHMCS\_PG-nowpayments/](https://download.puqcloud.com/WHMCS/gateways/PUQ_WHMCS_PG-nowpayments/)</p>

##### 2. Unzip the archive with the module.

```Powershell
unzip PUQ_WHMCS_PG-nowpayments-latest.zip
```

##### 3. Copy and Replace "puq\_nowpayments" to "WHMCS\_WEB\_DIR/modules/gateways/"

```Powershell
cp -r puq_nowpayments/ /path/to/your/whmcs/modules/gateways/
```

##### 4. Copy callback file to "WHMCS\_WEB\_DIR/modules/gateways/callback/"

```Powershell
cp callback/puq_nowpayments.php /path/to/your/whmcs/modules/gateways/callback/
```

##### 5. Configure the module in WHMCS Admin Area

Navigate to **Setup → Payments → Payment Gateways** and find "NOWPayments" in the list.

Click **"Activate"** and configure the following settings:

- **License Key:** Enter your module license key
- **Mode of Operation:** Choose between Production or Sandbox
- **API Key (Production):** Your production API key from [NOWPayments](https://account.nowpayments.io/store-settings#keys?link_id=4222128310)
- **IPN Secret Key (Production):** Your production IPN secret from [NOWPayments](https://account.nowpayments.io/store-settings#notifications?link_id=4222128310)
- **API Key (Sandbox):** Your sandbox API key from [NOWPayments Sandbox](https://account-sandbox.nowpayments.io/store-settings#keys?link_id=4222128310)
- **IPN Secret Key (Sandbox):** Your sandbox IPN secret from [NOWPayments Sandbox](https://account-sandbox.nowpayments.io/store-settings#notifications?link_id=4222128310)

##### 6. Configure Webhook in NOWPayments Account

Copy the **IPN Callback URL** from the module configuration and paste it into your NOWPayments account webhook settings:

- **Production:** [https://account.nowpayments.io/store-settings#notifications](https://account.nowpayments.io/store-settings#notifications?link_id=4222128310)
- **Sandbox:** [https://account-sandbox.nowpayments.io/store-settings#notifications](https://account-sandbox.nowpayments.io/store-settings#notifications?link_id=4222128310)

<p class="callout warning">7. Test the payment gateway</p>

Test the payment gateway in sandbox mode first to ensure everything is working correctly before switching to production mode.

<p class="callout info">Don't have a NOWPayments account yet? [Create your free account here](https://account.nowpayments.io/create-account?link_id=4222128310)</p>

<div id="bkmrk-"><div></div></div><div id="bkmrk--0"><div></div></div>