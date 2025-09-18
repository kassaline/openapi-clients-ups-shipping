# # ShipmentChargeBillShipper

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**accountNumber** | **string** | UPS account number.  Must be the same UPS account number as the one provided in Shipper/ShipperNumber.   Either this element or one of the sibling elements CreditCard or AlternatePaymentMethod must be provided, but all of them may not be provided. | [optional]
**creditCard** | [**\OpenAPIClientUPSShipping\Model\BillShipperCreditCard**](BillShipperCreditCard.md) |  | [optional]
**alternatePaymentMethod** | **string** | Alternate Payment Method.  Valid value: 01&#x3D; PayPal  Only valid for forward shipments. It is not valid for Return or Import Control shipments.   This element or one of the sibling elements CreditCard or AccountNumber must be provided, but all of them may not be provided.   PayPal 01: Is only valid for forward shipments. It is not valid for Return or Import Control shipments.   This element or one of the sibling elements CreditCard or AccountNumber must be provided, but all of them may not be provided. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
