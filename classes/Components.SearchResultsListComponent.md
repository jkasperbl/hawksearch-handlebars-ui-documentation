[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Components](../modules/Components.md) / SearchResultsListComponent

# Class: SearchResultsListComponent

[Components](../modules/Components.md).SearchResultsListComponent

The Search Results List component is a wrapper around a group of [Search Results Item](Components.SearchResultsItemComponent.md) components.

## Tag
The tag for this component is `<hawksearch-search-results-list>`.

## Default Template
The following is the default Handlebars template for this component. To create a custom template, it is recommended to use this as a starting point.
```
<div class="row search-results-list">
    {{#each items}}
        {{#if (eq type "content")}}
            <div class="column column--12">
                <hawksearch-search-results-item></hawksearch-search-results-item>
            </div>
        {{else}}
            <div class="column column--12 column-sm--6 column-lg--4">
                <hawksearch-search-results-item></hawksearch-search-results-item>
            </div>
        {{/if}}
    {{/each}}
</div>
```

## Hierarchy

- [`BaseComponent`](Components.BaseComponent.md)<[`SearchResultsListComponentConfig`](../interfaces/Models.SearchResultsListComponentConfig.md), [`SearchResultsItem`](../interfaces/Models.SearchResultsItem.md)[], [`SearchResultsListComponentModel`](../interfaces/Models.SearchResultsListComponentModel.md)\>

  ↳ **`SearchResultsListComponent`**

## Table of contents

### Properties

- [bindFromEvent](Components.SearchResultsListComponent.md#bindfromevent)
- [componentName](Components.SearchResultsListComponent.md#componentname)
- [contentModel](Components.SearchResultsListComponent.md#contentmodel)
- [data](Components.SearchResultsListComponent.md#data)
- [defaultHtml](Components.SearchResultsListComponent.md#defaulthtml)
- [handlebars](Components.SearchResultsListComponent.md#handlebars)

### Accessors

- [configuration](Components.SearchResultsListComponent.md#configuration)
- [rootElement](Components.SearchResultsListComponent.md#rootelement)

### Methods

- [bindChildElements](Components.SearchResultsListComponent.md#bindchildelements)
- [getContentModel](Components.SearchResultsListComponent.md#getcontentmodel)
- [interpolate](Components.SearchResultsListComponent.md#interpolate)
- [onRender](Components.SearchResultsListComponent.md#onrender)
- [registerHelpers](Components.SearchResultsListComponent.md#registerhelpers)
- [render](Components.SearchResultsListComponent.md#render)
- [renderContent](Components.SearchResultsListComponent.md#rendercontent)

## Properties

### bindFromEvent

• `Protected` **bindFromEvent**: `boolean` = `true`

#### Overrides

BaseComponent.bindFromEvent

#### Defined in

[src/components/search/search-results-list/search-results-list.component.ts:21](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/search-results-list/search-results-list.component.ts#lines-21)

___

### componentName

• `Protected` **componentName**: keyof [`HawkSearchComponents`](../interfaces/Models.HawkSearchComponents.md) = `'search-results-list'`

#### Overrides

BaseComponent.componentName

#### Defined in

[src/components/search/search-results-list/search-results-list.component.ts:19](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/search-results-list/search-results-list.component.ts#lines-19)

___

### contentModel

• `Protected` `Optional` **contentModel**: [`SearchResultsListComponentModel`](../interfaces/Models.SearchResultsListComponentModel.md)

The data bound to the Handlebars template.

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[contentModel](Components.BaseComponent.md#contentmodel)

#### Defined in

[src/components/base.component.ts:35](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-35)

___

### data

• `Optional` **data**: [`SearchResultsItem`](../interfaces/Models.SearchResultsItem.md)[]

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

[src/components/search/search-results-list/search-results-list.component.ts:20](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/search-results-list/search-results-list.component.ts#lines-20)

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

[src/components/search/search-results-list/search-results-list.component.ts:33](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/search-results-list/search-results-list.component.ts#lines-33)

___

### getContentModel

▸ `Protected` **getContentModel**(): [`SearchResultsListComponentModel`](../interfaces/Models.SearchResultsListComponentModel.md)

#### Returns

[`SearchResultsListComponentModel`](../interfaces/Models.SearchResultsListComponentModel.md)

#### Overrides

BaseComponent.getContentModel

#### Defined in

[src/components/search/search-results-list/search-results-list.component.ts:27](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/search-results-list/search-results-list.component.ts#lines-27)

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

Binds [contentModel](Components.SearchResultsListComponent.md#contentmodel) to the Handlebars template and renders the resulting HTML content.

#### Returns

`void`

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[render](Components.BaseComponent.md#render)

#### Defined in

[src/components/base.component.ts:171](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-171)

___

### renderContent

▸ `Protected` **renderContent**(): `boolean`

Determines whether the [data](Components.SearchResultsListComponent.md#data) meets the necessary conditions to perform data binding and render content.

#### Returns

`boolean`

Whether the component should be rendered. If `false`, the component will have empty contents and be set to `display: none;`.

#### Overrides

[BaseComponent](Components.BaseComponent.md).[renderContent](Components.BaseComponent.md#rendercontent)

#### Defined in

[src/components/search/search-results-list/search-results-list.component.ts:23](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/search-results-list/search-results-list.component.ts#lines-23)
