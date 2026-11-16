# WHMCS Installation and Update

### NOWPayments Payment Gateway module **[WHMCS](https://puqcloud.com/link.php?id=77)**
#####  [Order now](https://puqcloud.com/whmcs-payment-gateways.php) | [Download](https://download.puqcloud.com/WHMCS/gateways/PUQ_WHMCS_PG-nowpayments/) | [Community](https://community.puqcloud.com/)

## System requirements

| Requirement | Minimum |
|-------------|---------|
| **WHMCS** | 8.x+, 9.x+. |
| **PHP** | 7.4, 8.1, 8.2, 8.3, 8.4 |
| **ionCube Loader** | v15+ |

> **Note:** The module uses ionCube encoding. Make sure ionCube Loader is installed and active on your server.

## Installation

> **Note:** The module now uses **ionCube 15**, which provides universal out-of-the-box support for all encodings.
>
> All versions can be found at this link:
> `https://download.puqcloud.com/WHMCS/gateways/PUQ_WHMCS_PG-nowpayments/`
>
> Older module versions for WHMCS 8 are available in the archive directory:
> `https://download.puqcloud.com/WHMCS/gateways/PUQ_WHMCS_PG-nowpayments/archive/`

1. Download the latest version from the PUQ download page:
   ```bash
   wget https://download.puqcloud.com/WHMCS/gateways/PUQ_WHMCS_PG-nowpayments/PUQ_WHMCS_PG-nowpayments-latest.zip
   ```

2. Unzip the archive:
   ```bash
   unzip PUQ_WHMCS_PG-nowpayments-latest.zip
   ```

3. Upload the module files to your WHMCS installation:
   Copy the extracted gateway files from the `puq_nowpayments/` archive folder into your WHMCS `modules/gateways/` directory:
   ```bash
   # Copy main gateway file, asset folder, and IPN webhook callback
   cp -f puq_nowpayments/puq_nowpayments.php /path/to/whmcs/modules/gateways/
   cp -rf puq_nowpayments/puq_nowpayments /path/to/whmcs/modules/gateways/
   cp -rf puq_nowpayments/callback /path/to/whmcs/modules/gateways/
   ```

4. Ensure proper ownership and file permissions for your web server user (e.g. `www-data`):
   ```bash
   chown -R www-data:www-data /path/to/whmcs/modules/gateways/puq_nowpayments*
   chown -R www-data:www-data /path/to/whmcs/modules/gateways/callback/
   ```

5. The module files are now in place. Proceed to the gateway configuration chapter.

## Update

The update procedure is the same as installation — replace the existing files with the new version:

1. Download the latest version as described in the Installation section.
2. Unzip the archive.
3. For gateway modules, simply overwrite the existing files. No deactivation is needed:
   ```bash
   cp -f puq_nowpayments/puq_nowpayments.php /path/to/whmcs/modules/gateways/
   cp -rf puq_nowpayments/puq_nowpayments /path/to/whmcs/modules/gateways/
   cp -rf puq_nowpayments/callback /path/to/whmcs/modules/gateways/
   ```
4. Verify the version number in the module interface matches the new release.
