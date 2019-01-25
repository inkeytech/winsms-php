# winsms\CreditsApi

All URIs are relative to *https://www.winsms.co.za/api/rest/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getCreditBalance**](CreditsApi.md#getCreditBalance) | **GET** /credits/balance | Get your current WinSMS credit balance
[**transferCredits**](CreditsApi.md#transferCredits) | **POST** /credits/transfer | Transfer credits between main and sub accounts.


# **getCreditBalance**
> \winsms\Models\CreditBalanceResponse getCreditBalance()

Get your current WinSMS credit balance

Get the current remaining credit balance for the account.  ***Note*** - The credit balance is expressed as a value with a single decimal place.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: APIKeyHeader
$config = winsms\Configuration::getDefaultConfiguration()->setApiKey('AUTHORIZATION', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = winsms\Configuration::getDefaultConfiguration()->setApiKeyPrefix('AUTHORIZATION', 'Bearer');

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

### Parameters
This endpoint does not need any parameter.

### Return type

[**\winsms\Models\CreditBalanceResponse**](../Model/CreditBalanceResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **transferCredits**
> \winsms\Models\CreditTransferResponse transferCredits($creditTransferDetails)

Transfer credits between main and sub accounts.

Transfer credits between accounts. - From Main account to Sub account.  - From Sub account to Main account.  - From Sub account to another Sub account.  Your WinSMS account number and sub account number/s can be obtained by logging in to the WinSMS Client Zone (www.winsms.co.za/cz) with the main account's credentials.  The main account number is on the home tab and the sub account numbers are under the sub accounts tab.  Account numbers should be submitted as integers. Do not add the 'W' prefix.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: APIKeyHeader
$config = winsms\Configuration::getDefaultConfiguration()->setApiKey('AUTHORIZATION', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = winsms\Configuration::getDefaultConfiguration()->setApiKeyPrefix('AUTHORIZATION', 'Bearer');

$apiInstance = new winsms\Api\CreditsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$creditTransferDetails = new \winsms\Models\CreditTransferDetails(); // \winsms\Models\CreditTransferDetails | The details of the credit transfer. Sender account number, recipient account number, and number of credits to transfer.

try {
    $result = $apiInstance->transferCredits($creditTransferDetails);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreditsApi->transferCredits: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **creditTransferDetails** | [**\winsms\Models\CreditTransferDetails**](../Model/CreditTransferDetails.md)| The details of the credit transfer. Sender account number, recipient account number, and number of credits to transfer. |

### Return type

[**\winsms\Models\CreditTransferResponse**](../Model/CreditTransferResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

