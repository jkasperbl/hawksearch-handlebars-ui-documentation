[@bridgeline-digital/hawksearch-handlebars-ui](../README.md) / [Modules](../modules.md) / [Components](../modules/Components.md) / DatePickerComponent

# Class: DatePickerComponent

[Components](../modules/Components.md).DatePickerComponent

The Date Picker component provides an intuitive interface that allows the user to select a range in ISO format. This component is currently only used within the [Date Range Facet Component](Components.DateRangeFacetComponent.md).

## Tag
The tag for this component is `<hawksearch-date-picker>`.

## Attributes
| Name | Value |
| :- | :- |
| label | `string` |
| min | `Date` |
| max | `Date` |
| value | `Date` |

## Event-Binding Attributes
| Name | Value |
| :- | :- |
| hawksearch-input | |

The input element must have this attribute. When this element is clicked, the date picker modal will be displayed.

| Name | Value |
| :- | :- |
| hawksearch-modal | |

This root element of the date picker modal must have this attribute to calculate modal positioning.

| Name | Value |
| :- | :- |
| hawksearch-month | |

This attribute is used to identify the form element used to select a specific month.

| Name | Value |
| :- | :- |
| hawksearch-year | |

This attribute is used to identify the form element used to select a specific year.

| Name | Value |
| :- | :- |
| hawksearch-select-month | |

When an element with this attribute is clicked, the month specified by `hawksearch-month` and `hawksearch-year` to be displayed in the date picker modal.

| Name | Value |
| :- | :- |
| hawksearch-previous | |

When an element with this attribute is clicked, the previous month will be displayed in the date picker modal.

| Name | Value |
| :- | :- |
| hawksearch-next | |

When an element with this attribute is clicked, the next month will be displayed in the date picker modal.

| Name | Value |
| :- | :- |
| hawksearch-month-selector | |

When an element with this attribute is clicked, the month selector will be displayed in the date picker modal to quickly jump to a particular month rather than using pagination.

| Name | Value |
| :- | :- |
| hawksearch-date | `string` (ISO date format) |

When an element with this attribute is clicked, the specified date will be selected and displayed in the input element.

## Events
| Name | Data Type |
| :- | :- |
| hawksearch:date-picker-changed | `Date` |

This event fires whenever the user selects a date.

## Handlebars Helpers
| Name | Parameter |
| :- | :- |
| dayOfMonth | `Date` |

This helper function returns the zero-padded day of the month from a provided date object.

