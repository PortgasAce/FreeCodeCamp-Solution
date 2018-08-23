React and Redux: Manage State Locally First
Here you'll finish creating the DisplayMessages component.


First, in the render() method, have the component render an input element, button element, and ul element. When the input element changes, it should trigger a handleChange() method. Also, the input element should render the value of input that's in the component's state. The button element should trigger a submitMessage() method when it's clicked.

Second, write these two methods. The handleChange() method should update the input with what the user is typing. The submitMessage() method should concatenate the current message (stored in input) to the messages array in local state, and clear the value of the input.

Finally, use the ul to map over the array of messages and render it to the screen as a list of li elements.
```
class DisplayMessages extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      input: '',
      messages: []
    }
    this.handleChange = this.handleChange.bind(this)
    this.submitMessage = this.submitMessage.bind(this)
  }
  // add handleChange() and submitMessage() methods here
  handleChange(event){
    this.setState({
      input:event.target.value
    })
  }

  submitMessage(){
    let intputVal = this.state.input;
    let arr = [...this.state.messages,intputVal];
    this.setState({
      input:'',
      messages:arr
    })

  }

  render() {
    const items = this.state.messages.map((items) => (<li>{items}</li>));

    return (
      <div>
        <h2>Type in a new Message:</h2>
        { /* render an input, button, and ul here */ }
        <input 
        type="text"
        onChange={this.handleChange} 
        value={this.state.input} ></input>
        <button onClick={this.submitMessage}>submit</button>
        <ul>
          {items}
        </ul>
        { /* change code above this line */ }
      </div>
    );
  }
};
```