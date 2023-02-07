[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Components](../modules/Components.md) / QuerySuggestionsComponent

# Class: QuerySuggestionsComponent

[Components](../modules/Components.md).QuerySuggestionsComponent

The Query Suggestions component displays a list of possible queries that the search engine detects the user may be looking for.

## Tag
The tag for this component is `<hawksearch-query-suggestions>`.

## Event-Binding Attributes
| Name | Value |
| :- | :- |
| hawksearch-query | `string` |

When an element with this attribute is clicked, a new search will be formed for the specified query.

## Handlebars Helpers
| Name | Parameter |
| :- | :- |
| query-suggestions | `Array<string>` |

This helper function creates a comma-separated list of links with the `hawksearch-query` attribute, using the word “or” before the last link.

## Default Template
The following is the default Handlebars template for this component. To create a custom template, it is recommended to use this as a starting point.
```
<div class="query-suggestions">
    <p>{{query-suggestions querySuggestions}}</p>
</div>
```

## Hierarchy

- [`BaseComponent`](Components.BaseComponent.md)<[`QuerySuggestionsComponentConfig`](../interfaces/Models.QuerySuggestionsComponentConfig.md), [`QuerySuggestionsData`](../interfaces/Models.QuerySuggestionsData.md), [`QuerySuggestionsComponentModel`](../interfaces/Models.QuerySuggestionsComponentModel.md)\>

  ↳ **`QuerySuggestionsComponent`**

## Table of contents

### Properties

- [bindFromEvent](Components.QuerySuggestionsComponent.md#bindfromevent)
- [componentName](Components.QuerySuggestionsComponent.md#componentname)
- [contentModel](Components.QuerySuggestionsComponent.md#contentmodel)
- [data](Components.QuerySuggestionsComponent.md#data)
- [defaultHtml](Components.QuerySuggestionsComponent.md#defaulthtml)
- [handlebars](Components.QuerySuggestionsComponent.md#handlebars)

### Accessors

- [configuration](Components.QuerySuggestionsComponent.md#configuration)
- [rootElement](Components.QuerySuggestionsComponent.md#rootelement)

### Methods

- [bindChildElements](Components.QuerySuggestionsComponent.md#bindchildelements)
- [getContentModel](Components.QuerySuggestionsComponent.md#getcontentmodel)
- [interpolate](Components.QuerySuggestionsComponent.md#interpolate)
- [onRender](Components.QuerySuggestionsComponent.md#onrender)
- [registerHelpers](Components.QuerySuggestionsComponent.md#registerhelpers)
- [render](Components.QuerySuggestionsComponent.md#render)
- [renderContent](Components.QuerySuggestionsComponent.md#rendercontent)

## Properties

### bindFromEvent

• `Protected` **bindFromEvent**: `boolean` = `true`

#### Overrides

BaseComponent.bindFromEvent

#### Defined in

[src/components/search/query-suggestions/query-suggestions.component.ts:38](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/query-suggestions/query-suggestions.component.ts#lines-38)

___

### componentName

• `Protected` **componentName**: keyof [`HawkSearchComponents`](../interfaces/Models.HawkSearchComponents.md) = `'query-suggestions'`

#### Overrides

BaseComponent.componentName

#### Defined in

[src/components/search/query-suggestions/query-suggestions.component.ts:36](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/query-suggestions/query-suggestions.component.ts#lines-36)

___

### contentModel

• `Protected` `Optional` **contentModel**: [`QuerySuggestionsComponentModel`](../interfaces/Models.QuerySuggestionsComponentModel.md)

The data bound to the Handlebars template.

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[contentModel](Components.BaseComponent.md#contentmodel)

#### Defined in

[src/components/base.component.ts:35](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-35)

___

### data

• `Optional` **data**: [`QuerySuggestionsData`](../interfaces/Models.QuerySuggestionsData.md)

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

[src/components/search/query-suggestions/query-suggestions.component.ts:37](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/query-suggestions/query-suggestions.component.ts#lines-37)

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

[src/components/search/query-suggestions/query-suggestions.component.ts:84](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/query-suggestions/query-suggestions.component.ts#lines-84)

___

### getContentModel

▸ `Protected` **getContentModel**(): [`QuerySuggestionsComponentModel`](../interfaces/Models.QuerySuggestionsComponentModel.md)

#### Returns

[`QuerySuggestionsComponentModel`](../interfaces/Models.QuerySuggestionsComponentModel.md)

#### Overrides

BaseComponent.getContentModel

#### Defined in

[src/components/search/query-suggestions/query-suggestions.component.ts:78](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/query-suggestions/query-suggestions.component.ts#lines-78)

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

#### Overrides

[BaseComponent](Components.BaseComponent.md).[registerHelpers](Components.BaseComponent.md#registerhelpers)

#### Defined in

[src/components/search/query-suggestions/query-suggestions.component.ts:40](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/query-suggestions/query-suggestions.component.ts#lines-40)

___

### render

▸ **render**(): `void`

Binds [contentModel](Components.QuerySuggestionsComponent.md#contentmodel) to the Handlebars template and renders the resulting HTML content.

#### Returns

`void`

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[render](Components.BaseComponent.md#render)

#### Defined in

[src/components/base.component.ts:171](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-171)

___

### renderContent

▸ `Protected` **renderContent**(): `boolean`

Determines whether the [data](Components.QuerySuggestionsComponent.md#data) meets the necessary conditions to perform data binding and render content.

#### Returns

`boolean`

Whether the component should be rendered. If `false`, the component will have empty contents and be set to `display: none;`.

#### Overrides

[BaseComponent](Components.BaseComponent.md).[renderContent](Components.BaseComponent.md#rendercontent)

#### Defined in

[src/components/search/query-suggestions/query-suggestions.component.ts:74](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/query-suggestions/query-suggestions.component.ts#lines-74)
