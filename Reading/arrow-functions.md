# Arrow functions

Arrow functions are a concise way to write JavaScript functions. They were introduced in ES6 (ECMAScript 2015) and provide a more compact syntax compared to traditional function expressions. Arrow functions are especially useful for writing short, one-line functions or for functions that do not require their own `this` context.

Here's the basic syntax of an arrow function:

```javascript
const functionName = (parameters) => {
  // function body
  return result;
};
```

And here are a few examples of arrow functions:

1. **Simple Arrow Function:**

```javascript
const greet = (name) => {
  return `Hello, ${name}!`;
};

console.log(greet("Alice")); // Output: Hello, Alice!
```

2. **Arrow Function with One Parameter:**

```javascript
const square = (num) => num * num;

console.log(square(5)); // Output: 25
```

3. **Arrow Function with No Parameters:**

```javascript
const getRandomNumber = () => Math.random();

console.log(getRandomNumber()); // Output: A random number between 0 and 1
```

4. **Arrow Function with Multiple Statements:**

```javascript
const calculateSum = (a, b) => {
  const sum = a + b;
  return sum;
};

console.log(calculateSum(3, 7)); // Output: 10
```


Arrow functions provide a concise and straightforward way to define functions in JavaScript. 


