[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Services](../modules/Services.md) / RecommendationsService

# Class: RecommendationsService

[Services](../modules/Services.md).RecommendationsService

## Hierarchy

- `BaseService`

  ↳ **`RecommendationsService`**

## Table of contents

### Constructors

- [constructor](Services.RecommendationsService.md#constructor)

### Properties

- [baseUrl](Services.RecommendationsService.md#baseurl)
- [fieldMappings](Services.RecommendationsService.md#fieldmappings)
- [queryStringParams](Services.RecommendationsService.md#querystringparams)
- [searchUrl](Services.RecommendationsService.md#searchurl)

### Methods

- [bindComponents](Services.RecommendationsService.md#bindcomponents)
- [generateGuid](Services.RecommendationsService.md#generateguid)
- [getItems](Services.RecommendationsService.md#getitems)
- [getVisitId](Services.RecommendationsService.md#getvisitid)
- [getVisitorId](Services.RecommendationsService.md#getvisitorid)
- [httpPost](Services.RecommendationsService.md#httppost)
- [stripHtml](Services.RecommendationsService.md#striphtml)
- [triggerBindEvent](Services.RecommendationsService.md#triggerbindevent)
- [triggerEvent](Services.RecommendationsService.md#triggerevent)

## Constructors

### constructor

• **new RecommendationsService**()

#### Inherited from

BaseService.constructor

## Properties

### baseUrl

• `Protected` **baseUrl**: `string`

#### Overrides

BaseService.baseUrl

#### Defined in

[src/services/recommendations.service.ts:7](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/recommendations.service.ts#lines-7)

___

### fieldMappings

• **fieldMappings**: `Object`

#### Type declaration

| Name | Type |
| :------ | :------ |
| `description` | `string` |
| `imageUrl` | `string` |
| `price` | `string` |
| `salePrice` | `string` |
| `title` | `string` |
| `type` | `string` |
| `url` | `string` |

#### Inherited from

BaseService.fieldMappings

#### Defined in

[src/services/base.service.ts:10](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/base.service.ts#lines-10)

___

### queryStringParams

• **queryStringParams**: `Object`

#### Type declaration

| Name | Type |
| :------ | :------ |
| `disableSpellcheck` | `string` |
| `facet` | `string` |
| `page` | `string` |
| `pageSize` | `string` |
| `query` | `string` |
| `searchWithin` | `string` |
| `sort` | `string` |

#### Inherited from

BaseService.queryStringParams

#### Defined in

[src/services/base.service.ts:20](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/base.service.ts#lines-20)

___

### searchUrl

• **searchUrl**: `string`

#### Inherited from

BaseService.searchUrl

#### Defined in

[src/services/base.service.ts:30](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/base.service.ts#lines-30)

## Methods

### bindComponents

▸ **bindComponents**(`recommendationsResponse`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `recommendationsResponse` | [`RecommendationsResponse`](../interfaces/Models.RecommendationsResponse.md) |

#### Returns

`void`

#### Defined in

[src/services/recommendations.service.ts:83](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/recommendations.service.ts#lines-83)

___

### generateGuid

▸ `Protected` **generateGuid**(): `string`

#### Returns

`string`

#### Inherited from

BaseService.generateGuid

#### Defined in

[src/services/base.service.ts:95](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/base.service.ts#lines-95)

___

### getItems

▸ **getItems**(`recommendationsRequest`): `Promise`<[`RecommendationsResponse`](../interfaces/Models.RecommendationsResponse.md)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `recommendationsRequest` | [`RecommendationsRequest`](../interfaces/Models.RecommendationsRequest.md) |

#### Returns

`Promise`<[`RecommendationsResponse`](../interfaces/Models.RecommendationsResponse.md)\>

#### Defined in

[src/services/recommendations.service.ts:11](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/recommendations.service.ts#lines-11)

___

### getVisitId

▸ `Protected` **getVisitId**(): `string`

#### Returns

`string`

#### Inherited from

BaseService.getVisitId

#### Defined in

[src/services/base.service.ts:82](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/base.service.ts#lines-82)

___

### getVisitorId

▸ `Protected` **getVisitorId**(): `string`

#### Returns

`string`

#### Inherited from

BaseService.getVisitorId

#### Defined in

[src/services/base.service.ts:69](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/base.service.ts#lines-69)

___

### httpPost

▸ `Protected` **httpPost**<`T`\>(`relativeUrl`, `body?`): `Promise`<`T`\>

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `relativeUrl` | `string` |
| `body?` | `any` |

#### Returns

`Promise`<`T`\>

#### Inherited from

BaseService.httpPost

#### Defined in

[src/services/base.service.ts:32](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/base.service.ts#lines-32)

___

### stripHtml

▸ `Protected` **stripHtml**(`input`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `input` | `string` |

#### Returns

`string`

#### Inherited from

BaseService.stripHtml

#### Defined in

[src/services/base.service.ts:51](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/base.service.ts#lines-51)

___

### triggerBindEvent

▸ `Protected` **triggerBindEvent**<`T`\>(`component`, `data`, `filter?`): `void`

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `component` | keyof [`HawkSearchComponents`](../interfaces/Models.HawkSearchComponents.md) |
| `data` | `T` |
| `filter?` | `string` |

#### Returns

`void`

#### Inherited from

BaseService.triggerBindEvent

#### Defined in

[src/services/base.service.ts:99](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/base.service.ts#lines-99)

___

### triggerEvent

▸ `Protected` **triggerEvent**<`T`\>(`name`, `data`): `void`

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `name` | `string` |
| `data` | `T` |

#### Returns

`void`

#### Inherited from

BaseService.triggerEvent

#### Defined in

[src/services/base.service.ts:109](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/base.service.ts#lines-109)
