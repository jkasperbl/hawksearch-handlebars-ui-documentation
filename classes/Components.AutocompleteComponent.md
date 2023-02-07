[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Components](../modules/Components.md) / AutocompleteComponent

# Class: AutocompleteComponent

[Components](../modules/Components.md).AutocompleteComponent

The Autocomplete component displays a preview of search results after a user begins to type a query in the [SearchFieldComponent](Components.SearchFieldComponent.md).

## Tag
The tag for this component is `<hawksearch-autocomplete>`.

## Event-Binding Attributes
### Categories
| Name | Value |
| :- | :- |
| hawksearch-category-field | [field](../interfaces/Models.AutocompleteCategory.md#field) |
| hawksearch-category-field | [value](../interfaces/Models.AutocompleteCategory.md#value) |

### Content Results
| Name | Value |
| :- | :- |
| hawksearch-content | [id](../interfaces/Models.AutocompleteProductResult.md#id) |

When an element with this attribute is clicked, the click will be tracked and the user will be redirected to the page corresponding to that content item.

### Product Results
| Name | Value |
| :- | :- |
| hawksearch-product | [id](../interfaces/Models.AutocompleteProductResult.md#id) |

When an element with this attribute is clicked, the click will be tracked and the user will be redirected to the page corresponding to that content item.

### Query Results (Popular Queries)
| Name | Value |
| :- | :- |
| hawksearch-query | [query](../interfaces/Models.AutocompleteQuery.md#query) |

When an element with this attribute is clicked, the click will be tracked and the user will be redirected to the page corresponding to that product.

### View All Results
| Name | Value |
| :- | :- |
| hawksearch-view-all | |

When an element with this attribute is clicked, a new search will be executed with the query entered in the search box.

## Default Template
The following is the default Handlebars template for this component. To create a custom template, it is recommended to use this as a starting point.
```
<div class="autocomplete">
    <div class="row">
        {{#if products.results.length}}
            <div class="column column--12 column-md--8">
                <span class="autocomplete__title autocomplete__title--products">{{products.title}}</span>
                <div class="row autocomplete__products">
                    {{#each products.results}}
                        <div class="column column--12 column-sm--4">
                            <div class="autocomplete__product">
                                <a hawksearch-product="{{id}}" href="{{url}}" class="autocomplete__product__image">
                                    <img hawksearch-image src="{{imageUrl}}" alt="" />
                                </a>
                                <span class="autocomplete__product__title">
                                    <a hawksearch-product="{{id}}" href="{{url}}">{{html title}}</a>
                                </span>
                            </div>
                        </div>
                    {{/each}}
                </div>
            </div>
        {{/if}}
        {{#if (or categories.results.length content.results.length queries.results.length)}}
            <div class="column column--12 column-md--4">
                {{#if categories.results.length}}
                    <span class="autocomplete__title autocomplete__title--categories">{{categories.title}}</span>
                    <ul class="autocomplete__list">
                        {{#each categories.results}}
                            <li>
                                <a hawksearch-category-field="{{field}}" hawksearch-category-value="{{value}}" href="{{url}}">{{html title}}</a>
                            </li>
                        {{/each}}
                    </ul>
                {{/if}}
                {{#if content.results.length}}
                    <span class="autocomplete__title autocomplete__title--content">{{content.title}}</span>
                    <ul class="autocomplete__list">
                        {{#each content.results}}
                            <li>
                                <a hawksearch-content="{{id}}" href="{{url}}">{{html title}}</a>
                            </li>
                        {{/each}}
                    </ul>
                {{/if}}
                {{#if queries.results.length}}
                    <span class="autocomplete__title autocomplete__title--queries">{{queries.title}}</span>
                    <ul class="autocomplete__list">
                        {{#each queries.results}}
                            <li>
                                <a hawksearch-query="{{query}}" href="{{url}}">{{query}}</a>
                            </li>
                        {{/each}}
                    </ul>
                {{/if}}
            </div>
        {{/if}}
    </div>
    <div class="autocomplete__view-all">
        <a hawksearch-view-all>{{viewAllText}}</a>
    </div>
</div>
```

## Hierarchy

- [`BaseComponent`](Components.BaseComponent.md)<[`AutocompleteComponentConfig`](../interfaces/Models.AutocompleteComponentConfig.md), [`AutocompleteResponse`](../interfaces/Models.AutocompleteResponse.md), [`AutocompleteComponentModel`](../interfaces/Models.AutocompleteComponentModel.md)\>

  ↳ **`AutocompleteComponent`**

## Table of contents

### Properties

- [bindFromEvent](Components.AutocompleteComponent.md#bindfromevent)
- [componentName](Components.AutocompleteComponent.md#componentname)
- [contentModel](Components.AutocompleteComponent.md#contentmodel)
- [data](Components.AutocompleteComponent.md#data)
- [defaultHtml](Components.AutocompleteComponent.md#defaulthtml)
- [handlebars](Components.AutocompleteComponent.md#handlebars)

### Accessors

- [configuration](Components.AutocompleteComponent.md#configuration)
- [rootElement](Components.AutocompleteComponent.md#rootelement)

### Methods

- [bindChildElements](Components.AutocompleteComponent.md#bindchildelements)
- [getContentModel](Components.AutocompleteComponent.md#getcontentmodel)
- [interpolate](Components.AutocompleteComponent.md#interpolate)
- [onRender](Components.AutocompleteComponent.md#onrender)
- [registerHelpers](Components.AutocompleteComponent.md#registerhelpers)
- [render](Components.AutocompleteComponent.md#render)
- [renderContent](Components.AutocompleteComponent.md#rendercontent)

## Properties

### bindFromEvent

• `Protected` **bindFromEvent**: `boolean` = `true`

#### Overrides

BaseComponent.bindFromEvent

#### Defined in

[src/components/search/autocomplete/autocomplete.component.ts:65](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/autocomplete/autocomplete.component.ts#lines-65)

___

### componentName

• `Protected` **componentName**: keyof [`HawkSearchComponents`](../interfaces/Models.HawkSearchComponents.md) = `'autocomplete'`

#### Overrides

BaseComponent.componentName

#### Defined in

[src/components/search/autocomplete/autocomplete.component.ts:66](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/autocomplete/autocomplete.component.ts#lines-66)

___

### contentModel

• `Protected` `Optional` **contentModel**: [`AutocompleteComponentModel`](../interfaces/Models.AutocompleteComponentModel.md)

The data bound to the Handlebars template.

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[contentModel](Components.BaseComponent.md#contentmodel)

#### Defined in

[src/components/base.component.ts:35](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-35)

___

### data

• `Optional` **data**: [`AutocompleteResponse`](../interfaces/Models.AutocompleteResponse.md)

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

[src/components/search/autocomplete/autocomplete.component.ts:67](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/autocomplete/autocomplete.component.ts#lines-67)

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

[src/components/search/autocomplete/autocomplete.component.ts:80](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/autocomplete/autocomplete.component.ts#lines-80)

___

### getContentModel

▸ `Protected` **getContentModel**(): [`AutocompleteComponentModel`](../interfaces/Models.AutocompleteComponentModel.md)

#### Returns

[`AutocompleteComponentModel`](../interfaces/Models.AutocompleteComponentModel.md)

#### Overrides

BaseComponent.getContentModel

#### Defined in

[src/components/search/autocomplete/autocomplete.component.ts:73](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/autocomplete/autocomplete.component.ts#lines-73)

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

Binds [contentModel](Components.AutocompleteComponent.md#contentmodel) to the Handlebars template and renders the resulting HTML content.

#### Returns

`void`

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[render](Components.BaseComponent.md#render)

#### Defined in

[src/components/base.component.ts:171](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-171)

___

### renderContent

▸ `Protected` **renderContent**(): `boolean`

Determines whether the [data](Components.AutocompleteComponent.md#data) meets the necessary conditions to perform data binding and render content.

#### Returns

`boolean`

Whether the component should be rendered. If `false`, the component will have empty contents and be set to `display: none;`.

#### Overrides

[BaseComponent](Components.BaseComponent.md).[renderContent](Components.BaseComponent.md#rendercontent)

#### Defined in

[src/components/search/autocomplete/autocomplete.component.ts:69](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/autocomplete/autocomplete.component.ts#lines-69)
