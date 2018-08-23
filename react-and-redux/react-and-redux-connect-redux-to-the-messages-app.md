React and Redux: Connect Redux to the Messages App
Now that you understand how to use connect to connect React to Redux, you can apply what you've learned to your React component that handles messages.

In the last lesson, the component you connected to Redux was named Presentational, and this wasn't arbitrary. This term generally refers to React components that are not directly connected to Redux. They are simply responsible for the presentation of UI and do this as a function of the props they receive. By contrast, container components are connected to Redux. These are typically responsible for dispatching actions to the store and often pass store state to child components as props.


The code editor has all the code you've written in this section so far. The only change is that the React component is renamed to Presentational. Create a new component held in a constant called Container that uses connect to connect the Presentational component to Redux. Then, in the AppWrapper, render the React Redux Provider component. Pass Provider the Redux store as a prop and render Container as a child. Once everything is setup, you will see the messages app rendered to the page again.
```

```