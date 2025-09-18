# # ShipmentResultsPackageResults

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**trackingNumber** | **string** | Package 1Z number.   For Mail Innovations shipments, please use the USPSPICNumber when tracking packages (a non-1Z number Mail Manifest Id is returned). |
**rateModifier** | [**\OpenAPIClientUPSShipping\Model\PackageResultsRateModifier[]**](PackageResultsRateModifier.md) | Returned Package Information.  **NOTE:** For versions &gt;&#x3D; v2403, this element will always be returned as an array. For requests using versions &lt; v2403, this element will be returned as an array if there is more than one object and a single object if there is only 1. | [optional]
**baseServiceCharge** | [**\OpenAPIClientUPSShipping\Model\PackageResultsBaseServiceCharge**](PackageResultsBaseServiceCharge.md) |  | [optional]
**serviceOptionsCharges** | [**\OpenAPIClientUPSShipping\Model\PackageResultsServiceOptionsCharges**](PackageResultsServiceOptionsCharges.md) |  | [optional]
**shippingLabel** | [**\OpenAPIClientUPSShipping\Model\PackageResultsShippingLabel**](PackageResultsShippingLabel.md) |  | [optional]
**shippingReceipt** | [**\OpenAPIClientUPSShipping\Model\PackageResultsShippingReceipt**](PackageResultsShippingReceipt.md) |  | [optional]
**uSPSPICNumber** | **string** | USPSPICNumber is USPS Package Identification; it should be used for tracking Mail Innovations shipments. | [optional]
**cN22Number** | **string** | USPS defined CN22 ID number format varies based on destination country or territory.  Not applicable as of Jan 2015.  Mail Innovations shipments US to VI, PR, and GU are not considered international. | [optional]
**accessorial** | [**\OpenAPIClientUPSShipping\Model\PackageResultsAccessorial[]**](PackageResultsAccessorial.md) | The container for Accessorial indicators. This information would be returned only for UPS Worldwide Express Freight and UPS Worldwide Express Freight Mid-day service request with Dry Ice or Oversize Pallet and SubVersion greater than or equal to 1707. This is valid only for UPS Worldwide Express Freight and UPS Worldwide Express Freight Mid-day service.  **NOTE:** For versions &gt;&#x3D; v2403, this element will always be returned as an array. For requests using versions &lt; v2403, this element will be returned as an array if there is more than one object and a single object if there is only 1. | [optional]
**simpleRate** | [**\OpenAPIClientUPSShipping\Model\PackageResultsSimpleRate**](PackageResultsSimpleRate.md) |  | [optional]
**form** | [**\OpenAPIClientUPSShipping\Model\PackageResultsForm**](PackageResultsForm.md) |  | [optional]
**itemizedCharges** | [**\OpenAPIClientUPSShipping\Model\PackageResultsItemizedCharges[]**](PackageResultsItemizedCharges.md) | Itemized Charges are returned only when the subversion element is present and greater than or equal to 1607. Package level itemized charges are only returned for US domestic movements.  **NOTE:** For versions &gt;&#x3D; v2403, this element will always be returned as an array. For requests using versions &lt; v2403, this element will be returned as an array if there is more than one object and a single object if there is only 1. | [optional]
**negotiatedCharges** | [**\OpenAPIClientUPSShipping\Model\PackageResultsNegotiatedCharges**](PackageResultsNegotiatedCharges.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
