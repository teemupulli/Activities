### Lab: Rendering a List of Books in React

#### Objective:

In this lab, you will learn how to work with lists in React by importing a list of books from a file and rendering them using the `map()` function.

#### Instructions:

**Step 0: Setting Up Your React Environment**

Open your terminal and run:

```sh
npx create-react-app react-lists-lab
cd react-lists-lab
```

**Step 1: Set Up Your Project**

1. Open your React project in your code editor.
2. Make sure your project is running successfully by executing `npm install` and `npm start`.

**Step 2: Create a Data File**

1. Create a new JavaScript file named `booksData.js` in your project's source directory.
2. Define an array of book objects in the `booksData.js` file. For example:

```jsx
const booksData = [
  {
    id: 1,
    title: "The Great Gatsby",
    author: "F. Scott Fitzgerald",
    genre: "Fiction",
    year: 1925,
  },
  {
    id: 2,
    title: "To Kill a Mockingbird",
    author: "Harper Lee",
    genre: "Fiction",
    year: 1960,
  },
  // Add more book objects
];

export default booksData;
```

**Step 3: Create a Book Component**

1. Create a new file named `Book.js` in your project's components directory.
2. In the `Book.js` file, create a functional React component to display a single book. You can use the following template:

```jsx
import React from 'react';

function Book({ book }) {
  return (
    <div className="book">
      <h2 className="book-title">{book.title}</h2>
      <p><strong>Author:</strong> {book.author}</p>
      <p><strong>Genre:</strong> {book.genre}</p>
      <p><strong>Year:</strong> {book.year}</p>
    </div>
  );
}

export default Book;
```

**Step 4: Import and Display Books in App Component**

1. Open your `App.js` file in the src directory.
2. Import the `Book` component at the top of the `App.js` file.

```jsx
import Book from './components/Book';
```

3. In the `App.js` component, import the `booksData.js` file to access the list of books.

```jsx
import booksData from './booksData.js';
```

4. Inside the `App` component, use the `map()` function to render each book from the imported data.

```jsx
function App() {
  return (
    <div className="App">
      <h1>Book List</h1>
      <div className="book-list">
        {booksData.map((book) => (
          <Book key={book.id} book={book} />
        )}
      </div>
    </div>
  );
}

export default App;
```

**Step 5: Style Your Books**

Add CSS to style your `Book` component and the list of books to make it visually appealing.
- Create a new CSS file named `Book.css` in the same directory as your Book.js file.
- Add CSS styles to the `Book.css` file to style the book components as desired. For example:

```css
.book {
  background-color: #f9f9f9;
  border: 1px solid #ccc;
  padding: 15px;
  margin: 10px;
  border-radius: 5px;
}

.book-title {
  font-size: 1.2rem;
  margin: 0;
  color: #333;
}
```

**Step 6: Test Your Application**

1. Save your files and make sure your React development server is still running.
2. Open your web browser and visit `http://localhost:3000` (or the URL specified by your React project).
3. You should see a list of books rendered on the page.

**Step 7: Observe the Result Without the key Prop**

Replace the code in the App.js file with the following:

```jsx
function App() {
  return (
    <div className="App">
      <h1>Book List</h1>
      <div className="book-list">
        {booksData.map((book) => (
          <Book book={book} />
        )}
      </div>
    </div>
  );
}

export default App;
```

- Save your files and make sure your React development server is still running.
- Observe the result and take note of any warnings or issues in the browser console related to the missing key prop.
- Open your App.js file again and add the key prop back to the Book component when rendering the list of books.

```jsx
{booksData.map((book) => (
  <Book key={book.id} book={book} />
)}
```