# Step by step guide

**Step 0: Setting Up Your React Environment**

Open your terminal and run:

```sh
npx create-react-app react-nested-lists-lab
cd react-nested-lists-lab
```

**Step 1: Set Up Your Project**

1. Open your React project in your code editor.
2. Make sure your project is running successfully by executing `npm install` and `npm start`.


**Step 2: Create a Data File**
1. Create a new JavaScript file named `recipesData.js` in your project's source directory.
2. Define an array of recipe objects in the `recipesData.js` file. For example:

```jsx
const recipesData = [
  {
    id: 1,
    name: "Spaghetti Carbonara",
    ingredients: ["Spaghetti", "Eggs", "Pancetta", "Parmesan Cheese", "Black Pepper"],
    instructions: "..."
  },
  {
    id: 2,
    name: "Chicken Alfredo",
    ingredients: ["Fettuccine Pasta", "Chicken Breast", "Heavy Cream", "Parmesan Cheese", "Garlic"],
    instructions: "..."
  },
  // Add more recipes
];

export default recipesData;
```

**Step 3: Create a Recipe Component**
1. Create a new file named `Recipe.js` in your project's components directory.
2. In the `Recipe.js` file, create a functional React component to display a single recipe. You can use the following template:

```jsx
import React from 'react';

function Recipe({ recipe }) {
  return (
    <div className="recipe">
      <h2>{recipe.name}</h2>
      <ul>
        {recipe.ingredients.map((ingredient, index) => (
          <li key={index}>{ingredient}</li>
        )}
      </ul>
      <p>{recipe.instructions}</p>
    </div>
  );
}

export default Recipe;
```

**Step 4: Import and Display Recipes in App Component**
1. Open your `App.js` file in the src directory.
2. Import the `Recipe` component at the top of the `App.js` file.

```jsx
import Recipe from './components/Recipe';
```

3. In the `App.js` component, import the `recipesData.js` file to access the list of recipes.

```jsx
import recipesData from './recipesData.js';
```

4. Inside the `App` component, use the `map()` function to render each recipe from the imported data, utilizing the recipe's own index.

```jsx
function App() {
  return (
    <div className="App">
      <h1>Recipes</h1>
      <div className="recipe-list">
        {recipesData.map((recipe) => (
          <Recipe key={recipe.id} recipe={recipe} />
        )}
      </div>
    </div>
  );
}

export default App;
```

**Step 5: Style Your Recipes (Optional)**
1. You can add CSS to style your `Recipe` component and the list of recipes to make it visually appealing.

**Step 6: Test Your Application**
1. Save your files and make sure your React development server is still running.
2. Open your web browser and visit `http://localhost:3000` (or the URL specified by your React project).
3. You should see a list of recipes rendered on the page, utilizing the recipe's own index.

