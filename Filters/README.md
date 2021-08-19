## Filters

- Filters are used to format the data that is outputted from an expression in order for it to be displayed to the user
- Used in:
    - view templates
    - controllers
    - services

### How To Apply Filters To View Templates Syntax:

- {{ expression | filter }}

##### Applying A Filters to The Result of Another Filter i.e. Filter Chaining

- {{ expression | filter1 | filter2 | filter3 }}


### Filters Can Have Arguments passed to them

- {{ expression | filter1: arg1 : arg2 : arg3 : argn}}


### Filter Names and What They Do

- uppercase => Converts some text to uppercase
- lowercase => Converts some text to lowercase
- currency => Format the text to currency
- filter => Filter the array depending on some criteria
- orderby => Order the array depending on some criteria
