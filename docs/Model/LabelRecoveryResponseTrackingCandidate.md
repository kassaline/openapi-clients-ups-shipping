# # LabelRecoveryResponseTrackingCandidate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**trackingNumber** | **string** | Packaging Tracking Number  Only supported for the web small package shipment so only supported 18 digit |
**destinationPostalCode** | **string** | Destination postal code candidate | [optional]
**destinationCountryCode** | **string** | Destination country or territory code candidate, like US &#x3D; USA, CA &#x3D; Canada  Must be valid ups country or territory code. This is required, if MasterEUConsolidationIndicator is \&quot;1\&quot;. | [optional]
**pickupDateRange** | [**\OpenAPIClientUPSShipping\Model\TrackingCandidatePickupDateRange**](TrackingCandidatePickupDateRange.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
