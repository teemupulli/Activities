

Title: Introduction to npm and Creating a Simple Express Server

**Objective:** In this lab, you will learn the basics of using npm (Node Package Manager) to manage dependencies and set up a simple Express server. You will also explore package.json, configure scripts, and understand how to ignore the node_modules directory.

**Prerequisites:**
- Node.js and npm installed on your system.

### Part 1: Steps

**1. Initialize a Node.js Project:**

Open your terminal and navigate to the directory where you want to create your project e.g npm-lab. Then, run the following commands:

```bash
npm init -y
```

This will create a package.json file with default values.

**2. Install Dependencies:**

Install the Express package as a project dependency using the following command:

```bash
npm install express
```

This command installs Express and adds it to your package.json file.

**3. Install Dev Dependencies:**

Now, let's install a development dependency called nodemon. Nodemon is a tool that helps in automatically restarting your server during development to save you time. Use the following command:

```bash
npm install nodemon --save-dev
```

This installs nodemon and adds it as a dev dependency in package.json.

**4. Create an Express Server:**

Create a JavaScript file (e.g., `app.js`) in your project directory and add the following code to set up a simple Express server:

```javascript
const express = require('express');
const app = express();
const port = 3000;

app.get('/', (req, res) => {
  res.send('Hello, Express!');
});

app.listen(port, () => {
  console.log(`Server is running on port ${port}`);
});
```

**5. Configure npm Scripts:**

Edit your package.json file to add scripts for starting your server and running it in development mode. Open package.json and add the following lines inside the "scripts" section:

```json
"scripts": {
  "start": "node app.js",
  "dev": "nodemon app.js"
}
```

Your package.json file should now look like this:

```json
{
  "name": "npm-lab",
  "version": "1.0.0",
  "description": "A simple Express server project",
  "main": "app.js",
  "scripts": {
    "start": "node app.js",
    "dev": "nodemon app.js"
  },
  "dependencies": {
    "express": "^4.17.1"
  },
  "devDependencies": {
    "nodemon": "^2.0.7"
  },
  "author": "Your Name",
  "license": "MIT"
}
```

**6. Start the Server:**

Now you can start your Express server by running the following command:

```bash
npm start
```

Your server will start and listen on port 3000. Access it in your web browser at http://localhost:3000, and you should see "Hello, Express!".

**7. Start the Server in Development Mode:**

To run your server using nodemon in development mode (which automatically restarts when you make code changes), use the following command:

```bash
npm run dev
```

**8. Ignore node_modules:**

Create a `.gitignore` file in your project directory and add the following line to ignore the `node_modules` directory:

```
node_modules/
```

This prevents the `node_modules` directory from being included in version control systems like Git.


### Part 2: Local Git Repository

1. Make the project directory a Git repository by running:

```bash
git init
```

2. Stage all the changes:

```bash
git add .
```

3. Commit the changes:

```bash
git commit -m  "Message here"

```

### Part 3: Push to GitHub

1. Create a new repository on GitHub:

- Go to the GitHub website .
- Click on the plus sign icon in the top right corner of the page, and then select "New repository."
- Fill in the details for your new repository:
   - Repository name: Choose a name for your new repository.
   - Description (optional): Add a short description to explain the repository's purpose.
   - Visibility: Choose between "Public" or "Private," depending on who should have access.
   - Do not initialize the repository with a `README` file or a `.gitignore` file.
- Click the "Create repository" button to create your new repository.


2. Link your local repository to the GitHub repository:

```bash
git remote add origin <GitHub Repository URL>
```

3. Push your local repository to GitHub:

```bash
git push -u origin main
```

4. Refresh the GitHub repository page to see your changes.


