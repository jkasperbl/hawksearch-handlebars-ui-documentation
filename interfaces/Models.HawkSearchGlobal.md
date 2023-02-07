[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Models](../modules/Models.md) / HawkSearchGlobal

# Interface: HawkSearchGlobal

[Models](../modules/Models.md).HawkSearchGlobal

## Table of contents

### Properties

- [config](Models.HawkSearchGlobal.md#config)
- [handlebars](Models.HawkSearchGlobal.md#handlebars)
- [searchRequest](Models.HawkSearchGlobal.md#searchrequest)
- [searchResponse](Models.HawkSearchGlobal.md#searchresponse)
- [services](Models.HawkSearchGlobal.md#services)

## Properties

### config

• **config**: [`HawkSearchConfig`](Models.HawkSearchConfig.md)

#### Defined in

[src/models/global.models.ts:297](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/global.models.ts#lines-297)

___

### handlebars

• **handlebars**: typeof `Handlebars`

#### Defined in

[src/models/global.models.ts:298](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/global.models.ts#lines-298)

___

### searchRequest

• `Optional` **searchRequest**: [`SearchRequest`](Models.SearchRequest.md)

#### Defined in

[src/models/global.models.ts:299](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/global.models.ts#lines-299)

___

### searchResponse

• `Optional` **searchResponse**: [`SearchResponse`](Models.SearchResponse.md)

#### Defined in

[src/models/global.models.ts:300](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/global.models.ts#lines-300)

___

### services

• `Optional` **services**: `Object`

#### Type declaration

| Name | Type |
| :------ | :------ |
| `autocomplete` | [`AutocompleteService`](../classes/Services.AutocompleteService.md) |
| `recommendations` | [`RecommendationsService`](../classes/Services.RecommendationsService.md) |
| `search` | [`SearchService`](../classes/Services.SearchService.md) |
| `tracking` | [`TrackingService`](../classes/Services.TrackingService.md) |

#### Defined in

[src/models/global.models.ts:301](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/global.models.ts#lines-301)
