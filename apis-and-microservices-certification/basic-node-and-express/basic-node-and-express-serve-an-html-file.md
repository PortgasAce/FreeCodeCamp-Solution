Basic Node and Express - Serve an HTML File
We can respond with a file using the method res.sendFile(path).

You can put it inside the app.get('/', ...) route handler. Behind the scenes this method will set the appropriate headers to instruct your browser on how to handle the file you want to send, according to its type. Then it will read and send the file. This method needs an absolute file path. We recommend you to use the Node global variable __dirname to calculate the path.

e.g. absolutePath = __dirname + relativePath/file.ext.

The file to send is /views/index.html. Try to ‘Show Live’ your app, you should see a big HTML heading (and a form that we will use later…), with no style applied.

Note: You can edit the solution of the previous challenge, or create a new one. If you create a new solution, keep in mind that Express evaluates the routes from top to bottom. It executes the handler for the first match. You have to comment out the preceding solution, or the server will keep responding with a string.