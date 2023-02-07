[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Components](../modules/Components.md) / RecommendationsItemComponent

# Class: RecommendationsItemComponent

[Components](../modules/Components.md).RecommendationsItemComponent

The Recommendations Item component displays information for an individual product or page.

## Tag
The tag for this component is `<hawksearch-recommendations-item>`.

*Note: This component should only be used within the context of the [Recommendations component](Components.RecommendationsComponent.md).

## Event-Binding Attributes
| Name | Value |
| :- | :- |
| hawksearch-image | |

Image elements with this attribute will have their `src` value replaced with a placeholder image URL if the image fails to load.

| Name | Value |
| :- | :- |
| hawksearch-link | |

Anchor elements with this attribute will be tracked when clicked.

## Default Template
The following is the default Handlebars template for this component. To create a custom template, it is recommended to use this as a starting point.
```
<div class="recommendations__item">
    {{#if pinned}}
        <span class="recommendations__item__pin">
            <hawksearch-icon name="star"></hawksearch-icon>
        </span>
    {{/if}}
    {{#if (lt salePrice price)}}
        <span class="recommendations__item__sale-indicator">{{strings.sale}}</span>
    {{/if}}
    <a hawksearch-link href="{{url}}" class="recommendations__item__image" aria-label="{{title}}">
        <img hawksearch-image src="{{imageUrl}}" alt="" />
    </a>
    <div class="recommendations__item__title">
        <a hawksearch-link href="{{url}}">{{title}}</a>
    </div>
    {{#unless (eq salePrice undefined)}}
        <div class="recommendations__item__price" itemprop="offers" itemtype="http://schema.org/Offer" itemscope>
            {{#if (lt salePrice price)}}
                <span class="recommendations__item__price__original">{{currency price}}</span>
                <span class="recommendations__item__price__current" itemprop="price">{{currency salePrice}}</span>
            {{else}}
                <span class="recommendations__item__price-__current" itemprop="price">{{currency salePrice}}</span>
            {{/if}}
        </div>
    {{/unless}}
</div>
```

## Hierarchy

- [`BaseComponent`](Components.BaseComponent.md)<[`RecommendationsItemComponentConfig`](../interfaces/Models.RecommendationsItemComponentConfig.md), [`RecommendationsItem`](../interfaces/Models.RecommendationsItem.md), [`RecommendationsItemComponentModel`](../interfaces/Models.RecommendationsItemComponentModel.md)\>

  ↳ **`RecommendationsItemComponent`**

## Table of contents

### Properties

- [bindFromEvent](Components.RecommendationsItemComponent.md#bindfromevent)
- [componentName](Components.RecommendationsItemComponent.md#componentname)
- [contentModel](Components.RecommendationsItemComponent.md#contentmodel)
- [data](Components.RecommendationsItemComponent.md#data)
- [defaultHtml](Components.RecommendationsItemComponent.md#defaulthtml)
- [handlebars](Components.RecommendationsItemComponent.md#handlebars)

### Accessors

- [configuration](Components.RecommendationsItemComponent.md#configuration)
- [rootElement](Components.RecommendationsItemComponent.md#rootelement)

### Methods

- [bindChildElements](Components.RecommendationsItemComponent.md#bindchildelements)
- [getContentModel](Components.RecommendationsItemComponent.md#getcontentmodel)
- [interpolate](Components.RecommendationsItemComponent.md#interpolate)
- [onRender](Components.RecommendationsItemComponent.md#onrender)
- [registerHelpers](Components.RecommendationsItemComponent.md#registerhelpers)
- [render](Components.RecommendationsItemComponent.md#render)
- [renderContent](Components.RecommendationsItemComponent.md#rendercontent)

## Properties

### bindFromEvent

• `Protected` **bindFromEvent**: `boolean` = `false`

#### Overrides

BaseComponent.bindFromEvent

#### Defined in

[src/components/recommendations/recommendations-item/recommendations-item.component.ts:39](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/recommendations/recommendations-item/recommendations-item.component.ts#lines-39)

___

### componentName

• `Protected` **componentName**: keyof [`HawkSearchComponents`](../interfaces/Models.HawkSearchComponents.md) = `'recommendations-item'`

#### Overrides

BaseComponent.componentName

#### Defined in

[src/components/recommendations/recommendations-item/recommendations-item.component.ts:37](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/recommendations/recommendations-item/recommendations-item.component.ts#lines-37)

___

### contentModel

• `Protected` `Optional` **contentModel**: [`RecommendationsItemComponentModel`](../interfaces/Models.RecommendationsItemComponentModel.md)

The data bound to the Handlebars template.

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[contentModel](Components.BaseComponent.md#contentmodel)

#### Defined in

[src/components/base.component.ts:35](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-35)

___

### data

• `Optional` **data**: [`RecommendationsItem`](../interfaces/Models.RecommendationsItem.md)

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

[src/components/recommendations/recommendations-item/recommendations-item.component.ts:38](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/recommendations/recommendations-item/recommendations-item.component.ts#lines-38)

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

[src/components/recommendations/recommendations-item/recommendations-item.component.ts:62](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/recommendations/recommendations-item/recommendations-item.component.ts#lines-62)

___

### getContentModel

▸ `Protected` **getContentModel**(): [`RecommendationsItemComponentModel`](../interfaces/Models.RecommendationsItemComponentModel.md)

#### Returns

[`RecommendationsItemComponentModel`](../interfaces/Models.RecommendationsItemComponentModel.md)

#### Overrides

BaseComponent.getContentModel

#### Defined in

[src/components/recommendations/recommendations-item/recommendations-item.component.ts:53](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/recommendations/recommendations-item/recommendations-item.component.ts#lines-53)

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

Binds [contentModel](Components.RecommendationsItemComponent.md#contentmodel) to the Handlebars template and renders the resulting HTML content.

#### Returns

`void`

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[render](Components.BaseComponent.md#render)

#### Defined in

[src/components/base.component.ts:171](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-171)

___

### renderContent

▸ `Protected` **renderContent**(): `boolean`

Determines whether the [data](Components.RecommendationsItemComponent.md#data) meets the necessary conditions to perform data binding and render content.

#### Returns

`boolean`

Whether the component should be rendered. If `false`, the component will have empty contents and be set to `display: none;`.

#### Overrides

[BaseComponent](Components.BaseComponent.md).[renderContent](Components.BaseComponent.md#rendercontent)

#### Defined in

[src/components/recommendations/recommendations-item/recommendations-item.component.ts:49](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/recommendations/recommendations-item/recommendations-item.component.ts#lines-49)
