# winsms\ShortcodeApi

All URIs are relative to *https://www.winsms.co.za/api/rest/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getShortCodeMessages**](ShortcodeApi.md#getShortCodeMessages) | **GET** /shortcode/incoming | Get a list of incoming short/long code messages


# **getShortCodeMessages**
> \winsms\Models\ShortcodeMessageResponse getShortCodeMessages($offset, $limit)

Get a list of incoming short/long code messages

***Only available to users with a [WinSMS Short/Long Code](https://support.winsms.co.za/winsms-long-short-code-system/).*** Get a list of all incoming short/long code messages received by the account.  Only the first 100 incoming short/long code messages will be returned if no ***offset*** and ***limit*** parameters are specified.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: APIKeyHeader
$config = winsms\Configuration::getDefaultConfiguration()->setApiKey('AUTHORIZATION', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = winsms\Configuration::getDefaultConfiguration()->setApiKeyPrefix('AUTHORIZATION', 'Bearer');

$apiInstance = new winsms\Api\ShortcodeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$offset = 0; // int | ***Optional*** - The number of items to skip before starting to return results. Default 0. Minimum 0.
$limit = 100; // int | ***Optional*** - The number of items to return. Default 100. Minimum 1. Maximum 1000.

try {
    $result = $apiInstance->getShortCodeMessages($offset, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShortcodeApi->getShortCodeMessages: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **offset** | **int**| ***Optional*** - The number of items to skip before starting to return results. Default 0. Minimum 0. | [optional] [default to 0]
 **limit** | **int**| ***Optional*** - The number of items to return. Default 100. Minimum 1. Maximum 1000. | [optional] [default to 100]

### Return type

[**\winsms\Models\ShortcodeMessageResponse**](../Model/ShortcodeMessageResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

