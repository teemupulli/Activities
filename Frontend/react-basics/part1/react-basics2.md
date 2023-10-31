# Lab: Creating Your First React Component**

In this part, we'll create a simple React component to display information using JSX. We'll cover JSX syntax, importing/exporting components, JSX vs. HTML, and how to render JSX content.

### Part 1/3

### Step 1: Setting Up Your Environment

Before you start, ensure you have Node.js and npm (Node Package Manager) installed.

- Create a New React App based on this simple template 

```sh
npx create-react-app jsx-lab
cd jsx-lab
```
 
> If you receive error like this `npm ERR! enoent ENOENT: no such file or directory`, then one fix is to issue this command: `npm install npm -g` . 


### Step 2: Create a Simple Component**

1. **Create a New Component:**
   Open the `src` folder in your project directory. Inside the `src` folder, create a new file named `SimpleComponent.js`.

2. **Write the Component:**
   Open `SimpleComponent.js` and write the following code:

   ```jsx
   import React from 'react';

   // Defining a simple functional component
   function SimpleComponent() {
       return (
           <div>
               <h1>Hello, JSX Lab!</h1>
               <p>This is a simple React component using JSX.</p>
           </div>
       );
   }

   // Export the component
   export default SimpleComponent;
   ```

### Step 3: Display the Component

1. **Open `src/index.js`:**
   Open the `src/index.js` file and replace the existing code with the following:

```jsx
   import React from 'react'
   import ReactDOM from 'react-dom/client'

   import SimpleComponent from './SimpleComponent';

   const root = ReactDOM.createRoot(document.getElementById('root'))
   root.render(
  <React.StrictMode>
    <SimpleComponent />
  </React.StrictMode>
   )
```

**Step 4: Run the App**

1. **Start the App:**
   Save all your changes and return to the terminal. Make sure you're still in the `jsx-lab` directory. Install the dependencies and start the app by running:
```sh
npm install
npm start
```

2. **View in Browser:**
   Your app will automatically open in your default web browser. You should see the output of your `SimpleComponent`.




### Part 2/3: Local Git Repository

> When you use "create-react-app," it automatically initializes a Git repository for you, eliminating the need to run `git init` separately.

1. Make sure that you have the `.gitignore` file and exclude the `node_modules` directory from version control:

```
node_modules/
```

2. Stage all the changes:

```bash
git add .
```

3. Commit the changes:

```bash
git commit -m  "Add message here"

```

### Part 3/3: Push to GitHub

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




**Summary:**

In this lab, you learned how to create a basic React component using JSX. You explored importing and exporting components, compared JSX to HTML, and gained a better understanding of how React mixes markup with rendering logic. You also learned how to display information with JSX and the importance of not passing JavaScript directly in JSX using curly braces.

<!-- Links -->
[degit]:https://github.com/Rich-Harris/degit
