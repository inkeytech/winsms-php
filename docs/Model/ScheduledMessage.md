# ScheduledMessage

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**apiMessageId** | **int** | The WinSMS API Message Id identifying the SMS message. | 
**mobileNumber** | **string** | The mobile number of the recipient of the SMS message, using the international E164 (without the plus) format | 
**submitTime** | **int** | The date and time the message was originally submitted for scheduled delivery, in the format YYYYMMDDHHmm. | 
**scheduledSendTime** | **int** | The date and time the message is scheduled to be delivered to the recipient, in the format YYYYMMDDHHmm. | 
**creditCost** | **double** | The number of credits deducted from your account for the SMS to this recipient.  This is the number of credits that will be refunded if you delete this scheduled message. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


