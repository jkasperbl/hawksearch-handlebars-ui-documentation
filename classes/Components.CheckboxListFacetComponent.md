[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Components](../modules/Components.md) / CheckboxListFacetComponent

# Class: CheckboxListFacetComponent

[Components](../modules/Components.md).CheckboxListFacetComponent

The Checkbox List Facet component renders a checkbox for each facet and may be nested depending on the configuration in the Hawksearch admin.

## Tag
The tag for this component is `<hawksearch-checkbox-list-facet>`.

## Event-Binding Attributes
*Note: For Event-Binding attributes common to all facet type components, see [BaseFacetComponent](Components.BaseFacetComponent.md).*

## Handlebars Partials
| Name | Parameter |
| :- | :- |
| facet-checkbox-list | `Array<CheckboxListFacetValue>` |

This partial renders a checkbox for each facet value along with any applicable actions (include, exclude, toggle).

*Note: For more information, see [CheckboxListFacetValue](../interfaces/Models.CheckboxListFacetValue.md).*

{% raw %}
```
{{#if length}}
    <ul class="checkbox-list-facet__list">
        {{#each this}}
            {{#if visible}}
                <li
                    class="checkbox-list-facet__list__item{{attribute ' checkbox-list-facet__list__item--excluded' excluded}}{{attribute
                            ' checkbox-list-facet__list__item--collapsible'
                            hasChildren
                        }}"
                >
                    <div class="checkbox-list-facet__list__item__content">
                        {{#if selected}}
                            <input id="{{@root.id}}-{{value}}" type="checkbox" checked hawksearch-facet-value value="{{value}}" />
                        {{else}}
                            <input id="{{@root.id}}-{{value}}" type="checkbox" hawksearch-facet-value value="{{value}}" />
                        {{/if}}
                        <label for="{{@root.id}}-{{value}}" class="facet__value">
                            <span class="facet__value__title checkbox-list-facet__list__item__title">{{title}}</span>
                            {{#if @root.displayCount}}
                                <span class="facet__value__count checkbox-list-facet__list__item__count">({{count}})</span>
                            {{/if}}
                        </label>
                        {{#if toggled}}
                            {{> facet-checkbox-list children}}
                        {{/if}}
                    </div>
                    <div class="checkbox-list-facet__list__item__actions">
                        {{#if excluded}}
                            <span hawksearch-facet-value-include="{{value}}" class="checkbox-list-facet__list__item__actions__item" title="{{@root.strings.include}}">
                                <hawksearch-icon name="plus" class="facet__heading__actions__item"></hawksearch-icon>
                            </span>
                        {{else}}
                            <span hawksearch-facet-value-exclude="{{value}}" class="checkbox-list-facet__list__item__actions__item" title="{{@root.strings.exclude}}">
                                <hawksearch-icon name="minus" class="facet__heading__actions__item"></hawksearch-icon>
                            </span>
                        {{/if}}
                        {{#if hasChildren}}
                            <span hawksearch-facet-value-toggle="{{value}}" class="checkbox-list-facet__list__item__actions__item" title="{{if-else toggled @root.strings.collapse @root.strings.expand}}">
                                <hawksearch-icon name="{{if-else toggled 'chevron-down' 'chevron-right'}}" class="facet__heading__toggle"></hawksearch-icon>
                            </span>
                        {{/if}}
                    </div>
                </li>
            {{/if}}
        {{/each}}
    </ul>
{{/if}}
```
{% endraw %}

## Default Template
The following is the default Handlebars template for this component. To create a custom template, it is recommended to use this as a starting point.
```
<div class="checkbox-list-facet" {{attribute (concat 'style="max-height: ' maxHeight 'px;"') maxHeight}}>
    {{> facet-checkbox-list values}}
    {{#if showToggle}}
        <span hawksearch-facet-toggle class="link facet__toggle">{{strings.toggle}}</span>
    {{/if}}
</div>
```

## Hierarchy

- [`BaseFacetComponent`](Components.BaseFacetComponent.md)<[`CheckboxListFacetComponentConfig`](../interfaces/Models.CheckboxListFacetComponentConfig.md), [`CheckboxListFacetComponentModel`](../interfaces/Models.CheckboxListFacetComponentModel.md)\>

  ↳ **`CheckboxListFacetComponent`**

## Table of contents

### Properties

