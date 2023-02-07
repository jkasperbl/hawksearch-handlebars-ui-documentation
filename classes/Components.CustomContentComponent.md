[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Components](../modules/Components.md) / CustomContentComponent

# Class: CustomContentComponent

[Components](../modules/Components.md).CustomContentComponent

The Custom Content component renders HTML defined in Hawksearch.

## Tag
The tag for this component is `<hawksearch-custom-content>`.

## Default Template
The following is the default Handlebars template for this component. To create a custom template, it is recommended to use this as a starting point.
```
<div class="custom-content">
    {{html content}}
</div>
```

## Hierarchy

- [`BaseContentComponent`](Components.BaseContentComponent.md)<[`CustomContentComponentConfig`](../interfaces/Models.CustomContentComponentConfig.md), [`CustomContent`](../interfaces/Models.CustomContent.md), [`CustomContentComponentModel`](../interfaces/Models.CustomContentComponentModel.md)\>

  ↳ **`CustomContentComponent`**

## Table of contents

### Properties

- [bindFromEvent](Components.CustomContentComponent.md#bindfromevent)
- [componentName](Components.CustomContentComponent.md#componentname)
- [contentModel](Components.CustomContentComponent.md#contentmodel)
- [data](Components.CustomContentComponent.md#data)
- [defaultHtml](Components.CustomContentComponent.md#defaulthtml)
- [handlebars](Components.CustomContentComponent.md#handlebars)

### Accessors

- [configuration](Components.CustomContentComponent.md#configuration)
- [rootElement](Components.CustomContentComponent.md#rootelement)

### Methods

- [bindChildElements](Components.CustomContentComponent.md#bindchildelements)
- [getContentModel](Components.CustomContentComponent.md#getcontentmodel)
- [interpolate](Components.CustomContentComponent.md#interpolate)
- [onRender](Components.CustomContentComponent.md#onrender)
- [registerHelpers](Components.CustomContentComponent.md#registerhelpers)
- [render](Components.CustomContentComponent.md#render)
- [renderContent](Components.CustomContentComponent.md#rendercontent)

## Properties

### bindFromEvent

• `Protected` **bindFromEvent**: `boolean` = `false`

#### Inherited from

[BaseContentComponent](Components.BaseContentComponent.md).[bindFromEvent](Components.BaseContentComponent.md#bindfromevent)

#### Defined in

[src/components/content/content-types/base-content.component.ts:12](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/content/content-types/base-content.component.ts#lines-12)

___

### componentName

• `Protected` **componentName**: keyof [`HawkSearchComponents`](../interfaces/Models.HawkSearchComponents.md) = `'custom-content'`

#### Overrides

BaseContentComponent.componentName

#### Defined in

[src/components/content/content-types/custom-content/custom-content.component.ts:18](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/content/content-types/custom-content/custom-content.component.ts#lines-18)

___

### contentModel

• `Protected` `Optional` **contentModel**: [`CustomContentComponentModel`](../interfaces/Models.CustomContentComponentModel.md)

The data bound to the Handlebars template.

#### Inherited from

[BaseContentComponent](Components.BaseContentComponent.md).[contentModel](Components.BaseContentComponent.md#contentmodel)

#### Defined in

[src/components/base.component.ts:35](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-35)

___

### data

• `Optional` **data**: [`CustomContent`](../interfaces/Models.CustomContent.md)

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

[src/components/content/content-types/custom-content/custom-content.component.ts:19](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/content/content-types/custom-content/custom-content.component.ts#lines-19)

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

#### Inherited from

[BaseContentComponent](Components.BaseContentComponent.md).[bindChildElements](Components.BaseContentComponent.md#bindchildelements)

#### Defined in

[src/components/base.component.ts:257](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-257)

___

### getContentModel

▸ `Protected` **getContentModel**(): [`CustomContentComponentModel`](../interfaces/Models.CustomContentComponentModel.md)

#### Returns

[`CustomContentComponentModel`](../interfaces/Models.CustomContentComponentModel.md)

#### Overrides

BaseContentComponent.getContentModel

#### Defined in

[src/components/content/content-types/custom-content/custom-content.component.ts:25](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/content/content-types/custom-content/custom-content.component.ts#lines-25)

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

#### Inherited from

[BaseContentComponent](Components.BaseContentComponent.md).[onRender](Components.BaseContentComponent.md#onrender)

#### Defined in

[src/components/base.component.ts:264](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-264)

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

Binds [contentModel](Components.CustomContentComponent.md#contentmodel) to the Handlebars template and renders the resulting HTML content.

#### Returns

`void`

#### Inherited from

[BaseContentComponent](Components.BaseContentComponent.md).[render](Components.BaseContentComponent.md#render)

#### Defined in

[src/components/base.component.ts:171](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-171)

___

### renderContent

▸ `Protected` **renderContent**(): `boolean`

Determines whether the [data](Components.CustomContentComponent.md#data) meets the necessary conditions to perform data binding and render content.

#### Returns

`boolean`

Whether the component should be rendered. If `false`, the component will have empty contents and be set to `display: none;`.

#### Overrides

[BaseContentComponent](Components.BaseContentComponent.md).[renderContent](Components.BaseContentComponent.md#rendercontent)

#### Defined in

[src/components/content/content-types/custom-content/custom-content.component.ts:21](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/content/content-types/custom-content/custom-content.component.ts#lines-21)
