Basic Node and Express - Start a Working Express Server
In the first two lines of the file myApp.js you can see how it’s easy to create an Express app object. This object has several methods, and we will learn many of them in these challenges. One fundamental method is app.listen(port). It tells your server to listen on a given port, putting it in running state. You can see it at the bottom of the file. It is inside comments because for testing reasons we need the app to be running in background. All the code that you may want to add goes between these two fundamental parts. Glitch stores the port number in the environment variable process.env.PORT. Its value is 3000.

Let’s serve our first string! In Express, routes takes the following structure: app.METHOD(PATH, HANDLER). METHOD is an http method in lowercase. PATH is a relative path on the server (it can be a string, or even a regular expression). HANDLER is a function that Express calls when the route is matched.

Handlers take the form function(req, res) {...}, where req is the request object, and res is the response object. For example, the handler
```
function(req, res) {
res.send('Response String');
}
```
will serve the string 'Response String'.

Use the app.get() method to serve the string Hello Express, to GET requests matching the / root path. Be sure that your code works by looking at the logs, then see the results in your browser, clicking the button ‘Show Live’ in the Glitch UI.