- [bindFromEvent](Components.CheckboxListFacetComponent.md#bindfromevent)
- [componentName](Components.CheckboxListFacetComponent.md#componentname)
- [contentModel](Components.CheckboxListFacetComponent.md#contentmodel)
- [data](Components.CheckboxListFacetComponent.md#data)
- [defaultHtml](Components.CheckboxListFacetComponent.md#defaulthtml)
- [handlebars](Components.CheckboxListFacetComponent.md#handlebars)
- [state](Components.CheckboxListFacetComponent.md#state)

### Accessors

- [configuration](Components.CheckboxListFacetComponent.md#configuration)
- [rootElement](Components.CheckboxListFacetComponent.md#rootelement)

### Methods

- [bindChildElements](Components.CheckboxListFacetComponent.md#bindchildelements)
- [getContentModel](Components.CheckboxListFacetComponent.md#getcontentmodel)
- [interpolate](Components.CheckboxListFacetComponent.md#interpolate)
- [onRender](Components.CheckboxListFacetComponent.md#onrender)
- [registerHelpers](Components.CheckboxListFacetComponent.md#registerhelpers)
- [render](Components.CheckboxListFacetComponent.md#render)
- [renderContent](Components.CheckboxListFacetComponent.md#rendercontent)

## Properties

### bindFromEvent

• `Protected` **bindFromEvent**: `boolean` = `false`

#### Inherited from

[BaseFacetComponent](Components.BaseFacetComponent.md).[bindFromEvent](Components.BaseFacetComponent.md#bindfromevent)

#### Defined in

[src/components/search/facet-types/base-facet.component.ts:42](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/facet-types/base-facet.component.ts#lines-42)

___

### componentName

• `Protected` **componentName**: keyof [`HawkSearchComponents`](../interfaces/Models.HawkSearchComponents.md) = `'checkbox-list-facet'`

#### Overrides

BaseFacetComponent.componentName

#### Defined in

[src/components/search/facet-types/checkbox-list-facet/checkbox-list-facet.component.ts:33](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/facet-types/checkbox-list-facet/checkbox-list-facet.component.ts#lines-33)

___

### contentModel

• `Protected` `Optional` **contentModel**: [`CheckboxListFacetComponentModel`](../interfaces/Models.CheckboxListFacetComponentModel.md)

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

[src/components/search/facet-types/checkbox-list-facet/checkbox-list-facet.component.ts:34](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/facet-types/checkbox-list-facet/checkbox-list-facet.component.ts#lines-34)

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

▸ `Protected` **getContentModel**(): [`CheckboxListFacetComponentModel`](../interfaces/Models.CheckboxListFacetComponentModel.md)

#### Returns

[`CheckboxListFacetComponentModel`](../interfaces/Models.CheckboxListFacetComponentModel.md)

#### Overrides

BaseFacetComponent.getContentModel

#### Defined in

[src/components/search/facet-types/checkbox-list-facet/checkbox-list-facet.component.ts:46](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/facet-types/checkbox-list-facet/checkbox-list-facet.component.ts#lines-46)

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

#### Overrides

[BaseFacetComponent](Components.BaseFacetComponent.md).[registerHelpers](Components.BaseFacetComponent.md#registerhelpers)

#### Defined in

[src/components/search/facet-types/checkbox-list-facet/checkbox-list-facet.component.ts:36](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/facet-types/checkbox-list-facet/checkbox-list-facet.component.ts#lines-36)

___

### render

▸ **render**(): `void`

Binds [contentModel](Components.CheckboxListFacetComponent.md#contentmodel) to the Handlebars template and renders the resulting HTML content.

#### Returns

`void`

#### Inherited from

[BaseFacetComponent](Components.BaseFacetComponent.md).[render](Components.BaseFacetComponent.md#render)

#### Defined in

[src/components/base.component.ts:171](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-171)

___

### renderContent

▸ `Protected` **renderContent**(): `boolean`

Determines whether the [data](Components.CheckboxListFacetComponent.md#data) meets the necessary conditions to perform data binding and render content.

#### Returns

`boolean`

Whether the component should be rendered. If `false`, the component will have empty contents and be set to `display: none;`.

#### Overrides

[BaseFacetComponent](Components.BaseFacetComponent.md).[renderContent](Components.BaseFacetComponent.md#rendercontent)

#### Defined in

[src/components/search/facet-types/checkbox-list-facet/checkbox-list-facet.component.ts:42](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/search/facet-types/checkbox-list-facet/checkbox-list-facet.component.ts#lines-42)
