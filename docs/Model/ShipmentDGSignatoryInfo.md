# # ShipmentDGSignatoryInfo

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Name of the person signing the declaration.   Note: The name of person or department he/she is employed with, are both acceptable. | [optional]
**title** | **string** | Title of the person signing the declaration. Note: The title of the person or department he/she is employed with, are both acceptable. | [optional]
**place** | **string** | The city of the Signatory. | [optional]
**date** | **string** | Date of signing the declaration form.  Valid format is YYYYMMDD. | [optional]
**shipperDeclaration** | **string** | Valid values: 01 &#x3D; Shipment level 02 &#x3D; Package level                                              Valid only for the Shipper Declaration paper. If missing or invalid DGPaperImage will be returned at package level. | [optional]
**uploadOnlyIndicator** | **string** | Dangerous Goods Paper Upload Only Indicator. DG Paper will not be returned in response if UploadOnlyIndicator present. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
