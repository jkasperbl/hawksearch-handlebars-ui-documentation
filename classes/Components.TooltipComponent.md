[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Components](../modules/Components.md) / TooltipComponent

# Class: TooltipComponent

[Components](../modules/Components.md).TooltipComponent

The Tooltip component is used to display a brief explanation or contextual information when the user hovers over an element.

## Tag
The tag for this component is `<hawksearch-tooltip>`.

## Event-Binding Attributes
| Name | Value |
| :- | :- |
| hawksearch-tooltip | |
| hawksearch-tooltip-content | |

These attributes are used to position the tooltip based on the size and scroll position of the active window. The `hawksearch-tooltip` attribute should be present on an element containing both the element the tooltip is attached to (to display on hover) and the element containing the tooltip content, which should have a `hawksearch-tooltip-content` attribute.

## Default Template
The following is the default Handlebars template for this component. To create a custom template, it is recommended to use this as a starting point.
```
<span class="tooltip" hawksearch-tooltip>
    <span class="tooltip__icon">
        <hawksearch-icon name="help" class="facet__heading__tooltip"></hawksearch-icon>
    </span>
    <span class="tooltip__content" hawksearch-tooltip-content>{{text}}</span>
</span>
```

## Hierarchy

- [`BaseComponent`](Components.BaseComponent.md)<[`TooltipComponentConfig`](../interfaces/Models.TooltipComponentConfig.md), `string`, [`TooltipComponentModel`](../interfaces/Models.TooltipComponentModel.md)\>

  ↳ **`TooltipComponent`**

## Table of contents

### Properties

- [bindFromEvent](Components.TooltipComponent.md#bindfromevent)
- [componentName](Components.TooltipComponent.md#componentname)
- [contentModel](Components.TooltipComponent.md#contentmodel)
- [data](Components.TooltipComponent.md#data)
- [defaultHtml](Components.TooltipComponent.md#defaulthtml)
- [handlebars](Components.TooltipComponent.md#handlebars)

### Accessors

- [configuration](Components.TooltipComponent.md#configuration)
- [rootElement](Components.TooltipComponent.md#rootelement)

### Methods

- [bindChildElements](Components.TooltipComponent.md#bindchildelements)
- [getContentModel](Components.TooltipComponent.md#getcontentmodel)
- [interpolate](Components.TooltipComponent.md#interpolate)
- [onRender](Components.TooltipComponent.md#onrender)
- [registerHelpers](Components.TooltipComponent.md#registerhelpers)
- [render](Components.TooltipComponent.md#render)
- [renderContent](Components.TooltipComponent.md#rendercontent)

## Properties

### bindFromEvent

• `Protected` **bindFromEvent**: `boolean` = `false`

#### Overrides

BaseComponent.bindFromEvent

#### Defined in

[src/components/general/tooltip/tooltip.component.ts:28](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/general/tooltip/tooltip.component.ts#lines-28)

___

### componentName

• `Protected` **componentName**: keyof [`HawkSearchComponents`](../interfaces/Models.HawkSearchComponents.md) = `'tooltip'`

#### Overrides

BaseComponent.componentName

#### Defined in

[src/components/general/tooltip/tooltip.component.ts:26](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/general/tooltip/tooltip.component.ts#lines-26)

___

### contentModel

• `Protected` `Optional` **contentModel**: [`TooltipComponentModel`](../interfaces/Models.TooltipComponentModel.md)

The data bound to the Handlebars template.

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[contentModel](Components.BaseComponent.md#contentmodel)

#### Defined in

[src/components/base.component.ts:35](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-35)

___

### data

• `Optional` **data**: `string`

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

[src/components/general/tooltip/tooltip.component.ts:27](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/general/tooltip/tooltip.component.ts#lines-27)

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

#### Overrides

[BaseComponent](Components.BaseComponent.md).[bindChildElements](Components.BaseComponent.md#bindchildelements)

#### Defined in

[src/components/general/tooltip/tooltip.component.ts:44](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/general/tooltip/tooltip.component.ts#lines-44)

___

### getContentModel

▸ `Protected` **getContentModel**(): [`TooltipComponentModel`](../interfaces/Models.TooltipComponentModel.md)

#### Returns

[`TooltipComponentModel`](../interfaces/Models.TooltipComponentModel.md)

#### Overrides

BaseComponent.getContentModel

#### Defined in

[src/components/general/tooltip/tooltip.component.ts:38](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/general/tooltip/tooltip.component.ts#lines-38)

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

Binds [contentModel](Components.TooltipComponent.md#contentmodel) to the Handlebars template and renders the resulting HTML content.

#### Returns

`void`

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[render](Components.BaseComponent.md#render)

#### Defined in

[src/components/base.component.ts:171](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-171)

___

### renderContent

▸ `Protected` **renderContent**(): `boolean`

Determines whether the [data](Components.TooltipComponent.md#data) meets the necessary conditions to perform data binding and render content.

#### Returns

`boolean`

Whether the component should be rendered. If `false`, the component will have empty contents and be set to `display: none;`.

#### Overrides

[BaseComponent](Components.BaseComponent.md).[renderContent](Components.BaseComponent.md#rendercontent)

#### Defined in

[src/components/general/tooltip/tooltip.component.ts:34](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/general/tooltip/tooltip.component.ts#lines-34)
