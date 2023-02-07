[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Components](../modules/Components.md) / BaseFacetComponent

# Class: BaseFacetComponent<TConfig, TModel\>

[Components](../modules/Components.md).BaseFacetComponent

The Base Facet component is inherited by all facet type copmonents.

## Event-Binding Attributes
The following attributes are common to all facet type components. Individual facet types may support additional attribute bindings.

| Name | Value |
| :- | :- |
| hawksearch-facet-value | `string` (if applicable) |

When a checkbox input element with this attribute is checked or unchecked, the value of that element will be added or removed from the search request as appropriate. For non-input elements, the attribute value will be used instead of a form element value.

| Name | Value |
| :- | :- |
| hawksearch-facet-value-exclude | `string` |

When an element with this attribute is clicked, search results with the corresponding attribute value will be excluded from search results.

| Name | Value |
| :- | :- |
| hawksearch-facet-value-include | `string` |

When an element with this attribute is clicked, search results with the corresponding attribute value will no longer be excluded from search results.

*Note: Elements with this attribute value should only be displayed for facet values that are excluded.*

| Name | Value |
| :- | :- |
| hawksearch-facet-value-toggle | |

When an element with this attribute is clicked, child facet values will be displayed or hidden as appropriate.

*Note: This attribute should only be used for facets that support nested values.*

## Type parameters

| Name | Type |
| :------ | :------ |
| `TConfig` | extends [`BaseComponentConfig`](../interfaces/Models.BaseComponentConfig.md) |
| `TModel` | extends [`BaseComponentModel`](../interfaces/Models.BaseComponentModel.md) |

## Hierarchy

- [`BaseComponent`](Components.BaseComponent.md)<`TConfig`, [`Facet`](../interfaces/Models.Facet.md), `TModel`\>

  ↳ **`BaseFacetComponent`**

  ↳↳ [`CheckboxListFacetComponent`](Components.CheckboxListFacetComponent.md)

  ↳↳ [`ColorFacetComponent`](Components.ColorFacetComponent.md)

  ↳↳ [`DateRangeFacetComponent`](Components.DateRangeFacetComponent.md)

  ↳↳ [`LinkListFacetComponent`](Components.LinkListFacetComponent.md)

  ↳↳ [`NumericRangeFacetComponent`](Components.NumericRangeFacetComponent.md)

  ↳↳ [`RangeSliderFacetComponent`](Components.RangeSliderFacetComponent.md)

  ↳↳ [`RecentSearchesFacetComponent`](Components.RecentSearchesFacetComponent.md)

  ↳↳ [`RelatedSearchesFacetComponent`](Components.RelatedSearchesFacetComponent.md)

  ↳↳ [`SearchWithinFacetComponent`](Components.SearchWithinFacetComponent.md)

  ↳↳ [`SizeFacetComponent`](Components.SizeFacetComponent.md)

## Table of contents

### Properties

- [bindFromEvent](Components.BaseFacetComponent.md#bindfromevent)
- [contentModel](Components.BaseFacetComponent.md#contentmodel)
- [data](Components.BaseFacetComponent.md#data)
- [handlebars](Components.BaseFacetComponent.md#handlebars)
- [state](Components.BaseFacetComponent.md#state)

### Accessors

- [configuration](Components.BaseFacetComponent.md#configuration)
- [rootElement](Components.BaseFacetComponent.md#rootelement)

### Methods

- [bindChildElements](Components.BaseFacetComponent.md#bindchildelements)
- [interpolate](Components.BaseFacetComponent.md#interpolate)
- [onRender](Components.BaseFacetComponent.md#onrender)
- [registerHelpers](Components.BaseFacetComponent.md#registerhelpers)
- [render](Components.BaseFacetComponent.md#render)
- [renderContent](Components.BaseFacetComponent.md#rendercontent)

## Properties

### bindFromEvent

• `Protected` **bindFromEvent**: `boolean` = `false`

#### Overrides

BaseComponent.bindFromEvent

#### Defined in

[src/components/search/facet-types/base-facet.component.ts:42](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/facet-types/base-facet.component.ts#lines-42)

___

### contentModel

• `Protected` `Optional` **contentModel**: `TModel`

The data bound to the Handlebars template.

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[contentModel](Components.BaseComponent.md#contentmodel)

#### Defined in

[src/components/base.component.ts:35](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-35)

___

### data

• `Optional` **data**: [`Facet`](../interfaces/Models.Facet.md)

The data bound to the component.

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[data](Components.BaseComponent.md#data)

#### Defined in

[src/components/base.component.ts:18](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-18)

___

### handlebars

• `Protected` **handlebars**: typeof `Handlebars` = `HawkSearch.handlebars`

The Handlebars reference shared by all HawkSearch components.

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[handlebars](Components.BaseComponent.md#handlebars)

#### Defined in

[src/components/base.component.ts:23](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-23)

___

### state

• **state**: [`FacetState`](../modules/Models.md#facetstate)

#### Defined in

[src/components/search/facet-types/base-facet.component.ts:44](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/facet-types/base-facet.component.ts#lines-44)

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

[src/components/search/facet-types/base-facet.component.ts:46](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/facet-types/base-facet.component.ts#lines-46)

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

Binds [contentModel](Components.BaseFacetComponent.md#contentmodel) to the Handlebars template and renders the resulting HTML content.

#### Returns

`void`

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[render](Components.BaseComponent.md#render)

#### Defined in

[src/components/base.component.ts:171](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-171)

___

### renderContent

▸ `Protected` **renderContent**(): `boolean`

Determines whether the [data](Components.BaseFacetComponent.md#data) meets the necessary conditions to perform data binding and render content.

#### Returns

`boolean`

Whether the component should be rendered. If `false`, the component will have empty contents and be set to `display: none;`.

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[renderContent](Components.BaseComponent.md#rendercontent)

#### Defined in

[src/components/base.component.ts:240](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-240)
