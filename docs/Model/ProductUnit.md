# # ProductUnit

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**number** | **string** | Total quantity of each commodity to be shipped, measured in the units specified in the Unit of Measure field.  Required for Invoice forms and optional for Partial Invoice. Must be numeric. Valid characters are 0-9. |
**unitOfMeasurement** | [**\OpenAPIClientUPSShipping\Model\UnitUnitOfMeasurement**](UnitUnitOfMeasurement.md) |  |
**value** | **string** | Monetary amount used to specify the worth or price of the commodity. Amount should be greater than zero.  Applies to Invoice and Partial Invoice form. Required for Invoice forms and optional for Partial Invoice. Amount should be greater than zero.  Valid characters are 0-9 and. (Decimal point). Limit to 6 digits after the decimal. The maximum length of the field is 19 including &#39;.&#39; and can hold up to 6 decimal places.(#####.######, ######.#####, #######.####, ########.###, #########.##,##########.#,############). The value of this product  and the other products should be such that the invoice line total which is the sum of ( number*values) of all products should not exceed 9999999999999999.99 |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
