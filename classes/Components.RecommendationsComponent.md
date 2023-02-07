[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Components](../modules/Components.md) / RecommendationsComponent

# Class: RecommendationsComponent

[Components](../modules/Components.md).RecommendationsComponent

The Recommendations component displays a list of products determined by the rules configured in the HawkSearch admin.

## Tag
The tag for this component is `<hawksearch-recommendations>`.

## Attributes
| Name | Value | Required |
| :- | :- | :- |
| widget-id | `string` | Yes |

This attribute specifies which recommendation configuration created in the HawkSearch admin is retrieved from the API.

## Event-Binding Attributes

| Name | Value |
| :- | :- |
| hawksearch-carousel | |

This attribute should be placed on the element that contains each individual item element of a carousel. This is used to bind touch events.

| Name | Value |
| :- | :- |
| hawksearch-carousel-item | `number` |

When an element with this attribute is clicked, the carousel will move to display the range of items starting with the given index. This is typically used within pagination for the carousel.

| Name | Value |
| :- | :- |
| hawksearch-next | |

When an element with this attribute is clicked, the carousel will display the next range of items.

| Name | Value |
| :- | :- |
| hawksearch-previous | |

When an element with this attribute is clicked, the carousel will display the previous range of items.

## Default Template
The following is the default Handlebars template for this component. To create a custom template, it is recommended to use this as a starting point.
```
<div class="recommendations">
    {{#if headingEnabled}}
        <h2 class="heading recommendations__heading">{{title}}</h2>
    {{/if}}
    <div class="recommendations__content">
        {{#if (and carousel buttonsEnabled)}}
            <a hawksearch-previous class="recommendations__button recommendations__button--previous" title="{{strings.previous}}">
                <hawksearch-icon name="chevron-left"></hawksearch-icon>
            </a>
        {{/if}}
        <div class="recommendations__carousel">
            <div hawksearch-carousel class="recommendations__list{{attribute ' recommendations__list--carousel' carousel}}" style="left: {{carouselPosition}};">
                {{#each items}}
                    <div class="recommendations__carousel__item" style="width: {{@root.itemWidth}};">
                        <hawksearch-recommendations-item widget-id="{{@root.id}}" request-id="{{@root.requestId}}"></hawksearch-recommendations-item>
                    </div>
                {{/each}}
            </div>
            {{#if (and carousel paginationEnabled)}}
                <div class="recommendations__pagination">
                    {{#each paginationItems}}
                        <span
                            hawksearch-carousel-item="{{@index}}"
                            class="recommendations__pagination__item{{attribute ' recommendations__pagination__item--selected' selected}}"
                            title="{{title}}"
                        ></span>
                    {{/each}}
                </div>
            {{/if}}
        </div>
        {{#if (and carousel buttonsEnabled)}}
            <a
                hawksearch-next
                class="recommendations__button recommendations__button--next{{attribute ' recommendations__button--disabled' (eq nextEnabled false)}}"
                title="{{strings.next}}"
            >
                <hawksearch-icon name="chevron-right"></hawksearch-icon>
            </a>
        {{/if}}
    </div>
</div>
```

## Hierarchy

- [`BaseComponent`](Components.BaseComponent.md)<[`RecommendationsComponentConfig`](../interfaces/Models.RecommendationsComponentConfig.md), [`RecommendationsWidget`](../interfaces/Models.RecommendationsWidget.md), [`RecommendationsComponentModel`](../interfaces/Models.RecommendationsComponentModel.md)\>

  ↳ **`RecommendationsComponent`**

## Table of contents

### Constructors

