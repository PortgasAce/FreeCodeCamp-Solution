React and Redux: Use Provider to Connect Redux to React
In the last challenge, you created a Redux store to handle the messages array and created an action for adding new messages. The next step is to provide React access to the Redux store and the actions it needs to dispatch updates. React Redux provides its react-redux package to help accomplish these tasks.

React Redux provides a small API with two key features: Provider and connect. Another challenge covers connect. The Provider is a wrapper component from React Redux that wraps your React app. This wrapper then allows you to access the Redux store and dispatch functions throughout your component tree. Provider takes two props, the Redux store and the child components of your app. Defining the Provider for an App component might look like this:

<Provider store={store}>
  <App/>
</Provider>

The code editor now shows all your Redux and React code from the past several challenges. It includes the Redux store, actions, and the DisplayMessages component. The only new piece is the AppWrapper component at the bottom. Use this top level component to render the Provider from ReactRedux, and pass the Redux store as a prop. Then render the DisplayMessages component as a child. Once you are finished, you should see your React component rendered to the page.

Note: React Redux is available as a global variable here, so you can access the Provider with dot notation. The code in the editor takes advantage of this and sets it to a constant Provider for you to use in the AppWrapper render method.
```

```