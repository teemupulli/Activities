# Express Web Development Lab

In this part, you will learn how to create a simple Express app with two endpoints—one returning simple text and the other returning JSON. You'll also explore how to use `nodemon` for automatic server restarts during development. Along the way, we'll explain important concepts like port, `app.get()`, `res.json()`, and `res.send()`.

### Step 1: Set Up the Project

1. Create a new directory for your project and navigate to it in the terminal.

2. Initialize a new Node.js project by running:
```sh
npm init -y
```

3. Install `express` as a dependency:
```sh
npm install express
```

4. Install `nodemon` as a development dependency:
```sh
npm install nodemon --save-dev
```

### Step 2: Create the Express App

1. Create a file named `app.js` in your project directory.

2. Add the following code to set up the Express app:
   ```javascript
   const express = require('express');
   const app = express();
   const port = 3001;

   // Endpoint 1: Text Response
   app.get('/text', (req, res) => {
     res.send('This is a simple text response.');
   });

   // Endpoint 2: JSON Response
   app.get('/json', (req, res) => {
     const jsonData = {
       message: 'This is a JSON response.',
       timestamp: new Date()
     };

     res.json(jsonData);
   });

   // Start the server
   app.listen(port, () => {
     console.log(`Server is listening on port ${port}`);
   });
   ```

### Step 3: Using Nodemon

1. Open your `package.json` file in a text editor.

2. Add the following line inside the `"scripts"` section:
   ```json
   "dev": "nodemon app.js"
   ```

### Step 4: Understand Key Concepts

1. **Port:** The `port` is a number that defines which endpoint the server should listen on. In this lab, it's set to 3001, so the server listens at `http://localhost:3001`.

2. **`app.get()`:** This method sets up a route for handling HTTP GET requests. It takes two arguments: the route path and a callback function. When a GET request matches the route path, the callback function is executed.

3. **`res.json()` and `res.send()`:**
   - `res.json(data)`: Sends a JSON response. It converts the `data` object to JSON format.
   - `res.send(text)`: Sends a simple text response.

### Step 5: Running the Lab

1. In the terminal, run the server using the `dev` script you added:
```sh
npm run dev
```

2. Open a web browser or use a tool like `curl` to access the endpoints:
   - Text Endpoint: `http://localhost:3001/text`
   - JSON Endpoint: `http://localhost:3001/json`

### Step 6: Modifying `app.js` with Nodemon

In this section, we'll explore further with `nodemon`, understand how to run the server using `npm start`, delve into why `npm run dev` works while `npm dev` doesn't, implement a simple middleware, and grasp the functioning of middlewares.

1. Keep the terminal running with the `nodemon`-powered server.

2. Open the `app.js` file in your text editor.

3. Modify the message in the JSON response section:
   ```javascript
   const jsonData = {
     message: 'This is an updated JSON response.',
     timestamp: new Date()
   };
   ```

4. Save the file.

5. Watch the terminal where `nodemon` is running. You should see a message indicating that the server has restarted due to the file change.

### Step 7: Using `npm start` vs `npm run dev`

1. In your `package.json` file, add a script named `"start"`:
```json
"start": "node app.js"
```

2. Save the file.

3. Stop the `nodemon` process in your terminal if it's still running.

4. Start the server using:
```sh
npm start
```

Observe that the server is running. Does it behave the same as `npm run dev`?

> Running your application with `node app.js` is the standard way to start a Node.js application. It's a basic approach, but it lacks the automatic restart functionality of `nodemon`, [More info].(#differences-between-using-nodemon-and-node-appjs)

> The reason why `npm start` works without the `run` keyword (`npm run start`) is because `start` is a special script name recognized by npm. When you define a script named `"start"` in your `package.json` file, you can run it directly using `npm start`, [More info](#npm-start).


### Step 8: Understanding `npm run dev` vs `npm dev`

1. The `npm run` command is used to execute scripts defined in `package.json`.

2. When you use `npm run dev`, it searches for a script named "dev" in your `package.json` and executes it.

3. Using `npm dev` directly would imply that you're trying to run a globally installed package named "dev," which isn't what you intend.


----

## Push to GitHub

- Local Git Repository
  - Make the project directory a Git repository by running:
    ```bash
    git init
    ```
   - Create a `.gitignore` file to exclude `node_modules`  file from version control:

    ```
    node_modules/
    ```
  - Stage all the changes:

    ```bash
    git add .
    ```
  - Commit the changes:
    ```bash
    git commit -m  "meaningful message"
    ```

- Push to GitHub
  - Create a new repository on GitHub
  - Link your local repository to the GitHub repository:
    ```bash
    git remote add origin <GitHub Repository URL>
    ```
  - Push your local repository to GitHub:
    ```bash
    git push -u origin main
    ```

