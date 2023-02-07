[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Components](../modules/Components.md) / SizeFacetComponent

# Class: SizeFacetComponent

[Components](../modules/Components.md).SizeFacetComponent

The Size Facet component displays a list of product sizes in a grid format.

## Tag
The tag for this component is `<hawksearch-size-facet>`.

## Event-Binding Attributes
*Note: For Event-Binding attributes common to all facet type components, see [BaseFacetComponent](Components.BaseFacetComponent.md).*

## Default Template
The following is the default Handlebars template for this component. To create a custom template, it is recommended to use this as a starting point.
```
<div class="size-facet">
    <div class="row row--tight size-facet__items">
        {{#each values}}
            {{#if visible}}
                <div class="column column--3 size-facet__item{{attribute ' size-facet__item--selected' selected}}">
                    <div hawksearch-facet-value="{{value}}" class="size-facet__item__outer">
                        <div hawksearch-facet-value="{{value}}" class="size-facet__item__inner">
                            {{title}}
                        </div>
                    </div>
                    <span class="size-facet__item__actions">
                        {{#if excluded}}
                            <span hawksearch-facet-value-include="{{value}}" class="size-facet__item__actions__item" title="{{@root.strings.include}}">
                                <hawksearch-icon name="plus"></hawksearch-icon>
                            </span>
                        {{else}}
                            <span hawksearch-facet-value-exclude="{{value}}" class="size-facet__item__actions__item" title="{{@root.strings.exclude}}">
                                <hawksearch-icon name="minus"></hawksearch-icon>
                            </span>
                        {{/if}}
                    </span>
                </div>
            {{/if}}
        {{/each}}
    </div>
    {{#if showToggle}}
        <span hawksearch-facet-toggle class="link facet__toggle">{{strings.toggle}}</span>
    {{/if}}
</div>
```

## Hierarchy

- [`BaseFacetComponent`](Components.BaseFacetComponent.md)<[`SizeFacetComponentConfig`](../interfaces/Models.SizeFacetComponentConfig.md), [`SizeFacetComponentModel`](../interfaces/Models.SizeFacetComponentModel.md)\>

  ↳ **`SizeFacetComponent`**

## Table of contents

### Properties

