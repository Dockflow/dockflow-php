# Dockflow\Sdk\V3UpstreamApi



All URIs are relative to https://api.dockflow.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v3UpstreamGet()**](V3UpstreamApi.md#v3UpstreamGet) | **GET** /v3/upstream | Poll upstream events |


## `v3UpstreamGet()`

```php
v3UpstreamGet($since, $tradeflow, $container, $category, $code, $cursor, $active, $fields, $format, $per_page, $failsafe): \Dockflow\Sdk\Model\V3UpstreamGet200Response
```

Poll upstream events

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: ApiKey
$config = Dockflow\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dockflow\Sdk\Api\V3UpstreamApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$since = 'since_example'; // string | Only tradeflows changed after this ISO 8601 timestamp (exclusive), with an offset. Without since, cursor, tradeflow or container: the last 15 minutes.
$tradeflow = 'tradeflow_example'; // string | Your tradeflow reference. Returns that tradeflow regardless of when it changed.
$container = 'container_example'; // string | A container number. Returns its tradeflows regardless of when they changed.
$category = 'category_example'; // string | Keep only events of this category: MILESTONE, SHIPMENT or LOCATION.
$code = 'code_example'; // string | Keep only events whose code starts with this value. One of: GE, GN, AE, VD, VA, UV, GT, GD, GR, POS, A-BKD, A-RCS, A-DEP, A-ARR, A-RCF, A-NFD, A-DLV. Any other value returns 400.
$cursor = 'cursor_example'; // string | next_cursor from the previous page. Keep since identical across the pages of one cycle.
$active = 'active_example'; // string | true (active only), false, or both. Default: active plus recently deactivated.
$fields = ''; // string | Comma-separated blocks: events, locations, containers, shipment, vessels. Default: all but vessels.
$format = 'v3'; // string | Shape of `events`: `v3` (Dockflow milestones) or `dcsa-tnt-2.2` (DCSA Track & Trace 2.2). The rest of the record is identical.
$per_page = 56; // int | Tradeflows per page, 1 to 1000. Default 50.
$failsafe = 'failsafe_example'; // string | Set to 1 and Dockflow keeps your position per API key and filter set, so repeated identical polls skip nothing.

try {
    $result = $apiInstance->v3UpstreamGet($since, $tradeflow, $container, $category, $code, $cursor, $active, $fields, $format, $per_page, $failsafe);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling V3UpstreamApi->v3UpstreamGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **since** | **string**| Only tradeflows changed after this ISO 8601 timestamp (exclusive), with an offset. Without since, cursor, tradeflow or container: the last 15 minutes. | [optional] |
| **tradeflow** | **string**| Your tradeflow reference. Returns that tradeflow regardless of when it changed. | [optional] |
| **container** | **string**| A container number. Returns its tradeflows regardless of when they changed. | [optional] |
| **category** | **string**| Keep only events of this category: MILESTONE, SHIPMENT or LOCATION. | [optional] |
| **code** | **string**| Keep only events whose code starts with this value. One of: GE, GN, AE, VD, VA, UV, GT, GD, GR, POS, A-BKD, A-RCS, A-DEP, A-ARR, A-RCF, A-NFD, A-DLV. Any other value returns 400. | [optional] |
| **cursor** | **string**| next_cursor from the previous page. Keep since identical across the pages of one cycle. | [optional] |
| **active** | **string**| true (active only), false, or both. Default: active plus recently deactivated. | [optional] |
| **fields** | **string**| Comma-separated blocks: events, locations, containers, shipment, vessels. Default: all but vessels. | [optional] [default to &#39;&#39;] |
| **format** | **string**| Shape of &#x60;events&#x60;: &#x60;v3&#x60; (Dockflow milestones) or &#x60;dcsa-tnt-2.2&#x60; (DCSA Track &amp; Trace 2.2). The rest of the record is identical. | [optional] [default to &#39;v3&#39;] |
| **per_page** | **int**| Tradeflows per page, 1 to 1000. Default 50. | [optional] |
| **failsafe** | **string**| Set to 1 and Dockflow keeps your position per API key and filter set, so repeated identical polls skip nothing. | [optional] |

### Return type

[**\Dockflow\Sdk\Model\V3UpstreamGet200Response**](../Model/V3UpstreamGet200Response.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
