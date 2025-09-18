# # ContactsSoldTo

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Company Name. |
**attentionName** | **string** | Sold to contact name. |
**taxIdentificationNumber** | **string** | SoldTo Tax Identification Number. This element has been deprecated, replacement can be found in the GlobalTaxInformation container. | [optional]
**phone** | [**\OpenAPIClientUPSShipping\Model\SoldToPhone**](SoldToPhone.md) |  | [optional]
**option** | **string** | The text associated with the code will be printed in the sold to section of the NAFTA CO form.  The values indicate the following: 01 – Unknown.  Applies to NAFTA CO form. Possible Values are 01 and 02. | [optional]
**address** | [**\OpenAPIClientUPSShipping\Model\SoldToAddress**](SoldToAddress.md) |  |
**eMailAddress** | **string** | SoldTo email address. | [optional]
**accountNumber** | **string** | SoldTo AccountNumber | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
