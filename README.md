# Dockflow API SDK for PHP

The official PHP client for the [Dockflow](https://dockflow.com) API v3: container and shipment tracking events,
tradeflows, documents and the tracking widget.

## Install

```sh
composer require dockflow/dockflow-sdk
```

## Quickstart

Create an API key in the Dockflow console. Production is `https://api.dockflow.com`; test against the UAT sandbox at
`https://uat.dockflow.com` with a UAT key.

```php
$config = Dockflow\Sdk\Configuration::getDefaultConfiguration()
    ->setHost('https://api.dockflow.com')
    ->setAccessToken(getenv('DOCKFLOW_KEY'));
$upstream = new Dockflow\Sdk\Api\UpstreamApi(new GuzzleHttp\Client(), $config);
$page = $upstream->getUpstream(tradeflow: 'PO4564268');
```

The four API classes are `UpstreamApi`, `TradeflowsApi`, `DocumentsApi` and `WidgetApi`.

## Documentation

- Guides and examples: https://docs.dockflow.com/api/sdk/
- OpenAPI 3.1 spec: https://api.dockflow.com/v3/openapi.json
- All five SDKs (TypeScript, Python, C#, Java, PHP): https://github.com/Dockflow/dockflow-sdks

## Versioning

Released automatically whenever the API changes. Versions follow semver: a breaking API change bumps the major
version, everything else the minor or patch.

## License

MIT
