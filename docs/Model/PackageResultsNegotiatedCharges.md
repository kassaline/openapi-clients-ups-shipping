# # PackageResultsNegotiatedCharges

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**itemizedCharges** | [**\OpenAPIClientUPSShipping\Model\NegotiatedChargesItemizedCharges[]**](NegotiatedChargesItemizedCharges.md) | Negotiated Itemized Accessorial and SurCharges.  Negotiated itemized charges are only returned for certain contract-only shipments as well as Worldwide Express Freight, Ground Freight Pricing, and Hazmat movements. Negotiated Itemized Accessorial and Sur Charges are returned only when the subversion element is present and greater than or equal to 1607.  Package level itemized charges are only returned for US domestic movements  **NOTE:** For versions &gt;&#x3D; v2403, this element will always be returned as an array. For requests using versions &lt; v2403, this element will be returned as an array if there is more than one object and a single object if there is only 1. | [optional]
**rateModifier** | [**\OpenAPIClientUPSShipping\Model\NegotiatedChargesRateModifier[]**](NegotiatedChargesRateModifier.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
