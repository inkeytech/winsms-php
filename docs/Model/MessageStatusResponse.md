# MessageStatusResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timeStamp** | **string** | The date/time the request was processed, in the format YYYYMMDDhhmmssSSS | 
**version** | **string** | The current version of the API of the endpoint that was called | 
**statusCode** | **int** | The http status code returned - reflected in the body for convenience | 
**messageStatuses** | [**\winsms\Models\MessageStatus[]**](MessageStatus.md) | An array of ***messageStatus*** objects detailing the delivery status of each message | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


