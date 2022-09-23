 # Here is the answers of the question asked in the assignment and the updated codes are in the index.js file

# Explain what the simple list component does?
Answer-->: This simple list component basically renders the items present in the array in the form of lists.Further the click handler is assigned to each and every list which changes the value of the "setSelected" state .While displaying the list of items it sets the background color of the items dynamically .If any list item is clicked then its background color is changed to green otherwise their default color will be red.This list uses different hooks namely useState,useEffect,memo(for memoization purpose) and the most importantly the ['prop-types'] which is used to validate the data types of the default props present or the props passed to any other component while rendering.


# What problems / warnings are there with the code?
Answer--->: There are several warnings / problems which need to be fixed are as follows :

* ["Error-01"]:-> prop_types__WEBPACK_IMPORTED_MODULE_2___default(...).shapeOf is not a function 
         (solution):-> In place of shapeOf we should use shape() only.
 

* ["Error-02"]:->Calling PropTypes validators directly is not supported by the `prop-types` package. Use `PropTypes.checkPropTypes()` to call them.
     (solution):-> In place of PropTypes.array() we should use PropTypes.arrayOf().


* ["Error"]:-> cannot read properties of null (reading map).
    (solution):->  Instead of using {items.map()} use {items && items.map()} .


* ["Error-03"]:-> setSelectedState is not a function.
    (solution)->  Here we are destructuring the returned value of useState in wrong way ,we are treating the current state as a function. Instead we should use the function returned from usedState to set the state.


* ["warning"]:-> Each child in the list should have unique key prop.
    (solution)->  Set the key attribute to all the items rendered through map.     
  

* ["warning"]:-> Each child in the list should have unique key prop.
    (solution)->  Set the key attribute to all the items rendered through map.      


* ["warning"]:-> Failed prop type: Invalid prop `isSelected` of type `function` supplied to   `WrappedSingleListItem`, expected `boolean`
    (solution)->  set only the boolean values as true/false to the `isSelected` prop.


* ["Warning]:-> Cannot update a component (`WrappedListComponent`) while rendering a     different component (`WrappedSingleListItem`).
    