# ShortcodeMessageResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timeStamp** | **string** | The date/time the request was processed, in the format YYYYMMDDhhmmssSSS | 
**version** | **string** | The current version of the API of the endpoint that was called | 
**statusCode** | **int** | The http status code returned - reflected in the body for convenience | 
**resultsOffset** | **int** | The number of items skipped before the results were returned. This is the value specified in the ***offset*** parameter sent to the endpoint. If the parameter was not specified, this defaults to 0. | 
**resultsLimit** | **int** | The number of items returned in the results. This is the value specified in the ***limit*** parameter sent to the endpoint. If the parameter was not specified, this defaults to 100. | 
**resultsTotalAvailable** | **int** | The total number of results available for retrieval. The ***offset*** and ***limit*** properties specify which of the total available results have been returned. | 
**shortcodeMessages** | [**\winsms\Models\ShortcodeMessage[]**](ShortcodeMessage.md) | An array of ***shortcodeMessage*** objects containing properties of each incoming shortcode message received by WinSMS. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


