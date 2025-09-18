# OpenAPIClient-php


The Shipping Package API gives the application many ways to manage the shipment of packages to their destination.
# Reference
- <a href=\"https://developer.ups.com/api/reference/shipping/business-rules\" target=\"_blank\" rel=\"noopener\">Business Rules</a>
- <a href=\"https://developer.ups.com/api/reference/shipping/appendix1\" target=\"_blank\" rel=\"noopener\">Appendix 1</a>
- <a href=\"https://developer.ups.com/api/reference/shipping/appendix2\" target=\"_blank\" rel=\"noopener\">Appendix 2</a>
- <a href=\"https://developer.ups.com/api/reference/shipping/errors\" target=\"_blank\" rel=\"noopener\">Errors</a>
- <a href=\"https://developer.ups.com/api/reference/shipping/faq\" target=\"_blank\" rel=\"noopener\">FAQ</a>
- <a href=\"https://developer.ups.com/api/reference/shipping/best-practices\" target=\"_blank\" rel=\"noopener noreferrer\"> Best Practices</a>

<br/><p>Try out UPS APIs with example requests using Postman and learn more about the UPS Postman Collection by visiting our <a href=\"https://developer.ups.com/api/reference/postman/guide\"
target=\"_blank\" rel=\"noopener\">Postman Guide</a>. Explore API documentation and sample applications through GitHub.</p>

<a href=\"https://god.gw.postman.com/run-collection/29542085-af2f70b3-405b-4aee-af8d-1eb715e4cebc?action=collection%2Ffork&source=rip_markdown&collection-url=entityId%3D29542085-af2f70b3-405b-4aee-af8d-1eb715e4cebc%26entityType%3Dcollection%26workspaceId%3D7e7595f0-4829-4f9a-aee1-75c126b9d417\" target=\"_blank\" rel=\"noopener noreferrer\">
  <img src=\"https://run.pstmn.io/button.svg\" alt=\"Run In Postman\" style=\"width: 128px; height: 32px;\"></a>
<a href=\"https://github.com/UPS-API\" target=\"_blank\" rel=\"noopener noreferrer\">
  <img src=\"https://www.ups.com/assets/resources/webcontent/images/gitHubButton.svg\" alt=\"Open in GitHub \" style=\"width: 128px; height: 32px;\">
</a>



## Installation & Usage

### Requirements

PHP 8.1 and later.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

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

## API Endpoints

