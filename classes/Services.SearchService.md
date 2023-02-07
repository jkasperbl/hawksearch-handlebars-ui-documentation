[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Services](../modules/Services.md) / SearchService

# Class: SearchService

[Services](../modules/Services.md).SearchService

## Hierarchy

- `BaseService`

  ↳ **`SearchService`**

## Table of contents

### Constructors

- [constructor](Services.SearchService.md#constructor)

### Properties

- [baseUrl](Services.SearchService.md#baseurl)
- [fieldMappings](Services.SearchService.md#fieldmappings)
- [queryStringParams](Services.SearchService.md#querystringparams)
- [searchUrl](Services.SearchService.md#searchurl)

### Methods

- [addFacetValue](Services.SearchService.md#addfacetvalue)
- [bindComponents](Services.SearchService.md#bindcomponents)
- [bindFacetsListComponent](Services.SearchService.md#bindfacetslistcomponent)
- [bindLandingPageComponent](Services.SearchService.md#bindlandingpagecomponent)
- [bindModifiedQueryComponent](Services.SearchService.md#bindmodifiedquerycomponent)
- [bindPageSizeComponent](Services.SearchService.md#bindpagesizecomponent)
- [bindPaginationComponent](Services.SearchService.md#bindpaginationcomponent)
- [bindQuerySuggestionsComponent](Services.SearchService.md#bindquerysuggestionscomponent)
- [bindSearchFieldComponent](Services.SearchService.md#bindsearchfieldcomponent)
- [bindSearchResultsComponent](Services.SearchService.md#bindsearchresultscomponent)
- [bindSearchResultsListComponent](Services.SearchService.md#bindsearchresultslistcomponent)
- [bindSelectedFacetsComponent](Services.SearchService.md#bindselectedfacetscomponent)
- [bindSortingComponent](Services.SearchService.md#bindsortingcomponent)
- [bindTabsComponent](Services.SearchService.md#bindtabscomponent)
- [bindZoneComponent](Services.SearchService.md#bindzonecomponent)
- [excludeFacetValue](Services.SearchService.md#excludefacetvalue)
- [generateGuid](Services.SearchService.md#generateguid)
- [getRequestFromUrl](Services.SearchService.md#getrequestfromurl)
- [getVisitId](Services.SearchService.md#getvisitid)
- [getVisitorId](Services.SearchService.md#getvisitorid)
- [httpPost](Services.SearchService.md#httppost)
- [includeFacetValue](Services.SearchService.md#includefacetvalue)
- [paginate](Services.SearchService.md#paginate)
- [query](Services.SearchService.md#query)
- [removeFacetValue](Services.SearchService.md#removefacetvalue)
- [search](Services.SearchService.md#search)
- [searchWithin](Services.SearchService.md#searchwithin)
- [selectTab](Services.SearchService.md#selecttab)
- [setFacetValue](Services.SearchService.md#setfacetvalue)
- [setPageSize](Services.SearchService.md#setpagesize)
- [setSeoElements](Services.SearchService.md#setseoelements)
- [sort](Services.SearchService.md#sort)
- [stripHtml](Services.SearchService.md#striphtml)
- [triggerBindEvent](Services.SearchService.md#triggerbindevent)
- [triggerEvent](Services.SearchService.md#triggerevent)

## Constructors

### constructor

• **new SearchService**()

#### Inherited from

BaseService.constructor

## Properties

### baseUrl

• `Protected` **baseUrl**: `string`

#### Overrides

BaseService.baseUrl

#### Defined in

[src/services/search.service.ts:44](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/search.service.ts#lines-44)

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

### addFacetValue

▸ **addFacetValue**(`field`, `value`): `Promise`<[`SearchResponse`](../interfaces/Models.SearchResponse.md)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `field` | `string` |
| `value` | `string` |

#### Returns

`Promise`<[`SearchResponse`](../interfaces/Models.SearchResponse.md)\>

#### Defined in

[src/services/search.service.ts:100](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/search.service.ts#lines-100)

___

### bindComponents

▸ **bindComponents**(`searchResponse`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `searchResponse` | [`SearchResponse`](../interfaces/Models.SearchResponse.md) |

#### Returns

`void`

#### Defined in

[src/services/search.service.ts:890](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/search.service.ts#lines-890)

___

### bindFacetsListComponent

▸ **bindFacetsListComponent**(`searchResponse`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `searchResponse` | `undefined` \| [`SearchResponse`](../interfaces/Models.SearchResponse.md) |

#### Returns

`void`

#### Defined in

[src/services/search.service.ts:909](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/search.service.ts#lines-909)

___

### bindLandingPageComponent

▸ **bindLandingPageComponent**(`searchResponse`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `searchResponse` | `undefined` \| [`SearchResponse`](../interfaces/Models.SearchResponse.md) |

#### Returns

`void`

#### Defined in

[src/services/search.service.ts:913](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/search.service.ts#lines-913)

___

### bindModifiedQueryComponent

▸ **bindModifiedQueryComponent**(`searchResponse`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `searchResponse` | `undefined` \| [`SearchResponse`](../interfaces/Models.SearchResponse.md) |

#### Returns

`void`

#### Defined in

[src/services/search.service.ts:917](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/search.service.ts#lines-917)

___

### bindPageSizeComponent

▸ **bindPageSizeComponent**(`searchResponse`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `searchResponse` | `undefined` \| [`SearchResponse`](../interfaces/Models.SearchResponse.md) |

#### Returns

`void`

#### Defined in

[src/services/search.service.ts:927](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/search.service.ts#lines-927)

___

### bindPaginationComponent

▸ **bindPaginationComponent**(`searchResponse`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `searchResponse` | `undefined` \| [`SearchResponse`](../interfaces/Models.SearchResponse.md) |

#### Returns

`void`

#### Defined in

[src/services/search.service.ts:931](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/search.service.ts#lines-931)

___

### bindQuerySuggestionsComponent

▸ **bindQuerySuggestionsComponent**(`searchResponse`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `searchResponse` | `undefined` \| [`SearchResponse`](../interfaces/Models.SearchResponse.md) |

#### Returns

`void`

#### Defined in

[src/services/search.service.ts:947](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/search.service.ts#lines-947)

___

### bindSearchFieldComponent

▸ **bindSearchFieldComponent**(`searchResponse`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `searchResponse` | `undefined` \| [`SearchResponse`](../interfaces/Models.SearchResponse.md) |

#### Returns

`void`

#### Defined in

[src/services/search.service.ts:935](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/search.service.ts#lines-935)

___

### bindSearchResultsComponent

▸ **bindSearchResultsComponent**(`searchResponse`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `searchResponse` | `undefined` \| [`SearchResponse`](../interfaces/Models.SearchResponse.md) |

#### Returns

`void`

#### Defined in

[src/services/search.service.ts:939](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/search.service.ts#lines-939)

___

### bindSearchResultsListComponent

▸ **bindSearchResultsListComponent**(`searchResponse`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `searchResponse` | `undefined` \| [`SearchResponse`](../interfaces/Models.SearchResponse.md) |

#### Returns

`void`

#### Defined in

[src/services/search.service.ts:943](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/search.service.ts#lines-943)

___

### bindSelectedFacetsComponent

▸ **bindSelectedFacetsComponent**(`searchResponse`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `searchResponse` | `undefined` \| [`SearchResponse`](../interfaces/Models.SearchResponse.md) |

#### Returns

`void`

#### Defined in

[src/services/search.service.ts:960](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/search.service.ts#lines-960)

___

### bindSortingComponent

▸ **bindSortingComponent**(`searchResponse`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `searchResponse` | `undefined` \| [`SearchResponse`](../interfaces/Models.SearchResponse.md) |

#### Returns

`void`

#### Defined in

[src/services/search.service.ts:956](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/search.service.ts#lines-956)

___

### bindTabsComponent

▸ **bindTabsComponent**(`searchResponse`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `searchResponse` | `undefined` \| [`SearchResponse`](../interfaces/Models.SearchResponse.md) |

#### Returns

`void`

#### Defined in

[src/services/search.service.ts:964](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/search.service.ts#lines-964)

___

### bindZoneComponent

▸ **bindZoneComponent**(`searchResponse`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `searchResponse` | `undefined` \| [`SearchResponse`](../interfaces/Models.SearchResponse.md) |

#### Returns

`void`

#### Defined in

[src/services/search.service.ts:971](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/search.service.ts#lines-971)

___

### excludeFacetValue

▸ **excludeFacetValue**(`field`, `value`): `Promise`<[`SearchResponse`](../interfaces/Models.SearchResponse.md)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `field` | `string` |
| `value` | `string` |

#### Returns

`Promise`<[`SearchResponse`](../interfaces/Models.SearchResponse.md)\>

#### Defined in

[src/services/search.service.ts:158](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/search.service.ts#lines-158)

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

### getRequestFromUrl

▸ **getRequestFromUrl**(): [`SearchRequest`](../interfaces/Models.SearchRequest.md)

#### Returns

[`SearchRequest`](../interfaces/Models.SearchRequest.md)

#### Defined in

[src/services/search.service.ts:979](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/search.service.ts#lines-979)

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

### includeFacetValue

▸ **includeFacetValue**(`field`, `value`): `Promise`<[`SearchResponse`](../interfaces/Models.SearchResponse.md)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `field` | `string` |
| `value` | `string` |

#### Returns

`Promise`<[`SearchResponse`](../interfaces/Models.SearchResponse.md)\>

#### Defined in

[src/services/search.service.ts:152](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/search.service.ts#lines-152)

___

### paginate

▸ **paginate**(`page`): `Promise`<[`SearchResponse`](../interfaces/Models.SearchResponse.md)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `page` | `number` |

#### Returns

`Promise`<[`SearchResponse`](../interfaces/Models.SearchResponse.md)\>

#### Defined in

[src/services/search.service.ts:286](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/search.service.ts#lines-286)

___

### query

▸ **query**(`query?`, `selectedFacets?`, `disableSpellcheck?`): `Promise`<`void` \| [`SearchResponse`](../interfaces/Models.SearchResponse.md)\>

#### Parameters

| Name | Type | Default value |
| :------ | :------ | :------ |
| `query?` | `string` | `undefined` |
| `selectedFacets` | `undefined` \| [`SelectedFacets`](../modules/Models.md#selectedfacets) | `undefined` |
| `disableSpellcheck` | `boolean` | `false` |

#### Returns

`Promise`<`void` \| [`SearchResponse`](../interfaces/Models.SearchResponse.md)\>

#### Defined in

[src/services/search.service.ts:56](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/search.service.ts#lines-56)

___

### removeFacetValue

▸ **removeFacetValue**(`field`, `value`): `Promise`<[`SearchResponse`](../interfaces/Models.SearchResponse.md)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `field` | `string` |
| `value` | `string` |

#### Returns

`Promise`<[`SearchResponse`](../interfaces/Models.SearchResponse.md)\>

#### Defined in

[src/services/search.service.ts:127](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/search.service.ts#lines-127)

___

### search

▸ **search**(`searchRequest`): `Promise`<[`SearchResponse`](../interfaces/Models.SearchResponse.md)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `searchRequest` | [`SearchRequest`](../interfaces/Models.SearchRequest.md) |

#### Returns

`Promise`<[`SearchResponse`](../interfaces/Models.SearchResponse.md)\>

#### Defined in

[src/services/search.service.ts:48](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/search.service.ts#lines-48)

___

### searchWithin

▸ **searchWithin**(`value`): `Promise`<[`SearchResponse`](../interfaces/Models.SearchResponse.md)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | `string` |

#### Returns

`Promise`<[`SearchResponse`](../interfaces/Models.SearchResponse.md)\>

#### Defined in

[src/services/search.service.ts:233](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/search.service.ts#lines-233)

___

### selectTab

▸ **selectTab**(`value?`): `Promise`<[`SearchResponse`](../interfaces/Models.SearchResponse.md)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `value?` | `string` |

#### Returns

`Promise`<[`SearchResponse`](../interfaces/Models.SearchResponse.md)\>

#### Defined in

[src/services/search.service.ts:253](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/search.service.ts#lines-253)

___

### setFacetValue

▸ **setFacetValue**(`field`, `value`): `Promise`<[`SearchResponse`](../interfaces/Models.SearchResponse.md)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `field` | `string` |
| `value` | `string` |

#### Returns

`Promise`<[`SearchResponse`](../interfaces/Models.SearchResponse.md)\>

#### Defined in

[src/services/search.service.ts:208](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/search.service.ts#lines-208)

___

### setPageSize

▸ **setPageSize**(`pageSize`): `Promise`<[`SearchResponse`](../interfaces/Models.SearchResponse.md)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `pageSize` | `number` |

#### Returns

`Promise`<[`SearchResponse`](../interfaces/Models.SearchResponse.md)\>

#### Defined in

[src/services/search.service.ts:301](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/search.service.ts#lines-301)

___

### setSeoElements

▸ `Protected` **setSeoElements**(`searchResponse`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `searchResponse` | [`SearchResponse`](../interfaces/Models.SearchResponse.md) |

#### Returns

`void`

#### Defined in

[src/services/search.service.ts:1126](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/search.service.ts#lines-1126)

___

### sort

▸ **sort**(`value?`): `Promise`<[`SearchResponse`](../interfaces/Models.SearchResponse.md)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `value?` | `string` |

#### Returns

`Promise`<[`SearchResponse`](../interfaces/Models.SearchResponse.md)\>

#### Defined in

[src/services/search.service.ts:317](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/search.service.ts#lines-317)

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
