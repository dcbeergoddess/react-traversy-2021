# React JS Crash Course 2021
Follow Along with [Traversy Media React Crash Course 2021](https://www.youtube.com/watch?v=w7ejDZ8SWv8)

## What is React?
* React is a library for building user interfaces
* React runs on the client as a SPA(Single Page App), but can be used to build full stack apps by communicating with a server/API (eg. MERN stack)
* React is often refereed to as a front-ent "framework" because it is capable and directly comparable to a framework such as Angular or Vue

## Why Would You Use React

* MVC (Model View Controller) --> Structure the "view" layer of your application
* Reusable components with their own state
* JSX - Dynamic markup --> write dynamic HTML (JS formatted like HTML)
* Interactive UIs with Virtual DOM --> Document Object Model --> Update parts of page without reloading it
* Performance & Testing --> All Data immutable (can't mutate directly), easier to work on teams
* Very Popular in the Industry

## UI Components
* When using React, think of your UI as a bunch of separate components

## Components: Functions vs. Classes
![Functions vs. Classes](assets/react.png)
* Focus on Functions with Hooks
* JSX (JavaScript Syntax Extension) - syntactic sugar
* Can pass in "props" --> essentially attributes

## Working with State
* Components can have "state" which is an object that determines how a component renders and behaves (ex: collapsible menu, list of tasks, any data you bring into your compnents)
* **"App"** or **"global"** state refers to state that is available to the entire UI, not just a single component (share data with multiple components when global state gets complicated --> Redux (3rd Party Manager) or Context API)
* Prior to React 16.8, we had to use class based components to use state. Now we can use functional component with **HOOKS** (functional components used to be dumb components)

## React Hooks
React Hooks are functions that le us hook into the React state and lifecyle features from function components
- `useState` --> Returns a stateful value and a function to update it
- `useEffect` --> Perform side effects in function components --> when making HTTP requests
- `useContext`, `useReducer`, `useRef` --> Beyond the scope of this course
- You can also create your own Custom Hooks

## Create a New React App
* [Documentation](https://reactjs.org/docs/create-a-new-react-app.html)
* [React Developer Tools Chrome Extension](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi?hl=en)
* To start up new Application

```js
  npx create-react-app my-app
  cd my-app
  npm start
```
* [GITHUB REPO OF REACT TASK TRACKER APP](https://github.com/dcbeergoddess/react-tast-tracker)
* Here's a look at what you get, in the package.json you have some dependencies --> if in react native you would see `react-native` instead of `react-dom`
![new react app](assets/react1.png)
* Look of the index.js and index.html --> `App` is the Route Component (every component we create will end up in main App component)
![index.js and index.html](assets/react2.png)
* Use index.html to add Bootstrap CDN, etc.
* In `App.js` --> we see function component with JSX(looks like HTML)
![React App.js](assets/react3.png)
- instead of `for` attribute use `htmlFor`
- instead of `class` attribute use `className`
- dynamic --> can have JS expressions and variables `src={logo}`
- Clean up some files and delete what is in the div
- CAN ONLY HAVE ONE PARENT ELEMENT, CAN NOT ADD NEW H2 AFTER THE DIV
![Clean up App.js](assets/react4.png)
- if you didn't want a div inside a div you can use fragments `<>` to surround the two headers. 
![html in dev console](assets/react5.png)
- You can create variables, ternary operators, ect. and use with JSX
![JSX EXAMPLES](assets/react6.png)

## CREATE COMPONENTS
* GREAT VS CODE EXTENSION
```js
Name: ES7 React/Redux/GraphQL/React-Native snippets
Id: dsznajder.es7-react-js-snippets
Description: Simple extensions for React, Redux and Graphql in JS/TS with ES7 syntax
Version: 3.1.1
Publisher: dsznajder
VS Marketplace Link: https://marketplace.visualstudio.com/items?itemName=dsznajder.es7-react-js-snippets
```
- `rcc` - class based component
- `rce` - class component and export at bottom
- `rafce` - arrow function that exports at bottom
* Creates boilerplate of a function component --> DO NOT NEED IMPORT REACT ANYMORE (unless you are creating a class)
![function boilerplate](assets/react7.png)
```js
//EXAMPLE OF USING A CLASS
import React, { Component } from 'react'

export class Header extends Component {
  render() {
    return (
      <div>
        
      </div>
    )
  }
}

export default Header
```
* import component into `App.js`
![import component](assets/react8.png)
```js
//EXAMPLE OF IMPORTING A CLASS
import React from 'react'
import Header from './components/Header'

class App extends React.Component {
  render() {
    return <h1>Hello from a class</h1>
  }
} 
```

## Pass in Component `Props`
* How to pass in props and use them
![pass in title props](assets/props.png)
* can set default props if none is passed in
![default props](assets/props1.png)
* can destructure props 
![destructure props](assets/props2.png)
* There are also Prop Types --> make code more robust --> use `impt` with extension --> you can also use Typescript with React
* Use and pass in number instead of string for title, will render with warnings in the console
![setting prop types](assets/props3.png)
* Set `PropType` to be required
![require prop types](assets/props4.png)

