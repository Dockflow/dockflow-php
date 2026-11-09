# Dockflow\Sdk\WidgetApi



All URIs are relative to https://api.dockflow.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**searchWidget()**](WidgetApi.md#searchWidget) | **GET** /v3/widget/search | Search a shipment for the embeddable tracking widget |


## `searchWidget()`

```php
searchWidget($q): \Dockflow\Sdk\Model\WidgetSearchResult
```

Search a shipment for the embeddable tracking widget

Matches a container number, booking or bill of lading within the token's entity and returns the best match.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: ApiKey
$config = Dockflow\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dockflow\Sdk\Api\WidgetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$q = 'q_example'; // string | Container number, booking or bill of lading reference.

try {
    $result = $apiInstance->searchWidget($q);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WidgetApi->searchWidget: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **q** | **string**| Container number, booking or bill of lading reference. | |

### Return type

[**\Dockflow\Sdk\Model\WidgetSearchResult**](../Model/WidgetSearchResult.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
