# React

## Conditional Rendering

In React, you can create distinct components that encapsulate behavior you need. Then, you can render only some of them,
depending on the state of your application.

Conditional rendering in React works the same way conditions work in JavaScript. Use JavaScript operators like if or the
conditional operator to create elements representing the current state, and let React update the UI to match them.

### Element Variables
You can use variables to store elements. This can help you conditionally render a part of the component while the rest
of the output doesn’t change.

### Inline If with Logical && Operator
You may embed expressions in JSX by wrapping them in curly braces. This includes the JavaScript logical && operator.

### Inline If-Else with Conditional Operator
Another method for conditionally rendering elements inline is to use the JavaScript conditional operator condition ? true : false.

### Preventing Component from Rendering
In rare cases you might want a component to hide itself even though it was rendered by another component. To do this return null instead of its render output.









