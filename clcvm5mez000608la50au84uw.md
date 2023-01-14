# Using hooks and sharing data between components using props in reactjs

## **Using hooks**

In React, hooks are functions that allow you to use state and other React features in functional components, instead of having to use class components. There are several built-in hooks, such as `useState` and `useEffect`, that can be used to add functionality to your functional components.

`useState` is a hook that allows you to add state to your functional component. It takes an initial value as an argument, and returns an array with two items: the current state value and a function to update it.

```javascript
const [count, setCount] = useState(0);
```

`useEffect` is a hook that allows you to run side effects in your functional component, such as fetching data or updating the DOM. It takes two arguments: a callback function to run, and an array of dependencies.

```javascript
useEffect(() => {
    console.log('Effect ran');
}, [count]);
```

You can also create your own custom hooks to share logic between different components.

```javascript
import { useState, useEffect } from 'react';

function useFriendStatus(friendID) {
  const [isOnline, setIsOnline] = useState(null);

  useEffect(() => {
    function handleStatusChange(status) {
      setIsOnline(status.isOnline);
    }

    ChatAPI.subscribeToFriendStatus(friendID, handleStatusChange);
    return () => {
      ChatAPI.unsubscribeFromFriendStatus(friendID, handleStatusChange);
    };
  }, [friendID]);

  return isOnline;
}
```

Hooks allow you to write more reusable and composable components and make it easier to manage state and side effects in your application.

## **Sharing data between components**

Often you’ll need components to *share data and always update together*. For example:

To make two components named `MyButton` display the same `count` and update together, you need to move the state from the individual buttons “upwards” to the closest component containing all of them. That is their parent component

In this example, it is `MyApp`:

![Diagram showing a tree of three components, one parent labeled MyApp and two children labeled MyButton. MyApp contains a count value of zero which is passed down to both of the MyButton components, which also show value zero.](https://beta.reactjs.org/_next/image?url=%2Fimages%2Fdocs%2Fdiagrams%2Fsharing_data_parent.png&w=828&q=75 align="left")

Initially, `MyApp`’s `count` state is `0` and is passed down to both children

![The same diagram as the previous, with the count of the parent MyApp component highlighted indicating a click with the value incremented to one. The flow to both of the children MyButton components is also highlighted, and the count value in each child is set to one indicating the value was passed down.](https://beta.reactjs.org/_next/image?url=%2Fimages%2Fdocs%2Fdiagrams%2Fsharing_data_parent_clicked.png&w=828&q=75 align="left")

On click, `MyApp` updates its `count` state to `1` and passes it down to both children

Now when you click either button, the `count` in `MyApp` will change, which will change both of the counts in `MyButton`. Here’s how you can express this in code.

Note: Any information passed down from a parent component to a child component it's called a `prop.`

MyApp.js

```javascript
import React, { useState } from "react";
import MyButton from "../mybutton/MyButton";
import "./myapp.css"; // Imported css stylesheet

function MyApp() {
  const [count, setCount] = useState(0);

  function handleClick() {
    setCount(count + 1);
  }
  return (
    <div className="header">
      <h1>Counters that update separately</h1>
      <MyButton count={count} onClick={handleClick} />
      <MyButton count={count} onClick={handleClick} />
    </div>
  );
}

export default MyApp;
```

MyButton.js

```javascript
import React from "react";

function MyButton({ count, onClick }) { // used two props: count, onClick
  return (
    <div className="mybutton">
      {/* Any time the button is clicked the count value increases by 1" */}
      <button
        onClick={onClick}
        className="main-btn"
        style={{ margin: "3rem auto", padding: "0.5rem" }}
      >
        Clicked {count} times
      </button>
      {/* inline styles */}
    </div>
  );
}

export default MyButton;
```

# Conclusion

Hooks and props are two important concepts in React.js that allow developers to share data and state between components. Hooks provide a way to use state and other React features in functional components, whereas props allow components to receive data from their parent component. Together, these features allow for greater flexibility and reusability in building React applications.

# Weekly podcast

%[https://podcasts.google.com/feed/aHR0cHM6Ly9mZWVkcy50cmFuc2lzdG9yLmZtL3NjcmltYmE/episode/YmRiNjEyM2ItZGE1Yy00OGVjLTk3NDgtODgzYTk3OTI4OTgz?sa=X&ved=0CAUQkfYCahcKEwiInKDnwMb8AhUAAAAAHQAAAAAQLA]