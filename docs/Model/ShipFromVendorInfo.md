# # ShipFromVendorInfo

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**vendorCollectIDTypeCode** | **string** | Code that identifies the type of Vendor Collect ID Number. Valid Values - 0000 &#x3D; Unknown/Other - 0356 &#x3D; IOSS Registration Number - 0357 &#x3D; VOEC Registration Number - 0358 &#x3D; Deprecated - 0359 &#x3D; PVA Registration Number - 1051 &#x3D; Singapore GST Registration Number - 1052 &#x3D; ARN Registration Number - 1053 &#x3D; IRD Registration Number - 1054 &#x3D; Malaysia Low Value Goods Sales Tax Registration  Vendor Collect ID Number type code will be printed on commercial invoice if present. |
**vendorCollectIDNumber** | **string** | Shipper&#39;s VAT Tax collection registration number to be entered by Shipper at time of shipment creation. Presence of this number as part of the shipment information implies the shipper has collected/paid the required VAT tax (outside of UPS/UPS systems). Vendor Colect ID Number will be printed on commercial invoice if present.  Sample Values:   &#39;IMDEU1234567&#39; (IOSS #),  &#39;VOEC1234567&#39; (VOEC #),  &#39;GB1234567&#39; (HMRC #)  Required if the shipment is subject to Vendor Collect ID collection |
**consigneeType** | **string** | Consignee Type. 01 &#x3D; Business  02 &#x3D; Consumer NA &#x3D; Not Applicable | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
