Basic Node and Express - Use body-parser to Parse POST Requests
Besides GET there is another common http verb, it is POST. POST is the default method used to send client data with HTML forms. In the REST convention POST is used to send data to create new items in the database (a new user, or a new blog post). We don’t have a database in this project, but we are going to learn how to handle POST requests anyway.

In these kind of requests the data doesn’t appear in the URL, it is hidden in the request body. This is a part of the HTML request, also called payload. Since HTML is text based, even if you don’t see the data, it doesn’t mean that they are secret. The raw content of an HTTP POST request is shown below:

POST /path/subpath HTTP/1.0
From: john@example.com
User-Agent: someBrowser/1.0
Content-Type: application/x-www-form-urlencoded
Content-Length: 20
name=John+Doe&age=25
As you can see the body is encoded like the query string. This is the default format used by HTML forms. With Ajax we can also use JSON to be able to handle data having a more complex structure. There is also another type of encoding: multipart/form-data. This one is used to upload binary files.

In this exercise we will use an urlencoded body.

To parse the data coming from POST requests, you have to install a package: the body-parser. This package allows you to use a series of middleware, which can decode data in different formats. See the docs here.

Install the body-parser module in your package.json. Then require it at the top of the file. Store it in a variable named bodyParser.

The middleware to handle url encoded data is returned by bodyParser.urlencoded({extended: false}). extended=false is a configuration option that tells the parser to use the classic encoding. When using it, values can be only strings or arrays. The extended version allows more data flexibility, but it is outmatched by JSON. Pass to app.use() the function returned by the previous method call. As usual, the middleware must be mounted before all the routes which need it.