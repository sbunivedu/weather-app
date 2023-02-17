# The Weather App

Please following the instructions in the book chapter to build this app.

## Get started
You can build on this repo after install the required node packages with "npm install".
You can also create a new project as follows:
```
npx create-expo-app --template
```
and choose the "blank" template.

```
cd weather
npx expo start
```

You should see "Open cup App.js to start working on your app!"

## Notes

In order to use a Component, it needs to be imported using the "import" statements.

A custom component can be a [function component](https://www.reactnative.express/react/components/function_components) or a [class component](https://www.reactnative.express/react/components/class_components).

A function component receives `props` via the input parameter. A class component can access its `props` using `this.props`. The keyword `this` refers to the class component instance.

You can lookup React Native built-in Core Components in [React Native API specifications](https://reactnative.dev/docs/components-and-apis).

We can pass functions to components as `props` to handle events that happen to the components.

Because `props` are "owned" by its parent, they are immutable. For a component to store/remember mutable data, which changes over time, we must define and initialize `this.state` in the class component constructor and should _always_ use `setState` to modify the state. A stateless component is called a _representational_ component because its job is to "present" data given by the parent component.

The `constructor` method is called before the component is _first_ mounted/instantiated, so it should be used to initialize state. The `render` method is called whenever the view needs to be updated as an reaction to state change, e.g. the view presents data derived from the state.

React Navtive provides "lifecycle methods" we can override to "hook" into lifecycles events, in which components are instantiated, changed, or destroyed. `componentDidMount()` is called _after_ the component is mounted, so it is common to trigger network requests to fetch data that the component would need. For a visual reference, check out [this lifecycle diagram](https://projects.wojtekmaj.pl/react-lifecycle-methods-diagram/).

To log messages to JavaScript console, you can use `console.log()`, `console.warn()`, or `console.error()` according the severity of the messages.

## Stage 1
This version shows a piece of place holder text in the center of the screen. The steps are covered in chapter 1 up to page 27.

## Stage 2
This version shows static weather info with style. The steps to arrive at this stage are covered in chapter 1 up to page 40.

## Stage 3
This version factors TextInput into a custom component "SearchInput". The steps to arrive at this stage are covered in chapter 1 up to page 46.

## Stage 4
This version adds an image background to the screen. The steps to arrive at this stage are covered in chapter 1 up to page 52.


## Stage 5
This version allows users to enter a city name and updates the location name on the screen. The steps to arrive at this stage are covered in chapter 1 up to page 66.

## Stage 6
This version fetch weather data from an API. The steps to arrive at this stage are covered in chapter 1 up to page 82.

Because "metaweather.com" API is no longer available. We will change the API URL to a mock API. Please check out the `api.js` for details.
