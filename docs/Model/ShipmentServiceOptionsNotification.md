# # ShipmentServiceOptionsNotification

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**notificationCode** | **string** | The type of notification requested.  Note: - QVN Exception notification and return notification are not applicable to GFP. - QV In-transit and Return Notifications are only valid for ImportControl and Return shipment. - QV In-transit Notification is allowed for return shipments only. - QV Ship Notification is allowed for forward moving shipments only.  Valid values: - 5 - QV In-transit Notification - 6 - QV Ship Notification - 7 - QV Exception Notification - 8 - QV Delivery Notification - 2 - Return Notification or Label Creation Notification - 012 - Alternate Delivery Location Notification - 013 - UAP Shipper Notification. |
**eMail** | [**\OpenAPIClientUPSShipping\Model\NotificationEMail**](NotificationEMail.md) |  |
**voiceMessage** | [**\OpenAPIClientUPSShipping\Model\NotificationVoiceMessage**](NotificationVoiceMessage.md) |  | [optional]
**textMessage** | [**\OpenAPIClientUPSShipping\Model\NotificationTextMessage**](NotificationTextMessage.md) |  | [optional]
**locale** | [**\OpenAPIClientUPSShipping\Model\NotificationLocale**](NotificationLocale.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
