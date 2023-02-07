[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Services](../modules/Services.md) / TrackingService

# Class: TrackingService

[Services](../modules/Services.md).TrackingService

## Hierarchy

- `BaseService`

  ↳ **`TrackingService`**

## Table of contents

### Constructors

- [constructor](Services.TrackingService.md#constructor)

### Properties

- [baseUrl](Services.TrackingService.md#baseurl)
- [fieldMappings](Services.TrackingService.md#fieldmappings)
- [queryStringParams](Services.TrackingService.md#querystringparams)
- [searchUrl](Services.TrackingService.md#searchurl)

### Methods

- [generateGuid](Services.TrackingService.md#generateguid)
- [getVisitId](Services.TrackingService.md#getvisitid)
- [getVisitorId](Services.TrackingService.md#getvisitorid)
- [httpPost](Services.TrackingService.md#httppost)
- [stripHtml](Services.TrackingService.md#striphtml)
- [trackAddToCart](Services.TrackingService.md#trackaddtocart)
- [trackAddToCartMultiple](Services.TrackingService.md#trackaddtocartmultiple)
- [trackAutocompleteClick](Services.TrackingService.md#trackautocompleteclick)
- [trackBannerClick](Services.TrackingService.md#trackbannerclick)
- [trackBannerImpression](Services.TrackingService.md#trackbannerimpression)
- [trackEvent](Services.TrackingService.md#trackevent)
- [trackOrder](Services.TrackingService.md#trackorder)
- [trackPageLoad](Services.TrackingService.md#trackpageload)
- [trackRating](Services.TrackingService.md#trackrating)
- [trackRecommendationClick](Services.TrackingService.md#trackrecommendationclick)
- [trackSearch](Services.TrackingService.md#tracksearch)
- [trackSearchResultClick](Services.TrackingService.md#tracksearchresultclick)
- [triggerBindEvent](Services.TrackingService.md#triggerbindevent)
- [triggerEvent](Services.TrackingService.md#triggerevent)

## Constructors

### constructor

• **new TrackingService**()

#### Inherited from

BaseService.constructor

## Properties

### baseUrl

• `Protected` **baseUrl**: `string`

#### Overrides

BaseService.baseUrl

#### Defined in

[src/services/tracking.service.ts:7](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/tracking.service.ts#lines-7)

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

### trackAddToCart

▸ **trackAddToCart**(`productId`, `quantity`, `price`, `currencyIsoCode`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `productId` | `string` |
| `quantity` | `number` |
| `price` | `number` |
| `currencyIsoCode` | `string` |

#### Returns

`Promise`<`void`\>

#### Defined in

[src/services/tracking.service.ts:9](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/tracking.service.ts#lines-9)

___

### trackAddToCartMultiple

▸ **trackAddToCartMultiple**(`items`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `items` | { `currencyIsoCode`: `string` ; `price`: `number` ; `productId`: `string` ; `quantity`: `number`  }[] |

#### Returns

`Promise`<`void`\>

#### Defined in

[src/services/tracking.service.ts:20](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/tracking.service.ts#lines-20)

___

### trackAutocompleteClick

▸ **trackAutocompleteClick**(`query`, `itemType`, `title`, `url`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `query` | `string` |
| `itemType` | [`AutocompleteItemType`](../enums/Models.AutocompleteItemType.md) |
| `title` | `string` |
| `url` | `string` |

#### Returns

`Promise`<`void`\>

#### Defined in

[src/services/tracking.service.ts:33](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/tracking.service.ts#lines-33)

___

### trackBannerClick

▸ **trackBannerClick**(`bannerId`, `campaignId`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `bannerId` | `number` |
| `campaignId` | `number` |

#### Returns

`Promise`<`void`\>

#### Defined in

[src/services/tracking.service.ts:44](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/tracking.service.ts#lines-44)

___

### trackBannerImpression

▸ **trackBannerImpression**(`bannerId`, `campaignId`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `bannerId` | `number` |
| `campaignId` | `number` |

#### Returns

`Promise`<`void`\>

#### Defined in

[src/services/tracking.service.ts:58](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/tracking.service.ts#lines-58)

___

### trackEvent

▸ **trackEvent**(`type`, `data`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `type` | [`EventType`](../enums/Models.EventType.md) |
| `data` | `any` |

#### Returns

`Promise`<`void`\>

#### Defined in

[src/services/tracking.service.ts:171](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/tracking.service.ts#lines-171)

___

### trackOrder

▸ **trackOrder**(`orderId`, `items`, `subTotal`, `tax`, `total`, `currencyIsoCode`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `orderId` | `string` |
| `items` | { `price`: `number` ; `productId`: `string` ; `quantity`: `number`  }[] |
| `subTotal` | `number` |
| `tax` | `number` |
| `total` | `number` |
| `currencyIsoCode` | `string` |

#### Returns

`Promise`<`void`\>

#### Defined in

[src/services/tracking.service.ts:72](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/tracking.service.ts#lines-72)

___

### trackPageLoad

▸ **trackPageLoad**(`pageType`, `productId?`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `pageType` | [`PageType`](../enums/Models.PageType.md) |
| `productId?` | `string` |

#### Returns

`Promise`<`void`\>

#### Defined in

[src/services/tracking.service.ts:96](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/tracking.service.ts#lines-96)

___

### trackRating

▸ **trackRating**(`productId`, `rating`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `productId` | `string` |
| `rating` | `number` |

#### Returns

`Promise`<`void`\>

#### Defined in

[src/services/tracking.service.ts:113](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/tracking.service.ts#lines-113)

___

### trackRecommendationClick

▸ **trackRecommendationClick**(`widgetId`, `requestId`, `productId`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `widgetId` | `string` |
| `requestId` | `string` |
| `productId` | `string` |

#### Returns

`Promise`<`void`\>

#### Defined in

[src/services/tracking.service.ts:122](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/tracking.service.ts#lines-122)

___

### trackSearch

▸ **trackSearch**(`query`, `newSearch`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `query` | `undefined` \| `string` |
| `newSearch` | `boolean` |

#### Returns

`Promise`<`void`\>

#### Defined in

[src/services/tracking.service.ts:154](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/tracking.service.ts#lines-154)

___

### trackSearchResultClick

▸ **trackSearchResultClick**(`id`, `url`, `event?`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `id` | `string` |
| `url` | `string` |
| `event?` | `PointerEvent` |

#### Returns

`Promise`<`void`\>

#### Defined in

[src/services/tracking.service.ts:132](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/services/tracking.service.ts#lines-132)

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
