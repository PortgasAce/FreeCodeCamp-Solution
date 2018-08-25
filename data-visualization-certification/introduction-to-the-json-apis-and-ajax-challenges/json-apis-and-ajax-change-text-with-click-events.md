JSON APIs and Ajax: Change Text with click Events
When the click event happens, you can use JavaScript to update an HTML element.

For example, when a user clicks the "Get Message" button, it changes the text of the element with the class message to say "Here is the message".

This works by adding the following code within the click event:

document.getElementsByClassName('message')[0].textContent="Here is the message";


Add code inside the onclick event handler to change the text inside the message element to say "Here is the message".
```

```