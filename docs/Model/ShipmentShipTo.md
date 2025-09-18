# # ShipmentShipTo

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Consignee&#39;s company name.  All other accounts must be either a daily pickup account or an occasional account. |
**attentionName** | **string** | Contact name at the consignee&#39;s location.  Required for: UPS Next Day Air® Early service, and when ShipTo country or territory is different than ShipFrom country or territory.  Required if Invoice International form is requested. | [optional]
**companyDisplayableName** | **string** | Not applicable for ShipTo | [optional]
**taxIdentificationNumber** | **string** | Consignee&#39;s tax identification number. This element has been deprecated, replacement can be found in the GlobalTaxInformation container. | [optional]
**phone** | [**\OpenAPIClientUPSShipping\Model\ShipToPhone**](ShipToPhone.md) |  | [optional]
**faxNumber** | **string** | Consignee&#39;s fax number.  If ShipTo country or territory is US 10 digits allowed, otherwise 1-15 digits allowed. | [optional]
**eMailAddress** | **string** | Consignee&#39;s email address. | [optional]
**address** | [**\OpenAPIClientUPSShipping\Model\ShipToAddress**](ShipToAddress.md) |  |
**locationID** | **string** | Location ID is a unique identifier referring to a specific shipping/receiving location.  Location ID must be alphanumeric characters. All letters must be capitalized. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