All URIs are relative to *https://wwwcie.ups.com/api*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ShippingApi* | [**deprecatedShipment**](docs/Api/ShippingApi.md#deprecatedshipment) | **POST** /shipments/{deprecatedVersion}/ship | Shipment
*ShippingApi* | [**deprecatedVoidShipment**](docs/Api/ShippingApi.md#deprecatedvoidshipment) | **DELETE** /shipments/{deprecatedVersion}/void/cancel/{shipmentidentificationnumber} | Void Shipment
*ShippingApi* | [**labelRecovery**](docs/Api/ShippingApi.md#labelrecovery) | **POST** /labels/{version}/recovery | Label Recovery
*ShippingApi* | [**shipment**](docs/Api/ShippingApi.md#shipment) | **POST** /shipments/{version}/ship | Shipment
*ShippingApi* | [**voidShipment**](docs/Api/ShippingApi.md#voidshipment) | **DELETE** /shipments/{version}/void/cancel/{shipmentidentificationnumber} | Void Shipment

## Models

- [AddressPOE](docs/Model/AddressPOE.md)
- [AdjustedHeightUnitOfMeasurement](docs/Model/AdjustedHeightUnitOfMeasurement.md)
- [AgentTaxIdentificationNumberTaxIdentificationNumber](docs/Model/AgentTaxIdentificationNumberTaxIdentificationNumber.md)
- [AlternateDeliveryAddressAddress](docs/Model/AlternateDeliveryAddressAddress.md)
- [BillReceiverAddress](docs/Model/BillReceiverAddress.md)
- [BillShipperCreditCard](docs/Model/BillShipperCreditCard.md)
- [BillThirdPartyAddress](docs/Model/BillThirdPartyAddress.md)
- [BillingWeightUnitOfMeasurement](docs/Model/BillingWeightUnitOfMeasurement.md)
- [CN22ContentCN22ContentWeight](docs/Model/CN22ContentCN22ContentWeight.md)
- [CN22ContentWeightUnitOfMeasurement](docs/Model/CN22ContentWeightUnitOfMeasurement.md)
- [CN22FormCN22Content](docs/Model/CN22FormCN22Content.md)
- [CODCODAmount](docs/Model/CODCODAmount.md)
- [CODTurnInPageImage](docs/Model/CODTurnInPageImage.md)
- [CODTurnInPageImageImageFormat](docs/Model/CODTurnInPageImageImageFormat.md)
- [ChildLTLCharges](docs/Model/ChildLTLCharges.md)
- [ChildLTLPackage](docs/Model/ChildLTLPackage.md)
- [ChildProduct](docs/Model/ChildProduct.md)
- [CommodityNMFC](docs/Model/CommodityNMFC.md)
- [CommonErrorResponse](docs/Model/CommonErrorResponse.md)
- [ContactsForwardAgent](docs/Model/ContactsForwardAgent.md)
- [ContactsIntermediateConsignee](docs/Model/ContactsIntermediateConsignee.md)
- [ContactsProducer](docs/Model/ContactsProducer.md)
- [ContactsSoldTo](docs/Model/ContactsSoldTo.md)
- [ContactsUltimateConsignee](docs/Model/ContactsUltimateConsignee.md)
- [ControlLogReceiptImageFormat](docs/Model/ControlLogReceiptImageFormat.md)
- [CreditCardAddress](docs/Model/CreditCardAddress.md)
- [DDTCInformationUnitOfMeasurement](docs/Model/DDTCInformationUnitOfMeasurement.md)
- [DeclaredValueType](docs/Model/DeclaredValueType.md)
- [DimWeightUnitOfMeasurement](docs/Model/DimWeightUnitOfMeasurement.md)
- [DimensionsUnitOfMeasurement](docs/Model/DimensionsUnitOfMeasurement.md)
- [DryIceDryIceWeight](docs/Model/DryIceDryIceWeight.md)
- [DryIceWeightUnitOfMeasurement](docs/Model/DryIceWeightUnitOfMeasurement.md)
- [EEIFilingOptionShipperFiled](docs/Model/EEIFilingOptionShipperFiled.md)
- [EEIFilingOptionUPSFiled](docs/Model/EEIFilingOptionUPSFiled.md)
- [EEIInformationDDTCInformation](docs/Model/EEIInformationDDTCInformation.md)
- [EEIInformationLicense](docs/Model/EEIInformationLicense.md)
- [ErrorMessage](docs/Model/ErrorMessage.md)
- [ErrorResponse](docs/Model/ErrorResponse.md)
- [FRSPaymentInformationAddress](docs/Model/FRSPaymentInformationAddress.md)
- [FRSPaymentInformationType](docs/Model/FRSPaymentInformationType.md)
- [FRSShipmentDataFreightDensityRate](docs/Model/FRSShipmentDataFreightDensityRate.md)
- [FRSShipmentDataHandlingUnits](docs/Model/FRSShipmentDataHandlingUnits.md)
- [FRSShipmentDataTransportationCharges](docs/Model/FRSShipmentDataTransportationCharges.md)
- [FormImage](docs/Model/FormImage.md)
- [ForwardAgentAddress](docs/Model/ForwardAgentAddress.md)
- [FreightDensityInfoAdjustedHeight](docs/Model/FreightDensityInfoAdjustedHeight.md)
- [FreightDensityInfoHandlingUnits](docs/Model/FreightDensityInfoHandlingUnits.md)
- [FreightShipmentInformationFreightDensityInfo](docs/Model/FreightShipmentInformationFreightDensityInfo.md)
- [GlobalTaxInformationAgentTaxIdentificationNumber](docs/Model/GlobalTaxInformationAgentTaxIdentificationNumber.md)
- [HandlingUnitsAdjustedHeight](docs/Model/HandlingUnitsAdjustedHeight.md)
- [HandlingUnitsDimensions](docs/Model/HandlingUnitsDimensions.md)
- [HandlingUnitsType](docs/Model/HandlingUnitsType.md)
- [HandlingUnitsUnitOfMeasurement](docs/Model/HandlingUnitsUnitOfMeasurement.md)
- [HighValueReportImage](docs/Model/HighValueReportImage.md)
- [HighValueReportImageImageFormat](docs/Model/HighValueReportImageImageFormat.md)
- [ImageImageFormat](docs/Model/ImageImageFormat.md)
- [IntermediateConsigneeAddress](docs/Model/IntermediateConsigneeAddress.md)
- [InternationalFormsBlanketPeriod](docs/Model/InternationalFormsBlanketPeriod.md)
- [InternationalFormsCN22Form](docs/Model/InternationalFormsCN22Form.md)
- [InternationalFormsContacts](docs/Model/InternationalFormsContacts.md)
- [InternationalFormsDiscount](docs/Model/InternationalFormsDiscount.md)
- [InternationalFormsEEIFilingOption](docs/Model/InternationalFormsEEIFilingOption.md)
- [InternationalFormsFreightCharges](docs/Model/InternationalFormsFreightCharges.md)
- [InternationalFormsInsuranceCharges](docs/Model/InternationalFormsInsuranceCharges.md)
- [InternationalFormsOtherCharges](docs/Model/InternationalFormsOtherCharges.md)
- [InternationalFormsProduct](docs/Model/InternationalFormsProduct.md)
- [InternationalFormsUPSPremiumCareForm](docs/Model/InternationalFormsUPSPremiumCareForm.md)
- [InternationalFormsUserCreatedForm](docs/Model/InternationalFormsUserCreatedForm.md)
- [LABELRECOVERYRequestWrapper](docs/Model/LABELRECOVERYRequestWrapper.md)
- [LABELRECOVERYResponseWrapper](docs/Model/LABELRECOVERYResponseWrapper.md)
- [LRCODTurnInPageImage](docs/Model/LRCODTurnInPageImage.md)
- [LRCODTurnInPageImageImageFormat](docs/Model/LRCODTurnInPageImageImageFormat.md)
- [LRFormImage](docs/Model/LRFormImage.md)
- [LRRequestTransactionReference](docs/Model/LRRequestTransactionReference.md)
- [LRResponseResponseStatus](docs/Model/LRResponseResponseStatus.md)
- [LRResponseTransactionReference](docs/Model/LRResponseTransactionReference.md)
- [LTLDimensions](docs/Model/LTLDimensions.md)
- [LTLHandlingUnits](docs/Model/LTLHandlingUnits.md)
- [LTLOtherCharges](docs/Model/LTLOtherCharges.md)
- [LTLPackageWeightType](docs/Model/LTLPackageWeightType.md)
- [LTLReferenceNumber](docs/Model/LTLReferenceNumber.md)
- [LabelDeliveryEMail](docs/Model/LabelDeliveryEMail.md)
- [LabelImageLabelImageFormat](docs/Model/LabelImageLabelImageFormat.md)
- [LabelRecoveryFormImage](docs/Model/LabelRecoveryFormImage.md)
- [LabelRecoveryImageImageFormat](docs/Model/LabelRecoveryImageImageFormat.md)
- [LabelRecoveryLabelSpecificationLabelImageFormat](docs/Model/LabelRecoveryLabelSpecificationLabelImageFormat.md)
- [LabelRecoveryLabelSpecificationLabelStockSize](docs/Model/LabelRecoveryLabelSpecificationLabelStockSize.md)
- [LabelRecoveryRequest](docs/Model/LabelRecoveryRequest.md)
- [LabelRecoveryRequestLabelDelivery](docs/Model/LabelRecoveryRequestLabelDelivery.md)
- [LabelRecoveryRequestLabelSpecification](docs/Model/LabelRecoveryRequestLabelSpecification.md)
- [LabelRecoveryRequestReferenceValues](docs/Model/LabelRecoveryRequestReferenceValues.md)
- [LabelRecoveryRequestRequest](docs/Model/LabelRecoveryRequestRequest.md)
- [LabelRecoveryRequestTranslate](docs/Model/LabelRecoveryRequestTranslate.md)
- [LabelRecoveryRequestUPSPremiumCareForm](docs/Model/LabelRecoveryRequestUPSPremiumCareForm.md)
- [LabelRecoveryResponse](docs/Model/LabelRecoveryResponse.md)
- [LabelRecoveryResponseCODTurnInPage](docs/Model/LabelRecoveryResponseCODTurnInPage.md)
- [LabelRecoveryResponseForm](docs/Model/LabelRecoveryResponseForm.md)
- [LabelRecoveryResponseHighValueReport](docs/Model/LabelRecoveryResponseHighValueReport.md)
- [LabelRecoveryResponseLabelResults](docs/Model/LabelRecoveryResponseLabelResults.md)
- [LabelRecoveryResponseResponse](docs/Model/LabelRecoveryResponseResponse.md)
- [LabelRecoveryResponseTrackingCandidate](docs/Model/LabelRecoveryResponseTrackingCandidate.md)
- [LabelResultsForm](docs/Model/LabelResultsForm.md)
- [LabelResultsLabelImage](docs/Model/LabelResultsLabelImage.md)
- [LabelResultsMailInnovationsLabelImage](docs/Model/LabelResultsMailInnovationsLabelImage.md)
- [LabelResultsReceipt](docs/Model/LabelResultsReceipt.md)
- [LabelSpecificationInstruction](docs/Model/LabelSpecificationInstruction.md)
- [LabelSpecificationLabelImageFormat](docs/Model/LabelSpecificationLabelImageFormat.md)
- [LabelSpecificationLabelStockSize](docs/Model/LabelSpecificationLabelStockSize.md)
- [MailInnovationsLabelImageLabelImageFormat](docs/Model/MailInnovationsLabelImageLabelImageFormat.md)
- [MasterPickup](docs/Model/MasterPickup.md)
- [MasterSoldTo](docs/Model/MasterSoldTo.md)
- [MasterTradeComplianceDetails](docs/Model/MasterTradeComplianceDetails.md)
- [NegotiatedChargesItemizedCharges](docs/Model/NegotiatedChargesItemizedCharges.md)
- [NegotiatedChargesRateModifier](docs/Model/NegotiatedChargesRateModifier.md)
- [NegotiatedRateChargesItemizedCharges](docs/Model/NegotiatedRateChargesItemizedCharges.md)
- [NegotiatedRateChargesRateModifier](docs/Model/NegotiatedRateChargesRateModifier.md)
- [NegotiatedRateChargesTaxCharges](docs/Model/NegotiatedRateChargesTaxCharges.md)
- [NegotiatedRateChargesTotalCharge](docs/Model/NegotiatedRateChargesTotalCharge.md)
- [NegotiatedRateChargesTotalChargesWithTaxes](docs/Model/NegotiatedRateChargesTotalChargesWithTaxes.md)
- [NotificationEMail](docs/Model/NotificationEMail.md)
- [NotificationLocale](docs/Model/NotificationLocale.md)
- [NotificationTextMessage](docs/Model/NotificationTextMessage.md)
- [NotificationVoiceMessage](docs/Model/NotificationVoiceMessage.md)
- [PackageCommodity](docs/Model/PackageCommodity.md)
- [PackageDimWeight](docs/Model/PackageDimWeight.md)
- [PackageDimensions](docs/Model/PackageDimensions.md)
- [PackageHazMatPackageInformation](docs/Model/PackageHazMatPackageInformation.md)
- [PackageLevelResultsStatus](docs/Model/PackageLevelResultsStatus.md)
- [PackagePackageServiceOptions](docs/Model/PackagePackageServiceOptions.md)
- [PackagePackageWeight](docs/Model/PackagePackageWeight.md)
- [PackagePackaging](docs/Model/PackagePackaging.md)
- [PackageReferenceNumber](docs/Model/PackageReferenceNumber.md)
- [PackageResultsAccessorial](docs/Model/PackageResultsAccessorial.md)
- [PackageResultsBaseServiceCharge](docs/Model/PackageResultsBaseServiceCharge.md)
- [PackageResultsForm](docs/Model/PackageResultsForm.md)
- [PackageResultsItemizedCharges](docs/Model/PackageResultsItemizedCharges.md)
- [PackageResultsNegotiatedCharges](docs/Model/PackageResultsNegotiatedCharges.md)
- [PackageResultsRateModifier](docs/Model/PackageResultsRateModifier.md)
- [PackageResultsServiceOptionsCharges](docs/Model/PackageResultsServiceOptionsCharges.md)
- [PackageResultsShippingLabel](docs/Model/PackageResultsShippingLabel.md)
- [PackageResultsShippingReceipt](docs/Model/PackageResultsShippingReceipt.md)
- [PackageResultsSimpleRate](docs/Model/PackageResultsSimpleRate.md)
- [PackageServiceOptionsAccessPointCOD](docs/Model/PackageServiceOptionsAccessPointCOD.md)
- [PackageServiceOptionsCOD](docs/Model/PackageServiceOptionsCOD.md)
- [PackageServiceOptionsCODCODAmount](docs/Model/PackageServiceOptionsCODCODAmount.md)
- [PackageServiceOptionsDeclaredValue](docs/Model/PackageServiceOptionsDeclaredValue.md)
- [PackageServiceOptionsDeliveryConfirmation](docs/Model/PackageServiceOptionsDeliveryConfirmation.md)
- [PackageServiceOptionsDryIce](docs/Model/PackageServiceOptionsDryIce.md)
- [PackageServiceOptionsHazMat](docs/Model/PackageServiceOptionsHazMat.md)
- [PackageServiceOptionsNotification](docs/Model/PackageServiceOptionsNotification.md)
- [PackageServiceOptionsNotificationEMail](docs/Model/PackageServiceOptionsNotificationEMail.md)
- [PackageSimpleRate](docs/Model/PackageSimpleRate.md)
- [PackageUPSPremier](docs/Model/PackageUPSPremier.md)
- [PackageWeightUnitOfMeasurement](docs/Model/PackageWeightUnitOfMeasurement.md)
- [PackingListInfoPackageAssociated](docs/Model/PackingListInfoPackageAssociated.md)
- [PaymentInformationShipmentCharge](docs/Model/PaymentInformationShipmentCharge.md)
- [PreAlertNotificationEMailMessage](docs/Model/PreAlertNotificationEMailMessage.md)
- [PreAlertNotificationLocale](docs/Model/PreAlertNotificationLocale.md)
- [PreAlertNotificationTextMessage](docs/Model/PreAlertNotificationTextMessage.md)
- [PreAlertNotificationVoiceMessage](docs/Model/PreAlertNotificationVoiceMessage.md)
- [ProducerAddress](docs/Model/ProducerAddress.md)
- [ProducerPhone](docs/Model/ProducerPhone.md)
- [ProductEEIInformation](docs/Model/ProductEEIInformation.md)
- [ProductExcludeFromForm](docs/Model/ProductExcludeFromForm.md)
- [ProductNetCostDateRange](docs/Model/ProductNetCostDateRange.md)
- [ProductPackingListInfo](docs/Model/ProductPackingListInfo.md)
- [ProductProductWeight](docs/Model/ProductProductWeight.md)
- [ProductScheduleB](docs/Model/ProductScheduleB.md)
- [ProductUnit](docs/Model/ProductUnit.md)
- [ProductWeightUnitOfMeasurement](docs/Model/ProductWeightUnitOfMeasurement.md)
- [ReceiptImage](docs/Model/ReceiptImage.md)
- [ReceiptImageImageFormat](docs/Model/ReceiptImageImageFormat.md)
- [ReceiptSpecificationImageFormat](docs/Model/ReceiptSpecificationImageFormat.md)
- [ReferenceValuesReferenceNumber](docs/Model/ReferenceValuesReferenceNumber.md)
- [RequestTransactionReference](docs/Model/RequestTransactionReference.md)
- [ResponseAlert](docs/Model/ResponseAlert.md)
- [ResponseResponseStatus](docs/Model/ResponseResponseStatus.md)
- [ResponseTransactionReference](docs/Model/ResponseTransactionReference.md)
- [SHIPRequestWrapper](docs/Model/SHIPRequestWrapper.md)
- [SHIPResponseWrapper](docs/Model/SHIPResponseWrapper.md)
- [ScheduleBUnitOfMeasurement](docs/Model/ScheduleBUnitOfMeasurement.md)
- [ShipFromAddress](docs/Model/ShipFromAddress.md)
- [ShipFromPhone](docs/Model/ShipFromPhone.md)
- [ShipFromTaxIDType](docs/Model/ShipFromTaxIDType.md)
- [ShipFromVendorInfo](docs/Model/ShipFromVendorInfo.md)
- [ShipToAddress](docs/Model/ShipToAddress.md)
- [ShipToPhone](docs/Model/ShipToPhone.md)
- [ShipmentAlternateDeliveryAddress](docs/Model/ShipmentAlternateDeliveryAddress.md)
- [ShipmentChargeBillReceiver](docs/Model/ShipmentChargeBillReceiver.md)
- [ShipmentChargeBillShipper](docs/Model/ShipmentChargeBillShipper.md)
- [ShipmentChargeBillThirdParty](docs/Model/ShipmentChargeBillThirdParty.md)
- [ShipmentChargesBaseServiceCharge](docs/Model/ShipmentChargesBaseServiceCharge.md)
- [ShipmentChargesItemizedCharges](docs/Model/ShipmentChargesItemizedCharges.md)
- [ShipmentChargesServiceOptionsCharges](docs/Model/ShipmentChargesServiceOptionsCharges.md)
- [ShipmentChargesTaxCharges](docs/Model/ShipmentChargesTaxCharges.md)
- [ShipmentChargesTotalCharges](docs/Model/ShipmentChargesTotalCharges.md)
- [ShipmentChargesTotalChargesWithTaxes](docs/Model/ShipmentChargesTotalChargesWithTaxes.md)
- [ShipmentChargesTransportationCharges](docs/Model/ShipmentChargesTransportationCharges.md)
- [ShipmentDGSignatoryInfo](docs/Model/ShipmentDGSignatoryInfo.md)
- [ShipmentFRSPaymentInformation](docs/Model/ShipmentFRSPaymentInformation.md)
- [ShipmentFreightShipmentInformation](docs/Model/ShipmentFreightShipmentInformation.md)
- [ShipmentGlobalTaxInformation](docs/Model/ShipmentGlobalTaxInformation.md)
- [ShipmentInvoiceLineTotal](docs/Model/ShipmentInvoiceLineTotal.md)
- [ShipmentPackage](docs/Model/ShipmentPackage.md)
- [ShipmentPaymentInformation](docs/Model/ShipmentPaymentInformation.md)
- [ShipmentPromotionalDiscountInformation](docs/Model/ShipmentPromotionalDiscountInformation.md)
- [ShipmentReferenceNumber](docs/Model/ShipmentReferenceNumber.md)
- [ShipmentRequest](docs/Model/ShipmentRequest.md)
- [ShipmentRequestLabelSpecification](docs/Model/ShipmentRequestLabelSpecification.md)
- [ShipmentRequestReceiptSpecification](docs/Model/ShipmentRequestReceiptSpecification.md)
- [ShipmentRequestRequest](docs/Model/ShipmentRequestRequest.md)
- [ShipmentRequestShipment](docs/Model/ShipmentRequestShipment.md)
- [ShipmentResponse](docs/Model/ShipmentResponse.md)
- [ShipmentResponseResponse](docs/Model/ShipmentResponseResponse.md)
- [ShipmentResponseShipmentResults](docs/Model/ShipmentResponseShipmentResults.md)
- [ShipmentResultsBillingWeight](docs/Model/ShipmentResultsBillingWeight.md)
- [ShipmentResultsCODTurnInPage](docs/Model/ShipmentResultsCODTurnInPage.md)
- [ShipmentResultsControlLogReceipt](docs/Model/ShipmentResultsControlLogReceipt.md)
- [ShipmentResultsDisclaimer](docs/Model/ShipmentResultsDisclaimer.md)
- [ShipmentResultsFRSShipmentData](docs/Model/ShipmentResultsFRSShipmentData.md)
- [ShipmentResultsForm](docs/Model/ShipmentResultsForm.md)
- [ShipmentResultsFormImage](docs/Model/ShipmentResultsFormImage.md)
- [ShipmentResultsHighValueReport](docs/Model/ShipmentResultsHighValueReport.md)
- [ShipmentResultsImageImageFormat](docs/Model/ShipmentResultsImageImageFormat.md)
- [ShipmentResultsNegotiatedRateCharges](docs/Model/ShipmentResultsNegotiatedRateCharges.md)
- [ShipmentResultsPackageResults](docs/Model/ShipmentResultsPackageResults.md)
- [ShipmentResultsPalletLabel](docs/Model/ShipmentResultsPalletLabel.md)
- [ShipmentResultsShipmentCharges](docs/Model/ShipmentResultsShipmentCharges.md)
- [ShipmentReturnService](docs/Model/ShipmentReturnService.md)
- [ShipmentService](docs/Model/ShipmentService.md)
- [ShipmentServiceOptionsAccessPointCOD](docs/Model/ShipmentServiceOptionsAccessPointCOD.md)
- [ShipmentServiceOptionsCOD](docs/Model/ShipmentServiceOptionsCOD.md)
- [ShipmentServiceOptionsDeliveryConfirmation](docs/Model/ShipmentServiceOptionsDeliveryConfirmation.md)
- [ShipmentServiceOptionsInternationalForms](docs/Model/ShipmentServiceOptionsInternationalForms.md)
- [ShipmentServiceOptionsLabelDelivery](docs/Model/ShipmentServiceOptionsLabelDelivery.md)
- [ShipmentServiceOptionsLabelMethod](docs/Model/ShipmentServiceOptionsLabelMethod.md)
- [ShipmentServiceOptionsNotification](docs/Model/ShipmentServiceOptionsNotification.md)
- [ShipmentServiceOptionsPreAlertNotification](docs/Model/ShipmentServiceOptionsPreAlertNotification.md)
- [ShipmentServiceOptionsRestrictedArticles](docs/Model/ShipmentServiceOptionsRestrictedArticles.md)
- [ShipmentShipFrom](docs/Model/ShipmentShipFrom.md)
- [ShipmentShipTo](docs/Model/ShipmentShipTo.md)
- [ShipmentShipmentIndicationType](docs/Model/ShipmentShipmentIndicationType.md)
- [ShipmentShipmentRatingOptions](docs/Model/ShipmentShipmentRatingOptions.md)
- [ShipmentShipmentServiceOptions](docs/Model/ShipmentShipmentServiceOptions.md)
- [ShipmentShipper](docs/Model/ShipmentShipper.md)
- [ShipmentTradeDirect](docs/Model/ShipmentTradeDirect.md)
- [ShipmentWorldEase](docs/Model/ShipmentWorldEase.md)
- [ShipmentWorldEasePortOfEntry](docs/Model/ShipmentWorldEasePortOfEntry.md)
- [ShipperAddress](docs/Model/ShipperAddress.md)
- [ShipperPhone](docs/Model/ShipperPhone.md)
- [ShippingLabelImageFormat](docs/Model/ShippingLabelImageFormat.md)
- [ShippingReceiptImageFormat](docs/Model/ShippingReceiptImageFormat.md)
- [SoldToAddress](docs/Model/SoldToAddress.md)
- [SoldToPhone](docs/Model/SoldToPhone.md)
- [SummaryResultStatus](docs/Model/SummaryResultStatus.md)
- [TrackingCandidatePickupDateRange](docs/Model/TrackingCandidatePickupDateRange.md)
- [TradeDirectAddress](docs/Model/TradeDirectAddress.md)
- [TradeDirectChild](docs/Model/TradeDirectChild.md)
- [TradeDirectMaster](docs/Model/TradeDirectMaster.md)
- [TradeDirectNotificationBeforeDelivery](docs/Model/TradeDirectNotificationBeforeDelivery.md)
- [TradeDirectPhone](docs/Model/TradeDirectPhone.md)
- [TransportationChargesDiscountAmount](docs/Model/TransportationChargesDiscountAmount.md)
- [TransportationChargesGrossCharge](docs/Model/TransportationChargesGrossCharge.md)
- [TransportationChargesNetCharge](docs/Model/TransportationChargesNetCharge.md)
- [UPSFiledPOA](docs/Model/UPSFiledPOA.md)
- [UPSPremierHandlingInstructions](docs/Model/UPSPremierHandlingInstructions.md)
- [UPSPremiumCareFormLanguageForUPSPremiumCare](docs/Model/UPSPremiumCareFormLanguageForUPSPremiumCare.md)
- [UltimateConsigneeAddress](docs/Model/UltimateConsigneeAddress.md)
- [UltimateConsigneeUltimateConsigneeType](docs/Model/UltimateConsigneeUltimateConsigneeType.md)
- [UnitUnitOfMeasurement](docs/Model/UnitUnitOfMeasurement.md)
- [VOIDSHIPMENTRequestWrapper](docs/Model/VOIDSHIPMENTRequestWrapper.md)
- [VOIDSHIPMENTResponseWrapper](docs/Model/VOIDSHIPMENTResponseWrapper.md)
- [VoidRequestTransactionReference](docs/Model/VoidRequestTransactionReference.md)
- [VoidResponseResponseStatus](docs/Model/VoidResponseResponseStatus.md)
- [VoidResponseTransactionReference](docs/Model/VoidResponseTransactionReference.md)
- [VoidShipmentRequest](docs/Model/VoidShipmentRequest.md)
- [VoidShipmentRequestRequest](docs/Model/VoidShipmentRequestRequest.md)
- [VoidShipmentRequestVoidShipment](docs/Model/VoidShipmentRequestVoidShipment.md)
- [VoidShipmentResponse](docs/Model/VoidShipmentResponse.md)
- [VoidShipmentResponsePackageLevelResults](docs/Model/VoidShipmentResponsePackageLevelResults.md)
- [VoidShipmentResponseResponse](docs/Model/VoidShipmentResponseResponse.md)
- [VoidShipmentResponseSummaryResult](docs/Model/VoidShipmentResponseSummaryResult.md)

## Authorization

Authentication schemes defined for the API:
### OAuth2

- **Type**: `OAuth`
- **Flow**: `application`
- **Authorization URL**: ``
- **Scopes**: N/A

## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: ``
    - Generator version: `7.14.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
