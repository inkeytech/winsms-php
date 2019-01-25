# DeleteScheduledResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timeStamp** | **string** | The date/time the request was processed, in the format YYYYMMDDhhmmssSSS | 
**version** | **string** | The current version of the API of the endpoint that was called | 
**statusCode** | **int** | The http status code returned - reflected in the body for convenience | 
**deletedMessageStatuses** | [**\winsms\Models\DeletedMessageStatus[]**](DeletedMessageStatus.md) | An array of ***deletedMessageStatus*** objects detailing the deleted status of each message requested for deletion. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


