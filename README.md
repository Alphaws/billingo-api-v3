# SwaggerClient-php
This is a Billingo API v3 documentation. Our API based on REST software architectural style. API has resource-oriented URLs, accepts JSON-encoded request bodies and returns JSON-encoded responses. To use this API you have to generate a new API key on our [site](https://app.billingo.hu/api-key). After that, you can test your API key on this page.

This PHP package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 3.0.14
- Build package: io.swagger.codegen.v3.generators.php.PhpClientCodegen
For more information, please visit [https://www.billingo.hu/kapcsolat](https://www.billingo.hu/kapcsolat)

## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
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
    require_once('/path/to/SwaggerClient-php/vendor/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');

$apiInstance = new Swagger\Client\Api\BankAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\BankAccount(); // \Swagger\Client\Model\BankAccount | BankAccount object that you would like to store.

try {
    $result = $apiInstance->createBankAccount($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BankAccountApi->createBankAccount: ', $e->getMessage(), PHP_EOL;
}

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');

$apiInstance = new Swagger\Client\Api\BankAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | 

try {
    $apiInstance->deleteBankAccount($id);
} catch (Exception $e) {
    echo 'Exception when calling BankAccountApi->deleteBankAccount: ', $e->getMessage(), PHP_EOL;
}

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');

$apiInstance = new Swagger\Client\Api\BankAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | 

try {
    $result = $apiInstance->getBankAccount($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BankAccountApi->getBankAccount: ', $e->getMessage(), PHP_EOL;
}

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');

$apiInstance = new Swagger\Client\Api\BankAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int | 
$per_page = 25; // int | 

try {
    $result = $apiInstance->listBankAccount($page, $per_page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BankAccountApi->listBankAccount: ', $e->getMessage(), PHP_EOL;
}

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');

$apiInstance = new Swagger\Client\Api\BankAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\BankAccount(); // \Swagger\Client\Model\BankAccount | Bank account object that you would like to update.
$id = 56; // int | 

try {
    $result = $apiInstance->updateBankAccount($body, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BankAccountApi->updateBankAccount: ', $e->getMessage(), PHP_EOL;
}
?>
```

## Documentation for API Endpoints

All URIs are relative to *https://api.billingo.hu/v3*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*BankAccountApi* | [**createBankAccount**](docs/Api/BankAccountApi.md#createbankaccount) | **POST** /bank-accounts | Create a bank account
*BankAccountApi* | [**deleteBankAccount**](docs/Api/BankAccountApi.md#deletebankaccount) | **DELETE** /bank-accounts/{id} | Delete a bank account
*BankAccountApi* | [**getBankAccount**](docs/Api/BankAccountApi.md#getbankaccount) | **GET** /bank-accounts/{id} | Retrieve a bank account
*BankAccountApi* | [**listBankAccount**](docs/Api/BankAccountApi.md#listbankaccount) | **GET** /bank-accounts | List all bank account
*BankAccountApi* | [**updateBankAccount**](docs/Api/BankAccountApi.md#updatebankaccount) | **PUT** /bank-accounts/{id} | Update a bank account
*CurrencyApi* | [**getConversionRate**](docs/Api/CurrencyApi.md#getconversionrate) | **GET** /currencies | Get currencies exchange rate.
*DocumentApi* | [**archiveDocument**](docs/Api/DocumentApi.md#archivedocument) | **PUT** /documents/{id}/archive | Archive a proforma document.
*DocumentApi* | [**cancelDocument**](docs/Api/DocumentApi.md#canceldocument) | **POST** /documents/{id}/cancel | Cancel a document
*DocumentApi* | [**createDocument**](docs/Api/DocumentApi.md#createdocument) | **POST** /documents | Create a document
*DocumentApi* | [**createDocumentFromDraft**](docs/Api/DocumentApi.md#createdocumentfromdraft) | **PUT** /documents/{id} | Converts a draft to an invoice.
*DocumentApi* | [**createDocumentFromProforma**](docs/Api/DocumentApi.md#createdocumentfromproforma) | **POST** /documents/{id}/create-from-proforma | Create a document from proforma.
*DocumentApi* | [**createModificationDocument**](docs/Api/DocumentApi.md#createmodificationdocument) | **POST** /documents/{id}/create-modification-document | Create a modification document.
*DocumentApi* | [**deleteDocument**](docs/Api/DocumentApi.md#deletedocument) | **DELETE** /documents/{id} | Delete a draft.
*DocumentApi* | [**deletePayment**](docs/Api/DocumentApi.md#deletepayment) | **DELETE** /documents/{id}/payments | Delete all payment history on document
*DocumentApi* | [**documentCopy**](docs/Api/DocumentApi.md#documentcopy) | **POST** /documents/{id}/copy | Copy a document
*DocumentApi* | [**downloadDocument**](docs/Api/DocumentApi.md#downloaddocument) | **GET** /documents/{id}/download | Download a document in PDF format.
*DocumentApi* | [**getDocument**](docs/Api/DocumentApi.md#getdocument) | **GET** /documents/{id} | Retrieve a document
*DocumentApi* | [**getOnlineSzamlaStatus**](docs/Api/DocumentApi.md#getonlineszamlastatus) | **GET** /documents/{id}/online-szamla | Retrieve a document Online Számla status
*DocumentApi* | [**getPayment**](docs/Api/DocumentApi.md#getpayment) | **GET** /documents/{id}/payments | Retrieve a payment histroy
*DocumentApi* | [**getPublicUrl**](docs/Api/DocumentApi.md#getpublicurl) | **GET** /documents/{id}/public-url | Retrieve a document download public url.
*DocumentApi* | [**listDocument**](docs/Api/DocumentApi.md#listdocument) | **GET** /documents | List all documents
*DocumentApi* | [**posPrint**](docs/Api/DocumentApi.md#posprint) | **GET** /documents/{id}/print/pos | Returns a printable POS PDF
*DocumentApi* | [**sendDocument**](docs/Api/DocumentApi.md#senddocument) | **POST** /documents/{id}/send | Send invoice to given email adresses.
*DocumentApi* | [**updatePayment**](docs/Api/DocumentApi.md#updatepayment) | **PUT** /documents/{id}/payments | Update payment history
*DocumentBlockApi* | [**listDocumentBlock**](docs/Api/DocumentBlockApi.md#listdocumentblock) | **GET** /document-blocks | List all document blocks
*DocumentExportApi* | [**create**](docs/Api/DocumentExportApi.md#create) | **POST** /document-export | Create document export.
*DocumentExportApi* | [**download**](docs/Api/DocumentExportApi.md#download) | **GET** /document-export/{id}/download | Return exported binary file.
*DocumentExportApi* | [**poll**](docs/Api/DocumentExportApi.md#poll) | **GET** /document-export/{id}/poll | Retrieve export state.
*OrganizationApi* | [**getOrganizationData**](docs/Api/OrganizationApi.md#getorganizationdata) | **GET** /organization | Retrieve a organization data.
*PartnerApi* | [**createPartner**](docs/Api/PartnerApi.md#createpartner) | **POST** /partners | Create a partner
*PartnerApi* | [**deletePartner**](docs/Api/PartnerApi.md#deletepartner) | **DELETE** /partners/{id} | Delete a partner
*PartnerApi* | [**getPartner**](docs/Api/PartnerApi.md#getpartner) | **GET** /partners/{id} | Retrieve a partner
*PartnerApi* | [**listPartner**](docs/Api/PartnerApi.md#listpartner) | **GET** /partners | List all partners
*PartnerApi* | [**updatePartner**](docs/Api/PartnerApi.md#updatepartner) | **PUT** /partners/{id} | Update a partner
*ProductApi* | [**createProduct**](docs/Api/ProductApi.md#createproduct) | **POST** /products | Create a product
*ProductApi* | [**deleteProduct**](docs/Api/ProductApi.md#deleteproduct) | **DELETE** /products/{id} | Delete a product
*ProductApi* | [**getProduct**](docs/Api/ProductApi.md#getproduct) | **GET** /products/{id} | Retrieve a product
*ProductApi* | [**listProduct**](docs/Api/ProductApi.md#listproduct) | **GET** /products | List all product
*ProductApi* | [**updateProduct**](docs/Api/ProductApi.md#updateproduct) | **PUT** /products/{id} | Update a product
*SpendingApi* | [**spendingDelete**](docs/Api/SpendingApi.md#spendingdelete) | **DELETE** /spendings/{id} | Deletes a spending.
*SpendingApi* | [**spendingList**](docs/Api/SpendingApi.md#spendinglist) | **GET** /spendings | Lists all spending
*SpendingApi* | [**spendingSave**](docs/Api/SpendingApi.md#spendingsave) | **POST** /spendings | Creates a new spending.
*SpendingApi* | [**spendingShow**](docs/Api/SpendingApi.md#spendingshow) | **GET** /spendings/{id} | Retrieves one specific spending.
*SpendingApi* | [**spendingUpdate**](docs/Api/SpendingApi.md#spendingupdate) | **PUT** /spendings/{id} | Updates a spending item.
*UtilApi* | [**checkTaxNumber**](docs/Api/UtilApi.md#checktaxnumber) | **GET** /utils/check-tax-number/{tax_number} | Check tax number.
*UtilApi* | [**getId**](docs/Api/UtilApi.md#getid) | **GET** /utils/convert-legacy-id/{id} | Convert legacy ID to v3 ID.

## Documentation For Models

 - [Address](docs/Model/Address.md)
 - [BankAccount](docs/Model/BankAccount.md)
 - [BankAccountList](docs/Model/BankAccountList.md)
 - [Category](docs/Model/Category.md)
 - [CheckTaxNumberMessage](docs/Model/CheckTaxNumberMessage.md)
 - [ClientError](docs/Model/ClientError.md)
 - [ClientErrorResponse](docs/Model/ClientErrorResponse.md)
 - [ConversationRate](docs/Model/ConversationRate.md)
 - [CorrectionType](docs/Model/CorrectionType.md)
 - [Country](docs/Model/Country.md)
 - [CreateDocumentExport](docs/Model/CreateDocumentExport.md)
 - [Currency](docs/Model/Currency.md)
 - [Discount](docs/Model/Discount.md)
 - [DiscountType](docs/Model/DiscountType.md)
 - [Document](docs/Model/Document.md)
 - [DocumentAncestor](docs/Model/DocumentAncestor.md)
 - [DocumentBankAccount](docs/Model/DocumentBankAccount.md)
 - [DocumentBlock](docs/Model/DocumentBlock.md)
 - [DocumentBlockList](docs/Model/DocumentBlockList.md)
 - [DocumentCancellation](docs/Model/DocumentCancellation.md)
 - [DocumentExportFilterExtra](docs/Model/DocumentExportFilterExtra.md)
 - [DocumentExportId](docs/Model/DocumentExportId.md)
 - [DocumentExportOtherOptions](docs/Model/DocumentExportOtherOptions.md)
 - [DocumentExportQueryType](docs/Model/DocumentExportQueryType.md)
 - [DocumentExportSortBy](docs/Model/DocumentExportSortBy.md)
 - [DocumentExportStatus](docs/Model/DocumentExportStatus.md)
 - [DocumentExportStatusState](docs/Model/DocumentExportStatusState.md)
 - [DocumentExportType](docs/Model/DocumentExportType.md)
 - [DocumentForm](docs/Model/DocumentForm.md)
 - [DocumentFormat](docs/Model/DocumentFormat.md)
 - [DocumentInsert](docs/Model/DocumentInsert.md)
 - [DocumentInsertType](docs/Model/DocumentInsertType.md)
 - [DocumentItem](docs/Model/DocumentItem.md)
 - [DocumentItemData](docs/Model/DocumentItemData.md)
 - [DocumentLanguage](docs/Model/DocumentLanguage.md)
 - [DocumentList](docs/Model/DocumentList.md)
 - [DocumentNotificationStatus](docs/Model/DocumentNotificationStatus.md)
 - [DocumentOrganization](docs/Model/DocumentOrganization.md)
 - [DocumentPartner](docs/Model/DocumentPartner.md)
 - [DocumentProductData](docs/Model/DocumentProductData.md)
 - [DocumentPublicUrl](docs/Model/DocumentPublicUrl.md)
 - [DocumentSettings](docs/Model/DocumentSettings.md)
 - [DocumentSummary](docs/Model/DocumentSummary.md)
 - [DocumentType](docs/Model/DocumentType.md)
 - [DocumentVatRateSummary](docs/Model/DocumentVatRateSummary.md)
 - [Entitlement](docs/Model/Entitlement.md)
 - [Id](docs/Model/Id.md)
 - [InvoiceSettings](docs/Model/InvoiceSettings.md)
 - [LedgerNumberInformation](docs/Model/LedgerNumberInformation.md)
 - [ModificationDocumentInsert](docs/Model/ModificationDocumentInsert.md)
 - [OneOfDocumentDiscount](docs/Model/OneOfDocumentDiscount.md)
 - [OneOfDocumentInsertDiscount](docs/Model/OneOfDocumentInsertDiscount.md)
 - [OneOfDocumentInsertItemsItems](docs/Model/OneOfDocumentInsertItemsItems.md)
 - [OneOfInvoiceSettingsDocumentFormat](docs/Model/OneOfInvoiceSettingsDocumentFormat.md)
 - [OneOfInvoiceSettingsDocumentType](docs/Model/OneOfInvoiceSettingsDocumentType.md)
 - [OneOfModificationDocumentInsertItemsItems](docs/Model/OneOfModificationDocumentInsertItemsItems.md)
 - [OnlinePayment](docs/Model/OnlinePayment.md)
 - [OnlineSzamlaStatus](docs/Model/OnlineSzamlaStatus.md)
 - [OnlineSzamlaStatusEnum](docs/Model/OnlineSzamlaStatusEnum.md)
 - [OnlineSzamlaStatusMessage](docs/Model/OnlineSzamlaStatusMessage.md)
 - [OrganizationData](docs/Model/OrganizationData.md)
 - [Partner](docs/Model/Partner.md)
 - [PartnerCustomBillingSettings](docs/Model/PartnerCustomBillingSettings.md)
 - [PartnerList](docs/Model/PartnerList.md)
 - [PartnerTaxType](docs/Model/PartnerTaxType.md)
 - [PaymentHistory](docs/Model/PaymentHistory.md)
 - [PaymentMethod](docs/Model/PaymentMethod.md)
 - [PaymentStatus](docs/Model/PaymentStatus.md)
 - [Product](docs/Model/Product.md)
 - [ProductList](docs/Model/ProductList.md)
 - [Round](docs/Model/Round.md)
 - [SendDocument](docs/Model/SendDocument.md)
 - [ServerError](docs/Model/ServerError.md)
 - [ServerErrorResponse](docs/Model/ServerErrorResponse.md)
 - [Spending](docs/Model/Spending.md)
 - [SpendingList](docs/Model/SpendingList.md)
 - [SpendingListItem](docs/Model/SpendingListItem.md)
 - [SpendingPartner](docs/Model/SpendingPartner.md)
 - [SpendingPaymentMethod](docs/Model/SpendingPaymentMethod.md)
 - [SpendingSave](docs/Model/SpendingSave.md)
 - [Subscription](docs/Model/Subscription.md)
 - [SubscriptionErrorResponse](docs/Model/SubscriptionErrorResponse.md)
 - [TaxNumber](docs/Model/TaxNumber.md)
 - [TooManyRequestsResponse](docs/Model/TooManyRequestsResponse.md)
 - [UnitPriceType](docs/Model/UnitPriceType.md)
 - [ValidationError](docs/Model/ValidationError.md)
 - [ValidationErrorResponse](docs/Model/ValidationErrorResponse.md)
 - [Vat](docs/Model/Vat.md)

## Documentation For Authorization


## api_key

- **Type**: API key
- **API key parameter name**: X-API-KEY
- **Location**: HTTP header


## Author

hello@billingo.hu

