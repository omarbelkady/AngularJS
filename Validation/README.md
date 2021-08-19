## Validation 

#### CSS Validation

```css
    /*If The User's Input Is Not Correct set 
    the background to Red
    
    To give your user a great exp always make sure to set background-red 
    to tell the User he made an error in Input*/
    input.ng-touched.ng-invalid {
        background-color:red;
    }

    /*If The User Tabs Out Or If The User
     Enters Something Correctly set the background to Green */
    input.ng-touched.ng-valid {
        background-color:green;
    }
```


#### CSS Validation Class In Angular

- ng-dirty => Set this CSS class whenever the user changes the details in a form field
- ng-invalid => Set this CSS class when the user input is invalid
- ng-pristine => Set this CSS class when the user has not interracted with this yet
- ng-submitted => Set this CSS class when the user has clicked on the submit button within a form
- ng-touched => Set this CSS class when the user has tabbed out from the input field within a form
- ng-untouched => Set this CSS class when the user has not tabbed out from the input field within a form
- ng-valid => Set this CSS class when the user input is valid