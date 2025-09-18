# # ShipmentResultsNegotiatedRateCharges

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**itemizedCharges** | [**\OpenAPIClientUPSShipping\Model\NegotiatedRateChargesItemizedCharges[]**](NegotiatedRateChargesItemizedCharges.md) | Itemized Charges are returned only when the Subversion element is present and greater than or equal to 1601.  Negotiated itemized charges are only returned for certain contract-only shipments as well as Worldwide Express Freight, Ground Freight Pricing, and Hazmat movements.  **NOTE:** For versions &gt;&#x3D; v2403, this element will always be returned as an array. For requests using versions &lt; v2403, this element will be returned as an array if there is more than one object and a single object if there is only 1. | [optional]
**taxCharges** | [**\OpenAPIClientUPSShipping\Model\NegotiatedRateChargesTaxCharges[]**](NegotiatedRateChargesTaxCharges.md) | TaxCharges container are returned only when TaxInformationIndicator is present in request. TaxCharges container contains Tax information for a given shipment.  **NOTE:** For versions &gt;&#x3D; v2403, this element will always be returned as an array. For requests using versions &lt; v2403, this element will be returned as an array if there is more than one object and a single object if there is only 1. | [optional]
**totalCharge** | [**\OpenAPIClientUPSShipping\Model\NegotiatedRateChargesTotalCharge**](NegotiatedRateChargesTotalCharge.md) |  | [optional]
**rateModifier** | [**\OpenAPIClientUPSShipping\Model\NegotiatedRateChargesRateModifier[]**](NegotiatedRateChargesRateModifier.md) |  | [optional]
**totalChargesWithTaxes** | [**\OpenAPIClientUPSShipping\Model\NegotiatedRateChargesTotalChargesWithTaxes**](NegotiatedRateChargesTotalChargesWithTaxes.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
