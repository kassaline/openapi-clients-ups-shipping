# # LabelRecoveryResponseLabelResults

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**trackingNumber** | **string** | Package Tracking number.  Package 1Z number. Returned only if TrackingNumber or Combination of Reference Number and Shipper Number present in request. | [optional]
**labelImage** | [**\OpenAPIClientUPSShipping\Model\LabelResultsLabelImage**](LabelResultsLabelImage.md) |  | [optional]
**mailInnovationsTrackingNumber** | **string** | Mail Innovations Tracking Number.  Applicable for Single Mail Innovations Returns and Dual Mail Innovations Returns shipment. Returned only if MailInnovationsTrackingNumber is provided in request. | [optional]
**mailInnovationsLabelImage** | [**\OpenAPIClientUPSShipping\Model\LabelResultsMailInnovationsLabelImage**](LabelResultsMailInnovationsLabelImage.md) |  | [optional]
**receipt** | [**\OpenAPIClientUPSShipping\Model\LabelResultsReceipt**](LabelResultsReceipt.md) |  | [optional]
**form** | [**\OpenAPIClientUPSShipping\Model\LabelResultsForm**](LabelResultsForm.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
