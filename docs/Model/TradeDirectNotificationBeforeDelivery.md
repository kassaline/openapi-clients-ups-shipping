# # TradeDirectNotificationBeforeDelivery

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**requestType** | **string** | The type of notification request.  Valid values are:  - 001 &#x3D; QV Ship Notification - 002 &#x3D; QV Delivery Notification - 003 &#x3D; QV Exception Notification | [optional]
**mediaTypeCode** | **string** | The media type code for the notification.  Valid values are:  - 03 &#x3D; Email - 04 &#x3D; Fax | [optional]
**language** | **string** | The language for the notification. | [optional]
**dialect** | **string** | The dialect for the notification. | [optional]
**shipFromCompanyName** | **string** | The name of the company for the ship from address. | [optional]
**companyName** | **string** | The name of the company for the notification. | [optional]
**phone** | [**\OpenAPIClientUPSShipping\Model\TradeDirectPhone**](TradeDirectPhone.md) |  | [optional]
**subjectLine** | **string** | Subject line for the notification. | [optional]
**memo** | **string** | Memo for the notification. | [optional]
**name** | **string** | The name of the contact person for the notification. | [optional]
**eMailAddress** | **string** | Email address to send notification to. |
**alternateEmailAddress** | **string** | Alternate email address for the notification. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
