# Displaying data and conditional rendering in reactjs

## **Displaying data**

There are several ways to display data in ReactJS, some of which include:

1. <mark>Using props</mark>: Props are a way to pass data from a parent component to a child component. For example, if a parent component has an array of data that needs to be displayed in a child component, it can pass that data as a prop to the child component.
    
2. <mark>Using state</mark>: State is a way to store data that can change over time. For example, if a component needs to display data that is retrieved from an API call, it can store that data in its state and update the component's view when the data is received.
    
3. <mark>Using hooks:</mark> Hooks are a way to use state and other features of React components in functional components. For example, the useState hook can be used to store data in a functional component, and the useEffect hook can be used to retrieve data from an API and update the component's view.
    
4. <mark>Using a library</mark>: Several libraries can be used to display data in React, such as react-table, react-virtualized, and react-grid-layout. These libraries provide additional functionality for displaying data in a specific format, such as tables, grids, or lists.
    

JSX lets you put markup into JavaScript. Curly braces let you <mark>“escape back”</mark> into JavaScript so that you can embed some variable from your code and display it to the user. For example, this will display [`user.name`](http://user.name):

```javascript
return (  <h1>    {user.name}  </h1>);
```

You can also “escape into JavaScript” from JSX attributes, but you have to use curly braces *instead of* quotes. For example, `className="avatar"` passes the `"avatar"` string as the CSS class, but `src={user.imageUrl}` reads the JavaScript `user.imageUrl` variable value, and then passes that value as the `src` attribute:

```javascript
return (  <img    className="avatar"    src={user.imageUrl}  />);
```

You can put more complex expressions inside the JSX curly braces too, for example

```javascript
import React from "react";
import "./myself.css";

const user = {
  name: "Hedy Lamarr",
  age: 30,
  gender: "female",
  imageUrl: "https://i.imgur.com/yXOvdOSs.jpg",
  imageSize: 120,
};

function MySelf() {
  return (
    <div className="myself">
      <h1>{user.name}</h1>
      <p>{user.age}</p>
      <p>{user.gender}</p>
      <img
        className="avatar"
        src={user.imageUrl}
        alt={"Photo of " + user.name}
      />
    </div>
  );
}

export default MySelf;
```

## **Conditional rendering**

In React, you can use JavaScript expressions to conditionally render elements by using the ternary operator or the `if` statement.

The ternary operator is a shorthand for an `if` statement, and can be used to conditionally render a component based on a single condition. The basic syntax for using the ternary operator to conditionally render a component is as follows:

```javascript
{condition ? <ComponentToRenderIfTrue /> : <ComponentToRenderIfFalse />}
```

For example, you can use a ternary operator to conditionally render a message based on a `isLoggedIn` state:

```javascript
{isLoggedIn ? <WelcomeMessage /> : <LoginPrompt />}
```

You can also use an `if` statement to conditionally render a component. This approach allows you to check multiple conditions, or to use more complex logic to determine whether a component should be rendered. Here's an example of how you might use an `if` statement to conditionally render a component based on a `isLoggedIn` state:

```javascript
{
  if(isLoggedIn) {
    return <WelcomeMessage />;
  } else {
    return <LoginPrompt />;
  }
}
```

You can also use short circuit evaluation to return components based on conditions, by exploiting the logical OR operator:

```javascript
Copy code{isLoggedIn && <WelcomeMessage />}
```

In this example, if `isLoggedIn` is true, the component `<WelcomeMessage />` is rendered, if not, nothing is rendered.

From the previous components, I have rendered the myApp component if `isLoggedIn` is true:

```javascript
import React from "react";
import MyButton from "../mybutton/MyButton";
import MyApp from "../myapp/MyApp";

function conditionalRender() {
  let isLoggedIn = true;
  return <div>{isLoggedIn ? <MyApp /> : <MyButton />}</div>; //Here is the example
}

export default conditionalRender;
```

## **Rendering lists**

In React, you can use the `map()` function to render a list of components based on an array of data. The `map()` the function takes an array and returns a new array with the results of calling a provided function on every element in the array.

Example:

```javascript
import React from "react";
import "./friendList.css";

function MyFriendList() {
  const friends = [
    { name: "Peter", age: 25, id: 1 },
    { name: "james", age: 34, id: 2 },
    { name: "Hannah", age: 70, id: 3 },
  ]; // arrray list
  return (
    <div className="friend__list">
      {friends.map((friend) => (
        <ul>
          <li key={friend.id}>{friend.name}</li>
          <p>{friend.age}</p>
        </ul>
      ))}
    </div> {/* maped list */}
  );
}

export default MyFriendList;
```