## Default Template
The following is the default Handlebars template for this component. To create a custom template, it is recommended to use this as a starting point.
```
<div class="date-picker">
    <input type="text" value="{{value}}" hawksearch-input readonly class="date-picker__input" aria-label="{{strings.label}}" />
    {{#if modalVisible}}
        <div hawksearch-modal class="date-picker__modal">
            {{#if monthSelectorVisible}}
                <div class="date-picker__modal__header">
                    <span class="date-picker__modal__header__month">{{strings.selectMonth}}</span>
                </div>
                <div class="row">
                    <div class="column column--12">
                        <select hawksearch-month>
                            {{#each months}}
                                {{#if (eq this @root.currentMonth)}}
                                    <option value="{{@index}}" selected>{{this}}</option>
                                {{else}}
                                    <option value="{{@index}}">{{this}}</option>
                                {{/if}}
                            {{/each}}
                        </select>
                    </div>
                    <div class="column column--12">
                        <select hawksearch-year>
                            {{#each years}}
                                {{#if (eq this @root.currentYear)}}
                                    <option value="{{this}}" selected>{{this}}</option>
                                {{else}}
                                    <option value="{{this}}">{{this}}</option>
                                {{/if}}
                            {{/each}}
                        </select>
                    </div>
                    <div class="column column--12">
                        <button hawksearch-select-month class="button button--full-width">{{strings.viewCalendar}}</button>
                    </div>
                </div>
            {{else}}
                <div class="date-picker__modal__header">
                    <a hawksearch-previous class="date-picker__modal__header__previous" title="{{strings.previous}}">
                        <hawksearch-icon name="chevron-left"></hawksearch-icon>
                    </a>
                    <a hawksearch-month-selector class="date-picker__modal__header__month">{{strings.heading}}</a>
                    <a hawksearch-next class="date-picker__modal__header__next" title="{{strings.next}}">
                        <hawksearch-icon name="chevron-right"></hawksearch-icon>
                    </a>
                </div>
                <table class="date-picker__calendar" cellspacing="0" cellpadding="0">
                    <thead>
                        <tr>
                            <th scope="col">{{dayAbbreviation 0}}</th>
                            <th scope="col">{{dayAbbreviation 1}}</th>
                            <th scope="col">{{dayAbbreviation 2}}</th>
                            <th scope="col">{{dayAbbreviation 3}}</th>
                            <th scope="col">{{dayAbbreviation 4}}</th>
                            <th scope="col">{{dayAbbreviation 5}}</th>
                            <th scope="col">{{dayAbbreviation 6}}</th>
                        </tr>
                    </thead>
                    <tbody>
                        {{#each weeks}}
                            <tr>
                                {{#each this}}
                                    <td
                                        hawksearch-date="{{value}}"
                                        class="date-picker__calendar__day
                                            {{attribute ' date-picker__calendar__day--alternate' (eq currentMonth false)}}
                                            {{attribute ' date-picker__calendar__day--selected' selected}}
                                            {{attribute ' date-picker__calendar__day--disabled' (eq enabled false)}}"
                                    >
                                        <span>{{dayOfMonth date}}</span>
                                    </td>
                                {{/each}}
                            </tr>
                        {{/each}}
                    </tbody>
                </table>
            {{/if}}
        </div>
    {{/if}}
</div>
```

## Hierarchy

- [`BaseComponent`](Components.BaseComponent.md)<[`DatePickerComponentConfig`](../interfaces/Models.DatePickerComponentConfig.md), `never`, [`DatePickerComponentModel`](../interfaces/Models.DatePickerComponentModel.md)\>

  ↳ **`DatePickerComponent`**

## Table of contents

### Properties

