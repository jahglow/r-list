# r-list
An element to wrap around Reportal WYSIWYG List element to restyle its contents according to Material Design spec.
One doesn't need to provide type of the list element, because it's calculated automatically.
These are Polymer polyfills which hide original Reportal markup and reflect entered data into respective Reportal forms.
The multiselect list is a dropdown with checkboxes on the side to denote selected options.

Example:

```html
    <r-list label="Some title">
      <confirmit:wysiwygcomponent type="ReportalDropDown" id="39860b07-abd2-4972-b62f-d0d00900fb63" />
    </r-list>
```    

You may OPTIONALLY specify a label text that will show above the list component.
It can be done via attribute label="Some text label" on <r-list> tag or via a span inside tag's content (see initialisation example above).
The latter is useful when building multilingual report and one needs to pass the title via Language Text element.

Example:

```html
    <r-list>
      <span id="label">Some title</span>
      <confirmit:wysiwygcomponent type="ReportalDropDown" id="39860b07-abd2-4972-b62f-d0d00900fb63" />
    </r-list>
```


### Styling

The following custom properties and mixins are also available for styling:

Custom property | Description | Default
----------------|-------------|----------
`--r-list` | A mixin that is applied to the element host | `{}`
`--r-list-checkbox` | A mixin that is applied to the checkbox | `{}`
`--r-list-radio-group` | A mixin that is applied to the  radio group | `{}`
`--r-list-radio-button` | A mixin that is applied to the radio button | `{}`
`--r-list-label` | A mixin that is applied to the Custom label | `{}`
`--r-list-dropdown` | A mixin that is applied to the the dropdown | `{}`

You can also use any of the `paper-input-container` and `paper-menu-button`
style mixins and custom properties to style the internal input and menu button
respectively.