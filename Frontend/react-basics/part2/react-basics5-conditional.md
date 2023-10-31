# Lab: Conditionally Returning JSX in a React Project

In this lab, you'll create a React component that demonstrates how to conditionally render different JSX content based on certain conditions. This is a fundamental concept in building dynamic user interfaces.

### Part 1/3:

**Step 1: Setting Up Your Environment**

Open your terminal and run:

```sh
npx create-react-app react-conditional-jsx-lab
cd react-conditional-jsx-lab
```

**Step 2: Creating a Component with Conditional Rendering**

1. **Create a New Component:**
   Open the `src` folder in your project directory. Inside the `src` folder, create a new file named `UserGreeting.js`.

2. **Write the Component:**
   Open `UserGreeting.js` and write the following code:

   ```jsx
    function UserGreeting(props) {
        const isLoggedIn = props.isLoggedIn;

        let greetingContent;
        if (isLoggedIn) {
            greetingContent = <h1>Welcome back, User!</h1>;
        } else {
            greetingContent = <h1>Please log in to continue</h1>;
        }

        return (
            <div>
                {greetingContent}
            </div>
        );
    }

   export default UserGreeting;
   ```

**Step 3: Using the Component and Passing Props**

1. **Open `src/App.js`:**
   Open the `src/App.js` file and replace the existing code with the following:

   ```jsx
   import UserGreeting from './UserGreeting';

   function App() {
       return (
           <div className="App">
               <UserGreeting isLoggedIn={true} />
           </div>
       );
   }

   export default App;
   ```

**Step 4: Run the App**

1. **Start the App:**
   Save all your changes and return to the terminal. Make sure you're still in the `react-conditional-jsx-lab` directory. Start the app by running:

```sh
npm start
```

2. **View in Browser:**
   Your app will automatically open in your default web browser. You should see the output of the `UserGreeting` component with the content conditionally rendered based on the `isLoggedIn` prop value.

**Step 5: using a ternary operator**
Here's the modified `UserGreeting.js` component using ternary operator for conditional rendering:

```jsx
function UserGreeting(props) {
    const isLoggedIn = props.isLoggedIn;

    // Conditional rendering using the ternary operator
    return (
        <div>
               {isLoggedIn ? (
                   <h1>Welcome back, User!</h1>
               ) : (
                   <h1>Please log in to continue</h1>
               )}
        </div>
    );
}

export default UserGreeting;
```

The logic remains the same, but instead of using an `if` statement, the component uses a ternary operator to assign the appropriate JSX content to the `greetingContent` variable. This variable is then rendered inside the JSX. 

**Step 6: Run the App**

1. **Start the App:**

```sh
npm start
```

2. **View in Browser**


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

In this lab, you learned how to conditionally render JSX content in a React component. You created a component that uses the ternary operator to render different JSX based on a condition. This technique allows you to build dynamic user interfaces that adapt to different scenarios. By understanding conditional rendering, you can create more engaging and user-friendly React applications.