- [bindFromEvent](Components.SizeFacetComponent.md#bindfromevent)
- [componentName](Components.SizeFacetComponent.md#componentname)
- [contentModel](Components.SizeFacetComponent.md#contentmodel)
- [data](Components.SizeFacetComponent.md#data)
- [defaultHtml](Components.SizeFacetComponent.md#defaulthtml)
- [handlebars](Components.SizeFacetComponent.md#handlebars)
- [state](Components.SizeFacetComponent.md#state)

### Accessors

- [configuration](Components.SizeFacetComponent.md#configuration)
- [rootElement](Components.SizeFacetComponent.md#rootelement)

### Methods

- [bindChildElements](Components.SizeFacetComponent.md#bindchildelements)
- [getContentModel](Components.SizeFacetComponent.md#getcontentmodel)
- [interpolate](Components.SizeFacetComponent.md#interpolate)
- [onRender](Components.SizeFacetComponent.md#onrender)
- [registerHelpers](Components.SizeFacetComponent.md#registerhelpers)
- [render](Components.SizeFacetComponent.md#render)
- [renderContent](Components.SizeFacetComponent.md#rendercontent)

## Properties

### bindFromEvent

• `Protected` **bindFromEvent**: `boolean` = `false`

#### Inherited from

[BaseFacetComponent](Components.BaseFacetComponent.md).[bindFromEvent](Components.BaseFacetComponent.md#bindfromevent)

#### Defined in

[src/components/search/facet-types/base-facet.component.ts:42](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/facet-types/base-facet.component.ts#lines-42)

___

### componentName

• `Protected` **componentName**: keyof [`HawkSearchComponents`](../interfaces/Models.HawkSearchComponents.md) = `'size-facet'`

#### Overrides

BaseFacetComponent.componentName

#### Defined in

[src/components/search/facet-types/size-facet/size-facet.component.ts:21](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/facet-types/size-facet/size-facet.component.ts#lines-21)

___

### contentModel

• `Protected` `Optional` **contentModel**: [`SizeFacetComponentModel`](../interfaces/Models.SizeFacetComponentModel.md)

The data bound to the Handlebars template.

#### Inherited from

[BaseFacetComponent](Components.BaseFacetComponent.md).[contentModel](Components.BaseFacetComponent.md#contentmodel)

#### Defined in

[src/components/base.component.ts:35](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-35)

___

### data

• `Optional` **data**: [`Facet`](../interfaces/Models.Facet.md)

The data bound to the component.

#### Inherited from

[BaseFacetComponent](Components.BaseFacetComponent.md).[data](Components.BaseFacetComponent.md#data)

#### Defined in

[src/components/base.component.ts:18](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-18)

___

### defaultHtml

• `Protected` **defaultHtml**: `any` = `defaultHtml`

#### Overrides

BaseFacetComponent.defaultHtml

#### Defined in

[src/components/search/facet-types/size-facet/size-facet.component.ts:22](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/facet-types/size-facet/size-facet.component.ts#lines-22)

___

### handlebars

• `Protected` **handlebars**: typeof `Handlebars` = `HawkSearch.handlebars`

The Handlebars reference shared by all HawkSearch components.

#### Inherited from

[BaseFacetComponent](Components.BaseFacetComponent.md).[handlebars](Components.BaseFacetComponent.md#handlebars)

#### Defined in

[src/components/base.component.ts:23](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-23)

___

### state

• **state**: [`FacetState`](../modules/Models.md#facetstate)

#### Inherited from

[BaseFacetComponent](Components.BaseFacetComponent.md).[state](Components.BaseFacetComponent.md#state)

#### Defined in

[src/components/search/facet-types/base-facet.component.ts:44](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/facet-types/base-facet.component.ts#lines-44)

## Accessors

### configuration

• `Protected` `get` **configuration**(): `undefined` \| `TConfig`

The optional configuration object for this component.

#### Returns

`undefined` \| `TConfig`

#### Inherited from

BaseFacetComponent.configuration

#### Defined in

[src/components/base.component.ts:61](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-61)

___

### rootElement

• `Protected` `get` **rootElement**(): `ParentNode`

The root element which should be used for querying any child elements. This resolves to `this.shadowRoot` if the Shadow DOM is enabled, otherwise `this`.

#### Returns

`ParentNode`

#### Inherited from

BaseFacetComponent.rootElement

#### Defined in

[src/components/base.component.ts:78](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-78)

## Methods

### bindChildElements

▸ `Protected` **bindChildElements**(): `void`

After the component is rendered, this method is called to bind any child components.

#### Returns

`void`

#### Inherited from

[BaseFacetComponent](Components.BaseFacetComponent.md).[bindChildElements](Components.BaseFacetComponent.md#bindchildelements)

#### Defined in

[src/components/search/facet-types/base-facet.component.ts:46](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/facet-types/base-facet.component.ts#lines-46)

___

### getContentModel

▸ `Protected` **getContentModel**(): [`SizeFacetComponentModel`](../interfaces/Models.SizeFacetComponentModel.md)

#### Returns

[`SizeFacetComponentModel`](../interfaces/Models.SizeFacetComponentModel.md)

#### Overrides

BaseFacetComponent.getContentModel

#### Defined in

[src/components/search/facet-types/size-facet/size-facet.component.ts:28](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/facet-types/size-facet/size-facet.component.ts#lines-28)

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

[BaseFacetComponent](Components.BaseFacetComponent.md).[interpolate](Components.BaseFacetComponent.md#interpolate)

#### Defined in

[src/components/base.component.ts:308](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-308)

___

### onRender

▸ `Protected` **onRender**(): `void`

After the component is rendered, this method is called for any additional processing (such as attaching event listeners) which needs to occur.

#### Returns

`void`

#### Inherited from

[BaseFacetComponent](Components.BaseFacetComponent.md).[onRender](Components.BaseFacetComponent.md#onrender)

#### Defined in

[src/components/base.component.ts:264](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-264)

___

### registerHelpers

▸ `Protected` **registerHelpers**(): `void`

Optional method that can be overwritten to register Handlebars helper functions which can be accessed from the template. For more information, see [Custom Helpers](https://handlebarsjs.com/guide/#custom-helpers).

#### Returns

`void`

#### Inherited from

[BaseFacetComponent](Components.BaseFacetComponent.md).[registerHelpers](Components.BaseFacetComponent.md#registerhelpers)

#### Defined in

[src/components/base.component.ts:166](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-166)

___

### render

▸ **render**(): `void`

Binds [contentModel](Components.SizeFacetComponent.md#contentmodel) to the Handlebars template and renders the resulting HTML content.

#### Returns

`void`

#### Inherited from

[BaseFacetComponent](Components.BaseFacetComponent.md).[render](Components.BaseFacetComponent.md#render)

#### Defined in

[src/components/base.component.ts:171](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-171)

___

### renderContent

▸ `Protected` **renderContent**(): `boolean`

Determines whether the [data](Components.SizeFacetComponent.md#data) meets the necessary conditions to perform data binding and render content.

#### Returns

`boolean`

Whether the component should be rendered. If `false`, the component will have empty contents and be set to `display: none;`.

#### Overrides

[BaseFacetComponent](Components.BaseFacetComponent.md).[renderContent](Components.BaseFacetComponent.md#rendercontent)

#### Defined in

[src/components/search/facet-types/size-facet/size-facet.component.ts:24](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/facet-types/size-facet/size-facet.component.ts#lines-24)
