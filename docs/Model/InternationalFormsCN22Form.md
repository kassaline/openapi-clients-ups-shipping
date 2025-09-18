# # InternationalFormsCN22Form

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**labelSize** | **string** | Provide the valid values:  6 &#x3D; 4X6 1 &#x3D; 8.5X11   Required if the CN22 form container is present. |
**printsPerPage** | **string** | Number of label per page. Currently 1 per page is supported.  Required if the CN22 form container is present. |
**labelPrintType** | **string** | Valid Values are pdf, png, gif, zpl, star, epl2 and spl.   Required if the CN22 form container is present. |
**cN22Type** | **string** | Valid values:  1 &#x3D; GIFT 2 &#x3D; DOCUMENTS 3 &#x3D; COMMERCIAL SAMPLE 4 &#x3D; OTHER  Required if the CN22 form container is present. |
**cN22OtherDescription** | **string** | Required if CN22Type is OTHER.  Required if the CN22 form container is present. | [optional]
**foldHereText** | **string** | String will replace default \&quot;Fold Here\&quot; text displayed on the label. | [optional]
**cN22Content** | [**\OpenAPIClientUPSShipping\Model\CN22FormCN22Content[]**](CN22FormCN22Content.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