- [constructor](Components.RecommendationsComponent.md#constructor)

### Properties

- [bindFromEvent](Components.RecommendationsComponent.md#bindfromevent)
- [componentName](Components.RecommendationsComponent.md#componentname)
- [contentModel](Components.RecommendationsComponent.md#contentmodel)
- [data](Components.RecommendationsComponent.md#data)
- [defaultHtml](Components.RecommendationsComponent.md#defaulthtml)
- [eventFilter](Components.RecommendationsComponent.md#eventfilter)
- [handlebars](Components.RecommendationsComponent.md#handlebars)

### Accessors

- [configuration](Components.RecommendationsComponent.md#configuration)
- [rootElement](Components.RecommendationsComponent.md#rootelement)

### Methods

- [bindChildElements](Components.RecommendationsComponent.md#bindchildelements)
- [connectedCallback](Components.RecommendationsComponent.md#connectedcallback)
- [disconnectedCallback](Components.RecommendationsComponent.md#disconnectedcallback)
- [getContentModel](Components.RecommendationsComponent.md#getcontentmodel)
- [interpolate](Components.RecommendationsComponent.md#interpolate)
- [onRender](Components.RecommendationsComponent.md#onrender)
- [registerHelpers](Components.RecommendationsComponent.md#registerhelpers)
- [render](Components.RecommendationsComponent.md#render)
- [renderContent](Components.RecommendationsComponent.md#rendercontent)

## Constructors

### constructor

• **new RecommendationsComponent**()

#### Overrides

BaseComponent&lt;RecommendationsComponentConfig, RecommendationsWidget, RecommendationsComponentModel\&gt;.constructor

#### Defined in

[src/components/recommendations/recommendations/recommendations.component.ts:120](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/recommendations/recommendations/recommendations.component.ts#lines-120)

## Properties

### bindFromEvent

• `Protected` **bindFromEvent**: `boolean` = `true`

#### Overrides

BaseComponent.bindFromEvent

#### Defined in

[src/components/recommendations/recommendations/recommendations.component.ts:66](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/recommendations/recommendations/recommendations.component.ts#lines-66)

___

### componentName

• `Protected` **componentName**: keyof [`HawkSearchComponents`](../interfaces/Models.HawkSearchComponents.md) = `'recommendations'`

#### Overrides

BaseComponent.componentName

#### Defined in

[src/components/recommendations/recommendations/recommendations.component.ts:64](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/recommendations/recommendations/recommendations.component.ts#lines-64)

___

### contentModel

• `Protected` `Optional` **contentModel**: [`RecommendationsComponentModel`](../interfaces/Models.RecommendationsComponentModel.md)

The data bound to the Handlebars template.

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[contentModel](Components.BaseComponent.md#contentmodel)

#### Defined in

[src/components/base.component.ts:35](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-35)

___

### data

• `Optional` **data**: [`RecommendationsWidget`](../interfaces/Models.RecommendationsWidget.md)

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

[src/components/recommendations/recommendations/recommendations.component.ts:65](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/recommendations/recommendations/recommendations.component.ts#lines-65)

___

### eventFilter

• `Protected` **eventFilter**: `undefined` \| `string`

#### Overrides

BaseComponent.eventFilter

#### Defined in

[src/components/recommendations/recommendations/recommendations.component.ts:67](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/recommendations/recommendations/recommendations.component.ts#lines-67)

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

[src/components/recommendations/recommendations/recommendations.component.ts:180](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/recommendations/recommendations/recommendations.component.ts#lines-180)

___

### connectedCallback

▸ **connectedCallback**(): `void`

#### Returns

`void`

#### Overrides

BaseComponent.connectedCallback

#### Defined in

[src/components/recommendations/recommendations/recommendations.component.ts:134](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/recommendations/recommendations/recommendations.component.ts#lines-134)

___

### disconnectedCallback

▸ **disconnectedCallback**(): `void`

#### Returns

`void`

#### Overrides

BaseComponent.disconnectedCallback

#### Defined in

[src/components/recommendations/recommendations/recommendations.component.ts:146](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/recommendations/recommendations/recommendations.component.ts#lines-146)

___

### getContentModel

▸ `Protected` **getContentModel**(): [`RecommendationsComponentModel`](../interfaces/Models.RecommendationsComponentModel.md)

#### Returns

[`RecommendationsComponentModel`](../interfaces/Models.RecommendationsComponentModel.md)

#### Overrides

BaseComponent.getContentModel

#### Defined in

[src/components/recommendations/recommendations/recommendations.component.ts:158](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/recommendations/recommendations/recommendations.component.ts#lines-158)

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

#### Overrides

[BaseComponent](Components.BaseComponent.md).[onRender](Components.BaseComponent.md#onrender)

#### Defined in

[src/components/recommendations/recommendations/recommendations.component.ts:234](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/recommendations/recommendations/recommendations.component.ts#lines-234)

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

Binds [contentModel](Components.RecommendationsComponent.md#contentmodel) to the Handlebars template and renders the resulting HTML content.

#### Returns

`void`

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[render](Components.BaseComponent.md#render)

#### Defined in

[src/components/base.component.ts:171](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-171)

___

### renderContent

▸ `Protected` **renderContent**(): `boolean`

Determines whether the [data](Components.RecommendationsComponent.md#data) meets the necessary conditions to perform data binding and render content.

#### Returns

`boolean`

Whether the component should be rendered. If `false`, the component will have empty contents and be set to `display: none;`.

#### Overrides

[BaseComponent](Components.BaseComponent.md).[renderContent](Components.BaseComponent.md#rendercontent)

#### Defined in

[src/components/recommendations/recommendations/recommendations.component.ts:154](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/recommendations/recommendations/recommendations.component.ts#lines-154)
