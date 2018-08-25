JSON APIs and Ajax: Handle Click Events with JavaScript using the onclick property
You want your code to execute only once your page has finished loading. For that purpose, you can attach a JavaScript event to the document called DOMContentLoaded. Here's the code that does this:

document.addEventListener('DOMContentLoaded',function() {

});
You can implement event handlers that go inside of the DOMContentLoaded function. You can implement an onclick event handler which triggers when the user clicks on the element with id getMessage, by adding the following code:

document.getElementById('getMessage').onclick=function(){};

Add a click event handler inside of the DOMContentLoaded function for the element with id of getMessage.
```

```