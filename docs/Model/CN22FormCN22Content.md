# # CN22FormCN22Content

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cN22ContentQuantity** | **string** | Total number of items associated with this content.  Required if the CN22 form container is present. |
**cN22ContentDescription** | **string** | Detailed description of the content.  If the combined MI package and CN22 label is requested, only the first 30 characters will appear on the combined label.  Required if the CN22 form container is present. |
**cN22ContentWeight** | [**\OpenAPIClientUPSShipping\Model\CN22ContentCN22ContentWeight**](CN22ContentCN22ContentWeight.md) |  |
**cN22ContentTotalValue** | **string** | Total value of the items associated with this content.  Required if the CN22 form container is present. |
**cN22ContentCurrencyCode** | **string** | Currently only USD is supported.  Required if the CN22 form container is present. |
**cN22ContentCountryOfOrigin** | **string** | Country or Territory of Origin from where the CN22 contents originated. | [optional]
**cN22ContentTariffNumber** | **string** | The tariff number associated with the CN22 contents. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
