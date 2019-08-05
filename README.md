# react-picky
We are Implementing ok and cancel button and search customization.
This approach is fine for smaller lists. When you have options for 20, 30, 100+ options that the use can select, it becomes unmanigable.

What Picky is:
Picky provides a medium amount of flexibility, you can custom render: Options, List (useful for creating a virtualized menu), and SelectAll. Any further customisation and it's a little out of scope for Picky. It was built with a common pattern in mind so you can get up and running with little-to-no work. If you need Picky to be more flexible, I'm happy to take a PR if it would benefit the rest of the community.

Peer Dependencies:
 "prop-types": "^15.6.0",
 "react": "^16.5.0",
 "react-dom": "^16.5.0"
Installation:
  npm install --save react-picky
  # or
  yarn add react-picky
  
  Prop descriptions:
placeholder - Default message when no items are selected.
value - The selected value(s), array if multiple is true. Not needed if using as an uncontolled component
numberDisplayed - Then number of selected options displayed until it turns into '(selected count) selected'.
multiple - Set to true for a multiselect, defaults to false.
options - Array of possible options.
onChange - Called whenever selected value(s) have changed. Pass the selected value back into value.
open - Can open or close the dropdown manually. Defaults to false.
includeSelectAll - If set to true will add a Select All checkbox at the top of the list.
includeFilter - If set to true will add an input at the top of the dropdown for filtering the results.
filterDebounce - Debounce timeout, used to limit the rate the internal onFilterChange gets called. Defaults to 150ms.
dropdownHeight - The height of the dropdown. Defaults to 300px.
onFiltered - Called after a filter has been done with the filtered options.
onOpen - Called after the dropdown has opened.
onClose - Called after the dropdown has closed.
valueKey - If supplying an array of objects as options, this is required. It's used to identify which property on the object is the value.
labelKey - If supplying an array of objects as options, this is required. It's used to identify which property on the object is the label.
render - Used for custom rendering of items in the dropdown. More info below.
tabIndex - Pass tabIndex to component for accessibility. Defaults to 0
keepOpen - Default true. Single selects close automatically when selecting a value unless this is set to true.
manySelectedPlaceholder - Default "%s selected" where %s is the number of items selected. This gets used when the number if items selected is more than the numberDisplayed prop and when all options are not selected.
allSelectedPlaceholder - Default "%s selected" where %s is the number of items selected. This gets used when all options are selected.
selectAllText - Default "Select all", use this to override "Select all" text from top of dropdown when included with includeSelectAll.
renderSelectAll - Used for rendering a custom select all
defaultFocusFilter - If set to true, will focus the filter by default when opened.
renderList - Render prop for whole list, you can use this to add virtualization/windowing if necessary
filterPlaceholder - Override the filter placeholder. Defaults to 'Filter...'
getFilterValue - Will provide the input value of filter to the picky dropdown, so that if we have a larger list of options then we can only supply the matching options based on this value.
caseSensitiveFilter - If true options will be returned when they match case
buttonProps - Additional props to apply the the button component, useful for supplying class names.

isSelected - boolean - true if item is selected. Use this for styling accordingly.
item - object | number | string - The item to render.
labelKey - Used to get the label if item is an object
valueKey - Used to get the value if item is an object, good for keys.
selectValue - function(item) - Selects the item on click
multiple - boolean - Indicates if is a multiselect.

