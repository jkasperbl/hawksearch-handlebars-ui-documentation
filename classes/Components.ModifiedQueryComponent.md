[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Components](../modules/Components.md) / ModifiedQueryComponent

# Class: ModifiedQueryComponent

[Components](../modules/Components.md).ModifiedQueryComponent

The Modified Query component is rendered when the spellchecker detects a spelling error and searches for the correctly-spelled query instead.

*Note: This component is only visible for new searches. If the spellchecker revises a query and the user then performs an action such as applying facet or moving to another page of results, it is implied that the user accepts the correction.*

## Tag
The tag for this component is `<hawksearch-modified-query>`.

## Event-Binding Attributes
| Name | Value |
| :- | :- |
| hawksearch-query | `string` |

When an element with this attribute is clicked, a new search will be executed with the specified query and spellcheck functionality disabled. This is useful when the spellchecker mistakes a valid entry for another term.

## Default Template
The following is the default Handlebars template for this component. To create a custom template, it is recommended to use this as a starting point.
```
<div class="modified-query">
    <p>
        {{strings.showingResultsFor}}
        <span class="modified-query__modified">{{modifiedQuery}}</span>.
        {{strings.searchInsteadFor}}
        <a class="modified-query__original" hawksearch-query="{{query}}">{{query}}</a>.
    </p>
</div>
```

## Hierarchy

- [`BaseComponent`](Components.BaseComponent.md)<[`ModifiedQueryComponentConfig`](../interfaces/Models.ModifiedQueryComponentConfig.md), [`ModifiedQueryData`](../interfaces/Models.ModifiedQueryData.md), [`ModifiedQueryComponentModel`](../interfaces/Models.ModifiedQueryComponentModel.md)\>

  ↳ **`ModifiedQueryComponent`**

## Table of contents

### Properties

- [bindFromEvent](Components.ModifiedQueryComponent.md#bindfromevent)
- [componentName](Components.ModifiedQueryComponent.md#componentname)
- [contentModel](Components.ModifiedQueryComponent.md#contentmodel)
- [data](Components.ModifiedQueryComponent.md#data)
- [defaultHtml](Components.ModifiedQueryComponent.md#defaulthtml)
- [handlebars](Components.ModifiedQueryComponent.md#handlebars)

### Accessors

- [configuration](Components.ModifiedQueryComponent.md#configuration)
- [rootElement](Components.ModifiedQueryComponent.md#rootelement)

### Methods

- [bindChildElements](Components.ModifiedQueryComponent.md#bindchildelements)
- [getContentModel](Components.ModifiedQueryComponent.md#getcontentmodel)
- [interpolate](Components.ModifiedQueryComponent.md#interpolate)
- [onRender](Components.ModifiedQueryComponent.md#onrender)
- [registerHelpers](Components.ModifiedQueryComponent.md#registerhelpers)
- [render](Components.ModifiedQueryComponent.md#render)
- [renderContent](Components.ModifiedQueryComponent.md#rendercontent)

## Properties

### bindFromEvent

• `Protected` **bindFromEvent**: `boolean` = `true`

#### Overrides

BaseComponent.bindFromEvent

#### Defined in

[src/components/search/modified-query/modified-query.component.ts:30](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/modified-query/modified-query.component.ts#lines-30)

___

### componentName

• `Protected` **componentName**: keyof [`HawkSearchComponents`](../interfaces/Models.HawkSearchComponents.md) = `'modified-query'`

#### Overrides

BaseComponent.componentName

#### Defined in

[src/components/search/modified-query/modified-query.component.ts:28](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/modified-query/modified-query.component.ts#lines-28)

___

### contentModel

• `Protected` `Optional` **contentModel**: [`ModifiedQueryComponentModel`](../interfaces/Models.ModifiedQueryComponentModel.md)

The data bound to the Handlebars template.

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[contentModel](Components.BaseComponent.md#contentmodel)

#### Defined in

[src/components/base.component.ts:35](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-35)

___

### data

• `Optional` **data**: [`ModifiedQueryData`](../interfaces/Models.ModifiedQueryData.md)

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

[src/components/search/modified-query/modified-query.component.ts:29](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/modified-query/modified-query.component.ts#lines-29)

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

[src/components/search/modified-query/modified-query.component.ts:47](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/modified-query/modified-query.component.ts#lines-47)

___

### getContentModel

▸ `Protected` **getContentModel**(): [`ModifiedQueryComponentModel`](../interfaces/Models.ModifiedQueryComponentModel.md)

#### Returns

[`ModifiedQueryComponentModel`](../interfaces/Models.ModifiedQueryComponentModel.md)

#### Overrides

BaseComponent.getContentModel

#### Defined in

[src/components/search/modified-query/modified-query.component.ts:36](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/modified-query/modified-query.component.ts#lines-36)

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

Binds [contentModel](Components.ModifiedQueryComponent.md#contentmodel) to the Handlebars template and renders the resulting HTML content.

#### Returns

`void`

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[render](Components.BaseComponent.md#render)

#### Defined in

[src/components/base.component.ts:171](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-171)

___

### renderContent

▸ `Protected` **renderContent**(): `boolean`

Determines whether the [data](Components.ModifiedQueryComponent.md#data) meets the necessary conditions to perform data binding and render content.

#### Returns

`boolean`

Whether the component should be rendered. If `false`, the component will have empty contents and be set to `display: none;`.

#### Overrides

[BaseComponent](Components.BaseComponent.md).[renderContent](Components.BaseComponent.md#rendercontent)

#### Defined in

[src/components/search/modified-query/modified-query.component.ts:32](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/modified-query/modified-query.component.ts#lines-32)
