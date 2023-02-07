[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Models](../modules/Models.md) / HawkSearchConfig

# Interface: HawkSearchConfig

[Models](../modules/Models.md).HawkSearchConfig

## Table of contents

### Properties

- [breakpoints](Models.HawkSearchConfig.md#breakpoints)
- [clientId](Models.HawkSearchConfig.md#clientid)
- [components](Models.HawkSearchConfig.md#components)
- [css](Models.HawkSearchConfig.md#css)
- [endpoints](Models.HawkSearchConfig.md#endpoints)
- [fieldMappings](Models.HawkSearchConfig.md#fieldmappings)
- [formatting](Models.HawkSearchConfig.md#formatting)
- [itemTypes](Models.HawkSearchConfig.md#itemtypes)
- [placeholderImageUrl](Models.HawkSearchConfig.md#placeholderimageurl)
- [queryStringMappings](Models.HawkSearchConfig.md#querystringmappings)
- [searchUrl](Models.HawkSearchConfig.md#searchurl)
- [shadowDom](Models.HawkSearchConfig.md#shadowdom)
- [trackingEnabled](Models.HawkSearchConfig.md#trackingenabled)
- [urlPrefixes](Models.HawkSearchConfig.md#urlprefixes)

## Properties

### breakpoints

• `Optional` **breakpoints**: [`Breakpoints`](Models.Breakpoints.md)<`number`\>

#### Defined in

[src/models/global.models.ts:249](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/global.models.ts#lines-249)

___

### clientId

• **clientId**: `string`

#### Defined in

[src/models/global.models.ts:248](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/global.models.ts#lines-248)

___

### components

• `Optional` **components**: [`HawkSearchComponents`](Models.HawkSearchComponents.md)

#### Defined in

[src/models/global.models.ts:250](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/global.models.ts#lines-250)

___

### css

• `Optional` **css**: `Object`

#### Type declaration

| Name | Type |
| :------ | :------ |
| `customStyles?` | `string` \| `string`[] |
| `defaultStyles?` | `boolean` |

#### Defined in

[src/models/global.models.ts:251](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/global.models.ts#lines-251)

___

### endpoints

• `Optional` **endpoints**: `Object`

#### Type declaration

| Name | Type |
| :------ | :------ |
| `recommendations` | `string` |
| `search` | `string` |
| `tracking` | `string` |

#### Defined in

[src/models/global.models.ts:255](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/global.models.ts#lines-255)

___

### fieldMappings

• `Optional` **fieldMappings**: `Object`

#### Type declaration

| Name | Type |
| :------ | :------ |
| `description?` | `string` |
| `imageUrl?` | `string` |
| `price?` | `string` |
| `salePrice?` | `string` |
| `title?` | `string` |
| `type?` | `string` |
| `url?` | `string` |

#### Defined in

[src/models/global.models.ts:260](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/global.models.ts#lines-260)

___

### formatting

• `Optional` **formatting**: `Object`

#### Type declaration

| Name | Type |
| :------ | :------ |
| `cultureIsoCode?` | `string` |
| `currencyIsoCode?` | `string` |

#### Defined in

[src/models/global.models.ts:269](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/global.models.ts#lines-269)

___

### itemTypes

• `Optional` **itemTypes**: `Object`

#### Type declaration

| Name | Type |
| :------ | :------ |
| `default` | [`SearchResultsItemType`](../modules/Models.md#searchresultsitemtype) |
| `productValues?` | `string`[] |

#### Defined in

[src/models/global.models.ts:273](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/global.models.ts#lines-273)

___

### placeholderImageUrl

• `Optional` **placeholderImageUrl**: `string`

#### Defined in

[src/models/global.models.ts:277](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/global.models.ts#lines-277)

___

### queryStringMappings

• `Optional` **queryStringMappings**: `Object`

#### Type declaration

| Name | Type |
| :------ | :------ |
| `disableSpellcheck?` | `string` |
| `facet?` | `string` |
| `page?` | `string` |
| `pageSize?` | `string` |
| `query?` | `string` |
| `searchWithin?` | `string` |
| `sort?` | `string` |

#### Defined in

[src/models/global.models.ts:278](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/global.models.ts#lines-278)

___

### searchUrl

• `Optional` **searchUrl**: `string`

#### Defined in

[src/models/global.models.ts:287](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/global.models.ts#lines-287)

___

### shadowDom

• `Optional` **shadowDom**: `boolean`

#### Defined in

[src/models/global.models.ts:288](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/global.models.ts#lines-288)

___

### trackingEnabled

• `Optional` **trackingEnabled**: `boolean`

#### Defined in

[src/models/global.models.ts:289](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/global.models.ts#lines-289)

___

### urlPrefixes

• `Optional` **urlPrefixes**: `Object`

#### Type declaration

| Name | Type |
| :------ | :------ |
| `assets?` | `string` |
| `content?` | `string` |

#### Defined in

[src/models/global.models.ts:290](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/global.models.ts#lines-290)
