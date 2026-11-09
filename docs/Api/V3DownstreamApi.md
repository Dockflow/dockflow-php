# Dockflow\Sdk\V3DownstreamApi



All URIs are relative to https://api.dockflow.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v3DownstreamDelete()**](V3DownstreamApi.md#v3DownstreamDelete) | **DELETE** /v3/downstream/tradeflows/{tradeflow_reference} | Delete a tradeflow |
| [**v3DownstreamPost()**](V3DownstreamApi.md#v3DownstreamPost) | **POST** /v3/downstream/tradeflows | Upsert tradeflows |


## `v3DownstreamDelete()`

```php
v3DownstreamDelete($tradeflow_reference, $confirm, $hard): string
```

Delete a tradeflow

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: ApiKey
$config = Dockflow\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dockflow\Sdk\Api\V3DownstreamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tradeflow_reference = 'tradeflow_reference_example'; // string
$confirm = 'confirm_example'; // string
$hard = True; // bool | true deletes the tradeflow permanently. Default: it is deactivated.

try {
    $result = $apiInstance->v3DownstreamDelete($tradeflow_reference, $confirm, $hard);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling V3DownstreamApi->v3DownstreamDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tradeflow_reference** | **string**|  | |
| **confirm** | **string**|  | [optional] |
| **hard** | **bool**| true deletes the tradeflow permanently. Default: it is deactivated. | [optional] |

### Return type

**string**

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v3DownstreamPost()`

```php
v3DownstreamPost($downstream_tradeflow): \Dockflow\Sdk\Model\V3DownstreamPost202Response
```

Upsert tradeflows

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: ApiKey
$config = Dockflow\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dockflow\Sdk\Api\V3DownstreamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$downstream_tradeflow = array(new \Dockflow\Sdk\Model\DownstreamTradeflow()); // \Dockflow\Sdk\Model\DownstreamTradeflow[]

try {
    $result = $apiInstance->v3DownstreamPost($downstream_tradeflow);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling V3DownstreamApi->v3DownstreamPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **downstream_tradeflow** | [**\Dockflow\Sdk\Model\DownstreamTradeflow[]**](../Model/DownstreamTradeflow.md)|  | |

### Return type

[**\Dockflow\Sdk\Model\V3DownstreamPost202Response**](../Model/V3DownstreamPost202Response.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
