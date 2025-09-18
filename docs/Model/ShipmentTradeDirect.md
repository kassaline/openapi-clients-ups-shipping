# # ShipmentTradeDirect

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**master** | [**\OpenAPIClientUPSShipping\Model\TradeDirectMaster**](TradeDirectMaster.md) |  | [optional]
**child** | [**\OpenAPIClientUPSShipping\Model\TradeDirectChild**](TradeDirectChild.md) |  | [optional]
**generalDescriptionOfGoods** | **string** | General description of the goods being shipped. It is required for master shipment. | [optional]
**shipmentType** | **string** | Consolidated shipment types.  Valid values: - TRADEDIRECTAIR &#x3D;  TradeDirect Air - consolidation, custom clearance, deconsolidation and delivery to multiple addresses                      within destination country, with Airport-to-door or door-to-door.                      - TRADEDIRECTOCEAN &#x3D; TradeDirect Ocean - consolidation, ocean transportation, customs clearance, deconsolidation and delivery                       to multiple addresses within a destination country, with port-to-door and door-to-door service from shipper to consignee. Available from more than 70 ports.                       - TRADEDIRECTCROSSBORDER &#x3D; TradeDirect CrossBoarder - consolidation, customs clearance, deconsolidation and delivery to multiple addresses                            within the destination country, with door-to-door service across North American borders. |
**currencyCode** | **string** | The currency code for the shipment as per ISO 4217. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
