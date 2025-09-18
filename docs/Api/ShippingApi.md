# OpenAPIClientUPSShipping\ShippingApi

All URIs are relative to https://wwwcie.ups.com/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deprecatedShipment()**](ShippingApi.md#deprecatedShipment) | **POST** /shipments/{deprecatedVersion}/ship | Shipment |
| [**deprecatedVoidShipment()**](ShippingApi.md#deprecatedVoidShipment) | **DELETE** /shipments/{deprecatedVersion}/void/cancel/{shipmentidentificationnumber} | Void Shipment |
| [**labelRecovery()**](ShippingApi.md#labelRecovery) | **POST** /labels/{version}/recovery | Label Recovery |
| [**shipment()**](ShippingApi.md#shipment) | **POST** /shipments/{version}/ship | Shipment |
| [**voidShipment()**](ShippingApi.md#voidShipment) | **DELETE** /shipments/{version}/void/cancel/{shipmentidentificationnumber} | Void Shipment |


## `deprecatedShipment()`

```php
deprecatedShipment($deprecatedVersion, $sHIPRequestWrapper, $transId, $transactionSrc, $additionaladdressvalidation): \OpenAPIClientUPSShipping\Model\SHIPResponseWrapper
```

Shipment

The Shipping API makes UPS shipping services available to client applications that communicate with UPS  using the Internet

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: OAuth2
$config = OpenAPIClientUPSShipping\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPIClientUPSShipping\Api\ShippingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$deprecatedVersion = 'v1'; // string | Indicates Ship API to display the new release features in Ship API response based on Ship release.  Valid values: - v1 - v1601 - v1607 - v1701 - v1707 - v1801 - v1807 - v2108 - v2205
$sHIPRequestWrapper = {"ShipmentRequest":{"Request":{"SubVersion":"1801","RequestOption":"nonvalidate","TransactionReference":{"CustomerContext":""}},"Shipment":{"Description":"Ship WS test","Shipper":{"Name":"ShipperName","AttentionName":"ShipperZs Attn Name","TaxIdentificationNumber":"123456","Phone":{"Number":"1115554758","Extension":" "},"ShipperNumber":" ","FaxNumber":"8002222222","Address":{"AddressLine":["2311 York Rd"],"City":"Timonium","StateProvinceCode":"MD","PostalCode":"21093","CountryCode":"US"}},"ShipTo":{"Name":"Happy Dog Pet Supply","AttentionName":"1160b_74","Phone":{"Number":"9225377171"},"Address":{"AddressLine":["123 Main St"],"City":"timonium","StateProvinceCode":"MD","PostalCode":"21030","CountryCode":"US"},"Residential":" "},"ShipFrom":{"Name":"T and T Designs","AttentionName":"1160b_74","Phone":{"Number":"1234567890"},"FaxNumber":"1234567890","Address":{"AddressLine":["2311 York Rd"],"City":"Alpharetta","StateProvinceCode":"GA","PostalCode":"30005","CountryCode":"US"}},"PaymentInformation":{"ShipmentCharge":{"Type":"01","BillShipper":{"AccountNumber":" "}}},"Service":{"Code":"03","Description":"Express"},"Package":{"Description":" ","Packaging":{"Code":"02","Description":"Nails"},"Dimensions":{"UnitOfMeasurement":{"Code":"IN","Description":"Inches"},"Length":"10","Width":"30","Height":"45"},"PackageWeight":{"UnitOfMeasurement":{"Code":"LBS","Description":"Pounds"},"Weight":"5"}}},"LabelSpecification":{"LabelImageFormat":{"Code":"GIF","Description":"GIF"},"HTTPUserAgent":"Mozilla/4.5"}}}; // \OpenAPIClientUPSShipping\Model\SHIPRequestWrapper | Generate sample code for popular API requests by selecting an example below. To view a full sample request and response, first click \"Authorize\" and enter your application credentials, then populate the required parameters above and click \"Try it out\".
$transId = 'transId_example'; // string | An identifier unique to the request. Length 32
$transactionSrc = 'testing'; // string | An identifier of the client/source application that is making the request.Length 512
$additionaladdressvalidation = 'additionaladdressvalidation_example'; // string | Valid Values:  city = validation will include city.Length 15

try {
    $result = $apiInstance->deprecatedShipment($deprecatedVersion, $sHIPRequestWrapper, $transId, $transactionSrc, $additionaladdressvalidation);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShippingApi->deprecatedShipment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **deprecatedVersion** | **string**| Indicates Ship API to display the new release features in Ship API response based on Ship release.  Valid values: - v1 - v1601 - v1607 - v1701 - v1707 - v1801 - v1807 - v2108 - v2205 | [default to &#39;v1&#39;] |
| **sHIPRequestWrapper** | [**\OpenAPIClientUPSShipping\Model\SHIPRequestWrapper**](../Model/SHIPRequestWrapper.md)| Generate sample code for popular API requests by selecting an example below. To view a full sample request and response, first click \&quot;Authorize\&quot; and enter your application credentials, then populate the required parameters above and click \&quot;Try it out\&quot;. | |
| **transId** | **string**| An identifier unique to the request. Length 32 | [optional] |
| **transactionSrc** | **string**| An identifier of the client/source application that is making the request.Length 512 | [optional] [default to &#39;testing&#39;] |
| **additionaladdressvalidation** | **string**| Valid Values:  city &#x3D; validation will include city.Length 15 | [optional] |

### Return type

[**\OpenAPIClientUPSShipping\Model\SHIPResponseWrapper**](../Model/SHIPResponseWrapper.md)

### Authorization

[OAuth2](../../README.md#OAuth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deprecatedVoidShipment()`

```php
deprecatedVoidShipment($deprecatedVersion, $shipmentidentificationnumber, $transId, $transactionSrc, $trackingnumber): \OpenAPIClientUPSShipping\Model\VOIDSHIPMENTResponseWrapper
```

Void Shipment

The Void Shipping API is used to cancel the previously scheduled shipment

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: OAuth2
$config = OpenAPIClientUPSShipping\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPIClientUPSShipping\Api\ShippingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$deprecatedVersion = 'v1'; // string | API Version.  Valid values: - v1
$shipmentidentificationnumber = 'shipmentidentificationnumber_example'; // string | The shipment's identification number  Alpha-numeric. Must pass 1Z rules. Must be  upper case. Length 18
$transId = 'transId_example'; // string | An identifier unique to the request. Length 32
$transactionSrc = 'testing'; // string | An identifier of the client/source application that is making the request.Length 512
$trackingnumber = 'trackingnumber_example'; // string | The package's tracking number. You may have  up to 20 different tracking numbers listed. If more than one tracking number, pass this  value as: trackingnumber=  [\"1ZISUS010330563105\",\"1ZISUS01033056310 8\"] with a coma separating each number. Alpha-numeric. Must pass 1Z rules. Must be  upper case. Length 18

try {
    $result = $apiInstance->deprecatedVoidShipment($deprecatedVersion, $shipmentidentificationnumber, $transId, $transactionSrc, $trackingnumber);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShippingApi->deprecatedVoidShipment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **deprecatedVersion** | **string**| API Version.  Valid values: - v1 | [default to &#39;v1&#39;] |
| **shipmentidentificationnumber** | **string**| The shipment&#39;s identification number  Alpha-numeric. Must pass 1Z rules. Must be  upper case. Length 18 | |
| **transId** | **string**| An identifier unique to the request. Length 32 | [optional] |
| **transactionSrc** | **string**| An identifier of the client/source application that is making the request.Length 512 | [optional] [default to &#39;testing&#39;] |
| **trackingnumber** | **string**| The package&#39;s tracking number. You may have  up to 20 different tracking numbers listed. If more than one tracking number, pass this  value as: trackingnumber&#x3D;  [\&quot;1ZISUS010330563105\&quot;,\&quot;1ZISUS01033056310 8\&quot;] with a coma separating each number. Alpha-numeric. Must pass 1Z rules. Must be  upper case. Length 18 | [optional] |

### Return type

[**\OpenAPIClientUPSShipping\Model\VOIDSHIPMENTResponseWrapper**](../Model/VOIDSHIPMENTResponseWrapper.md)

### Authorization

[OAuth2](../../README.md#OAuth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `labelRecovery()`

```php
labelRecovery($version, $lABELRECOVERYRequestWrapper, $transId, $transactionSrc): \OpenAPIClientUPSShipping\Model\LABELRECOVERYResponseWrapper
```

Label Recovery

The Label Shipping API allows us to retrieve forward and return labels.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: OAuth2
$config = OpenAPIClientUPSShipping\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPIClientUPSShipping\Api\ShippingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$version = 'v1'; // string | When UPS introduces new elements in the  response that are not associated with new  request elements, Subversion is used. This  ensures backward compatibility.  v1  original features of the application. No  support for CODTurn-inPage, HighValueReport  or InternationalForms features returned in the  response v1701  includes support for CODTurn-inPage  features returned in the response. V1903  Length 5
$lABELRECOVERYRequestWrapper = {"LabelRecoveryRequest":{"LabelDelivery":{"LabelLinkIndicator":"","ResendEmailIndicator":""},"LabelSpecification":{"HTTPUserAgent":"Mozilla/4.5","LabelImageFormat":{"Code":"ZPL"},"LabelStockSize":{"Height":"6","Width":"4"}},"Request":{"RequestOption":"Non_Validate","SubVersion":"1903","TransactionReference":{"CustomerContext":""}},"TrackingNumber":"1Z12345E8791315509","Translate":{"Code":"01","DialectCode":"US","LanguageCode":"eng"}}}; // \OpenAPIClientUPSShipping\Model\LABELRECOVERYRequestWrapper | Generate sample code for popular API requests by selecting an example below. To view a full sample request and response, first click \"Authorize\" and enter your application credentials, then populate the required parameters above and click \"Try it out\".
$transId = 'transId_example'; // string | An identifier unique to the request. Length 32
$transactionSrc = 'testing'; // string | An identifier of the client/source application that is making the request.Length 512

try {
    $result = $apiInstance->labelRecovery($version, $lABELRECOVERYRequestWrapper, $transId, $transactionSrc);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShippingApi->labelRecovery: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **version** | **string**| When UPS introduces new elements in the  response that are not associated with new  request elements, Subversion is used. This  ensures backward compatibility.  v1  original features of the application. No  support for CODTurn-inPage, HighValueReport  or InternationalForms features returned in the  response v1701  includes support for CODTurn-inPage  features returned in the response. V1903  Length 5 | [default to &#39;v1&#39;] |
| **lABELRECOVERYRequestWrapper** | [**\OpenAPIClientUPSShipping\Model\LABELRECOVERYRequestWrapper**](../Model/LABELRECOVERYRequestWrapper.md)| Generate sample code for popular API requests by selecting an example below. To view a full sample request and response, first click \&quot;Authorize\&quot; and enter your application credentials, then populate the required parameters above and click \&quot;Try it out\&quot;. | |
| **transId** | **string**| An identifier unique to the request. Length 32 | [optional] |
| **transactionSrc** | **string**| An identifier of the client/source application that is making the request.Length 512 | [optional] [default to &#39;testing&#39;] |

### Return type

[**\OpenAPIClientUPSShipping\Model\LABELRECOVERYResponseWrapper**](../Model/LABELRECOVERYResponseWrapper.md)

### Authorization

[OAuth2](../../README.md#OAuth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `shipment()`

```php
shipment($version, $sHIPRequestWrapper, $transId, $transactionSrc, $additionaladdressvalidation): \OpenAPIClientUPSShipping\Model\SHIPResponseWrapper
```

Shipment

The Shipping API makes UPS shipping services available to client applications that communicate with UPS  using the Internet

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: OAuth2
$config = OpenAPIClientUPSShipping\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPIClientUPSShipping\Api\ShippingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$version = 'v2409'; // string | Indicates Ship API to display the new release features in Ship API response based on Ship release.  Valid values: - v2409
$sHIPRequestWrapper = {"ShipmentRequest":{"Request":{"SubVersion":"1801","RequestOption":"nonvalidate","TransactionReference":{"CustomerContext":""}},"Shipment":{"Description":"Ship WS test","Shipper":{"Name":"ShipperName","AttentionName":"ShipperZs Attn Name","TaxIdentificationNumber":"123456","Phone":{"Number":"1115554758","Extension":" "},"ShipperNumber":" ","FaxNumber":"8002222222","Address":{"AddressLine":["2311 York Rd"],"City":"Timonium","StateProvinceCode":"MD","PostalCode":"21093","CountryCode":"US"}},"ShipTo":{"Name":"Happy Dog Pet Supply","AttentionName":"1160b_74","Phone":{"Number":"9225377171"},"Address":{"AddressLine":["123 Main St"],"City":"timonium","StateProvinceCode":"MD","PostalCode":"21030","CountryCode":"US"},"Residential":" "},"ShipFrom":{"Name":"T and T Designs","AttentionName":"1160b_74","Phone":{"Number":"1234567890"},"FaxNumber":"1234567890","Address":{"AddressLine":["2311 York Rd"],"City":"Alpharetta","StateProvinceCode":"GA","PostalCode":"30005","CountryCode":"US"}},"PaymentInformation":{"ShipmentCharge":{"Type":"01","BillShipper":{"AccountNumber":" "}}},"Service":{"Code":"03","Description":"Express"},"Package":{"Description":" ","Packaging":{"Code":"02","Description":"Nails"},"Dimensions":{"UnitOfMeasurement":{"Code":"IN","Description":"Inches"},"Length":"10","Width":"30","Height":"45"},"PackageWeight":{"UnitOfMeasurement":{"Code":"LBS","Description":"Pounds"},"Weight":"5"}}},"LabelSpecification":{"LabelImageFormat":{"Code":"GIF","Description":"GIF"},"HTTPUserAgent":"Mozilla/4.5"}}}; // \OpenAPIClientUPSShipping\Model\SHIPRequestWrapper | Generate sample code for popular API requests by selecting an example below. To view a full sample request and response, first click \"Authorize\" and enter your application credentials, then populate the required parameters above and click \"Try it out\".
$transId = 'transId_example'; // string | An identifier unique to the request. Length 32
$transactionSrc = 'testing'; // string | An identifier of the client/source application that is making the request.Length 512
$additionaladdressvalidation = 'additionaladdressvalidation_example'; // string | Valid Values:  city = validation will include city.Length 15

try {
    $result = $apiInstance->shipment($version, $sHIPRequestWrapper, $transId, $transactionSrc, $additionaladdressvalidation);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShippingApi->shipment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **version** | **string**| Indicates Ship API to display the new release features in Ship API response based on Ship release.  Valid values: - v2409 | [default to &#39;v2409&#39;] |
| **sHIPRequestWrapper** | [**\OpenAPIClientUPSShipping\Model\SHIPRequestWrapper**](../Model/SHIPRequestWrapper.md)| Generate sample code for popular API requests by selecting an example below. To view a full sample request and response, first click \&quot;Authorize\&quot; and enter your application credentials, then populate the required parameters above and click \&quot;Try it out\&quot;. | |
| **transId** | **string**| An identifier unique to the request. Length 32 | [optional] |
| **transactionSrc** | **string**| An identifier of the client/source application that is making the request.Length 512 | [optional] [default to &#39;testing&#39;] |
| **additionaladdressvalidation** | **string**| Valid Values:  city &#x3D; validation will include city.Length 15 | [optional] |

### Return type

[**\OpenAPIClientUPSShipping\Model\SHIPResponseWrapper**](../Model/SHIPResponseWrapper.md)

### Authorization

[OAuth2](../../README.md#OAuth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `voidShipment()`

```php
voidShipment($version, $shipmentidentificationnumber, $transId, $transactionSrc, $trackingnumber): \OpenAPIClientUPSShipping\Model\VOIDSHIPMENTResponseWrapper
```

Void Shipment

The Void Shipping API is used to cancel the previously scheduled shipment

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: OAuth2
$config = OpenAPIClientUPSShipping\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPIClientUPSShipping\Api\ShippingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$version = 'v2409'; // string | API Version  Valid values: - v2409
$shipmentidentificationnumber = 'shipmentidentificationnumber_example'; // string | The shipment's identification number  Alpha-numeric. Must pass 1Z rules. Must be  upper case. Length 18
$transId = 'transId_example'; // string | An identifier unique to the request. Length 32
$transactionSrc = 'testing'; // string | An identifier of the client/source application that is making the request.Length 512
$trackingnumber = 'trackingnumber_example'; // string | The package's tracking number. You may have  up to 20 different tracking numbers listed. If more than one tracking number, pass this  value as: trackingnumber=  [\"1ZISUS010330563105\",\"1ZISUS01033056310 8\"] with a coma separating each number. Alpha-numeric. Must pass 1Z rules. Must be  upper case. Length 18

try {
    $result = $apiInstance->voidShipment($version, $shipmentidentificationnumber, $transId, $transactionSrc, $trackingnumber);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShippingApi->voidShipment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **version** | **string**| API Version  Valid values: - v2409 | [default to &#39;v2409&#39;] |
| **shipmentidentificationnumber** | **string**| The shipment&#39;s identification number  Alpha-numeric. Must pass 1Z rules. Must be  upper case. Length 18 | |
| **transId** | **string**| An identifier unique to the request. Length 32 | [optional] |
| **transactionSrc** | **string**| An identifier of the client/source application that is making the request.Length 512 | [optional] [default to &#39;testing&#39;] |
| **trackingnumber** | **string**| The package&#39;s tracking number. You may have  up to 20 different tracking numbers listed. If more than one tracking number, pass this  value as: trackingnumber&#x3D;  [\&quot;1ZISUS010330563105\&quot;,\&quot;1ZISUS01033056310 8\&quot;] with a coma separating each number. Alpha-numeric. Must pass 1Z rules. Must be  upper case. Length 18 | [optional] |

### Return type

[**\OpenAPIClientUPSShipping\Model\VOIDSHIPMENTResponseWrapper**](../Model/VOIDSHIPMENTResponseWrapper.md)

### Authorization

[OAuth2](../../README.md#OAuth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
