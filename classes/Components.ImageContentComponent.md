[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Components](../modules/Components.md) / ImageContentComponent

# Class: ImageContentComponent

[Components](../modules/Components.md).ImageContentComponent

The Image Content component displays an image defined in Hawksearch.

## Tag
The tag for this component is `<hawksearch-image-content>`.

## Default Template
The following is the default Handlebars template for this component. To create a custom template, it is recommended to use this as a starting point.
```
<div class="image-content">
    {{#if link}}
        <a hawksearch-link href="{{link.url}}" target="{{link.target}}">
            <img
                src="{{image.url}}"
                class="image-content__image"
                height="{{image.height}}"
                width="{{image.width}}"
                alt="{{image.altText}}"
                title="{{image.title}}"
            />
        </a>
    {{else}}
        <img
            src="{{image.url}}"
            class="image-content__image"
            height="{{image.height}}"
            width="{{image.width}}"
            alt="{{image.altText}}"
            title="{{image.title}}"
        />
    {{/if}}
</div>
```

## Hierarchy

- [`BaseContentComponent`](Components.BaseContentComponent.md)<[`ImageContentComponentConfig`](../interfaces/Models.ImageContentComponentConfig.md), [`ImageContent`](../interfaces/Models.ImageContent.md), [`ImageContentComponentModel`](../interfaces/Models.ImageContentComponentModel.md)\>

  ↳ **`ImageContentComponent`**

## Table of contents

### Properties

