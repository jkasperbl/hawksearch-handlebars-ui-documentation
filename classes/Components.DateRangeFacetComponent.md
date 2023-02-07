[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Components](../modules/Components.md) / DateRangeFacetComponent

# Class: DateRangeFacetComponent

[Components](../modules/Components.md).DateRangeFacetComponent

The Date Range Facet component renders number input elements for minimum and maximum value.

## Tag
The tag for this component is `<hawksearch-date-range-facet>`.

## Event-Binding Attributes
| Name | Value |
| :- | :- |
| hawksearch-start | |
| hawksearch-end | |

These attributes should be placed on [Date Picker](Components.DatePickerComponent.md) elements. When these elements lose focus (blurred), the entered range will be applied as a facet value.

## Default Template
The following is the default Handlebars template for this component. To create a custom template, it is recommended to use this as a starting point.
```
<div class="date-range-facet">
    <div class="row">
        <div class="column column--6">
            <hawksearch-date-picker
                hawksearch-start
                value="{{startValue}}"
                min="{{minValue}}"
                max="{{endValue}}"
                label="{{strings.startDate}}"
            ></hawksearch-date-picker>
        </div>
        <div class="column column--6">
            <hawksearch-date-picker
                hawksearch-end
                value="{{endValue}}"
                min="{{startValue}}"
                max="{{maxValue}}"
                label="{{strings.endDate}}"
            ></hawksearch-date-picker>
        </div>
    </div>
</div>
```

## Hierarchy

- [`BaseFacetComponent`](Components.BaseFacetComponent.md)<[`DateRangeFacetComponentConfig`](../interfaces/Models.DateRangeFacetComponentConfig.md), [`DateRangeFacetComponentModel`](../interfaces/Models.DateRangeFacetComponentModel.md)\>

  ↳ **`DateRangeFacetComponent`**

## Table of contents

### Properties

