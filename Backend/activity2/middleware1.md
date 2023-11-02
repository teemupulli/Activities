# Lab: Middleware

1. Begin by opening the `server.js` [file](./api/server.js) in your project.

2. Create the `requestLogger` middleware by adding the following code block to your `server.js`:

```javascript
   const requestLogger = (request, response, next) => {
     console.log('Method:', request.method);
     console.log('Path:  ', request.path);
     console.log('Body:  ', request.body);
     console.log('---');
     next();
   }
```

3. Define the `unknownEndpoint` middleware by adding the following code block to your `server.js`:

```javascript
   const unknownEndpoint = (request, response) => {
     response.status(404).send({ error: 'unknown endpoint' });
   }
```

4. Insert the `requestLogger` middleware into your Express application. You can do this right below the creation of your Express app instance using the `app.use` method:

```javascript
app.use(requestLogger);
```

This middleware will log request information for each incoming request.

5. Insert the `unknownEndpoint` middleware just before the `app.listen()`  using `app.use`:

```javascript
app.use(unknownEndpoint);
```

The `unknownEndpoint` middleware will handle requests to unknown endpoints by responding with a 404 error and an "unknown endpoint" message.

> It's important to test your modified API server to ensure that the added middlewares work correctly. You can do this by running your server and making requests to various endpoints to confirm that the logging and unknown endpoint handling are functioning as expected.
