React and Redux: Connect Redux to React
Now that you've written both the mapStateToProps() and the mapDispatchToProps() functions, you can use them to map state and dispatch to the props of one of your React components. The connect method from React Redux can handle this task. This method takes two optional arguments, mapStateToProps() and mapDispatchToProps(). They are optional because you may have a component that only needs access to state but doesn't need to dispatch any actions, or vice versa.

To use this method, pass in the functions as arguments, and immediately call the result with your component. This syntax is a little unusual and looks like:

connect(mapStateToProps, mapDispatchToProps)(MyComponent)

Note: If you want to omit one of the arguments to the connect method, you pass null in its place.


The code editor has the mapStateToProps() and mapDispatchToProps() functions and a new React component called Presentational. Connect this component to Redux with the connect method from the ReactRedux global object, and call it immediately on the Presentational component. Assign the result to a new const called ConnectedComponent that represents the connected component. That's it, now you're connected to Redux! Try changing either of connect's arguments to null and observe the test results.
```

```