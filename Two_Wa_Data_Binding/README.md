## Two Data Binding In Angular

- Enabling My Angular application to share data in between its components
- Combines Property Binding with Event Binding


### What can I do with it?

- It enables me to know when events in App take place and update my vals when this event takes place
- When updating my values since it is two-way I  update them in the parent && child components at the same time

### Syntax:

- Use parentheses and brackets when performing two-way data binding for property binding
- parentheses for event binding
- brackets for property binding

### Event Binding

- Enables me to listen to and reply to user actions e.g. user keystokes, mouse movements, 
click events and touch events
- i.e. listen to an event which changes the element

#### Syntax:

```js
<button (click)="onSave()">Save</button>
//(click) is the event I am targetting onSave is the template statment
```


### Property Binding

- The process of setting an property to an element
- When binding to a property use square brackets
- By using square brackets I am identifying it as a target property
- The target property is the property in the DOM you want to give it a value
- Below for example I am binding the src to img tag property

```js
<img [src] = "urlOfImage">
```