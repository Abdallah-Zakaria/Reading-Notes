# Express Routing & Connected API 

#### Name 3 real world use cases where you’d want to change the request with custom middleware.
- Authentication , check if the user is login if any route happen.
- Validate a data before store it in database.
- Add log of each action on server on it time.

#### True or false: The route handler is middleware?
False.

#### In what ways can a middleware function end the process and send data to the browser?
Always end when send a data as a response.

#### At what point in the request lifecycle can you “inject” middleware?
limited unless you call the handler that have a response or no next() in side it .

#### What can cause express to error with “Request headers sent twice, cannot start a second response
Response more than once for the same request.

- **Middleware:**  functions are functions that have access to the request object ( req ), the response object ( res ), and the next function in the application's request-response cycle.
- **Request Object:**  request object allows you to submit a POST or GET request to an URL. Essentially it provides a way to make REST API requests to another URL.
- **Response Object:** The res object represents the HTTP response that an Express app sends when it gets an HTTP request.
- **Application Middleware:** Bind application-level middleware to an instance of the app object.
- **Routing Middleware:** Router-level middleware works in the same way as application-level middleware, except it is bound to an instance of express.Router().

## Routing
Routing refers to how an application’s endpoints (URIs) respond to client requests.
A route method is derived from one of the HTTP methods, and is attached to an instance of the express class.

- example of routes that are defined for the GET and the POST methods to the root of the app.
```
// GET method route
app.get('/', function (req, res) {
  res.send('GET request to the homepage')
})

// POST method route
app.post('/', function (req, res) {
  res.send('POST request to the homepage')
})
```

### Route paths
Route paths, in combination with a request method, define the endpoints at which requests can be made. Route paths can be strings, string patterns, or regular expressions.

The characters ?, +, *, and () are subsets of their regular expression counterparts. The hyphen (-) and the dot (.) are interpreted literally by string-based paths.

- examples of route paths based on strings

```
app.get('/', function (req, res) {
  res.send('root')
})
```

```
app.get('/about', function (req, res) {
  res.send('about')
})
```

```
app.get('/random.text', function (req, res) {
  res.send('random.text')
})
```

```
app.get('/ab*cd', function (req, res) {
  res.send('ab*cd')
})
```

```
app.get('/ab(cd)?e', function (req, res) {
  res.send('ab(cd)?e')
})
```
