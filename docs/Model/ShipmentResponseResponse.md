# # ShipmentResponseResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**responseStatus** | [**\OpenAPIClientUPSShipping\Model\ResponseResponseStatus**](ResponseResponseStatus.md) |  |
**alert** | [**\OpenAPIClientUPSShipping\Model\ResponseAlert[]**](ResponseAlert.md) | Alert Container.  There can be zero to many alert containers with code and description.  **NOTE:** For versions &gt;&#x3D; v2403, this element will always be returned as an array. For requests using versions &lt; v2403, this element will be returned as an array if there is more than one object and a single object if there is only 1. | [optional]
**transactionReference** | [**\OpenAPIClientUPSShipping\Model\ResponseTransactionReference**](ResponseTransactionReference.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
