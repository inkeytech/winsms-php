# winsms\SmsApi

All URIs are relative to *https://www.winsms.co.za/api/rest/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteScheduledMessages**](SmsApi.md#deleteScheduledMessages) | **POST** /sms/scheduled/delete | Delete scheduled SMS messages and refund credits
[**getIncomingMessages**](SmsApi.md#getIncomingMessages) | **GET** /sms/incoming | Get a list of incoming SMS messages
[**getOptoutMessages**](SmsApi.md#getOptoutMessages) | **GET** /sms/incoming/optout | Get a list of incoming opt-out SMS messages
[**getScheduledMessages**](SmsApi.md#getScheduledMessages) | **GET** /sms/scheduled | Get a list of scheduled SMS messages
[**smsSend**](SmsApi.md#smsSend) | **POST** /sms/outgoing/send | Send SMS messages
[**smsStatus**](SmsApi.md#smsStatus) | **POST** /sms/outgoing/status | Get SMS delivery statuses


# **deleteScheduledMessages**
> \winsms\Models\DeleteScheduledResponse deleteScheduledMessages($messageDeleteRequest)

Delete scheduled SMS messages and refund credits

Delete a list of previously scheduled SMS messages that have not yet been sent.  Credits originally deducted for each SMS message will be refunded to your account upon successful deletion.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: APIKeyHeader
$config = winsms\Configuration::getDefaultConfiguration()->setApiKey('AUTHORIZATION', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = winsms\Configuration::getDefaultConfiguration()->setApiKeyPrefix('AUTHORIZATION', 'Bearer');

$apiInstance = new winsms\Api\SmsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$messageDeleteRequest = array(new \winsms\Models\int[]()); // int[] | An array of WinSMS API Ids received after submitting scheduled messages to the ***_/sms/outgoing/send*** endpoint.<br> A maximum of 1000 API Ids can be supplied in a single request.

try {
    $result = $apiInstance->deleteScheduledMessages($messageDeleteRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsApi->deleteScheduledMessages: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **messageDeleteRequest** | **int[]**| An array of WinSMS API Ids received after submitting scheduled messages to the ***_/sms/outgoing/send*** endpoint.&lt;br&gt; A maximum of 1000 API Ids can be supplied in a single request. |

### Return type

[**\winsms\Models\DeleteScheduledResponse**](../Model/DeleteScheduledResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getIncomingMessages**
> \winsms\Models\IncomingMessageResponse getIncomingMessages($offset, $limit)

Get a list of incoming SMS messages

Get a list of all incoming SMS messages received by the account.  Only the first 100 incoming messages will be returned if no ***offset*** and ***limit*** parameters are specified.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: APIKeyHeader
$config = winsms\Configuration::getDefaultConfiguration()->setApiKey('AUTHORIZATION', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = winsms\Configuration::getDefaultConfiguration()->setApiKeyPrefix('AUTHORIZATION', 'Bearer');

$apiInstance = new winsms\Api\SmsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$offset = 0; // int | ***Optional*** - The number of items to skip before starting to return results. Default 0. Minimum 0.
$limit = 100; // int | ***Optional*** - The number of items to return. Default 100. Minimum 1. Maximum 1000.

try {
    $result = $apiInstance->getIncomingMessages($offset, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsApi->getIncomingMessages: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **offset** | **int**| ***Optional*** - The number of items to skip before starting to return results. Default 0. Minimum 0. | [optional] [default to 0]
 **limit** | **int**| ***Optional*** - The number of items to return. Default 100. Minimum 1. Maximum 1000. | [optional] [default to 100]

### Return type

[**\winsms\Models\IncomingMessageResponse**](../Model/IncomingMessageResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getOptoutMessages**
> \winsms\Models\OptoutMessageResponse getOptoutMessages()

Get a list of incoming opt-out SMS messages

Get a list of all opt-out SMS messages received by the account, as well as all manually added opt-out numbers.<br>

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: APIKeyHeader
$config = winsms\Configuration::getDefaultConfiguration()->setApiKey('AUTHORIZATION', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = winsms\Configuration::getDefaultConfiguration()->setApiKeyPrefix('AUTHORIZATION', 'Bearer');

$apiInstance = new winsms\Api\SmsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getOptoutMessages();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsApi->getOptoutMessages: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\winsms\Models\OptoutMessageResponse**](../Model/OptoutMessageResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getScheduledMessages**
> \winsms\Models\ScheduledMessageResponse getScheduledMessages($offset, $limit)

Get a list of scheduled SMS messages

Get a list of all scheduled SMS messages that have not yet been sent.  Only the first 100 scheduled messages will be returned if no ***offset*** and ***limit*** parameters are specified.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: APIKeyHeader
$config = winsms\Configuration::getDefaultConfiguration()->setApiKey('AUTHORIZATION', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = winsms\Configuration::getDefaultConfiguration()->setApiKeyPrefix('AUTHORIZATION', 'Bearer');

$apiInstance = new winsms\Api\SmsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$offset = 0; // int | ***Optional*** - The number of items to skip before starting to return results. Default 0. Minimum 0.
$limit = 100; // int | ***Optional*** - The number of items to return. Default 100. Minimum 1. Maximum 1000.

try {
    $result = $apiInstance->getScheduledMessages($offset, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsApi->getScheduledMessages: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **offset** | **int**| ***Optional*** - The number of items to skip before starting to return results. Default 0. Minimum 0. | [optional] [default to 0]
 **limit** | **int**| ***Optional*** - The number of items to return. Default 100. Minimum 1. Maximum 1000. | [optional] [default to 100]

### Return type

[**\winsms\Models\ScheduledMessageResponse**](../Model/ScheduledMessageResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **smsSend**
> \winsms\Models\NewMessageResponse smsSend($newMessageDetails)

Send SMS messages

Submit 1 or more SMS messages to be sent by WinSMS. Maximum 1000 recipients per request.  The SMS message text can be a maximum of 918 characters long. If you are submitting a message longer than 160 characters, you should change the value of ***maxSegments***.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: APIKeyHeader
$config = winsms\Configuration::getDefaultConfiguration()->setApiKey('AUTHORIZATION', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = winsms\Configuration::getDefaultConfiguration()->setApiKeyPrefix('AUTHORIZATION', 'Bearer');

$apiInstance = new winsms\Api\SmsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$newMessageDetails = new \winsms\Models\NewMessageDetails(); // \winsms\Models\NewMessageDetails | The message, recipients and delivery options of an SMS message to be sent.

try {
    $result = $apiInstance->smsSend($newMessageDetails);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsApi->smsSend: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **newMessageDetails** | [**\winsms\Models\NewMessageDetails**](../Model/NewMessageDetails.md)| The message, recipients and delivery options of an SMS message to be sent. |

### Return type

[**\winsms\Models\NewMessageResponse**](../Model/NewMessageResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **smsStatus**
> \winsms\Models\MessageStatusResponse smsStatus($messageStatusRequest)

Get SMS delivery statuses

Get a list of previously submitted SMS message delivery statuses.  Post an array of API Message Ids received from the ***_/sms/outgoing/send*** endpoint.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: APIKeyHeader
$config = winsms\Configuration::getDefaultConfiguration()->setApiKey('AUTHORIZATION', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = winsms\Configuration::getDefaultConfiguration()->setApiKeyPrefix('AUTHORIZATION', 'Bearer');

$apiInstance = new winsms\Api\SmsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$messageStatusRequest = array(new \winsms\Models\int[]()); // int[] | An array of WinSMS API Ids received after submitting messages to the ***_/sms/outgoing/send*** endpoint.  A maximum of 1000 API Ids can be supplied in a single request.

try {
    $result = $apiInstance->smsStatus($messageStatusRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsApi->smsStatus: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **messageStatusRequest** | **int[]**| An array of WinSMS API Ids received after submitting messages to the ***_/sms/outgoing/send*** endpoint.  A maximum of 1000 API Ids can be supplied in a single request. |

### Return type

[**\winsms\Models\MessageStatusResponse**](../Model/MessageStatusResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

