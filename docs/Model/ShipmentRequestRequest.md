# # ShipmentRequestRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**requestOption** | **string** | Optional Processing.    Note: Full address validation is not performed. Therefore, it is the responsibility of the Shipping Tool User to ensure the address entered is correct to avoid an address correction fee.  Valid values: nonvalidate &#x3D; No street level address validation would be performed, but Postal Code/State combination validation would still be performed.  validate &#x3D; No street level address validation would be performed, but City/State/Postal Code/ combination validation would still be performed. |
**subVersion** | **string** | When UPS introduces new elements in the response that are not associated with new request elements, Subversion is used. This ensures backward compatibility.  To get such elements you need to have the right Subversion. The value of the subversion is explained in the Response element Description.  Example: Itemized Charges are returned only when the Subversion element is present and greater than or equal to 1601.   Format: YYMM &#x3D; Year and month of the release.  Example: 1607 &#x3D; 2016 July  Supported values: 1601, 1607, 1701, 1707, 1801, 1807, 2108, 2205 | [optional]
**transactionReference** | [**\OpenAPIClientUPSShipping\Model\RequestTransactionReference**](RequestTransactionReference.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
