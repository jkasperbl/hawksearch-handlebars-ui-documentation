[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Components](../modules/Components.md) / SelectedFacetsComponent

# Class: SelectedFacetsComponent

[Components](../modules/Components.md).SelectedFacetsComponent

The Selected Facets component displays a list of facets that have been selected by the user.

## Tag
The tag for this component is `<hawksearch-selected-facets>`.

## Event-Binding Attributes
| Name | Value |
| :- | :- |
| hawksearch-facet-field | `string` |
| hawksearch-facet-value | `string` |

When an element with both of these attributes is clicked, that facet selection will be removed and the search results will be updated.

## Default Template
The following is the default Handlebars template for this component. To create a custom template, it is recommended to use this as a starting point.
```
<div class="flex-gap flex-gap--xs selected-facets">
    {{#each selections}}
        <span class="selected-facets__item">
            <span class="selected-facets__item__field">{{title}}</span>
            <span class="selected-facets__item__value{{attribute ' selected-facets__item__value--excluded' excluded}}">{{selectionTitle}}</span>
            <a
                hawksearch-facet-field="{{field}}"
                hawksearch-facet-value="{{selectionValue}}"
                class="selected-facets__item__remove"
                title="{{@root.strings.remove}}"
            >
                <hawksearch-icon name="cross" size="0.9em"></hawksearch-icon>
            </a>
        </span>
    {{/each}}
</div>
```

## Hierarchy

- [`BaseComponent`](Components.BaseComponent.md)<[`SelectedFacetsComponentConfig`](../interfaces/Models.SelectedFacetsComponentConfig.md), [`SelectedFacet`](../interfaces/Models.SelectedFacet.md)[], [`SelectedFacetsComponentModel`](../interfaces/Models.SelectedFacetsComponentModel.md)\>

  ↳ **`SelectedFacetsComponent`**

## Table of contents

### Properties

- [bindFromEvent](Components.SelectedFacetsComponent.md#bindfromevent)
- [componentName](Components.SelectedFacetsComponent.md#componentname)
- [contentModel](Components.SelectedFacetsComponent.md#contentmodel)
- [data](Components.SelectedFacetsComponent.md#data)
- [defaultHtml](Components.SelectedFacetsComponent.md#defaulthtml)
- [handlebars](Components.SelectedFacetsComponent.md#handlebars)

### Accessors

- [configuration](Components.SelectedFacetsComponent.md#configuration)
- [rootElement](Components.SelectedFacetsComponent.md#rootelement)

### Methods

- [bindChildElements](Components.SelectedFacetsComponent.md#bindchildelements)
- [getContentModel](Components.SelectedFacetsComponent.md#getcontentmodel)
- [interpolate](Components.SelectedFacetsComponent.md#interpolate)
- [onRender](Components.SelectedFacetsComponent.md#onrender)
- [registerHelpers](Components.SelectedFacetsComponent.md#registerhelpers)
- [render](Components.SelectedFacetsComponent.md#render)
- [renderContent](Components.SelectedFacetsComponent.md#rendercontent)

## Properties

### bindFromEvent

• `Protected` **bindFromEvent**: `boolean` = `true`

#### Overrides

BaseComponent.bindFromEvent

#### Defined in

[src/components/search/selected-facets/selected-facets.component.ts:30](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/selected-facets/selected-facets.component.ts#lines-30)

___

### componentName

• `Protected` **componentName**: keyof [`HawkSearchComponents`](../interfaces/Models.HawkSearchComponents.md) = `'selected-facets'`

#### Overrides

BaseComponent.componentName

#### Defined in

[src/components/search/selected-facets/selected-facets.component.ts:28](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/selected-facets/selected-facets.component.ts#lines-28)

___

### contentModel

• `Protected` `Optional` **contentModel**: [`SelectedFacetsComponentModel`](../interfaces/Models.SelectedFacetsComponentModel.md)

The data bound to the Handlebars template.

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[contentModel](Components.BaseComponent.md#contentmodel)

#### Defined in

[src/components/base.component.ts:35](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-35)

___

### data

• `Optional` **data**: [`SelectedFacet`](../interfaces/Models.SelectedFacet.md)[]

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

[src/components/search/selected-facets/selected-facets.component.ts:29](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/selected-facets/selected-facets.component.ts#lines-29)

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

[src/components/search/selected-facets/selected-facets.component.ts:110](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/selected-facets/selected-facets.component.ts#lines-110)

___

### getContentModel

▸ `Protected` **getContentModel**(): [`SelectedFacetsComponentModel`](../interfaces/Models.SelectedFacetsComponentModel.md)

#### Returns

[`SelectedFacetsComponentModel`](../interfaces/Models.SelectedFacetsComponentModel.md)

#### Overrides

BaseComponent.getContentModel

#### Defined in

[src/components/search/selected-facets/selected-facets.component.ts:36](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/selected-facets/selected-facets.component.ts#lines-36)

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

Binds [contentModel](Components.SelectedFacetsComponent.md#contentmodel) to the Handlebars template and renders the resulting HTML content.

#### Returns

`void`

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[render](Components.BaseComponent.md#render)

#### Defined in

[src/components/base.component.ts:171](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-171)

___

### renderContent

▸ `Protected` **renderContent**(): `boolean`

Determines whether the [data](Components.SelectedFacetsComponent.md#data) meets the necessary conditions to perform data binding and render content.

#### Returns

`boolean`

Whether the component should be rendered. If `false`, the component will have empty contents and be set to `display: none;`.

#### Overrides

[BaseComponent](Components.BaseComponent.md).[renderContent](Components.BaseComponent.md#rendercontent)

#### Defined in

[src/components/search/selected-facets/selected-facets.component.ts:32](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/selected-facets/selected-facets.component.ts#lines-32)
