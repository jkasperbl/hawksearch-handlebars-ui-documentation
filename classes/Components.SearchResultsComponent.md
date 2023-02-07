[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Components](../modules/Components.md) / SearchResultsComponent

# Class: SearchResultsComponent

[Components](../modules/Components.md).SearchResultsComponent

The Search Results component encapsulates all components relating to search-results.

## Tag
The tag for this component is `<hawksearch-search-results>`.

## Default Template
The following is the default Handlebars template for this component. To create a custom template, it is recommended to use this as a starting point.
```
<hawksearch-modified-query></hawksearch-modified-query>
<hawksearch-query-suggestions></hawksearch-query-suggestions>
<div class="row">
    <div class="column column--12 column-md--4">
        <hawksearch-content-zone name="LeftTop"></hawksearch-content-zone>
        <hawksearch-facets-list></hawksearch-facets-list>
        <hawksearch-content-zone name="LeftBottom"></hawksearch-content-zone>
    </div>
    <div class="column column--12 column-md--8">
        <hawksearch-content-zone name="Top"></hawksearch-content-zone>
        <hawksearch-content-zone name="Top2"></hawksearch-content-zone>
        <hawksearch-tabs></hawksearch-tabs>
        <hawksearch-selected-facets></hawksearch-selected-facets>
        <div class="row">
            <div class="column column--12 column-sm--6 flex-vertical-sm-center">
                <hawksearch-pagination></hawksearch-pagination>
            </div>
            <div class="column column--12 column-md--6">
                <div class="row row--tight">
                    <div class="column column--12 column-sm--6 flex-vertical-sm-center">
                        <hawksearch-page-size></hawksearch-page-size>
                    </div>
                    <div class="column column--12 column-sm--6 flex-vertical-sm-center">
                        <hawksearch-sorting></hawksearch-sorting>
                    </div>
                </div>
            </div>
        </div>
        <hawksearch-search-results-list></hawksearch-search-results-list>
        <hawksearch-content-zone name="Bottom"></hawksearch-content-zone>
        <hawksearch-content-zone name="Bottom2"></hawksearch-content-zone>
    </div>
</div>
```

## Hierarchy

- [`BaseComponent`](Components.BaseComponent.md)<[`SearchResultsComponentConfig`](../interfaces/Models.SearchResultsComponentConfig.md), [`SearchResponse`](../interfaces/Models.SearchResponse.md), [`SearchResultsComponentModel`](../interfaces/Models.SearchResultsComponentModel.md)\>

  ↳ **`SearchResultsComponent`**

## Table of contents

### Constructors

- [constructor](Components.SearchResultsComponent.md#constructor)

### Properties

- [bindFromEvent](Components.SearchResultsComponent.md#bindfromevent)
- [componentName](Components.SearchResultsComponent.md#componentname)
- [contentModel](Components.SearchResultsComponent.md#contentmodel)
- [data](Components.SearchResultsComponent.md#data)
- [defaultHtml](Components.SearchResultsComponent.md#defaulthtml)
- [handlebars](Components.SearchResultsComponent.md#handlebars)

### Accessors

- [configuration](Components.SearchResultsComponent.md#configuration)
- [mode](Components.SearchResultsComponent.md#mode)
- [rootElement](Components.SearchResultsComponent.md#rootelement)
- [url](Components.SearchResultsComponent.md#url)

### Methods

- [bindChildElements](Components.SearchResultsComponent.md#bindchildelements)
- [getContentModel](Components.SearchResultsComponent.md#getcontentmodel)
- [interpolate](Components.SearchResultsComponent.md#interpolate)
- [onRender](Components.SearchResultsComponent.md#onrender)
- [registerHelpers](Components.SearchResultsComponent.md#registerhelpers)
- [render](Components.SearchResultsComponent.md#render)
- [renderContent](Components.SearchResultsComponent.md#rendercontent)

## Constructors

### constructor

• **new SearchResultsComponent**()

#### Overrides

BaseComponent&lt;SearchResultsComponentConfig, SearchResponse, SearchResultsComponentModel\&gt;.constructor

#### Defined in

[src/components/search/search-results/search-results.component.ts:46](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/search-results/search-results.component.ts#lines-46)

## Properties

### bindFromEvent

• `Protected` **bindFromEvent**: `boolean` = `true`

#### Overrides

BaseComponent.bindFromEvent

#### Defined in

[src/components/search/search-results/search-results.component.ts:21](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/search-results/search-results.component.ts#lines-21)

___

### componentName

• `Protected` **componentName**: keyof [`HawkSearchComponents`](../interfaces/Models.HawkSearchComponents.md) = `'search-results'`

#### Overrides

BaseComponent.componentName

#### Defined in

[src/components/search/search-results/search-results.component.ts:19](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/search-results/search-results.component.ts#lines-19)

___

### contentModel

• `Protected` `Optional` **contentModel**: [`SearchResultsComponentModel`](../interfaces/Models.SearchResultsComponentModel.md)

The data bound to the Handlebars template.

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[contentModel](Components.BaseComponent.md#contentmodel)

#### Defined in

[src/components/base.component.ts:35](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-35)

___

### data

• `Optional` **data**: [`SearchResponse`](../interfaces/Models.SearchResponse.md)

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

[src/components/search/search-results/search-results.component.ts:20](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/search-results/search-results.component.ts#lines-20)

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

### mode

• `Protected` `get` **mode**(): [`SearchResultsMode`](../modules/Models.md#searchresultsmode)

Speficies the context that the component is being used. This is determined by the `mode` attribute on the HTML element.

**`Default Value`**

`'search-results'`

#### Returns

[`SearchResultsMode`](../modules/Models.md#searchresultsmode)

#### Defined in

[src/components/search/search-results/search-results.component.ts:28](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/search-results/search-results.component.ts#lines-28)

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

### url

• `Protected` `get` **url**(): `string`

If [mode](Components.SearchResultsComponent.md#mode) is set to `'landing-page'`, this specifies the URL sent to retrieve content from HawkSearch. This can be customized by setting the `url` attribute on the HTML element.

**`Default Value`**

`window.location.pathname`

#### Returns

`string`

#### Defined in

[src/components/search/search-results/search-results.component.ts:42](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/search-results/search-results.component.ts#lines-42)

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

▸ `Protected` **getContentModel**(): [`SearchResultsComponentModel`](../interfaces/Models.SearchResultsComponentModel.md)

#### Returns

[`SearchResultsComponentModel`](../interfaces/Models.SearchResultsComponentModel.md)

#### Overrides

BaseComponent.getContentModel

#### Defined in

[src/components/search/search-results/search-results.component.ts:58](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/search-results/search-results.component.ts#lines-58)

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

Binds [contentModel](Components.SearchResultsComponent.md#contentmodel) to the Handlebars template and renders the resulting HTML content.

#### Returns

`void`

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[render](Components.BaseComponent.md#render)

#### Defined in

[src/components/base.component.ts:171](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-171)

___

### renderContent

▸ `Protected` **renderContent**(): `boolean`

Determines whether the [data](Components.SearchResultsComponent.md#data) meets the necessary conditions to perform data binding and render content.

#### Returns

`boolean`

Whether the component should be rendered. If `false`, the component will have empty contents and be set to `display: none;`.

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[renderContent](Components.BaseComponent.md#rendercontent)

#### Defined in

[src/components/base.component.ts:240](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-240)
