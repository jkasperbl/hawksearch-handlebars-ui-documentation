[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Components](../modules/Components.md) / BaseComponent

# Class: BaseComponent<TConfig, TData, TModel\>

[Components](../modules/Components.md).BaseComponent

## Type parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `TConfig` | extends [`BaseComponentConfig`](../interfaces/Models.BaseComponentConfig.md) | Component configuration |
| `TData` | `TData` | Component data |
| `TModel` | extends [`BaseComponentModel`](../interfaces/Models.BaseComponentModel.md) | Data bound to Handlebars template |

## Hierarchy

- `HTMLElement`

  ↳ **`BaseComponent`**

  ↳↳ [`BaseContentComponent`](Components.BaseContentComponent.md)

  ↳↳ [`FeaturedItemsContentItemComponent`](Components.FeaturedItemsContentItemComponent.md)

  ↳↳ [`ContentZoneComponent`](Components.ContentZoneComponent.md)

  ↳↳ [`DatePickerComponent`](Components.DatePickerComponent.md)

  ↳↳ [`IconComponent`](Components.IconComponent.md)

  ↳↳ [`RangeSliderComponent`](Components.RangeSliderComponent.md)

  ↳↳ [`TooltipComponent`](Components.TooltipComponent.md)

  ↳↳ [`LandingPageComponent`](Components.LandingPageComponent.md)

  ↳↳ [`RecommendationsComponent`](Components.RecommendationsComponent.md)

  ↳↳ [`RecommendationsItemComponent`](Components.RecommendationsItemComponent.md)

  ↳↳ [`AutocompleteComponent`](Components.AutocompleteComponent.md)

  ↳↳ [`BaseFacetComponent`](Components.BaseFacetComponent.md)

  ↳↳ [`FacetWrapperComponent`](Components.FacetWrapperComponent.md)

  ↳↳ [`FacetsListComponent`](Components.FacetsListComponent.md)

  ↳↳ [`ModifiedQueryComponent`](Components.ModifiedQueryComponent.md)

  ↳↳ [`PageSizeComponent`](Components.PageSizeComponent.md)

  ↳↳ [`PaginationComponent`](Components.PaginationComponent.md)

  ↳↳ [`QuerySuggestionsComponent`](Components.QuerySuggestionsComponent.md)

  ↳↳ [`SearchFieldComponent`](Components.SearchFieldComponent.md)

  ↳↳ [`SearchResultsItemComponent`](Components.SearchResultsItemComponent.md)

  ↳↳ [`SearchResultsListComponent`](Components.SearchResultsListComponent.md)

  ↳↳ [`SearchResultsComponent`](Components.SearchResultsComponent.md)

  ↳↳ [`SelectedFacetsComponent`](Components.SelectedFacetsComponent.md)

  ↳↳ [`SortingComponent`](Components.SortingComponent.md)

  ↳↳ [`TabsComponent`](Components.TabsComponent.md)

## Table of contents

### Properties

- [contentModel](Components.BaseComponent.md#contentmodel)
- [data](Components.BaseComponent.md#data)
- [handlebars](Components.BaseComponent.md#handlebars)

### Accessors

- [configuration](Components.BaseComponent.md#configuration)
- [rootElement](Components.BaseComponent.md#rootelement)

### Methods

- [bindChildElements](Components.BaseComponent.md#bindchildelements)
- [interpolate](Components.BaseComponent.md#interpolate)
- [onRender](Components.BaseComponent.md#onrender)
- [registerHelpers](Components.BaseComponent.md#registerhelpers)
- [render](Components.BaseComponent.md#render)
- [renderContent](Components.BaseComponent.md#rendercontent)

## Properties

### contentModel

• `Protected` `Optional` **contentModel**: `TModel`

The data bound to the Handlebars template.

#### Defined in

[src/components/base.component.ts:35](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-35)

___

### data

• `Optional` **data**: `TData`

The data bound to the component.

#### Defined in

[src/components/base.component.ts:18](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-18)

___

### handlebars

• `Protected` **handlebars**: typeof `Handlebars` = `HawkSearch.handlebars`

The Handlebars reference shared by all HawkSearch components.

#### Defined in

[src/components/base.component.ts:23](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-23)

## Accessors

### configuration

• `Protected` `get` **configuration**(): `undefined` \| `TConfig`

The optional configuration object for this component.

#### Returns

`undefined` \| `TConfig`

#### Defined in

[src/components/base.component.ts:61](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-61)

___

### rootElement

• `Protected` `get` **rootElement**(): `ParentNode`

The root element which should be used for querying any child elements. This resolves to `this.shadowRoot` if the Shadow DOM is enabled, otherwise `this`.

#### Returns

`ParentNode`

#### Defined in

[src/components/base.component.ts:78](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-78)

## Methods

### bindChildElements

▸ `Protected` **bindChildElements**(): `void`

After the component is rendered, this method is called to bind any child components.

#### Returns

`void`

#### Defined in

[src/components/base.component.ts:257](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-257)

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

#### Defined in

[src/components/base.component.ts:308](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-308)

___

### onRender

▸ `Protected` **onRender**(): `void`

After the component is rendered, this method is called for any additional processing (such as attaching event listeners) which needs to occur.

#### Returns

`void`

#### Defined in

[src/components/base.component.ts:264](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-264)

___

### registerHelpers

▸ `Protected` **registerHelpers**(): `void`

Optional method that can be overwritten to register Handlebars helper functions which can be accessed from the template. For more information, see [Custom Helpers](https://handlebarsjs.com/guide/#custom-helpers).

#### Returns

`void`

#### Defined in

[src/components/base.component.ts:166](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-166)

___

### render

▸ **render**(): `void`

Binds [contentModel](Components.BaseComponent.md#contentmodel) to the Handlebars template and renders the resulting HTML content.

#### Returns

`void`

#### Defined in

[src/components/base.component.ts:171](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-171)

___

### renderContent

▸ `Protected` **renderContent**(): `boolean`

Determines whether the [data](Components.BaseComponent.md#data) meets the necessary conditions to perform data binding and render content.

#### Returns

`boolean`

Whether the component should be rendered. If `false`, the component will have empty contents and be set to `display: none;`.

#### Defined in

[src/components/base.component.ts:240](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-240)
