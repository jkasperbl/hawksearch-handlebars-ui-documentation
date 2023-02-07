[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Components](../modules/Components.md) / PaginationComponent

# Class: PaginationComponent

[Components](../modules/Components.md).PaginationComponent

The Pagination component is used to navigate between different pages of a search results set.

*Note: If no maximum number of page links to display is configured in the Hawksearch admin, a default value of `9` will be used.*

## Tag
The tag for this component is `<hawksearch-pagination>`.

## Event-Binding Attributes
| Name | Value |
| :- | :- |
| hawksearch-page | `number` |

When an element with this attribute is clicked, the current search will be updated to display the results from the specified page.

## Handlebars Helpers
| Name | Parameter |
| :- | :- |
| pageUrl | `number` |

This helper function returns the URL for the specified page to enable crawling.

## Default Template
The following is the default Handlebars template for this component. To create a custom template, it is recommended to use this as a starting point.
```
<div class="pagination">
    {{#if strings.summary}}
        <div class="pagination__summary">{{strings.summary}}</div>
    {{/if}}
    <div class="pagination__pages">
        {{#if displayFirstLink}}
            <span hawksearch-page="1" class="link pagination__page pagination__page--first" title="{{strings.first}}">
                <hawksearch-icon name="chevron-back" size="1.2em"></hawksearch-icon>
            </span>
        {{/if}}
        {{#if displayPreviousLink}}
            <a
                hawksearch-page="{{subtract page 1}}"
                rel="prev"
                href="{{pageUrl (subtract page 1)}}"
                class="pagination__page pagination__page--previous"
                title="{{strings.previous}}"
            >
                <hawksearch-icon name="chevron-left" size="1.2em"></hawksearch-icon>
            </a>
        {{/if}}
        {{#each pages}}
            {{#if (eq this @root.page)}}
                <span class="pagination__page pagination__page--selected">{{this}}</span>
            {{else}}
                <a hawksearch-page="{{this}}" href="{{pageUrl this}}" class="pagination__page">{{this}}</a>
            {{/if}}
        {{/each}}
        {{#if displayNextLink}}
            <a
                hawksearch-page="{{add page 1}}"
                rel="next"
                href="{{pageUrl (add page 1)}}"
                class="pagination__page pagination__page--next"
                title="{{strings.next}}"
            >
                <hawksearch-icon name="chevron-right" size="1.2em"></hawksearch-icon>
            </a>
        {{/if}}
        {{#if displayLastLink}}
            <span hawksearch-page="{{totalPages}}" class="link pagination__page pagination__page--last" title="{{strings.last}}">
                <hawksearch-icon name="chevron-forward" size="1.2em"></hawksearch-icon>
            </span>
        {{/if}}
    </div>
</div>
```

## Hierarchy

- [`BaseComponent`](Components.BaseComponent.md)<[`PaginationComponentConfig`](../interfaces/Models.PaginationComponentConfig.md), [`Pagination`](../interfaces/Models.Pagination.md), [`PaginationComponentModel`](../interfaces/Models.PaginationComponentModel.md)\>

  ↳ **`PaginationComponent`**

## Table of contents

### Properties

- [bindFromEvent](Components.PaginationComponent.md#bindfromevent)
- [componentName](Components.PaginationComponent.md#componentname)
- [contentModel](Components.PaginationComponent.md#contentmodel)
- [data](Components.PaginationComponent.md#data)
- [defaultHtml](Components.PaginationComponent.md#defaulthtml)
- [handlebars](Components.PaginationComponent.md#handlebars)

### Accessors

- [configuration](Components.PaginationComponent.md#configuration)
- [rootElement](Components.PaginationComponent.md#rootelement)

### Methods

- [bindChildElements](Components.PaginationComponent.md#bindchildelements)
- [getContentModel](Components.PaginationComponent.md#getcontentmodel)
- [interpolate](Components.PaginationComponent.md#interpolate)
- [onRender](Components.PaginationComponent.md#onrender)
- [registerHelpers](Components.PaginationComponent.md#registerhelpers)
- [render](Components.PaginationComponent.md#render)
- [renderContent](Components.PaginationComponent.md#rendercontent)
- [setPage](Components.PaginationComponent.md#setpage)

## Properties

### bindFromEvent

• `Protected` **bindFromEvent**: `boolean` = `true`

#### Overrides

BaseComponent.bindFromEvent

#### Defined in

[src/components/search/pagination/pagination.component.ts:38](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/pagination/pagination.component.ts#lines-38)

___

### componentName

• `Protected` **componentName**: keyof [`HawkSearchComponents`](../interfaces/Models.HawkSearchComponents.md) = `'pagination'`

#### Overrides

BaseComponent.componentName

#### Defined in

[src/components/search/pagination/pagination.component.ts:36](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/pagination/pagination.component.ts#lines-36)

___

### contentModel

• `Protected` `Optional` **contentModel**: [`PaginationComponentModel`](../interfaces/Models.PaginationComponentModel.md)

The data bound to the Handlebars template.

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[contentModel](Components.BaseComponent.md#contentmodel)

#### Defined in

[src/components/base.component.ts:35](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-35)

___

### data

• `Optional` **data**: [`Pagination`](../interfaces/Models.Pagination.md)

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

[src/components/search/pagination/pagination.component.ts:37](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/pagination/pagination.component.ts#lines-37)

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

[src/components/search/pagination/pagination.component.ts:98](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/pagination/pagination.component.ts#lines-98)

___

### getContentModel

▸ `Protected` **getContentModel**(): [`PaginationComponentModel`](../interfaces/Models.PaginationComponentModel.md)

#### Returns

[`PaginationComponentModel`](../interfaces/Models.PaginationComponentModel.md)

#### Overrides

BaseComponent.getContentModel

#### Defined in

[src/components/search/pagination/pagination.component.ts:62](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/pagination/pagination.component.ts#lines-62)

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

[src/components/search/pagination/pagination.component.ts:42](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/pagination/pagination.component.ts#lines-42)

___

### render

▸ **render**(): `void`

Binds [contentModel](Components.PaginationComponent.md#contentmodel) to the Handlebars template and renders the resulting HTML content.

#### Returns

`void`

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[render](Components.BaseComponent.md#render)

#### Defined in

[src/components/base.component.ts:171](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-171)

___

### renderContent

▸ `Protected` **renderContent**(): `boolean`

Determines whether the [data](Components.PaginationComponent.md#data) meets the necessary conditions to perform data binding and render content.

#### Returns

`boolean`

Whether the component should be rendered. If `false`, the component will have empty contents and be set to `display: none;`.

#### Overrides

[BaseComponent](Components.BaseComponent.md).[renderContent](Components.BaseComponent.md#rendercontent)

#### Defined in

[src/components/search/pagination/pagination.component.ts:58](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/pagination/pagination.component.ts#lines-58)

___

### setPage

▸ `Protected` **setPage**(`page`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `page` | `number` |

#### Returns

`Promise`<`void`\>

#### Defined in

[src/components/search/pagination/pagination.component.ts:114](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/pagination/pagination.component.ts#lines-114)
