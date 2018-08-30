Basic Node and Express - Implement a Root-Level Request Logger Middleware
Before we introduced the express.static() middleware function. Now it’s time to see what middleware is, in more detail. Middleware functions are functions that take 3 arguments: the request object, the response object, and the next function in the application’s request-response cycle. These functions execute some code that can have side effects on the app, and usually add informations to the request or response objects. They can also end the cycle sending the response, when some condition is met. If they don’t send the response, when they are done they start the execution of the next function in the stack. This is triggered calling the 3rd argument next(). More information in the express documentation.

Look at the following example :
```
function(req, res, next) {
console.log("I'm a middleware...");
next();
}
```
Let’s suppose we mounted this function on a route. When a request matches the route, it displays the string “I’m a middleware…”. Then it executes the next function in the stack.

In this exercise we are going to build a root-level middleware. As we have seen in challenge 4, to mount a middleware function at root level we can use the method app.use(<mware-function>). In this case the function will be executed for all the requests, but you can also set more specific conditions. For example, if you want a function to be executed only for POST requests, you could use app.post(<mware-function>). Analogous methods exist for all the http verbs (GET, DELETE, PUT, …).

Build a simple logger. For every request, it should log in the console a string taking the following format: method path - ip. An example would look like: GET /json - ::ffff:127.0.0.1. Note that there is a space between method and path and that the dash separating path and ip is surrounded by a space on either side. You can get the request method (http verb), the relative route path, and the caller’s ip from the request object, using req.method, req.path and req.ip. Remember to call next() when you are done, or your server will be stuck forever. Be sure to have the ‘Logs’ opened, and see what happens when some request arrives…

Hint: Express evaluates functions in the order they appear in the code. This is true for middleware too. If you want it to work for all the routes, it should be mounted before them.