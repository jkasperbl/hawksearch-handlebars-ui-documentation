[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Services](../modules/Services.md) / AutocompleteService

# Class: AutocompleteService

[Services](../modules/Services.md).AutocompleteService

## Hierarchy

- `BaseService`

  ↳ **`AutocompleteService`**

## Table of contents

### Constructors

- [constructor](Services.AutocompleteService.md#constructor)

### Properties

- [baseUrl](Services.AutocompleteService.md#baseurl)
- [fieldMappings](Services.AutocompleteService.md#fieldmappings)
- [queryStringParams](Services.AutocompleteService.md#querystringparams)
- [searchUrl](Services.AutocompleteService.md#searchurl)

### Methods

- [bindComponent](Services.AutocompleteService.md#bindcomponent)
- [generateGuid](Services.AutocompleteService.md#generateguid)
- [getVisitId](Services.AutocompleteService.md#getvisitid)
- [getVisitorId](Services.AutocompleteService.md#getvisitorid)
- [httpPost](Services.AutocompleteService.md#httppost)
- [query](Services.AutocompleteService.md#query)
- [stripHtml](Services.AutocompleteService.md#striphtml)
- [triggerBindEvent](Services.AutocompleteService.md#triggerbindevent)
- [triggerEvent](Services.AutocompleteService.md#triggerevent)

## Constructors

### constructor

• **new AutocompleteService**()

#### Inherited from

BaseService.constructor

## Properties

### baseUrl

• `Protected` **baseUrl**: `string`

#### Overrides

BaseService.baseUrl

#### Defined in

[src/services/autocomplete.service.ts:7](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/autocomplete.service.ts#lines-7)

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

### bindComponent

▸ **bindComponent**(`autocompleteResponse`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `autocompleteResponse` | [`AutocompleteResponse`](../interfaces/Models.AutocompleteResponse.md) |

#### Returns

`void`

#### Defined in

[src/services/autocomplete.service.ts:97](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/autocomplete.service.ts#lines-97)

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

### query

▸ **query**(`query`): `Promise`<[`AutocompleteResponse`](../interfaces/Models.AutocompleteResponse.md)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `query` | `string` |

#### Returns

`Promise`<[`AutocompleteResponse`](../interfaces/Models.AutocompleteResponse.md)\>

#### Defined in

[src/services/autocomplete.service.ts:11](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/autocomplete.service.ts#lines-11)

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
