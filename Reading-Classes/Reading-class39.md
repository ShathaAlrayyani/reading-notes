# React

## What is React context?

React context allows us to pass down and use (consume) data in whatever component we need in our React app without using
props.

## When should you use React context?

React context is great when you are passing data that can be used in any component in your application.

These types of data include:

- Theme data (like dark or light mode)
- User data (the currently authenticated user)
- Location-specific data (like user language or locale)

## What problems does React context solve?

React context helps us avoid the problem of props drilling.

Props drilling is a term to describe when you pass props down multiple levels to a nested component, through components
that don't need it.

## How do I use React context?

Context is an API that is built into React, starting from React version 16.

This means that we can create and use context directly by importing React in any React project.

There are four steps to using React context:

- Create context using the createContext method.
- Take your created context and wrap the context provider around your component tree.
- Put any value you like on your context provider using the value prop.
- Read that value within any component by using the context consumer.

## What is the useContext hook?

Another way of consuming context became available in React 16.8 with the arrival of React hooks. We can now consume
context with the useContext hook.

Instead of using render props, we can pass the entire context object to React.useContext() to consume context at the top
of our component.








