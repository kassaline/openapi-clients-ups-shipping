# # ShipmentPackage

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**description** | **string** | Merchandise description of package.  Required for shipment with return service. | [optional]
**palletDescription** | **string** | Description of articles &amp; special marks. Applicable for Air Freight only | [optional]
**numOfPieces** | **string** | Number of Pieces. Applicable for Air Freight only | [optional]
**unitPrice** | **string** | Unit price of the commodity. Applicable for Air Freight only  Limit to 2 digit after the decimal. The maximum length of the field is 12 including &#39;.&#39; and can hold up to 2 decimal place. (e.g. 999999999.99) | [optional]
**packaging** | [**\OpenAPIClientUPSShipping\Model\PackagePackaging**](PackagePackaging.md) |  |
**dimensions** | [**\OpenAPIClientUPSShipping\Model\PackageDimensions**](PackageDimensions.md) |  | [optional]
**dimWeight** | [**\OpenAPIClientUPSShipping\Model\PackageDimWeight**](PackageDimWeight.md) |  | [optional]
**packageWeight** | [**\OpenAPIClientUPSShipping\Model\PackagePackageWeight**](PackagePackageWeight.md) |  | [optional]
**largePackageIndicator** | **string** | Presence of the indicator mentions that the package is Large Package.  This is an empty tag, any value inside is ignored. | [optional]
**oversizeIndicator** | **string** | Presence/Absence Indicator. Any value is ignored. If present, indicates that the package is over size.   Applicable for UPS Worldwide Economy DDU service. | [optional]
**minimumBillableWeightIndicator** | **string** | Presence/Absence Indicator. Any value is ignored. If present, indicates that the package is qualified for minimum billable weight.   Applicable for UPS Worldwide Economy DDU service. | [optional]
**referenceNumber** | [**\OpenAPIClientUPSShipping\Model\PackageReferenceNumber[]**](PackageReferenceNumber.md) |  | [optional]
**additionalHandlingIndicator** | **string** | Additional Handling Required. The presence indicates additional handling is required, the absence indicates no additional handling is required. Additional Handling indicator indicates it&#39;s a non-corrugated package. | [optional]
**simpleRate** | [**\OpenAPIClientUPSShipping\Model\PackageSimpleRate**](PackageSimpleRate.md) |  | [optional]
**uPSPremier** | [**\OpenAPIClientUPSShipping\Model\PackageUPSPremier**](PackageUPSPremier.md) |  | [optional]
**packageServiceOptions** | [**\OpenAPIClientUPSShipping\Model\PackagePackageServiceOptions**](PackagePackageServiceOptions.md) |  | [optional]
**commodity** | [**\OpenAPIClientUPSShipping\Model\PackageCommodity**](PackageCommodity.md) |  | [optional]
**hazMatPackageInformation** | [**\OpenAPIClientUPSShipping\Model\PackageHazMatPackageInformation**](PackageHazMatPackageInformation.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
