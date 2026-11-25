# LioX Web Translation Engine with Microsoft Azure Translator for TranslatePress

A Microsoft Azure Translator integration for TranslatePress by LioX Web.

This plugin adds Microsoft Azure Translator as an automatic translation engine for TranslatePress.

## Features

- Microsoft Azure Translator integration
- API Key, Region and Endpoint configuration
- Multiple target language support
- Compatible with existing TranslatePress translations
- Existing translations are not overwritten
- Automatically translates new untranslated strings
- Batch translation support
- API credential testing
- Configurable monthly character limit
- Monthly usage tracking
- Automatic monthly usage counter reset

## Requirements

- WordPress
- TranslatePress
- Microsoft Azure Translator resource

**Tested up to:** WordPress 7.2 (tested on 7.2 RC3 with TranslatePress 3.4.1).

## Installation

1. Download the plugin ZIP.
2. In WordPress, go to **Plugins → Add New → Upload Plugin**.
3. Upload the ZIP file.
4. Activate the plugin.
5. Go to **Settings → TranslatePress → Automatic Translation**.
6. Select **Microsoft Azure Translator (LioX Web)** as the translation engine.
7. Enter your Azure API Key, Azure Region and Azure Endpoint.
8. Save the settings.

## Monthly Character Limit

The plugin includes a configurable monthly safety limit for Azure translation requests.

The default value is **1,900,000 characters per calendar month**.

Set the value to **0** to disable the plugin-level monthly limit.

The plugin displays:

- Characters used during the current month
- Monthly limit
- Remaining characters

The counter resets automatically when a new calendar month begins.

## Existing Translations

Existing translations stored by TranslatePress are not overwritten.

The Azure translation engine is used only when TranslatePress requests translation for strings that do not already have a stored translation.

This allows existing translations created with another translation engine to remain unchanged while Azure Translator handles new untranslated content.

## Azure Free Account

After the 30-day trial or when you use your trial credit, upgrade your Azure subscription to pay-as-you-go to keep using Azure. Your Translator resource can stay on the F0 (Free) tier where available. See [Azure free account information](https://azure.microsoft.com/en-us/pricing/purchase-options/azure-account/) and [Translator pricing](https://azure.microsoft.com/en-us/pricing/details/translator/).

## External Service

This plugin connects to the Microsoft Azure Translator API.

Text submitted for automatic translation is sent to Microsoft Azure Translator when the site administrator enables the Azure translation engine.

A Microsoft Azure account and Translator resource are required.

Microsoft Azure Terms:
https://azure.microsoft.com/support/legal/

Microsoft Privacy Statement:
https://privacy.microsoft.com/privacystatement

## Security

Never publish your Microsoft Azure API Key in a public repository.

API credentials are stored through the WordPress and TranslatePress settings and are not included in the plugin source code.

If an API key is accidentally exposed, regenerate it immediately from the Microsoft Azure portal.

## Repository

https://github.com/lioxweb/liox-web-translation-engine-for-translatepress

## Changelog

### 1.1.5

- Keep tracking Azure character usage when the monthly hard limit is disabled.
- Accept whole-number hard limits in the settings and stop further batches after Azure errors.
- Handle invalid translation and credential-test responses without exposing API keys in diagnostics.
- Prevent requests carrying Azure credentials from following HTTP redirects.

## License

GPL-2.0-or-later

## Author

**LioX Web**

https://lioxweb.com/
