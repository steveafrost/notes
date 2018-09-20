# Complete Intro to React

## Objective

The objective of these notes & lecture viewing is to resolidify the basics of React and learn the new features from 16.0

## Resources

-   https://frontendmasters.com/courses/complete-react-v4

## Notes

-   React.js is the API layer
-   React DOM is the rendering layer

    -   There are also renderers for mobile, AR/VR, and IOT

-   A design paradigm of components made up of components. Therefore, each React app is one large component made up of smaller components
-   Creating a component without the current syntactical sugar looks like the snippet below. Arguments as listed:
    1. HTML element - `<div>`, `<h1>`, `<p>`, etc
    2. Attributes for that element - `class="some-class"`, `id="some-id`, etc
    3. Content of that element
-   Once a component is created, it must be rendered to a HTML node

_Create a Component_

```javascript
// component with one child
const App = () => {
    return React.createElement(
        'div',
        {},
        React.createElement('h1', {}, 'Text here')
    );
};

// component with multiple children
const Pet = () => {
    return React.createElement('div', {}, [
        React.createElement('h1', {} 'Enzo'),
        React.createElement('h2', {}, 'Dog'),
        React.createElement('h3', {}, 'Samoyed'),
    ])
}
```

_Render a Component_

```javascript
ReactDOM.render(React.createElement(App), document.getElementById('root'));
```

-   `createElement` when rendering a component creates an instance of that class. In this case, the class is `App`.

#### Class vs Function Component

```javascript
class App extends React.Compnent {
    render() {
        return React.createElement('h1', {}, []);
    }
}

// vs

const App = () => {
    return React.createElement('h1', {}, []);
};
```

-   Functional components are also known as stateless components. These are usually used when you don't need all the bells and whistles of React such as state and lifecycle methods.
