[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Models](../modules/Models.md) / RecommendationsComponentConfig

# Interface: RecommendationsComponentConfig

[Models](../modules/Models.md).RecommendationsComponentConfig

## Hierarchy

- [`BaseComponentConfig`](Models.BaseComponentConfig.md)

  ↳ **`RecommendationsComponentConfig`**

## Table of contents

### Properties

- [carousel](Models.RecommendationsComponentConfig.md#carousel)
- [headingEnabled](Models.RecommendationsComponentConfig.md#headingenabled)
- [itemsToDisplay](Models.RecommendationsComponentConfig.md#itemstodisplay)
- [shadowDom](Models.RecommendationsComponentConfig.md#shadowdom)
- [strings](Models.RecommendationsComponentConfig.md#strings)
- [template](Models.RecommendationsComponentConfig.md#template)

## Properties

### carousel

• `Optional` **carousel**: `Object`

#### Type declaration

| Name | Type |
| :------ | :------ |
| `autorotation?` | { `enabled?`: `boolean` ; `interval?`: `number`  } |
| `autorotation.enabled?` | `boolean` |
| `autorotation.interval?` | `number` |
| `buttonsEnabled?` | `boolean` |
| `enabled?` | `boolean` |
| `paginationEnabled?` | `boolean` |
| `paginationSelectedCssClass?` | `string` |

#### Defined in

[src/models/global.models.ts:140](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/global.models.ts#lines-140)

___

### headingEnabled

• `Optional` **headingEnabled**: `boolean`

#### Defined in

[src/models/global.models.ts:150](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/global.models.ts#lines-150)

___

### itemsToDisplay

• `Optional` **itemsToDisplay**: [`Breakpoints`](Models.Breakpoints.md)<`number`\>

#### Defined in

[src/models/global.models.ts:151](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/global.models.ts#lines-151)

___

### shadowDom

• `Optional` **shadowDom**: `boolean`

#### Inherited from

[BaseComponentConfig](Models.BaseComponentConfig.md).[shadowDom](Models.BaseComponentConfig.md#shadowdom)

#### Defined in

[src/models/global.models.ts:6](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/global.models.ts#lines-6)

___

### strings

• `Optional` **strings**: `Object`

#### Type declaration

| Name | Type |
| :------ | :------ |
| `next?` | `string` |
| `previous?` | `string` |

#### Defined in

[src/models/global.models.ts:152](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/global.models.ts#lines-152)

___

### template

• `Optional` **template**: `string`

#### Inherited from

[BaseComponentConfig](Models.BaseComponentConfig.md).[template](Models.BaseComponentConfig.md#template)

#### Defined in

[src/models/global.models.ts:7](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/global.models.ts#lines-7)
