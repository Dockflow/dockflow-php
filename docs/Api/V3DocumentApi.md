# Dockflow\Sdk\V3DocumentApi



All URIs are relative to https://api.dockflow.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**listDocumentTypes()**](V3DocumentApi.md#listDocumentTypes) | **GET** /v3/downstream/documents/types | List document types |
| [**v3DocumentDelete()**](V3DocumentApi.md#v3DocumentDelete) | **DELETE** /v3/downstream/documents/{reference} | Delete a document |
| [**v3DocumentGet()**](V3DocumentApi.md#v3DocumentGet) | **GET** /v3/downstream/documents/{reference} | List the documents of a tradeflow |
| [**v3DocumentPatch()**](V3DocumentApi.md#v3DocumentPatch) | **PATCH** /v3/downstream/documents/{reference} | Update a document |
| [**v3DocumentPost()**](V3DocumentApi.md#v3DocumentPost) | **POST** /v3/downstream/documents | Upload a document to a tradeflow |


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


$apiInstance = new Dockflow\Sdk\Api\V3DocumentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listDocumentTypes();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling V3DocumentApi->listDocumentTypes: ', $e->getMessage(), PHP_EOL;
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

## `v3DocumentDelete()`

```php
v3DocumentDelete($reference)
```

Delete a document

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: ApiKey
$config = Dockflow\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dockflow\Sdk\Api\V3DocumentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$reference = 'reference_example'; // string

try {
    $apiInstance->v3DocumentDelete($reference);
} catch (Exception $e) {
    echo 'Exception when calling V3DocumentApi->v3DocumentDelete: ', $e->getMessage(), PHP_EOL;
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

## `v3DocumentGet()`

```php
v3DocumentGet($reference): \Dockflow\Sdk\Model\V3DocumentGet200Response
```

List the documents of a tradeflow

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: ApiKey
$config = Dockflow\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dockflow\Sdk\Api\V3DocumentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$reference = 'reference_example'; // string

try {
    $result = $apiInstance->v3DocumentGet($reference);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling V3DocumentApi->v3DocumentGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **reference** | **string**|  | |

### Return type

[**\Dockflow\Sdk\Model\V3DocumentGet200Response**](../Model/V3DocumentGet200Response.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v3DocumentPatch()`

```php
v3DocumentPatch($reference, $document_update): \Dockflow\Sdk\Model\V3DocumentGet200ResponseDataInner
```

Update a document

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: ApiKey
$config = Dockflow\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dockflow\Sdk\Api\V3DocumentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$reference = 'reference_example'; // string
$document_update = new \Dockflow\Sdk\Model\DocumentUpdate(); // \Dockflow\Sdk\Model\DocumentUpdate

try {
    $result = $apiInstance->v3DocumentPatch($reference, $document_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling V3DocumentApi->v3DocumentPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **reference** | **string**|  | |
| **document_update** | [**\Dockflow\Sdk\Model\DocumentUpdate**](../Model/DocumentUpdate.md)|  | |

### Return type

[**\Dockflow\Sdk\Model\V3DocumentGet200ResponseDataInner**](../Model/V3DocumentGet200ResponseDataInner.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v3DocumentPost()`

```php
v3DocumentPost($document_upload): \Dockflow\Sdk\Model\V3DocumentPost202Response
```

Upload a document to a tradeflow

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: ApiKey
$config = Dockflow\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dockflow\Sdk\Api\V3DocumentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_upload = new \Dockflow\Sdk\Model\DocumentUpload(); // \Dockflow\Sdk\Model\DocumentUpload

try {
    $result = $apiInstance->v3DocumentPost($document_upload);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling V3DocumentApi->v3DocumentPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_upload** | [**\Dockflow\Sdk\Model\DocumentUpload**](../Model/DocumentUpload.md)|  | |

### Return type

[**\Dockflow\Sdk\Model\V3DocumentPost202Response**](../Model/V3DocumentPost202Response.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
