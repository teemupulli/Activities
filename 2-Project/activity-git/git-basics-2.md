# activity 2

## Part 1

- [Install Vscode](./setup.md#visual-studio-code)
- [Install Node](./setup.md#nodejs)

## Part 2: 

**1. Create a New Folder**

Open VSCode and create a new folder for your project. To do this, click on "File" > "Open Folder" and select or create a directory for your project.

> Other alternatives to create a folder and open Visual Studio Code (VSCode) in that folder [can be found here](./vscode-folders.md)

**2. Create a JavaScript File**

Inside your project folder, create a new JavaScript file, for example, `customModule.js`. This will be your custom Node module.

**3. Write Your Custom Module**

In `customModule.js`, write a simple Node module with a basic function that logs a message to the console.

```javascript
// customModule.js

function logMessage(message) {
    console.log(message);
}

module.exports = logMessage;
```

**4. Open the Integrated Terminal**

In VSCode, you can open an integrated terminal. To do this, press `Ctrl` + `~` (or `Cmd` + `~` on macOS) or click "Terminal" > "New Terminal" in the top menu.

**5. Navigate to Your Project Directory**

In the integrated terminal, navigate to your project folder. Use the `cd` command to change your current directory. For example:

```bash
cd /path/to/your/project
```

**6. Test Your Custom Module**

Create a test JavaScript file, for example, `test.js`, in your project folder to use your custom module.

```javascript
// test.js

const logMessage = require('./customModule');
logMessage('Hello from your custom module!');
```

**7. Execute Your Node Module**

In the integrated terminal, execute your `test.js` file using Node.js.

```bash
node test.js
```

You should see the following output in the terminal:

```sh
Hello from your custom module!
```

### Part 3: Local Git Repository

1. Make the project directory a Git repository by running:

```bash
git init
```
2. Create a secret file, for example, `mysecrets.txt`, in your project folder.

3. Create a `.gitignore` file to exclude `mysecrets.txt`  file from version control:

```
mysecrets.txt
```

3. Stage all the changes:

```bash
git add .
```

4. Commit the changes:

```bash
git commit -m  "meaningful message"
```

### Part 4: Push to GitHub

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

