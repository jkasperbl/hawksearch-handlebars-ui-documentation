[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Components](../modules/Components.md) / LandingPageComponent

# Class: LandingPageComponent

[Components](../modules/Components.md).LandingPageComponent

The Landing page component displays either a search results interface to display a subset of products, or a custom layout to display content items.

## Tag
The tag for this component is `<hawksearch-landing-page>`.

## Attributes
| Name | Value | Required |
| :- | :- | :- |
| url | `string` | No |

By default, the URL sent to the HawkSearch API matches the current browser URL as reflected in `window.location.pathname`. This attribute can be used to override this with a custom value.

## Default Template
The following is the default Handlebars template for this component. To create a custom template, it is recommended to use this as a starting point.
```
{{#if customLayout}}
    {{html customLayout}}
{{else}}
    <hawksearch-search-results mode="landing-page" url="{{url}}"></hawksearch-search-results>
{{/if}}
```

## Hierarchy

- [`BaseComponent`](Components.BaseComponent.md)<[`LandingPageComponentConfig`](../interfaces/Models.LandingPageComponentConfig.md), [`SearchResponse`](../interfaces/Models.SearchResponse.md), [`LandingPageComponentModel`](../interfaces/Models.LandingPageComponentModel.md)\>

  ↳ **`LandingPageComponent`**

## Table of contents

### Constructors

- [constructor](Components.LandingPageComponent.md#constructor)

### Properties

- [bindFromEvent](Components.LandingPageComponent.md#bindfromevent)
- [componentName](Components.LandingPageComponent.md#componentname)
- [contentModel](Components.LandingPageComponent.md#contentmodel)
- [data](Components.LandingPageComponent.md#data)
- [defaultHtml](Components.LandingPageComponent.md#defaulthtml)
- [handlebars](Components.LandingPageComponent.md#handlebars)

### Accessors

- [configuration](Components.LandingPageComponent.md#configuration)
- [rootElement](Components.LandingPageComponent.md#rootelement)
- [url](Components.LandingPageComponent.md#url)

### Methods

- [bindChildElements](Components.LandingPageComponent.md#bindchildelements)
- [getContentModel](Components.LandingPageComponent.md#getcontentmodel)
- [interpolate](Components.LandingPageComponent.md#interpolate)
- [onRender](Components.LandingPageComponent.md#onrender)
- [registerHelpers](Components.LandingPageComponent.md#registerhelpers)
- [render](Components.LandingPageComponent.md#render)
- [renderContent](Components.LandingPageComponent.md#rendercontent)

## Constructors

### constructor

• **new LandingPageComponent**()

#### Overrides

BaseComponent&lt;LandingPageComponentConfig, SearchResponse, LandingPageComponentModel\&gt;.constructor

#### Defined in

[src/components/landing-pages/landing-page/landing-page.component.ts:34](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/landing-pages/landing-page/landing-page.component.ts#lines-34)

## Properties

### bindFromEvent

• `Protected` **bindFromEvent**: `boolean` = `true`

#### Overrides

BaseComponent.bindFromEvent

#### Defined in

[src/components/landing-pages/landing-page/landing-page.component.ts:28](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/landing-pages/landing-page/landing-page.component.ts#lines-28)

___

### componentName

• `Protected` **componentName**: keyof [`HawkSearchComponents`](../interfaces/Models.HawkSearchComponents.md) = `'landing-page'`

#### Overrides

BaseComponent.componentName

#### Defined in

[src/components/landing-pages/landing-page/landing-page.component.ts:26](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/landing-pages/landing-page/landing-page.component.ts#lines-26)

___

### contentModel

• `Protected` `Optional` **contentModel**: [`LandingPageComponentModel`](../interfaces/Models.LandingPageComponentModel.md)

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

[src/components/landing-pages/landing-page/landing-page.component.ts:27](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/landing-pages/landing-page/landing-page.component.ts#lines-27)

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

___

### url

• `Protected` `get` **url**(): `string`

#### Returns

`string`

#### Defined in

[src/components/landing-pages/landing-page/landing-page.component.ts:30](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/landing-pages/landing-page/landing-page.component.ts#lines-30)

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

▸ `Protected` **getContentModel**(): [`LandingPageComponentModel`](../interfaces/Models.LandingPageComponentModel.md)

#### Returns

[`LandingPageComponentModel`](../interfaces/Models.LandingPageComponentModel.md)

#### Overrides

BaseComponent.getContentModel

#### Defined in

[src/components/landing-pages/landing-page/landing-page.component.ts:50](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/landing-pages/landing-page/landing-page.component.ts#lines-50)

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

Binds [contentModel](Components.LandingPageComponent.md#contentmodel) to the Handlebars template and renders the resulting HTML content.

#### Returns

`void`

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[render](Components.BaseComponent.md#render)

#### Defined in

[src/components/base.component.ts:171](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-171)

___

### renderContent

▸ `Protected` **renderContent**(): `boolean`

Determines whether the [data](Components.LandingPageComponent.md#data) meets the necessary conditions to perform data binding and render content.

#### Returns

`boolean`

Whether the component should be rendered. If `false`, the component will have empty contents and be set to `display: none;`.

#### Overrides

[BaseComponent](Components.BaseComponent.md).[renderContent](Components.BaseComponent.md#rendercontent)

#### Defined in

[src/components/landing-pages/landing-page/landing-page.component.ts:46](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/landing-pages/landing-page/landing-page.component.ts#lines-46)
