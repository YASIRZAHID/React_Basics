# React_Basics
React notes for future referencing

#React Basics
**Components are standalone parts od UI**
Famous because it streamlines the process of creating and composing components
**State is simply all the values of all the variable your app is working with at any instant**
Usability

1. Styling of react apps.
2. Event Handling.
3. Navigation and assets

Advantages
1. Rich-user interfaces
2. Speed
3. Scalability and flexibility

```
npm init react-app your-app-name
```

```
npm init react-app .
```


```
cd your-app-name
```

```
npm start
```
## Component Based Architecture
Practice of building software based on reusable components of code.
**Each component consists of well-defined functionality that can be inserted into an application without requiring modifcation of other components**

**React manpulates the virtual DOM when necessary to update the browser DOM minizing the updates**

Every react component must reneder atleast one component called **Root Component**

Javascript XML JSX (Combination of HTML and Javascript)
A react component won,t render untill its used as an JSX element.
First letter of component name must be  **Capitalized**
First letter of function name must be  **Capitalized**
Capitalized name - treated as jsx 
Non-capitalized - treated as normal HTML component

**Props must never modify its own prompts**
**Propa enable only Parent to Child oneway communication**

 createElement function receives three arguments:
 
The wrapping element to render. 

A null value (which is there to show an absence of an expected JavaScript object value). 

The inner content that will go inside the wrapping element. 

Easy understanding...
```
React.createElement(
  type,
  [props],
  [...children]
)
```

### Functional Components


### Class Components

## Folder Structure

## Using Properties (props)
Sending props
```
//app.js
import Heading from "./Heading";

function App() {
  return (
    <div className="App">
      <Heading firstName="Bob" />
      <Heading firstName="Yasir" />
    </div>
  );
}

export default App;
```

Receiving props
```
function Heading(props) {
    return (
        <h1>Hello, {props.firstName}</h1>
    )
}

export default Heading;
```

```
function Bag(props) {
    const bag = {
        padding: "20px",
        border: "1px solid gray",
        background: "#fff",
        margin: "20px 0"
    }
    return (
        <div style={bag}>
            {props.children}
        </div>
    )
}
export default Bag
```

--Manifest.JSON contains metadata for devices
--Index.css contains styles for entire app
--App.css contains styles for app.js
-- app.test.js , setuptests.js , reportwebvitals.js are for app testing
-- index.js is main file here
--use filname sequence to import e.g ./
