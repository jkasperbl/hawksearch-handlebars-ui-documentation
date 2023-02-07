[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Components](../modules/Components.md) / IconComponent

# Class: IconComponent

[Components](../modules/Components.md).IconComponent

The Icon component renders an SVG image inline with text content.

## Tag
The tag for this component is `<hawksearch-icon>`.

## Attributes
| Name | Type | Default Value | Required |
| :- | :- | :- | :- |
| name | [IconName](../modules/Models.md#iconname) | | Yes
| size | `string` | `number` | `1em` | No

## CSS Variables
The following CSS classes are available that allow you to bypass the [Shadow DOM](https://developer.mozilla.org/en-US/docs/Web/Web_Components/Using_shadow_DOM) and customize the appearance of this component without overriding the Handlebars template:

| Name | Default Value |
| :- | :- |
| --icon-color | `currentColor` |
| --icon-font-size | `1em` |

## Default Template
The following is the default Handlebars template for this component. To create a custom template, it is recommended to use this as a starting point.
```
{{html svg}}
<svg height="{{height}}" width="{{width}}" focusable="false" aria-hidden="true" class="icon">
    <use href="{{url}}"></use>
</svg>
```

## Hierarchy

- [`BaseComponent`](Components.BaseComponent.md)<[`IconComponentConfig`](../interfaces/Models.IconComponentConfig.md), `never`, [`IconComponentModel`](../interfaces/Models.IconComponentModel.md)\>

  ↳ **`IconComponent`**

## Table of contents

### Properties

- [bindFromEvent](Components.IconComponent.md#bindfromevent)
- [componentName](Components.IconComponent.md#componentname)
- [contentModel](Components.IconComponent.md#contentmodel)
- [data](Components.IconComponent.md#data)
- [defaultHtml](Components.IconComponent.md#defaulthtml)
- [handlebars](Components.IconComponent.md#handlebars)

### Accessors

- [configuration](Components.IconComponent.md#configuration)
- [rootElement](Components.IconComponent.md#rootelement)

### Methods

- [bindChildElements](Components.IconComponent.md#bindchildelements)
- [getContentModel](Components.IconComponent.md#getcontentmodel)
- [interpolate](Components.IconComponent.md#interpolate)
- [onRender](Components.IconComponent.md#onrender)
- [registerHelpers](Components.IconComponent.md#registerhelpers)
- [render](Components.IconComponent.md#render)
- [renderContent](Components.IconComponent.md#rendercontent)

## Properties

### bindFromEvent

• `Protected` **bindFromEvent**: `boolean` = `false`

#### Overrides

BaseComponent.bindFromEvent

#### Defined in

[src/components/general/icon/icon.component.ts:35](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/general/icon/icon.component.ts#lines-35)

___

### componentName

• `Protected` **componentName**: keyof [`HawkSearchComponents`](../interfaces/Models.HawkSearchComponents.md) = `'icon'`

#### Overrides

BaseComponent.componentName

#### Defined in

[src/components/general/icon/icon.component.ts:33](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/general/icon/icon.component.ts#lines-33)

___

### contentModel

• `Protected` `Optional` **contentModel**: [`IconComponentModel`](../interfaces/Models.IconComponentModel.md)

The data bound to the Handlebars template.

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[contentModel](Components.BaseComponent.md#contentmodel)

#### Defined in

[src/components/base.component.ts:35](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-35)

___

### data

• `Optional` **data**: `undefined`

The data bound to the component.

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[data](Components.BaseComponent.md#data)

#### Defined in

[src/components/base.component.ts:18](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-18)

___

### defaultHtml

• `Protected` **defaultHtml**: `any` = `defaultHtml`

#### Overrides

BaseComponent.defaultHtml

#### Defined in

[src/components/general/icon/icon.component.ts:34](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/general/icon/icon.component.ts#lines-34)

___

### handlebars

• `Protected` **handlebars**: typeof `Handlebars` = `HawkSearch.handlebars`

The Handlebars reference shared by all HawkSearch components.

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[handlebars](Components.BaseComponent.md#handlebars)

#### Defined in

[src/components/base.component.ts:23](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-23)

## Accessors

### configuration

• `Protected` `get` **configuration**(): `undefined` \| `TConfig`

The optional configuration object for this component.

#### Returns

`undefined` \| `TConfig`

#### Inherited from

BaseComponent.configuration

#### Defined in

[src/components/base.component.ts:61](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-61)

___

### rootElement

• `Protected` `get` **rootElement**(): `ParentNode`

The root element which should be used for querying any child elements. This resolves to `this.shadowRoot` if the Shadow DOM is enabled, otherwise `this`.

#### Returns

`ParentNode`

#### Inherited from

BaseComponent.rootElement

#### Defined in

[src/components/base.component.ts:78](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-78)

## Methods

### bindChildElements

▸ `Protected` **bindChildElements**(): `void`

After the component is rendered, this method is called to bind any child components.

#### Returns

`void`

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[bindChildElements](Components.BaseComponent.md#bindchildelements)

#### Defined in

[src/components/base.component.ts:257](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-257)

___

### getContentModel

▸ `Protected` **getContentModel**(): [`IconComponentModel`](../interfaces/Models.IconComponentModel.md)

#### Returns

[`IconComponentModel`](../interfaces/Models.IconComponentModel.md)

#### Overrides

BaseComponent.getContentModel

#### Defined in

[src/components/general/icon/icon.component.ts:59](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/general/icon/icon.component.ts#lines-59)

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

[BaseComponent](Components.BaseComponent.md).[interpolate](Components.BaseComponent.md#interpolate)

#### Defined in

[src/components/base.component.ts:308](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-308)

___

### onRender

▸ `Protected` **onRender**(): `void`

After the component is rendered, this method is called for any additional processing (such as attaching event listeners) which needs to occur.

#### Returns

`void`

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[onRender](Components.BaseComponent.md#onrender)

#### Defined in

[src/components/base.component.ts:264](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-264)

___

### registerHelpers

▸ `Protected` **registerHelpers**(): `void`

Optional method that can be overwritten to register Handlebars helper functions which can be accessed from the template. For more information, see [Custom Helpers](https://handlebarsjs.com/guide/#custom-helpers).

#### Returns

`void`

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[registerHelpers](Components.BaseComponent.md#registerhelpers)

#### Defined in

[src/components/base.component.ts:166](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-166)

___

### render

▸ **render**(): `void`

Binds [contentModel](Components.IconComponent.md#contentmodel) to the Handlebars template and renders the resulting HTML content.

#### Returns

`void`

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[render](Components.BaseComponent.md#render)

#### Defined in

[src/components/base.component.ts:171](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-171)

___

### renderContent

▸ `Protected` **renderContent**(): `boolean`

Determines whether the [data](Components.IconComponent.md#data) meets the necessary conditions to perform data binding and render content.

#### Returns

`boolean`

Whether the component should be rendered. If `false`, the component will have empty contents and be set to `display: none;`.

#### Overrides

[BaseComponent](Components.BaseComponent.md).[renderContent](Components.BaseComponent.md#rendercontent)

#### Defined in

[src/components/general/icon/icon.component.ts:55](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/general/icon/icon.component.ts#lines-55)
