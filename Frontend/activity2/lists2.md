# Nested lists in one component 

> Feel free to attempt this activity independently. If you encounter any difficulties or need guidance, you can refer to this [step-by-step guide](./guide.md) for assistance.

### Lab Instructions

Make a list of recipes from the array `recipes` below! For each recipe in the array, display its name as an `<h2>` and list its ingredients in a `<ul>`.

> This will require nesting two different `map` calls.

Here's the App.js

```js App.js
import { recipes } from './data.js';

export default function RecipeList() {
  return (
    <div>
      <h1>Recipes</h1>
    </div>
  );
}
```

Here's the array of recipes:

```js data.js
export const recipes = [{
  id: 'greek-salad',
  name: 'Greek Salad',
  ingredients: ['tomatoes', 'cucumber', 'onion', 'olives', 'feta']
}, {
  id: 'hawaiian-pizza',
  name: 'Hawaiian Pizza',
  ingredients: ['pizza crust', 'pizza sauce', 'mozzarella', 'ham', 'pineapple']
}, {
  id: 'hummus',
  name: 'Hummus',
  ingredients: ['chickpeas', 'olive oil', 'garlic cloves', 'lemon', 'tahini']
}];
```

