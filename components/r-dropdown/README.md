# r-dropdown

[DEMO and API Docs](http://jahglow.github.io/r-dropdown)

Material design: [Dropdown menus](https://www.google.com/design/spec/components/buttons.html#buttons-dropdown-buttons)

`r-dropdown` is similar to a native browser select element.
`r-dropdown` works with selectable content. The currently selected
item is displayed in the control. If no item is selected, the `label` is
displayed instead.

Besides common functionality of `paper-dropdown-menu` r-dropdown can be multiselectable (if `multi` is passed to the `r-dropdown` and `paper-listbox`)
 and display all selected labels in the control as a comma-separated list. There is an option to replace the list of labels with a custom title, e.g. "3 items".
 The dropdown stays open (doesn't close on iron-selected) if it's `multi`.

The child element with the class `dropdown-content` will be used as the dropdown
menu. It could be a `paper-menu` or element that triggers `iron-select` when
selecting its children.

Example of a multi-select dropdown:
```html
    <r-dropdown label="Your favourite pastry" multi>
      <paper-listbox class="dropdown-content" attr-for-selected="selected" multi>
        <paper-icon-item><iron-icon icon="check"></iron-icon>Croissant</paper-item>
        <paper-icon-item><iron-icon icon="check"></iron-icon>Donut</paper-item>
        <paper-icon-item><iron-icon icon="check"></iron-icon>Financier</paper-item>
        <paper-icon-item><iron-icon icon="check"></iron-icon>Madeleine</paper-item>
      </paper-listbox>
    </r-dropdown>
```
This example renders a dropdown menu with 4 options.

Similarly to using `iron-select`, `iron-deselect` events will cause the
current selection of the `r-dropdown` to be cleared.

### Styling

The following custom properties and mixins are also available for styling:

Custom property | Description | Default
----------------|-------------|----------
`--r-dropdown` | A mixin that is applied to the element host | `{}`
`--r-dropdown-disabled` | A mixin that is applied to the element host when disabled | `{}`
`--r-dropdown-ripple` | A mixin that is applied to the internal ripple | `{}`
`--r-dropdown-button` | A mixin that is applied to the internal menu button | `{}`
`--r-dropdown-input` | A mixin that is applied to the internal paper input | `{}`
`--r-dropdown-icon` | A mixin that is applied to the internal icon | `{}`

You can also use any of the `paper-input-container` and `paper-menu-button`
style mixins and custom properties to style the internal input and menu button
respectively.
