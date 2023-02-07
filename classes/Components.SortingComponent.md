[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Components](../modules/Components.md) / SortingComponent

# Class: SortingComponent

[Components](../modules/Components.md).SortingComponent

The Sorting component is used to select the logic for ordering search results.

## Tag
The tag for this component is `<hawksearch-sorting>`.

## Event-Binding Attributes
| Name | Value |
| :- | :- |
| hawksearch-sort | |

When a `select` element with this attribute changes in value, the search will be updated to use that value as the new sort order.

## Default Template
The following is the default Handlebars template for this component. To create a custom template, it is recommended to use this as a starting point.
```
<div class="sorting">
    <select hawksearch-sort>
        {{#each options}}
            {{#if selected}}
                <option value="{{value}}" selected>{{title}}</option>
            {{else}}
                <option value="{{value}}">{{title}}</option>
            {{/if}}
        {{/each}}
    </select>
</div>
```

## Hierarchy

- [`BaseComponent`](Components.BaseComponent.md)<[`SortingComponentConfig`](../interfaces/Models.SortingComponentConfig.md), [`Sorting`](../interfaces/Models.Sorting.md), [`SortingComponentModel`](../interfaces/Models.SortingComponentModel.md)\>

  ↳ **`SortingComponent`**

## Table of contents

### Properties

- [bindFromEvent](Components.SortingComponent.md#bindfromevent)
- [componentName](Components.SortingComponent.md#componentname)
- [contentModel](Components.SortingComponent.md#contentmodel)
- [data](Components.SortingComponent.md#data)
- [defaultHtml](Components.SortingComponent.md#defaulthtml)
- [handlebars](Components.SortingComponent.md#handlebars)

### Accessors

- [configuration](Components.SortingComponent.md#configuration)
- [rootElement](Components.SortingComponent.md#rootelement)

### Methods

- [bindChildElements](Components.SortingComponent.md#bindchildelements)
- [getContentModel](Components.SortingComponent.md#getcontentmodel)
- [interpolate](Components.SortingComponent.md#interpolate)
- [onRender](Components.SortingComponent.md#onrender)
- [registerHelpers](Components.SortingComponent.md#registerhelpers)
- [render](Components.SortingComponent.md#render)
- [renderContent](Components.SortingComponent.md#rendercontent)

## Properties

### bindFromEvent

• `Protected` **bindFromEvent**: `boolean` = `true`

#### Overrides

BaseComponent.bindFromEvent

#### Defined in

[src/components/search/sorting/sorting.component.ts:28](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/sorting/sorting.component.ts#lines-28)

___

### componentName

• `Protected` **componentName**: keyof [`HawkSearchComponents`](../interfaces/Models.HawkSearchComponents.md) = `'sorting'`

#### Overrides

BaseComponent.componentName

#### Defined in

[src/components/search/sorting/sorting.component.ts:26](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/sorting/sorting.component.ts#lines-26)

___

### contentModel

• `Protected` `Optional` **contentModel**: [`SortingComponentModel`](../interfaces/Models.SortingComponentModel.md)

The data bound to the Handlebars template.

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[contentModel](Components.BaseComponent.md#contentmodel)

#### Defined in

[src/components/base.component.ts:35](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-35)

___

### data

• `Optional` **data**: [`Sorting`](../interfaces/Models.Sorting.md)

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

[src/components/search/sorting/sorting.component.ts:27](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/sorting/sorting.component.ts#lines-27)

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

[src/components/search/sorting/sorting.component.ts:40](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/sorting/sorting.component.ts#lines-40)

___

### getContentModel

▸ `Protected` **getContentModel**(): [`SortingComponentModel`](../interfaces/Models.SortingComponentModel.md)

#### Returns

[`SortingComponentModel`](../interfaces/Models.SortingComponentModel.md)

#### Overrides

BaseComponent.getContentModel

#### Defined in

[src/components/search/sorting/sorting.component.ts:34](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/sorting/sorting.component.ts#lines-34)

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

Binds [contentModel](Components.SortingComponent.md#contentmodel) to the Handlebars template and renders the resulting HTML content.

#### Returns

`void`

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[render](Components.BaseComponent.md#render)

#### Defined in

[src/components/base.component.ts:171](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-171)

___

### renderContent

▸ `Protected` **renderContent**(): `boolean`

Determines whether the [data](Components.SortingComponent.md#data) meets the necessary conditions to perform data binding and render content.

#### Returns

`boolean`

Whether the component should be rendered. If `false`, the component will have empty contents and be set to `display: none;`.

#### Overrides

[BaseComponent](Components.BaseComponent.md).[renderContent](Components.BaseComponent.md#rendercontent)

#### Defined in

[src/components/search/sorting/sorting.component.ts:30](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/sorting/sorting.component.ts#lines-30)
