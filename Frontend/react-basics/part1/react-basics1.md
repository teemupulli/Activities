# Lab: Creating a React Project and Understanding Dependencies

In this part, you'll create a new React project and explore its dependencies, including dev dependencies. You'll also understand why `import` is used instead of `require` in modern React projects.

### Part 1/3

**Step 1: Setting Up Your Environment**

1. **Create a New React App:**
   Open your terminal and run:
   
```sh
npx create-react-app react-dependencies-lab
cd react-dependencies-lab
```
> If you receive error like this `npm ERR! enoent ENOENT: no such file or directory`, then one fix is to issue this command: `npm install npm -g` . 

**Step 2: Exploring Project Dependencies and Dev Dependencies**

1. **Open `package.json`:**
   Open the `package.json` file located in your project's root directory. This file lists the dependencies and dev dependencies of your project.

2. **Project Dependencies:**
   Look for the `"dependencies"` section in `package.json`. These are the packages required for your app to run properly. Some common dependencies might include `react` and `react-dom`. You can install these packages using `npm install`.

   Hints: 
   - Look for lines like `"react": "^18.2.0"` and `"react-dom": "^18.2.0"` under `"dependencies"`.

3. **Dev Dependencies:**
   Dev dependencies are packages required during development, but not in production. They include tools for testing, code linting, bundling, etc. They should be listed under the `"devDependencies"` section.

   - Do you see `"devDependencies"` section in `package.json`. 

   Hint: Check this [thread]


**Step 3: Understanding `import` vs. `require`**

1. **`import` vs. `require` in Modern React:**

   In modern React projects, including those created with Create React App, the preferred way to import modules is using the `import` statement. This is because `import` is part of the ES6 module syntax, which offers various benefits:

   - `import` supports named imports and default imports.
   - `import` allows for tree shaking, which optimizes unused code during the build.
   - `import` is statically analyzable, aiding tooling and optimizations.

   **Why `import` Over `require`:**

   React projects are set up to use ES6 modules and the `import` syntax. While `require` is common in Node.js (CommonJS), using `require` in modern React projects could lead to compatibility issues and errors.

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

In this lab, you created a new React project and explored its dependencies, including project dependencies and dev dependencies. You learned the distinction between them and how to identify them in the `package.json` file. Additionally, you understood why the `import` statement is favored over `require` in modern React projects, thanks to its compatibility with ES6 modules and its advantages in terms of code optimization and tooling.

<!-- Links -->

[thread]:https://stackoverflow.com/questions/44868453/create-react-app