- [bindFromEvent](Components.ImageContentComponent.md#bindfromevent)
- [componentName](Components.ImageContentComponent.md#componentname)
- [contentModel](Components.ImageContentComponent.md#contentmodel)
- [data](Components.ImageContentComponent.md#data)
- [defaultHtml](Components.ImageContentComponent.md#defaulthtml)
- [handlebars](Components.ImageContentComponent.md#handlebars)

### Accessors

- [configuration](Components.ImageContentComponent.md#configuration)
- [rootElement](Components.ImageContentComponent.md#rootelement)

### Methods

- [bindChildElements](Components.ImageContentComponent.md#bindchildelements)
- [getContentModel](Components.ImageContentComponent.md#getcontentmodel)
- [interpolate](Components.ImageContentComponent.md#interpolate)
- [onRender](Components.ImageContentComponent.md#onrender)
- [registerHelpers](Components.ImageContentComponent.md#registerhelpers)
- [render](Components.ImageContentComponent.md#render)
- [renderContent](Components.ImageContentComponent.md#rendercontent)

## Properties

### bindFromEvent

• `Protected` **bindFromEvent**: `boolean` = `false`

#### Inherited from

[BaseContentComponent](Components.BaseContentComponent.md).[bindFromEvent](Components.BaseContentComponent.md#bindfromevent)

#### Defined in

[src/components/content/content-types/base-content.component.ts:12](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/content/content-types/base-content.component.ts#lines-12)

___

### componentName

• `Protected` **componentName**: keyof [`HawkSearchComponents`](../interfaces/Models.HawkSearchComponents.md) = `'image-content'`

#### Overrides

BaseContentComponent.componentName

#### Defined in

[src/components/content/content-types/image-content/image-content.component.ts:19](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/content/content-types/image-content/image-content.component.ts#lines-19)

___

### contentModel

• `Protected` `Optional` **contentModel**: [`ImageContentComponentModel`](../interfaces/Models.ImageContentComponentModel.md)

The data bound to the Handlebars template.

#### Inherited from

[BaseContentComponent](Components.BaseContentComponent.md).[contentModel](Components.BaseContentComponent.md#contentmodel)

#### Defined in

[src/components/base.component.ts:35](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-35)

___

### data

• `Optional` **data**: [`ImageContent`](../interfaces/Models.ImageContent.md)

The data bound to the component.

#### Inherited from

[BaseContentComponent](Components.BaseContentComponent.md).[data](Components.BaseContentComponent.md#data)

#### Defined in

[src/components/base.component.ts:18](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-18)

___

### defaultHtml

• `Protected` **defaultHtml**: `any` = `defaultHtml`

#### Overrides

BaseContentComponent.defaultHtml

#### Defined in

[src/components/content/content-types/image-content/image-content.component.ts:20](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/content/content-types/image-content/image-content.component.ts#lines-20)

___

### handlebars

• `Protected` **handlebars**: typeof `Handlebars` = `HawkSearch.handlebars`

The Handlebars reference shared by all HawkSearch components.

#### Inherited from

[BaseContentComponent](Components.BaseContentComponent.md).[handlebars](Components.BaseContentComponent.md#handlebars)

#### Defined in

[src/components/base.component.ts:23](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-23)

## Accessors

### configuration

• `Protected` `get` **configuration**(): `undefined` \| `TConfig`

The optional configuration object for this component.

#### Returns

`undefined` \| `TConfig`

#### Inherited from

BaseContentComponent.configuration

#### Defined in

[src/components/base.component.ts:61](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-61)

___

### rootElement

• `Protected` `get` **rootElement**(): `ParentNode`

The root element which should be used for querying any child elements. This resolves to `this.shadowRoot` if the Shadow DOM is enabled, otherwise `this`.

#### Returns

`ParentNode`

#### Inherited from

BaseContentComponent.rootElement

#### Defined in

[src/components/base.component.ts:78](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-78)

## Methods

### bindChildElements

▸ `Protected` **bindChildElements**(): `void`

After the component is rendered, this method is called to bind any child components.

#### Returns

`void`

#### Overrides

[BaseContentComponent](Components.BaseContentComponent.md).[bindChildElements](Components.BaseContentComponent.md#bindchildelements)

#### Defined in

[src/components/content/content-types/image-content/image-content.component.ts:38](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/content/content-types/image-content/image-content.component.ts#lines-38)

___

### getContentModel

▸ `Protected` **getContentModel**(): [`ImageContentComponentModel`](../interfaces/Models.ImageContentComponentModel.md)

#### Returns

[`ImageContentComponentModel`](../interfaces/Models.ImageContentComponentModel.md)

#### Overrides

BaseContentComponent.getContentModel

#### Defined in

[src/components/content/content-types/image-content/image-content.component.ts:26](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/content/content-types/image-content/image-content.component.ts#lines-26)

___

### interpolate

▸ `Protected` **interpolate**(`template`, `values`): `string`

Replaces placeholders in a given string with values from a data object.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `template` | `string` | The template string. |
| `values` | `Record`<`string`, `string`\> | The object containing properties which will be bound to `template`. |

#### Returns

`string`

The `template` string with all placeholders replaced by the values specified in `values`.

#### Inherited from

[BaseContentComponent](Components.BaseContentComponent.md).[interpolate](Components.BaseContentComponent.md#interpolate)

#### Defined in

[src/components/base.component.ts:308](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-308)

___

### onRender

▸ `Protected` **onRender**(): `void`

After the component is rendered, this method is called for any additional processing (such as attaching event listeners) which needs to occur.

#### Returns

`void`

#### Overrides

[BaseContentComponent](Components.BaseContentComponent.md).[onRender](Components.BaseContentComponent.md#onrender)

#### Defined in

[src/components/content/content-types/image-content/image-content.component.ts:32](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/content/content-types/image-content/image-content.component.ts#lines-32)

___

### registerHelpers

▸ `Protected` **registerHelpers**(): `void`

Optional method that can be overwritten to register Handlebars helper functions which can be accessed from the template. For more information, see [Custom Helpers](https://handlebarsjs.com/guide/#custom-helpers).

#### Returns

`void`

#### Inherited from

[BaseContentComponent](Components.BaseContentComponent.md).[registerHelpers](Components.BaseContentComponent.md#registerhelpers)

#### Defined in

[src/components/base.component.ts:166](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-166)

___

### render

▸ **render**(): `void`

Binds [contentModel](Components.ImageContentComponent.md#contentmodel) to the Handlebars template and renders the resulting HTML content.

#### Returns

`void`

#### Inherited from

[BaseContentComponent](Components.BaseContentComponent.md).[render](Components.BaseContentComponent.md#render)

#### Defined in

[src/components/base.component.ts:171](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-171)

___

### renderContent

▸ `Protected` **renderContent**(): `boolean`

Determines whether the [data](Components.ImageContentComponent.md#data) meets the necessary conditions to perform data binding and render content.

#### Returns

`boolean`

Whether the component should be rendered. If `false`, the component will have empty contents and be set to `display: none;`.

#### Overrides

[BaseContentComponent](Components.BaseContentComponent.md).[renderContent](Components.BaseContentComponent.md#rendercontent)

#### Defined in

[src/components/content/content-types/image-content/image-content.component.ts:22](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/content/content-types/image-content/image-content.component.ts#lines-22)
