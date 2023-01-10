# Creating and nesting react components

## React component

A React component is a piece of code that represents a specific part of a user interface in a React application. It is a reusable, modular piece of code that can be easily integrated into other parts of the application. Components can be used to create elements like buttons, forms, and other interactive elements, and they can also be used to create entire pages or sections of an application. Components are defined using JavaScript and are typically rendered using JSX, a syntax extension for JavaScript that allows developers to write HTML-like elements in their code.

> React apps are made out of *components*. A component is a piece of the UI (user interface) that has its own logic and appearance. A component can be as small as a button, or as large as an entire page.

React components are JavaScript functions that return markup:

```javascript
import React from 'react';

function MyButton() {
    return (
        <div>
            <button>Click Here</button>
        </div>
    );
}

export default MyButton;
```

output:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1673339551074/68aec01c-7ed8-42cd-9011-47c377e95246.png align="center")

Now that you’ve declared `MyButton`, you can nest it into another component:

## Nested component

> ```javascript
> import React from 'react';
> import MyButton from './MyButton'; // Imported MyButton component
> 
> function MyApp() {
>     return (
>         <div>
>             <h1>Welcome to My App</h1>
>             <MyButton /> {/* Nested MyButton component */}
>         </div>
>     );
> }
> 
> export default MyApp;
> ```

Output:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1673339705379/935ad6c2-b24d-40f9-9c6f-3f1b20a61b9f.png align="center")

Notice that <mark>&lt;MyButton /&gt;</mark> starts with a capital letter. That’s how you know it’s a React component. React component names must always start with a capital letter, while HTML tags must be lowercase.

## **Writing markup with JSX**

JSX is a syntax extension for JavaScript that allows developers to write markup within their JavaScript code. It is commonly used in React, a JavaScript library for building user interfaces.

In JSX, elements are written as HTML-like tags, but they are actually JavaScript objects.

JSX also allows for the use of JavaScript expressions within the markup, by wrapping them in curly braces {}. For example, to insert a variable in a JSX element, it would be written as:

```javascript
const name = "John";

<div>Hello, {name}!</div>
```

JSX allows for more seamless integration of markup and logic in React applications, allowing for more efficient and organized code. It ultimately helps the developer to understand the structure of a component better as they can see both its logic and layout at the same time.

## **Adding styles**

There are a few ways to add styles in React:

1. <mark>Inline Styles</mark>: You can add styles directly to an element using the `style` attribute and passing in an object with CSS properties and their values.
    

```javascript
<div style={{color: 'red', fontSize: '20px'}}>Hello, World!</div>
```

1. <mark>CSS Stylesheets:</mark> You can create a CSS stylesheet and import it into your React component.
    

```javascript
import './styles.css';

function MyComponent() {
  return <div className="my-style">Hello, World!</div>;
}
```

1. <mark>CSS Modules</mark>: CSS modules are a way of scoping CSS styles to a specific component. This means that the styles defined in a CSS module will only affect the component that imports it. To use CSS modules, you need to configure webpack and install the `css-loader` package.
    

```javascript
import styles from './styles.module.css';

function MyComponent() {
  return <div className={styles.myStyle}>Hello, World!</div>;
}
```

1. <mark>Styled Components</mark>: Styled component is a library that allows you to create React components with a specific set of styles. This allows you to add styles to a component while also keeping the component's logic and layout together.
    

```javascript
import styled from 'styled-components';

const MyStyledDiv = styled.div`
  color: red;
  font-size: 20px;
`;

function MyComponent() {
  return <MyStyledDiv>Hello, World!</MyStyledDiv>;
}
```

It is important to note that the choice of how to style your component will depend on the specific needs of the project and the personal preference of the developer.

For this series, I will be using **inline styles and CSS stylesheet**

## Conclusion

In conclusion, React components are an essential part of building modern web applications. They provide a way to organize and structure code, making it easier to understand and maintain. Components can be reused throughout the application, reducing code duplication and making it more efficient.