- [bindFromEvent](Components.DatePickerComponent.md#bindfromevent)
- [componentName](Components.DatePickerComponent.md#componentname)
- [contentModel](Components.DatePickerComponent.md#contentmodel)
- [data](Components.DatePickerComponent.md#data)
- [defaultHtml](Components.DatePickerComponent.md#defaulthtml)
- [handlebars](Components.DatePickerComponent.md#handlebars)

### Accessors

- [configuration](Components.DatePickerComponent.md#configuration)
- [rootElement](Components.DatePickerComponent.md#rootelement)
- [observedAttributes](Components.DatePickerComponent.md#observedattributes)

### Methods

- [attributeChangedCallback](Components.DatePickerComponent.md#attributechangedcallback)
- [bindChildElements](Components.DatePickerComponent.md#bindchildelements)
- [connectedCallback](Components.DatePickerComponent.md#connectedcallback)
- [disconnectedCallback](Components.DatePickerComponent.md#disconnectedcallback)
- [getContentModel](Components.DatePickerComponent.md#getcontentmodel)
- [interpolate](Components.DatePickerComponent.md#interpolate)
- [onRender](Components.DatePickerComponent.md#onrender)
- [registerHelpers](Components.DatePickerComponent.md#registerhelpers)
- [render](Components.DatePickerComponent.md#render)
- [renderContent](Components.DatePickerComponent.md#rendercontent)

## Properties

### bindFromEvent

• `Protected` **bindFromEvent**: `boolean` = `false`

#### Overrides

BaseComponent.bindFromEvent

#### Defined in

[src/components/general/date-picker/date-picker.component.ts:103](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/general/date-picker/date-picker.component.ts#lines-103)

___

### componentName

• `Protected` **componentName**: keyof [`HawkSearchComponents`](../interfaces/Models.HawkSearchComponents.md) = `'date-picker'`

#### Overrides

BaseComponent.componentName

#### Defined in

[src/components/general/date-picker/date-picker.component.ts:101](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/general/date-picker/date-picker.component.ts#lines-101)

___

### contentModel

• `Protected` `Optional` **contentModel**: [`DatePickerComponentModel`](../interfaces/Models.DatePickerComponentModel.md)

The data bound to the Handlebars template.

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[contentModel](Components.BaseComponent.md#contentmodel)

#### Defined in

[src/components/base.component.ts:35](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-35)

___

### data

• `Optional` **data**: `undefined`

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

[src/components/general/date-picker/date-picker.component.ts:102](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/general/date-picker/date-picker.component.ts#lines-102)

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

### observedAttributes

• `Static` `get` **observedAttributes**(): `string`[]

#### Returns

`string`[]

#### Defined in

[src/components/general/date-picker/date-picker.component.ts:97](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/general/date-picker/date-picker.component.ts#lines-97)

## Methods

### attributeChangedCallback

▸ **attributeChangedCallback**(`name`, `oldValue`, `newValue`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `name` | `string` |
| `oldValue` | ``null`` \| `string` |
| `newValue` | ``null`` \| `string` |

#### Returns

`void`

#### Defined in

[src/components/general/date-picker/date-picker.component.ts:144](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/general/date-picker/date-picker.component.ts#lines-144)

___

### bindChildElements

▸ `Protected` **bindChildElements**(): `void`

After the component is rendered, this method is called to bind any child components.

#### Returns

`void`

#### Overrides

[BaseComponent](Components.BaseComponent.md).[bindChildElements](Components.BaseComponent.md#bindchildelements)

#### Defined in

[src/components/general/date-picker/date-picker.component.ts:203](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/general/date-picker/date-picker.component.ts#lines-203)

___

### connectedCallback

▸ **connectedCallback**(): `void`

#### Returns

`void`

#### Overrides

BaseComponent.connectedCallback

#### Defined in

[src/components/general/date-picker/date-picker.component.ts:115](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/general/date-picker/date-picker.component.ts#lines-115)

___

### disconnectedCallback

▸ **disconnectedCallback**(): `void`

#### Returns

`void`

#### Overrides

BaseComponent.disconnectedCallback

#### Defined in

[src/components/general/date-picker/date-picker.component.ts:137](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/general/date-picker/date-picker.component.ts#lines-137)

___

### getContentModel

▸ `Protected` **getContentModel**(): [`DatePickerComponentModel`](../interfaces/Models.DatePickerComponentModel.md)

#### Returns

[`DatePickerComponentModel`](../interfaces/Models.DatePickerComponentModel.md)

#### Overrides

BaseComponent.getContentModel

#### Defined in

[src/components/general/date-picker/date-picker.component.ts:182](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/general/date-picker/date-picker.component.ts#lines-182)

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

#### Overrides

[BaseComponent](Components.BaseComponent.md).[registerHelpers](Components.BaseComponent.md#registerhelpers)

#### Defined in

[src/components/general/date-picker/date-picker.component.ts:170](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/general/date-picker/date-picker.component.ts#lines-170)

___

### render

▸ **render**(): `void`

Binds [contentModel](Components.DatePickerComponent.md#contentmodel) to the Handlebars template and renders the resulting HTML content.

#### Returns

`void`

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[render](Components.BaseComponent.md#render)

#### Defined in

[src/components/base.component.ts:171](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-171)

___

### renderContent

▸ `Protected` **renderContent**(): `boolean`

Determines whether the [data](Components.DatePickerComponent.md#data) meets the necessary conditions to perform data binding and render content.

#### Returns

`boolean`

Whether the component should be rendered. If `false`, the component will have empty contents and be set to `display: none;`.

#### Inherited from

[BaseComponent](Components.BaseComponent.md).[renderContent](Components.BaseComponent.md#rendercontent)

#### Defined in

[src/components/base.component.ts:240](https://bitbucket.org/bridgelinedigital/frontend-handlebars-ui/src/db3ebfe/src/components/base.component.ts#lines-240)
