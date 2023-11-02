
# Lab: Building an Express Server with Custom Logging Middleware

In this lab, you will learn how to create a basic Express server and implement a custom logging middleware. The server will log incoming requests and respond with a simple "Hello, Express with Logging!" message. This lab will help you get started with building web servers using Express.

## Prerequisites

Before starting this lab, make sure you have Node.js and npm (Node Package Manager) installed on your system. You'll also need a code editor, such as Visual Studio Code, for writing and running the server.

## Lab Objectives

By the end of this lab, you will be able to:

- Create an Express server and define routes.
- Implement a custom logging middleware to log incoming requests.
- Start the Express server and listen for incoming requests.

## Lab Instructions

Follow these step-by-step instructions to build the Express server with logging middleware:

### Step 1: Set Up Your Project

1. Create a new directory for your project and navigate to it in your terminal.

2. Initialize a new Node.js project by running the following command:

```bash
npm init -y
```

This command will create a `package.json` file for your project.

1. Install the Express.js framework by running the following command:

```bash
npm install express
```

2. Create a JavaScript file (e.g., `server.js`) in your project directory. This file will contain the code for your Express server.

### Step 2: Write the Express Server Code

Open the `server.js` file in your code editor and add the following code to create an Express server with logging middleware:

```javascript
const express = require('express');
const app = express();

// Define a custom middleware function for logging
const logMiddleware = (req, res, next) => {
  console.log(`[${new Date().toLocaleString()}] ${req.method} ${req.url}`);
  next(); // Continue to the next middleware or route handler
};

// Use the logging middleware for all routes
app.use(logMiddleware);

// Define a route
app.get('/', (req, res) => {
  res.send('Hello, Express with Logging!');
});

// Start the server
const port = process.env.PORT || 3000;
app.listen(port, () => {
  console.log(`Server is running on port ${port}`);
});
```

This code does the following:

- Requires the `express` module to create the Express application.

- Defines a custom logging middleware function (`logMiddleware`) that logs information about incoming requests, including the request method and URL. It then calls the `next()` function to pass control to the next middleware or route handler.

- Uses the logging middleware for all routes using `app.use(logMiddleware)`.

- Defines a single route that listens for HTTP GET requests at the root path ("/") and responds with the message "Hello, Express with Logging!"

- Starts the Express server, specifying the port as either the value from the `PORT` environment variable or 3000 if no environment variable is provided. The server will log a message indicating that it's running.

### Step 3: Run the Express Server

1. In your terminal, navigate to the project directory containing the `server.js` file.

2. Start the Express server by running the following command:

```bash
node server.js
```

You should see the server's startup message indicating that it's running on a specific port.

1. Open your web browser and access the server by navigating to `http://localhost:3000` (or the specified port if you set the `PORT` environment variable). You should see the "Hello, Express with Logging!" message.

2. In the terminal where your server is running, you will also see logs for incoming requests, which include the request method and URL.

