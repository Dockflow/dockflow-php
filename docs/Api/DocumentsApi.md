# Dockflow\Sdk\DocumentsApi



All URIs are relative to https://api.dockflow.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteDocument()**](DocumentsApi.md#deleteDocument) | **DELETE** /v3/downstream/documents/{reference} | Delete a document |
| [**getDocument()**](DocumentsApi.md#getDocument) | **GET** /v3/downstream/documents/{reference} | List the documents of a tradeflow |
| [**listDocumentTypes()**](DocumentsApi.md#listDocumentTypes) | **GET** /v3/downstream/documents/types | List document types |
| [**updateDocument()**](DocumentsApi.md#updateDocument) | **PATCH** /v3/downstream/documents/{reference} | Update a document |
| [**uploadDocument()**](DocumentsApi.md#uploadDocument) | **POST** /v3/downstream/documents | Upload a document to a tradeflow |


## `deleteDocument()`

```php
deleteDocument($reference)
```

Delete a document

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: ApiKey
$config = Dockflow\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dockflow\Sdk\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$reference = 'reference_example'; // string

try {
    $apiInstance->deleteDocument($reference);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->deleteDocument: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **reference** | **string**|  | |

### Return type

void (empty response body)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getDocument()`

```php
getDocument($reference): \Dockflow\Sdk\Model\GetDocument200Response
```

List the documents of a tradeflow

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: ApiKey
$config = Dockflow\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dockflow\Sdk\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$reference = 'reference_example'; // string

try {
    $result = $apiInstance->getDocument($reference);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->getDocument: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **reference** | **string**|  | |

### Return type

[**\Dockflow\Sdk\Model\GetDocument200Response**](../Model/GetDocument200Response.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listDocumentTypes()`

```php
listDocumentTypes(): \Dockflow\Sdk\Model\ListDocumentTypes200ResponseInner[]
```

List document types

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: ApiKey
$config = Dockflow\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dockflow\Sdk\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listDocumentTypes();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->listDocumentTypes: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Dockflow\Sdk\Model\ListDocumentTypes200ResponseInner[]**](../Model/ListDocumentTypes200ResponseInner.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateDocument()`

```php
updateDocument($reference, $document_update): \Dockflow\Sdk\Model\GetDocument200ResponseDataInner
```

Update a document

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: ApiKey
$config = Dockflow\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dockflow\Sdk\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$reference = 'reference_example'; // string
$document_update = new \Dockflow\Sdk\Model\DocumentUpdate(); // \Dockflow\Sdk\Model\DocumentUpdate

try {
    $result = $apiInstance->updateDocument($reference, $document_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->updateDocument: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **reference** | **string**|  | |
| **document_update** | [**\Dockflow\Sdk\Model\DocumentUpdate**](../Model/DocumentUpdate.md)|  | |

### Return type

[**\Dockflow\Sdk\Model\GetDocument200ResponseDataInner**](../Model/GetDocument200ResponseDataInner.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `uploadDocument()`

```php
uploadDocument($document_upload): \Dockflow\Sdk\Model\UploadDocument202Response
```

Upload a document to a tradeflow

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: ApiKey
$config = Dockflow\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dockflow\Sdk\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_upload = new \Dockflow\Sdk\Model\DocumentUpload(); // \Dockflow\Sdk\Model\DocumentUpload

try {
    $result = $apiInstance->uploadDocument($document_upload);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->uploadDocument: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_upload** | [**\Dockflow\Sdk\Model\DocumentUpload**](../Model/DocumentUpload.md)|  | |

### Return type

[**\Dockflow\Sdk\Model\UploadDocument202Response**](../Model/UploadDocument202Response.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
