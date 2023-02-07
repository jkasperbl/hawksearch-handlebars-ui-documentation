[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Models](../modules/Models.md) / ImageContent

# Interface: ImageContent

[Models](../modules/Models.md).ImageContent

## Hierarchy

- [`ContentType`](Models.ContentType.md)

  ↳ **`ImageContent`**

  ↳↳ [`ImageContentComponentModel`](Models.ImageContentComponentModel.md)

## Table of contents

### Properties

- [campaignId](Models.ImageContent.md#campaignid)
- [id](Models.ImageContent.md#id)
- [image](Models.ImageContent.md#image)
- [link](Models.ImageContent.md#link)
- [title](Models.ImageContent.md#title)
- [type](Models.ImageContent.md#type)
- [zone](Models.ImageContent.md#zone)

## Properties

### campaignId

• **campaignId**: `number`

#### Inherited from

[ContentType](Models.ContentType.md).[campaignId](Models.ContentType.md#campaignid)

#### Defined in

[src/models/content.models.ts:5](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/content.models.ts#lines-5)

___

### id

• **id**: `number`

#### Inherited from

[ContentType](Models.ContentType.md).[id](Models.ContentType.md#id)

#### Defined in

[src/models/content.models.ts:4](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/content.models.ts#lines-4)

___

### image

• **image**: `Object`

#### Type declaration

| Name | Type |
| :------ | :------ |
| `altText?` | `string` |
| `height?` | `number` |
| `title?` | `string` |
| `url` | `string` |
| `width?` | `number` |

#### Defined in

[src/models/content.models.ts:28](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/content.models.ts#lines-28)

___

### link

• `Optional` **link**: `Object`

#### Type declaration

| Name | Type |
| :------ | :------ |
| `target` | `string` |
| `url` | `string` |

#### Defined in

[src/models/content.models.ts:35](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/content.models.ts#lines-35)

___

### title

• **title**: `string`

#### Inherited from

[ContentType](Models.ContentType.md).[title](Models.ContentType.md#title)

#### Defined in

[src/models/content.models.ts:7](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/content.models.ts#lines-7)

___

### type

• **type**: ``"image"``

#### Overrides

[ContentType](Models.ContentType.md).[type](Models.ContentType.md#type)

#### Defined in

[src/models/content.models.ts:27](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/content.models.ts#lines-27)

___

### zone

• **zone**: `string`

#### Inherited from

[ContentType](Models.ContentType.md).[zone](Models.ContentType.md#zone)

#### Defined in

[src/models/content.models.ts:8](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/models/content.models.ts#lines-8)
