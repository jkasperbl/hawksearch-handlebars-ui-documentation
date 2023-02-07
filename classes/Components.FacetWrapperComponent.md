[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Components](../modules/Components.md) / FacetWrapperComponent

# Class: FacetWrapperComponent

[Components](../modules/Components.md).FacetWrapperComponent

The Facet Wrapper component adds functionality common to all facet types such as expand/collapse, tooltip, and value search.

## Tag
The tag for this component is `<hawksearch-facet-wrapper>`.

## Event-Binding Attributes
| Name | Value |
| :- | :- |
| hawksearch-facet-heading | |

When an element with this attribute is clicked, the [collapsed](../interfaces/Models.FacetWrapperComponentModel.md#collapsed) value will be reversed. This is intended to show/hide the list of facet values to make the list of facets more manageable.

| Name | Value |
| :- | :- |
| hawksearch-facet-search | |

When the user types in an input element with this attribute, the [values](../interfaces/Models.FacetWrapperComponentModel.md#values) collection will be filtered to show only values containing the entered text.

| Name | Value |
| :- | :- |
| hawksearch-facet | |

The tag for each facet type must have this attribute to have data bound to it.

This helper function returns the zero-padded day of the month from a provided date object.

## Default Template
The following is the default Handlebars template for this component. To create a custom template, it is recommended to use this as a starting point.
```
<div class="facet">
    <div hawksearch-facet-heading class="facet__heading{{attribute ' facet__heading--collapsible' collapsible}}">
        {{title}}
        {{#if tooltip}}
            <hawksearch-tooltip text="{{tooltip}}"></hawksearch-tooltip>
        {{/if}}
        {{#if collapsible}}
            <hawksearch-icon name="{{if-else collapsed 'chevron-right' 'chevron-down'}}" size="1.5em" class="facet__heading__toggle"></hawksearch-icon>
        {{/if}}
    </div>
    {{#unless collapsed}}
        <div class="facet__content">
            {{#if searchable}}
                <input type="text" placeholder="Quick Lookup" hawksearch-facet-search value="{{filter}}" class="facet__search" />
            {{/if}}
            {{#if (eq type "checkbox")}}
                <hawksearch-checkbox-list-facet hawksearch-facet></hawksearch-checkbox-list-facet>
            {{/if}}
            {{#if (eq type "color")}}
                <hawksearch-color-facet hawksearch-facet></hawksearch-color-facet>
            {{/if}}
            {{#if (eq type "date-range")}}
                <hawksearch-date-range-facet hawksearch-facet></hawksearch-date-range-facet>
            {{/if}}
            {{#if (eq type "link")}}
                <hawksearch-link-list-facet hawksearch-facet></hawksearch-link-list-facet>
            {{/if}}
            {{#if (eq type "numeric-range")}}
                <hawksearch-numeric-range-facet hawksearch-facet></hawksearch-numeric-range-facet>
            {{/if}}
            {{#if (eq type "range-slider")}}
                <hawksearch-range-slider-facet hawksearch-facet></hawksearch-range-slider-facet>
            {{/if}}
            {{#if (eq type "recent-searches")}}
                <hawksearch-recent-searches-facet hawksearch-facet></hawksearch-recent-searches-facet>
            {{/if}}
            {{#if (eq type "related-searches")}}
                <hawksearch-related-searches-facet hawksearch-facet></hawksearch-related-searches-facet>
            {{/if}}
            {{#if (eq type "search")}}
                <hawksearch-search-within-facet hawksearch-facet></hawksearch-search-within-facet>
            {{/if}}
            {{#if (eq type "size")}}
                <hawksearch-size-facet hawksearch-facet></hawksearch-size-facet>
            {{/if}}
        </div>
    {{/unless}}
</div>
```

## Hierarchy

- [`BaseComponent`](Components.BaseComponent.md)<[`FacetWrapperComponentConfig`](../interfaces/Models.FacetWrapperComponentConfig.md), [`Facet`](../interfaces/Models.Facet.md), [`FacetWrapperComponentModel`](../interfaces/Models.FacetWrapperComponentModel.md)\>

  ↳ **`FacetWrapperComponent`**

## Table of contents

### Properties

- [bindFromEvent](Components.FacetWrapperComponent.md#bindfromevent)
- [componentName](Components.FacetWrapperComponent.md#componentname)
- [contentModel](Components.FacetWrapperComponent.md#contentmodel)
- [data](Components.FacetWrapperComponent.md#data)
- [defaultHtml](Components.FacetWrapperComponent.md#defaulthtml)
- [handlebars](Components.FacetWrapperComponent.md#handlebars)
- [state](Components.FacetWrapperComponent.md#state)

### Accessors

- [configuration](Components.FacetWrapperComponent.md#configuration)
- [rootElement](Components.FacetWrapperComponent.md#rootelement)

### Methods

- [bindChildElements](Components.FacetWrapperComponent.md#bindchildelements)
- [getContentModel](Components.FacetWrapperComponent.md#getcontentmodel)
- [interpolate](Components.FacetWrapperComponent.md#interpolate)
- [onRender](Components.FacetWrapperComponent.md#onrender)
- [registerHelpers](Components.FacetWrapperComponent.md#registerhelpers)
- [render](Components.FacetWrapperComponent.md#render)
- [renderContent](Components.FacetWrapperComponent.md#rendercontent)

## Properties

### bindFromEvent

• `Protected` **bindFromEvent**: `boolean` = `false`

#### Overrides

BaseComponent.bindFromEvent

#### Defined in

[src/components/search/facet-wrapper/facet-wrapper.component.ts:42](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/facet-wrapper/facet-wrapper.component.ts#lines-42)

___

### componentName

• `Protected` **componentName**: keyof [`HawkSearchComponents`](../interfaces/Models.HawkSearchComponents.md) = `'facet-wrapper'`

#### Overrides

BaseComponent.componentName

#### Defined in

[src/components/search/facet-wrapper/facet-wrapper.component.ts:40](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/facet-wrapper/facet-wrapper.component.ts#lines-40)

___

### contentModel

• `Protected` `Optional` **contentModel**: [`FacetWrapperComponentModel`](../interfaces/Models.FacetWrapperComponentModel.md)

The data bound to the Handlebars template.

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[contentModel](Components.BaseComponent.md#contentmodel)

#### Defined in

[src/components/base.component.ts:35](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-35)

___

### data

• `Optional` **data**: [`Facet`](../interfaces/Models.Facet.md)

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

[src/components/search/facet-wrapper/facet-wrapper.component.ts:41](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/facet-wrapper/facet-wrapper.component.ts#lines-41)

___

### handlebars

• `Protected` **handlebars**: typeof `Handlebars` = `HawkSearch.handlebars`

The Handlebars reference shared by all HawkSearch components.

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[handlebars](Components.BaseComponent.md#handlebars)

#### Defined in

[src/components/base.component.ts:23](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-23)

___

### state

• **state**: [`FacetState`](../modules/Models.md#facetstate)

#### Defined in

[src/components/search/facet-wrapper/facet-wrapper.component.ts:44](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/facet-wrapper/facet-wrapper.component.ts#lines-44)

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

[src/components/search/facet-wrapper/facet-wrapper.component.ts:59](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/facet-wrapper/facet-wrapper.component.ts#lines-59)

___

### getContentModel

▸ `Protected` **getContentModel**(): [`FacetWrapperComponentModel`](../interfaces/Models.FacetWrapperComponentModel.md)

#### Returns

[`FacetWrapperComponentModel`](../interfaces/Models.FacetWrapperComponentModel.md)

#### Overrides

BaseComponent.getContentModel

#### Defined in

[src/components/search/facet-wrapper/facet-wrapper.component.ts:50](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/facet-wrapper/facet-wrapper.component.ts#lines-50)

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

Binds [contentModel](Components.FacetWrapperComponent.md#contentmodel) to the Handlebars template and renders the resulting HTML content.

#### Returns

`void`

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[render](Components.BaseComponent.md#render)

#### Defined in

[src/components/base.component.ts:171](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-171)

___

### renderContent

▸ `Protected` **renderContent**(): `boolean`

Determines whether the [data](Components.FacetWrapperComponent.md#data) meets the necessary conditions to perform data binding and render content.

#### Returns

`boolean`

Whether the component should be rendered. If `false`, the component will have empty contents and be set to `display: none;`.

#### Overrides

[BaseComponent](Components.BaseComponent.md).[renderContent](Components.BaseComponent.md#rendercontent)

#### Defined in

[src/components/search/facet-wrapper/facet-wrapper.component.ts:46](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/facet-wrapper/facet-wrapper.component.ts#lines-46)
