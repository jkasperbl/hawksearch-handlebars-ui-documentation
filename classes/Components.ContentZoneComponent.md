[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Components](../modules/Components.md) / ContentZoneComponent

# Class: ContentZoneComponent

[Components](../modules/Components.md).ContentZoneComponent

The Content Zone component renders a list of content items or Spotlight products as defined in the Merchandising section of Hawksearch.

## Tag
The tag for this component is `<hawksearch-content-zone>`.

## Attributes
| Name | Value | Required |
| :- | :- | :- |
| name | `string` | Yes |

The `name` attribute corresponds to the `Zone` property defined in Hawksearch. This is used to differentiate different content areas, allowing you to place content items exactly where you want within your search results page.

## Event-Binding Attributes
| Name | Value |
| :- | :- |
| index | `number` |

To render a content item, the `index` attribute must be present with a value corresponding to the item’s index in the [items](../interfaces/Models.ContentZoneComponentModel.md#items) array.

## Default Template
The following is the default Handlebars template for this component. To create a custom template, it is recommended to use this as a starting point.
```
<div class="content-zone">
    {{#each items}}
        {{#if (eq type "custom")}}
            <hawksearch-custom-content index="{{@index}}"></hawksearch-custom-content>
        {{/if}}
        {{#if (eq type "featured-items")}}
            <hawksearch-featured-items-content index="{{@index}}"></hawksearch-featured-items-content>
        {{/if}}
        {{#if (eq type "image")}}
            <hawksearch-image-content index="{{@index}}"></hawksearch-image-content>
        {{/if}}
        {{#if (eq type "popular-queries")}}
            <hawksearch-popular-queries-content index="{{@index}}"></hawksearch-popular-queries-content>
        {{/if}}
    {{/each}}
</div>
```

## Hierarchy

- [`BaseComponent`](Components.BaseComponent.md)<[`ContentZoneComponentConfig`](../interfaces/Models.ContentZoneComponentConfig.md), [`SearchResponse`](../interfaces/Models.SearchResponse.md), [`ContentZoneComponentModel`](../interfaces/Models.ContentZoneComponentModel.md)\>

  ↳ **`ContentZoneComponent`**

## Table of contents

### Properties

- [bindFromEvent](Components.ContentZoneComponent.md#bindfromevent)
- [componentName](Components.ContentZoneComponent.md#componentname)
- [contentModel](Components.ContentZoneComponent.md#contentmodel)
- [data](Components.ContentZoneComponent.md#data)
- [defaultHtml](Components.ContentZoneComponent.md#defaulthtml)
- [handlebars](Components.ContentZoneComponent.md#handlebars)

### Accessors

- [configuration](Components.ContentZoneComponent.md#configuration)
- [rootElement](Components.ContentZoneComponent.md#rootelement)

### Methods

- [bindChildElements](Components.ContentZoneComponent.md#bindchildelements)
- [connectedCallback](Components.ContentZoneComponent.md#connectedcallback)
- [disconnectedCallback](Components.ContentZoneComponent.md#disconnectedcallback)
- [getContentModel](Components.ContentZoneComponent.md#getcontentmodel)
- [interpolate](Components.ContentZoneComponent.md#interpolate)
- [onRender](Components.ContentZoneComponent.md#onrender)
- [registerHelpers](Components.ContentZoneComponent.md#registerhelpers)
- [render](Components.ContentZoneComponent.md#render)
- [renderContent](Components.ContentZoneComponent.md#rendercontent)

## Properties

### bindFromEvent

• `Protected` **bindFromEvent**: `boolean` = `true`

#### Overrides

BaseComponent.bindFromEvent

#### Defined in

[src/components/content/content-zone/content-zone.component.ts:46](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/content/content-zone/content-zone.component.ts#lines-46)

___

### componentName

• `Protected` **componentName**: keyof [`HawkSearchComponents`](../interfaces/Models.HawkSearchComponents.md) = `'content-zone'`

#### Overrides

BaseComponent.componentName

#### Defined in

[src/components/content/content-zone/content-zone.component.ts:44](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/content/content-zone/content-zone.component.ts#lines-44)

___

### contentModel

• `Protected` `Optional` **contentModel**: [`ContentZoneComponentModel`](../interfaces/Models.ContentZoneComponentModel.md)

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

[src/components/content/content-zone/content-zone.component.ts:45](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/content/content-zone/content-zone.component.ts#lines-45)

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

[src/components/content/content-zone/content-zone.component.ts:105](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/content/content-zone/content-zone.component.ts#lines-105)

___

### connectedCallback

▸ **connectedCallback**(): `void`

#### Returns

`void`

#### Overrides

BaseComponent.connectedCallback

#### Defined in

[src/components/content/content-zone/content-zone.component.ts:72](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/content/content-zone/content-zone.component.ts#lines-72)

___

### disconnectedCallback

▸ **disconnectedCallback**(): `void`

#### Returns

`void`

#### Overrides

BaseComponent.disconnectedCallback

#### Defined in

[src/components/content/content-zone/content-zone.component.ts:86](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/content/content-zone/content-zone.component.ts#lines-86)

___

### getContentModel

▸ `Protected` **getContentModel**(): [`ContentZoneComponentModel`](../interfaces/Models.ContentZoneComponentModel.md)

#### Returns

[`ContentZoneComponentModel`](../interfaces/Models.ContentZoneComponentModel.md)

#### Overrides

BaseComponent.getContentModel

#### Defined in

[src/components/content/content-zone/content-zone.component.ts:96](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/content/content-zone/content-zone.component.ts#lines-96)

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

Binds [contentModel](Components.ContentZoneComponent.md#contentmodel) to the Handlebars template and renders the resulting HTML content.

#### Returns

`void`

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[render](Components.BaseComponent.md#render)

#### Defined in

[src/components/base.component.ts:171](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-171)

___

### renderContent

▸ `Protected` **renderContent**(): `boolean`

Determines whether the [data](Components.ContentZoneComponent.md#data) meets the necessary conditions to perform data binding and render content.

#### Returns

`boolean`

Whether the component should be rendered. If `false`, the component will have empty contents and be set to `display: none;`.

#### Overrides

[BaseComponent](Components.BaseComponent.md).[renderContent](Components.BaseComponent.md#rendercontent)

#### Defined in

[src/components/content/content-zone/content-zone.component.ts:92](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/content/content-zone/content-zone.component.ts#lines-92)
