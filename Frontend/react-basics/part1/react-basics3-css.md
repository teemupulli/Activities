# Lab: Exploring Props and Styling in a React Project

In this lab, you'll create a React component, pass `props` to it, and `console.log()` the properties. You'll also gain an understanding of `props` as objects, use JavaScript expressions within `JSX` using curly braces, and apply CSS styles to your component.

### Part 1/3: 

**Step 1: Setting Up Your Environment**

Open your terminal and run:

```sh
npx create-react-app react-props-styling-lab
cd react-props-styling-lab
```

**Step 2: Creating and Using a Component with Props**

1. **Create a New Component:**
   Open the `src` folder in your project directory. Inside the `src` folder, create a new file named `Greeting.js`.

2. **Write the Component:**
   Open `Greeting.js` and write the following code:

   ```jsx
   function Greeting(props) {
       console.log(props); // Log the props object
       
       return (
           <div className="greeting">
               <h1>Welcome, {props.name}!</h1>
               <p>{props.message}</p>
           </div>
       );
   }

   export default Greeting;
   ```

**Step 3: Using the Component and Passing Props**

1. **Open `src/App.js`:**
   Open the `src/App.js` file and replace the existing code with the following:

   ```jsx
   import Greeting from './Greeting';
   import './App.css'; // Import CSS file

   function App() {
       return (
           <div className="App">
               <Greeting name="Alice" message="Welcome to the lab!" />
                <Greeting name="Bob" message="Good morning" />
           </div>
       );
   }

   export default App;
   ```

**Step 4: Console Logging Props and Styling with CSS**

1. **Open `src/App.css`:**
   Create a new file named `App.css` in the `src` folder and write some CSS rules:

   ```css
   .greeting {
       background-color: #f0f0f0;
       padding: 20px;
       border: 1px solid #ddd;
       text-align: center;
   }
   ```

**Step 5: Run the App**

1. **Start the App:**
   Save all your changes and return to the terminal. Make sure you're still in the `react-props-styling-lab` directory. Start the app by running:
   ```
   npm start
   ```

2. **View in Browser:**
   Your app will automatically open in your default web browser. You should see the output of the `Greeting` component, along with the CSS styles applied.


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

In this lab, you learned how to create a React component that accepts props and console.logs() the properties. You gained an understanding that props are passed as an object. You also used JavaScript expressions within JSX using curly braces. Additionally, you explored applying CSS styles to your component to enhance its visual appearance.