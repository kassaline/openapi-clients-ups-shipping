# # PackagePackageServiceOptions

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**deliveryConfirmation** | [**\OpenAPIClientUPSShipping\Model\PackageServiceOptionsDeliveryConfirmation**](PackageServiceOptionsDeliveryConfirmation.md) |  | [optional]
**declaredValue** | [**\OpenAPIClientUPSShipping\Model\PackageServiceOptionsDeclaredValue**](PackageServiceOptionsDeclaredValue.md) |  | [optional]
**cOD** | [**\OpenAPIClientUPSShipping\Model\PackageServiceOptionsCOD**](PackageServiceOptionsCOD.md) |  | [optional]
**accessPointCOD** | [**\OpenAPIClientUPSShipping\Model\PackageServiceOptionsAccessPointCOD**](PackageServiceOptionsAccessPointCOD.md) |  | [optional]
**shipperReleaseIndicator** | **string** | The presence indicates that the package may be released by driver without a signature from the consignee.  Empty Tag. Only available for US50/PR to US50/PR packages without return service. | [optional]
**notification** | [**\OpenAPIClientUPSShipping\Model\PackageServiceOptionsNotification**](PackageServiceOptionsNotification.md) |  | [optional]
**hazMat** | [**\OpenAPIClientUPSShipping\Model\PackageServiceOptionsHazMat[]**](PackageServiceOptionsHazMat.md) |  | [optional]
**hazMatTypeCode** | **string** | Field to be used when a shipment contains a HazMat. It will specify the existence of HazMat, and what type. Initially this will be used for UPS Ground saver and Mail Innovations &#39;USPS Limited Quantities HazMat&#39; Shipments (but may be extended for other types of HazMat in the future).  Valid values are 01.   - USPS Limited Quantities HazMat - 01 | [optional]
**dryIce** | [**\OpenAPIClientUPSShipping\Model\PackageServiceOptionsDryIce**](PackageServiceOptionsDryIce.md) |  | [optional]
**uPSPremiumCareIndicator** | **string** | An UPSPremiumCareIndicator indicates special handling is required for shipment having controlled substances. Empty Tag means indicator is present.  The UPSPremiumCareIndicator cannot be requested for package with Delivery Confirmation - Adult Signature Required and Delivery Confirmation- Signature Required.  UPSPremiumCareIndicator is valid for following Return services: - Returns Exchange (available with a contract) - Print Return Label - Print and Mail - Electronic Return Label - Return Service Three Attempt  The UPSPremiumCareIndicator can be requested with following UPS services: - UPS Express® Early - UPS Express - UPS Express Saver - UPS Standard - Valid only for Canada to Canada movements. | [optional]
**proactiveIndicator** | **string** | Presence/Absence Indicator. Any value is ignored. If present, the package is rated for UPS Proactive Response and proactive package tracking. Contractual accessorial for health care companies to allow package monitoring throughout the UPS system.  Shippers account needs to have valid contract for UPS Proactive Reponse. | [optional]
**packageIdentifier** | **string** | Identifies the package containing Dangerous Goods.  Required for Hazmat shipment if SubVersion is greater than or equal to 1701. | [optional]
**clinicalTrialsID** | **string** | Unique identifier for clinical trials | [optional]
**refrigerationIndicator** | **string** | Presence/Absence Indicator. Any value is ignored. If present, indicates that the package contains an item that needs refrigeration.  Shippers account needs to have a valid contract for Refrigeration. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
