# WinSMS - PHP Client

- API version: 1.0.0
- Package version: 1.0.0

For more information, please visit [http://support.winsms.co.za/](http://support.winsms.co.za/)

## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/winsms/winsms-php.git"
    }
  ]
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/winsms-php/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: APIKeyHeader
$config = winsms\Configuration::getDefaultConfiguration()->setApiKey('AUTHORIZATION', 'YOUR_API_KEY');

$apiInstance = new winsms\Api\CreditsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getCreditBalance();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreditsApi->getCreditBalance: ', $e->getMessage(), PHP_EOL;
}

?>
```

## Documentation for API Endpoints

All URIs are relative to *https://www.winsms.co.za/api/rest/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*CreditsApi* | [**getCreditBalance**](docs/Api/CreditsApi.md#getcreditbalance) | **GET** /credits/balance | Get your current WinSMS credit balance
*CreditsApi* | [**transferCredits**](docs/Api/CreditsApi.md#transfercredits) | **POST** /credits/transfer | Transfer credits between main and sub accounts.
*ShortcodeApi* | [**getShortCodeMessages**](docs/Api/ShortcodeApi.md#getshortcodemessages) | **GET** /shortcode/incoming | Get a list of incoming short/long code messages
*SmsApi* | [**deleteScheduledMessages**](docs/Api/SmsApi.md#deletescheduledmessages) | **POST** /sms/scheduled/delete | Delete scheduled SMS messages and refund credits
*SmsApi* | [**getIncomingMessages**](docs/Api/SmsApi.md#getincomingmessages) | **GET** /sms/incoming | Get a list of incoming SMS messages
*SmsApi* | [**getOptoutMessages**](docs/Api/SmsApi.md#getoptoutmessages) | **GET** /sms/incoming/optout | Get a list of incoming opt-out SMS messages
*SmsApi* | [**getScheduledMessages**](docs/Api/SmsApi.md#getscheduledmessages) | **GET** /sms/scheduled | Get a list of scheduled SMS messages
*SmsApi* | [**smsSend**](docs/Api/SmsApi.md#smssend) | **POST** /sms/outgoing/send | Send SMS messages
*SmsApi* | [**smsStatus**](docs/Api/SmsApi.md#smsstatus) | **POST** /sms/outgoing/status | Get SMS delivery statuses
*SubaccountsApi* | [**getSubAccounts**](docs/Api/SubaccountsApi.md#getsubaccounts) | **GET** /subaccounts | Get a list of all Sub Accounts.


## Documentation For Models

 - [CreditBalanceResponse](docs/Model/CreditBalanceResponse.md)
 - [CreditTransferDetails](docs/Model/CreditTransferDetails.md)
 - [CreditTransferResponse](docs/Model/CreditTransferResponse.md)
 - [DeleteScheduledResponse](docs/Model/DeleteScheduledResponse.md)
 - [DeletedMessageStatus](docs/Model/DeletedMessageStatus.md)
 - [ErrorDetails](docs/Model/ErrorDetails.md)
 - [IncomingMessage](docs/Model/IncomingMessage.md)
 - [IncomingMessageResponse](docs/Model/IncomingMessageResponse.md)
 - [IncomingOptoutMessage](docs/Model/IncomingOptoutMessage.md)
 - [MessageRecipientDetails](docs/Model/MessageRecipientDetails.md)
 - [MessageRecipientResponse](docs/Model/MessageRecipientResponse.md)
 - [MessageStatus](docs/Model/MessageStatus.md)
 - [MessageStatusResponse](docs/Model/MessageStatusResponse.md)
 - [NewMessageDetails](docs/Model/NewMessageDetails.md)
 - [NewMessageResponse](docs/Model/NewMessageResponse.md)
 - [OptoutMessageResponse](docs/Model/OptoutMessageResponse.md)
 - [ScheduledMessage](docs/Model/ScheduledMessage.md)
 - [ScheduledMessageResponse](docs/Model/ScheduledMessageResponse.md)
 - [ShortcodeMessage](docs/Model/ShortcodeMessage.md)
 - [ShortcodeMessageResponse](docs/Model/ShortcodeMessageResponse.md)
 - [SubAccount](docs/Model/SubAccount.md)
 - [SubAccountsResponse](docs/Model/SubAccountsResponse.md)


## Documentation For Authorization


## APIKeyHeader

- **Type**: API key
- **API key parameter name**: AUTHORIZATION
- **Location**: HTTP header


## Author

support@winsms.co.za


