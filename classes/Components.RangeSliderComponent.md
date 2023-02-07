[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Components](../modules/Components.md) / RangeSliderComponent

# Class: RangeSliderComponent

[Components](../modules/Components.md).RangeSliderComponent

The Range Slider component provides a draggable interface that allows the user to select a range between 0-100. This component is currently only used within the [Range Slider Facet Component](Components.RangeSliderFacetComponent.md).

## Tag
The tag for this component is `<hawksearch-range-slider>`.

## Event-Binding Attributes
| Name | Value |
| :- | :- |
| hawksearch-handle | `'start'` or `'end'` |

This component should always have exactly two elements with the `hawksearch-handle` attribute: one with a value of `'start'`, and one with a value of `'end'`. This are the elements that the user will drag to adjust the selected range.

## Events
| Name | Data Type |
| :- | :- |
| hawksearch:range-slider-changed | [RangeSliderEventData](../interfaces/Models.RangeSliderEventData.md) |

This event fires repeatedly while the user is dragging the handles; it does not wait until the user deselects a handle.

*Note: The `min` and `max` values will always be between `0` and `100` inclusive.*

## Default Template
The following is the default Handlebars template for this component. To create a custom template, it is recommended to use this as a starting point.
```
<div class="range-slider">
    <div class="range-slider__container">
        <div class="range-slider__bar">
            <div class="range-slider__bar__active" hawksearch-bar style="left: {{start}}%; right: {{subtract 100 end}}%;"></div>
        </div>
        <span class="range-slider__handle range-slider__handle--start" title="{{strings.start}}" hawksearch-handle="start" style="left: {{start}}%;"></span>
        <span class="range-slider__handle range-slider__handle--end" title="{{strings.end}}" hawksearch-handle="end" style="left: {{end}}%;"></span>
    </div>
</div>
```

## Hierarchy

- [`BaseComponent`](Components.BaseComponent.md)<[`RangeSliderComponentConfig`](../interfaces/Models.RangeSliderComponentConfig.md), `never`, [`RangeSliderComponentModel`](../interfaces/Models.RangeSliderComponentModel.md)\>

  ↳ **`RangeSliderComponent`**

## Table of contents

### Properties

- [bindFromEvent](Components.RangeSliderComponent.md#bindfromevent)
- [componentName](Components.RangeSliderComponent.md#componentname)
- [contentModel](Components.RangeSliderComponent.md#contentmodel)
- [data](Components.RangeSliderComponent.md#data)
- [defaultHtml](Components.RangeSliderComponent.md#defaulthtml)
- [handlebars](Components.RangeSliderComponent.md#handlebars)

### Accessors

- [configuration](Components.RangeSliderComponent.md#configuration)
- [rootElement](Components.RangeSliderComponent.md#rootelement)
- [observedAttributes](Components.RangeSliderComponent.md#observedattributes)

### Methods

- [attributeChangedCallback](Components.RangeSliderComponent.md#attributechangedcallback)
- [bindChildElements](Components.RangeSliderComponent.md#bindchildelements)
- [connectedCallback](Components.RangeSliderComponent.md#connectedcallback)
- [disconnectedCallback](Components.RangeSliderComponent.md#disconnectedcallback)
- [getContentModel](Components.RangeSliderComponent.md#getcontentmodel)
- [interpolate](Components.RangeSliderComponent.md#interpolate)
- [onRender](Components.RangeSliderComponent.md#onrender)
- [registerHelpers](Components.RangeSliderComponent.md#registerhelpers)
- [render](Components.RangeSliderComponent.md#render)
- [renderContent](Components.RangeSliderComponent.md#rendercontent)

## Properties

### bindFromEvent

• `Protected` **bindFromEvent**: `boolean` = `false`

#### Overrides

BaseComponent.bindFromEvent

#### Defined in

[src/components/general/range-slider/range-slider.component.ts:40](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/general/range-slider/range-slider.component.ts#lines-40)

___

### componentName

• `Protected` **componentName**: keyof [`HawkSearchComponents`](../interfaces/Models.HawkSearchComponents.md) = `'range-slider'`

#### Overrides

BaseComponent.componentName

#### Defined in

[src/components/general/range-slider/range-slider.component.ts:38](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/general/range-slider/range-slider.component.ts#lines-38)

___

### contentModel

• `Protected` `Optional` **contentModel**: [`RangeSliderComponentModel`](../interfaces/Models.RangeSliderComponentModel.md)

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

[src/components/general/range-slider/range-slider.component.ts:39](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/general/range-slider/range-slider.component.ts#lines-39)

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

___

### observedAttributes

• `Static` `get` **observedAttributes**(): `string`[]

#### Returns

`string`[]

#### Defined in

[src/components/general/range-slider/range-slider.component.ts:34](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/general/range-slider/range-slider.component.ts#lines-34)

## Methods

### attributeChangedCallback

▸ **attributeChangedCallback**(`name`, `oldValue`, `newValue`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `name` | `string` |
| `oldValue` | ``null`` \| `string` |
| `newValue` | ``null`` \| `string` |

#### Returns

`void`

#### Defined in

[src/components/general/range-slider/range-slider.component.ts:61](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/general/range-slider/range-slider.component.ts#lines-61)

___

### bindChildElements

▸ `Protected` **bindChildElements**(): `void`

After the component is rendered, this method is called to bind any child components.

#### Returns

`void`

#### Overrides

[BaseComponent](Components.BaseComponent.md).[bindChildElements](Components.BaseComponent.md#bindchildelements)

#### Defined in

[src/components/general/range-slider/range-slider.component.ts:112](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/general/range-slider/range-slider.component.ts#lines-112)

___

### connectedCallback

▸ **connectedCallback**(): `void`

#### Returns

`void`

#### Overrides

BaseComponent.connectedCallback

#### Defined in

[src/components/general/range-slider/range-slider.component.ts:51](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/general/range-slider/range-slider.component.ts#lines-51)

___

### disconnectedCallback

▸ **disconnectedCallback**(): `void`

#### Returns

`void`

#### Overrides

BaseComponent.disconnectedCallback

#### Defined in

[src/components/general/range-slider/range-slider.component.ts:74](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/general/range-slider/range-slider.component.ts#lines-74)

___

### getContentModel

▸ `Protected` **getContentModel**(): [`RangeSliderComponentModel`](../interfaces/Models.RangeSliderComponentModel.md)

#### Returns

[`RangeSliderComponentModel`](../interfaces/Models.RangeSliderComponentModel.md)

#### Overrides

BaseComponent.getContentModel

#### Defined in

[src/components/general/range-slider/range-slider.component.ts:101](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/general/range-slider/range-slider.component.ts#lines-101)

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

Binds [contentModel](Components.RangeSliderComponent.md#contentmodel) to the Handlebars template and renders the resulting HTML content.

#### Returns

`void`

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[render](Components.BaseComponent.md#render)

#### Defined in

[src/components/base.component.ts:171](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-171)

___

### renderContent

▸ `Protected` **renderContent**(): `boolean`

Determines whether the [data](Components.RangeSliderComponent.md#data) meets the necessary conditions to perform data binding and render content.

#### Returns

`boolean`

Whether the component should be rendered. If `false`, the component will have empty contents and be set to `display: none;`.

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[renderContent](Components.BaseComponent.md#rendercontent)

#### Defined in

[src/components/base.component.ts:240](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-240)
