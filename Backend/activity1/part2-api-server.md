# API Server

> While a sample answer is provided, you are  encouraged to attempt writing the API with your group first.
 
1. Create an API server that listens on port `4000`. You can use the code from the [Simple API with Express](./part1-express-lab.md) as a reference.

2. Make sure to set up your project with the following steps:
   - Initialize your Node.js project using `npm init`.
   - Install Express as a dependency.
   - Install Nodemon as a development dependency.
   - Add a script named "dev" in your package.json file for running the server using Nodemon.

3. Create endpoints as follows:
   - Implement an endpoint with a GET request to `/textmessage` that returns plain text.
   - Implement an endpoint with a GET request to `/jsonmessage` that returns JSON data.
   - Implement an endpoint with a GET request to `/htmlmessage` that returns HTML content.

4. Implement an additional endpoint with a GET request to `/info`.  This endpoint should return `HTML` that greets the user and displays the time the request was received. Hint: use `template literals` to generate multiline HTML page.

5. Ensure you maintain version control for your project with the following steps:
   - Initialize a Git repository in your project folder using `git init`.
   - Add all your project files to the Git staging area with `git add .`.
   - Commit your changes with a descriptive message using `git commit`.
   - Push your project to a GitHub repository.



<details>
<summary>Sample Answer</summary

[Here](../activity2/api/server.js)

</details>
