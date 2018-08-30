Basic Node and Express - Get Query Parameter Input from the Client
Another common way to get input from the client is by encoding the data after the route path, using a query string. The query string is delimited by a question mark (?), and includes field=value couples. Each couple is separated by an ampersand (&). Express can parse the data from the query string, and populate the object req.query. Some characters cannot be in URLs, they have to be encoded in a different format before you can send them. If you use the API from JavaScript, you can use specific methods to encode/decode these characters.

route_path: '/library'
actual_request_URL: '/library?userId=546&bookId=6754' 
req.query: {userId: '546', bookId: '6754'}
Build an API endpoint, mounted at GET /name. Respond with a JSON document, taking the structure { name: 'firstname lastname'}. The first and last name parameters should be encoded in a query string e.g. ?first=firstname&last=lastname.

TIP: In the following exercise we are going to receive data from a POST request, at the same /name route path. If you want you can use the method app.route(path).get(handler).post(handler). This syntax allows you to chain different verb handlers on the same path route. You can save a bit of typing, and have cleaner code.