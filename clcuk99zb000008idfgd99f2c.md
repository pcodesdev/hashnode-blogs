# Responding to events and updating the screen in reactjs

## **Responding to events**

In ReactJS, you can respond to events by defining event handlers, which are functions that are called in response to specific events. You can attach event handlers to elements by using the `on[event]` attribute in JSX, where `[event]` is the name of the event you want to handle. For example, you can attach a click event handler to a button like this:

```javascript
import React from "react";
import "./mybutton.css";

function MyButton() {
  //handle click function
  function handleClick() {
    alert("You clicked me!");
  }
  return (
      <div className="mybutton">
          {/* Any time the button is clicked a popup window appears with the message "you clicked me" */}
      <button
        onClick={handleClick}
        className="main-btn"
        style={{ margin: "3rem auto", padding: "0.5rem" }}
      >
        Click Here
      </button>{" "}
      {/* inline styles */}
    </div>
  );
}

export default MyButton;
```

Notice how `onClick={handleClick}` has no parentheses at the end! Do not *call* the event handler function: you only need to *pass it down*. React will call your event handler when the user clicks the button.

## **Updating the screen**

Often, you’ll want your component to “remember” some information and display it. For example, maybe you want to count the number of times a button is clicked. To do this, add *state* to your component.

First, import [`useState`](https://beta.reactjs.org/reference/react/useState) from React:

```javascript
import { useState } from 'react';
```

Now you can declare a *state variable* inside your component:

```javascript
function MyButton() {  const [count, setCount] = useState(0);
```

You will get two things from `useState`: the current state (`count`), and the function that lets you update it (`setCount`). You can give them any names, but the convention is to call them like `[something, setSomething]`.

The first time the button is displayed, `count` will be `0` because you passed `0` to `useState()`. When you want to change state, call `setCount()` and pass the new value to it. Clicking this button will increment the counter:

```javascript
import React, { useState } from "react";
function MyButton() {  
const [count, setCount] = useState(0);  //setting the state count to 0
function handleClick() {    
setCount(count + 1);  }  
return (    
<button onClick={handleClick}>  Clicked {count} times    </button> // passing state to the handleClick function and calling it 
);}
```

React will call your component function again. This time, `count` will be `1`. Then it will be `2`. And so on.