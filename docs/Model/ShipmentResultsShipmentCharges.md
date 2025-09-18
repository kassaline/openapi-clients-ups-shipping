# # ShipmentResultsShipmentCharges

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**rateChart** | **string** | Rate Type with which Shipment is rated. Possible RateChart values for different regions will be: US 48 origin: - 1 – Daily Rates - 3 – Standard List Rates - 4 – Retail Rates.  Alaska/Hawaii origin: - 1 – Daily Rates - 3 – Standard List Rates - 4 – Retail Rates.  All Other origins: - 1 – Rates - 5 - Regional Rates - 6 - General List Rates.  3 and 4 do not apply. | [optional]
**baseServiceCharge** | [**\OpenAPIClientUPSShipping\Model\ShipmentChargesBaseServiceCharge**](ShipmentChargesBaseServiceCharge.md) |  | [optional]
**transportationCharges** | [**\OpenAPIClientUPSShipping\Model\ShipmentChargesTransportationCharges**](ShipmentChargesTransportationCharges.md) |  |
**itemizedCharges** | [**\OpenAPIClientUPSShipping\Model\ShipmentChargesItemizedCharges[]**](ShipmentChargesItemizedCharges.md) | Itemized Charges are returned only when the Subversion element is present and greater than or equal to 1601.  **NOTE:** For versions &gt;&#x3D; v2403, this element will always be returned as an array. For requests using versions &lt; v2403, this element will be returned as an array if there is more than one object and a single object if there is only 1. | [optional]
**serviceOptionsCharges** | [**\OpenAPIClientUPSShipping\Model\ShipmentChargesServiceOptionsCharges**](ShipmentChargesServiceOptionsCharges.md) |  |
**taxCharges** | [**\OpenAPIClientUPSShipping\Model\ShipmentChargesTaxCharges[]**](ShipmentChargesTaxCharges.md) | TaxCharges container are returned only when TaxInformationIndicator is present in request and when Negotiated Rates are not applicable. TaxCharges container contains Tax information for a given shipment.  **NOTE:** For versions &gt;&#x3D; v2403, this element will always be returned as an array. For requests using versions &lt; v2403, this element will be returned as an array if there is more than one object and a single object if there is only 1. | [optional]
**totalCharges** | [**\OpenAPIClientUPSShipping\Model\ShipmentChargesTotalCharges**](ShipmentChargesTotalCharges.md) |  |
**totalChargesWithTaxes** | [**\OpenAPIClientUPSShipping\Model\ShipmentChargesTotalChargesWithTaxes**](ShipmentChargesTotalChargesWithTaxes.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
