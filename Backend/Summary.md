# key points

- [Prerequisites](#prerequisites)
- [Express Server](#express-server)
- [Middlewares](#middlewares)
- [Tools](#tools)
- [Misc.](#misc)

--------
## Prerequisites

### JSON (JavaScript Object Notation)

JSON (JavaScript Object Notation) is a lightweight data interchange format that is easy for humans to read and write, and easy for machines to parse and generate. It's commonly used for data transfer and configuration.

- **JSON**: JSON is a text-based data format that represents structured data using key-value pairs. It is a common data format with a simple and clear syntax.

- **JSON.parse()**: This is a JavaScript method used to parse JSON strings and convert them into JavaScript objects. It's helpful when working with JSON data received from external sources.

- **JSON.stringify()**: The `JSON.stringify()` method is used to convert JavaScript objects into JSON strings. It's useful when you want to send data to a server or store it in a file.

### Template Literals

Template literals are a way to embed expressions inside strings using backticks (`` ` ``). They allow you to create strings that span multiple lines and include variables or expressions enclosed in `${}`.

### TCP Ports

Transmission Control Protocol (TCP) is a standard that defines how to establish and maintain network connections. Ports are used to specify different services running on a single machine. Understanding TCP ports is essential when dealing with networking and server communication.

### HTTP Methods

HTTP (Hypertext Transfer Protocol) is the foundation of data communication on the World Wide Web. HTTP methods, such as GET, POST, PUT, and DELETE, define the actions a server can perform when handling client requests.

### Functions are First-Class Citizens

In JavaScript, functions are considered "first-class citizens." This means:

- **Ability to treat functions as values**: You can assign functions to variables, pass them as arguments, and return them from other functions.

- **Ability to pass a function as an argument**: Functions can be passed as parameters to other functions, allowing for dynamic behavior.

- **Ability to return a function from another function**: Functions can return other functions, enabling higher-order functions and closures.

--------
## Express Server

### Creating an Express Server

- `app.get()`: This is a method provided by Express to handle HTTP GET requests. You can use it to define the behavior when a specific route is accessed.

- `app.listen()`: This function starts the Express server, making it listen on a specified port.

- `req` and `res` objects: `req` represents the request made by the client, and `res` represents the response sent by the server. You can manipulate these objects to handle requests and send responses.

- `res.json()`: This method is used to send JSON responses to clients.

- Choosing a file name: When creating an Express application, you can name your main server file as `app.js`, `server.js`, or `index.js`. It's a convention, and the choice depends on your preference.


-------
## Middlewares

### Custom Middleware

- Logging middleware: A custom middleware that logs information about incoming requests, such as the request method and URL.

- 404: Not Found middleware: A custom middleware to handle routes that don't match any defined routes, typically used to respond with a "404 Not Found" message.

### Built-in Middleware

- `app.use(express.json())`: This built-in middleware parses JSON data in incoming requests, making it accessible as JavaScript objects.

- `app.use(express.static('public'))`: Express can serve static files like HTML, CSS, and JavaScript files from a specified directory.

- Error middleware (to be covered later): Error-handling middleware is used to handle errors that occur during request processing.

--------
## Tools

### Understanding npm and npx

- `npx` vs. `npm`: `npx` is a package runner tool that comes with npm 5.2 and higher. It's used to execute binaries from packages that aren't globally installed. `npm` is the Node.js package manager.

### Using Nodemon

Nodemon is a tool that helps in the development of Node.js applications by automatically restarting the server when changes are detected.

- Introduction to Nodemon: Nodemon monitors your source code files and automatically restarts the server when any changes are made.

- Installing Nodemon as a dev dependency: You can install Nodemon as a development dependency using `npm install nodemon --save-dev`.

- Setting up a Nodemon script: Create a script in your `package.json` file that uses Nodemon to run your server. For example: `"dev": "nodemon app.js"`.

- Running the script: You can start your server in development mode by running `npm run dev`.


------------
## Misc.

#### npm start

The reason why `npm start` works without the `run` keyword (`npm run start`) is because `start` is a special script name recognized by npm. When you define a script named `"start"` in your `package.json` file, you can run it directly using `npm start`.

Here's how it works:

1. **Special Scripts:**
   npm has a set of special scripts that can be executed without using the `run` keyword. These include `"start"`, `"test"`, and `"stop"`. When you use these special script names, npm automatically knows how to execute them.

2. **"start" Script:**
   When you define a `"start"` script in your `package.json` file, it's intended to start your application. This is a common convention for web development projects. When you run `npm start`, npm internally knows to execute the `"start"` script.

3. **Other Scripts:**
   For scripts that aren't one of the special script names (e.g., `"dev"`, `"build"`), you need to use the `run` keyword to explicitly tell npm that you're executing a script. For example, you would use `npm run dev` to execute a script named `"dev"`.


#### Differences between using `nodemon` and `node`

**Using `nodemon`**

`nodemon` is a utility that helps in development by monitoring changes in your files and automatically restarting your application when changes are detected. This is extremely useful as it saves you the trouble of manually stopping and restarting your server every time you make code changes.

1. **Convenience:** With `nodemon`, you don't need to manually restart your application every time you make changes to your code. The tool detects changes and handles the restart for you.

2. **Development Workflow:** During development, you often make frequent changes to your code. With `nodemon`, you can see your changes immediately without the hassle of stopping and restarting the server.

3. **Command:** To run your application using `nodemon`, you use the command:
   ```
   nodemon app.js
   ```
   This monitors your `app.js` file and restarts the application whenever you save changes.

**Using `node app.js`**

Running your application with `node app.js` is the standard way to start a Node.js application. It's a basic approach, but it lacks the automatic restart functionality of `nodemon`.

1. **Manual Restart:** When you use `node app.js`, you need to manually stop the server (Ctrl+C) and then restart it (using the same command) each time you make changes.

2. **Simplicity:** This method is straightforward and can be suitable for smaller projects where you don't expect to make frequent changes.

3. **Command:** To run your application using `node app.js`, you use the command:
   ```
   node app.js
   ```

**Comparison and Use Cases:**

- **Use `nodemon` when:**
   - You are actively developing and want a smoother development experience.
   - You want your server to automatically restart whenever you make code changes.
   - You're working on a project with multiple files or a more complex structure.

- **Use `node app.js` when:**
   - You're running your application in a more controlled or production-like environment.
   - You want a simpler way to run your application without automatic restarts.
