# React and Redux: Extract State Logic to Redux
Now that you finished the React component, you need to move the logic it's performing locally in its state into Redux. This is the first step to connect the simple React app to Redux. The only functionality your app has is to add new messages from the user to an unordered list. The example is simple in order to demonstrate how React and Redux work together.


First, define an action type 'ADD' and set it to a const ADD. Next, define an action creator addMessage() which creates the action to add a message. You'll need to pass a message to this action creator and include the message in the returned action.

Then create a reducer called messageReducer() that handles the state for the messages. The initial state should equal an empty array. This reducer should add a message to the array of messages held in state, or return the current state. Finally, create your Redux store and pass it the reducer.

```
// define ADD, addMessage(), messageReducer(), and store here:
const ADD = 'ADD'

let addMessage =(msg)=> {
    return {
        type: ADD,
        message: msg
    };
}

let messageReducer =(state = [],action) =>{
    switch(action.type){
        case ADD:
        return [...state,action.message];
        default:
        return state;
    }
}

let store = Redux.createStore(messageReducer);
```