- [bindFromEvent](Components.DateRangeFacetComponent.md#bindfromevent)
- [componentName](Components.DateRangeFacetComponent.md#componentname)
- [contentModel](Components.DateRangeFacetComponent.md#contentmodel)
- [data](Components.DateRangeFacetComponent.md#data)
- [defaultHtml](Components.DateRangeFacetComponent.md#defaulthtml)
- [handlebars](Components.DateRangeFacetComponent.md#handlebars)
- [state](Components.DateRangeFacetComponent.md#state)

### Accessors

- [configuration](Components.DateRangeFacetComponent.md#configuration)
- [rootElement](Components.DateRangeFacetComponent.md#rootelement)

### Methods

- [bindChildElements](Components.DateRangeFacetComponent.md#bindchildelements)
- [getContentModel](Components.DateRangeFacetComponent.md#getcontentmodel)
- [interpolate](Components.DateRangeFacetComponent.md#interpolate)
- [onRender](Components.DateRangeFacetComponent.md#onrender)
- [registerHelpers](Components.DateRangeFacetComponent.md#registerhelpers)
- [render](Components.DateRangeFacetComponent.md#render)
- [renderContent](Components.DateRangeFacetComponent.md#rendercontent)

## Properties

### bindFromEvent

• `Protected` **bindFromEvent**: `boolean` = `false`

#### Inherited from

[BaseFacetComponent](Components.BaseFacetComponent.md).[bindFromEvent](Components.BaseFacetComponent.md#bindfromevent)

#### Defined in

[src/components/search/facet-types/base-facet.component.ts:42](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/facet-types/base-facet.component.ts#lines-42)

___

### componentName

• `Protected` **componentName**: keyof [`HawkSearchComponents`](../interfaces/Models.HawkSearchComponents.md) = `'date-range-facet'`

#### Overrides

BaseFacetComponent.componentName

#### Defined in

[src/components/search/facet-types/date-range-facet/date-range-facet.component.ts:28](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/facet-types/date-range-facet/date-range-facet.component.ts#lines-28)

___

### contentModel

• `Protected` `Optional` **contentModel**: [`DateRangeFacetComponentModel`](../interfaces/Models.DateRangeFacetComponentModel.md)

The data bound to the Handlebars template.

#### Inherited from

[BaseFacetComponent](Components.BaseFacetComponent.md).[contentModel](Components.BaseFacetComponent.md#contentmodel)

#### Defined in

[src/components/base.component.ts:35](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-35)

___

### data

• `Optional` **data**: [`Facet`](../interfaces/Models.Facet.md)

The data bound to the component.

#### Inherited from

[BaseFacetComponent](Components.BaseFacetComponent.md).[data](Components.BaseFacetComponent.md#data)

#### Defined in

[src/components/base.component.ts:18](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-18)

___

### defaultHtml

• `Protected` **defaultHtml**: `any` = `defaultHtml`

#### Overrides

BaseFacetComponent.defaultHtml

#### Defined in

[src/components/search/facet-types/date-range-facet/date-range-facet.component.ts:29](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/facet-types/date-range-facet/date-range-facet.component.ts#lines-29)

___

### handlebars

• `Protected` **handlebars**: typeof `Handlebars` = `HawkSearch.handlebars`

The Handlebars reference shared by all HawkSearch components.

#### Inherited from

[BaseFacetComponent](Components.BaseFacetComponent.md).[handlebars](Components.BaseFacetComponent.md#handlebars)

#### Defined in

[src/components/base.component.ts:23](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-23)

___

### state

• **state**: [`FacetState`](../modules/Models.md#facetstate)

#### Inherited from

[BaseFacetComponent](Components.BaseFacetComponent.md).[state](Components.BaseFacetComponent.md#state)

#### Defined in

[src/components/search/facet-types/base-facet.component.ts:44](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/facet-types/base-facet.component.ts#lines-44)

## Accessors

### configuration

• `Protected` `get` **configuration**(): `undefined` \| `TConfig`

The optional configuration object for this component.

#### Returns

`undefined` \| `TConfig`

#### Inherited from

BaseFacetComponent.configuration

#### Defined in

[src/components/base.component.ts:61](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-61)

___

### rootElement

• `Protected` `get` **rootElement**(): `ParentNode`

The root element which should be used for querying any child elements. This resolves to `this.shadowRoot` if the Shadow DOM is enabled, otherwise `this`.

#### Returns

`ParentNode`

#### Inherited from

BaseFacetComponent.rootElement

#### Defined in

[src/components/base.component.ts:78](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-78)

## Methods

### bindChildElements

▸ `Protected` **bindChildElements**(): `void`

After the component is rendered, this method is called to bind any child components.

#### Returns

`void`

#### Overrides

[BaseFacetComponent](Components.BaseFacetComponent.md).[bindChildElements](Components.BaseFacetComponent.md#bindchildelements)

#### Defined in

[src/components/search/facet-types/date-range-facet/date-range-facet.component.ts:56](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/facet-types/date-range-facet/date-range-facet.component.ts#lines-56)

___

### getContentModel

▸ `Protected` **getContentModel**(): [`DateRangeFacetComponentModel`](../interfaces/Models.DateRangeFacetComponentModel.md)

#### Returns

[`DateRangeFacetComponentModel`](../interfaces/Models.DateRangeFacetComponentModel.md)

#### Overrides

BaseFacetComponent.getContentModel

#### Defined in

[src/components/search/facet-types/date-range-facet/date-range-facet.component.ts:43](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/facet-types/date-range-facet/date-range-facet.component.ts#lines-43)

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

[BaseFacetComponent](Components.BaseFacetComponent.md).[interpolate](Components.BaseFacetComponent.md#interpolate)

#### Defined in

[src/components/base.component.ts:308](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-308)

___

### onRender

▸ `Protected` **onRender**(): `void`

After the component is rendered, this method is called for any additional processing (such as attaching event listeners) which needs to occur.

#### Returns

`void`

#### Inherited from

[BaseFacetComponent](Components.BaseFacetComponent.md).[onRender](Components.BaseFacetComponent.md#onrender)

#### Defined in

[src/components/base.component.ts:264](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-264)

___

### registerHelpers

▸ `Protected` **registerHelpers**(): `void`

Optional method that can be overwritten to register Handlebars helper functions which can be accessed from the template. For more information, see [Custom Helpers](https://handlebarsjs.com/guide/#custom-helpers).

#### Returns

`void`

#### Inherited from

[BaseFacetComponent](Components.BaseFacetComponent.md).[registerHelpers](Components.BaseFacetComponent.md#registerhelpers)

#### Defined in

[src/components/base.component.ts:166](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-166)

___

### render

▸ **render**(): `void`

Binds [contentModel](Components.DateRangeFacetComponent.md#contentmodel) to the Handlebars template and renders the resulting HTML content.

#### Returns

`void`

#### Inherited from

[BaseFacetComponent](Components.BaseFacetComponent.md).[render](Components.BaseFacetComponent.md#render)

#### Defined in

[src/components/base.component.ts:171](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-171)

___

### renderContent

▸ `Protected` **renderContent**(): `boolean`

Determines whether the [data](Components.DateRangeFacetComponent.md#data) meets the necessary conditions to perform data binding and render content.

#### Returns

`boolean`

Whether the component should be rendered. If `false`, the component will have empty contents and be set to `display: none;`.

#### Overrides

[BaseFacetComponent](Components.BaseFacetComponent.md).[renderContent](Components.BaseFacetComponent.md#rendercontent)

#### Defined in

[src/components/search/facet-types/date-range-facet/date-range-facet.component.ts:39](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/facet-types/date-range-facet/date-range-facet.component.ts#lines-39)
