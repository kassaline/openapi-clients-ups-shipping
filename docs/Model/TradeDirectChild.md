# # TradeDirectChild

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uSI** | **string** | The unique shipment identifier (USI) is used to create Master, LTL and Child shipments. Used for Freight shipments. |
**hazMatIndicator** | **string** | Indicates the Presence/Absence of HazMat on the shipment. | [optional]
**type** | **string** | The type of shipment.   Valid values:   - LTL  - SMALLPACKAGE |
**product** | [**\OpenAPIClientUPSShipping\Model\ChildProduct**](ChildProduct.md) |  |
**ltlPackage** | [**\OpenAPIClientUPSShipping\Model\ChildLTLPackage**](ChildLTLPackage.md) |  |
**ltlCharges** | [**\OpenAPIClientUPSShipping\Model\ChildLTLCharges**](ChildLTLCharges.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
