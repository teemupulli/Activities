# Functions are first-class citizens in JS

In JavaScript, functions are considered first-class citizens, which means they are treated as regular values and have the same capabilities as other data types like strings, numbers, or objects. This property allows functions to be passed as arguments to other functions, returned from functions, and assigned to variables. Here are some examples that illustrate the concept of functions as first-class citizens:

1. **Assigning a Function to a Variable:**

You can assign a function to a variable, just like any other value.

```javascript
const add = function(a, b) {
  return a + b;
};

console.log(add(3, 5)); // Output: 8
```

2. **Passing a Function as an Argument:**

Functions can be passed as arguments to other functions, enabling higher-order functions.

```javascript
const calculate = function(operation, a, b) {
  return operation(a, b);
};

const multiply = function(x, y) {
  return x * y;
};

console.log(calculate(multiply, 4, 6)); // Output: 24
```

3. **Returning a Function from Another Function:**

Functions can also be returned from other functions, allowing the creation of closures.

```javascript
const powerOf = function(exponent) {
  return function(base) {
    return Math.pow(base, exponent);
  };
};

const square = powerOf(2);
const cube = powerOf(3);

console.log(square(5)); // Output: 25
console.log(cube(3));   // Output: 27
```

4. **Storing Functions in Arrays:**

You can store functions in arrays just like any other values.

```javascript
const operations = [
  function(a, b) { return a + b; },
  function(a, b) { return a - b; },
  function(a, b) { return a * b; }
];

console.log(operations[0](5, 3)); // Output: 8
console.log(operations[1](8, 4)); // Output: 4
```

5. **Object Properties as Functions:**

You can define functions as properties of objects.

```javascript
const calculator = {
  add: function(a, b) {
    return a + b;
  },
  subtract: function(a, b) {
    return a - b;
  }
};

console.log(calculator.add(10, 7));    // Output: 17
console.log(calculator.subtract(15, 3)); // Output: 12
```

6. **Creating Higher-Order Functions:**

Functions can create and return other functions, leading to more dynamic and flexible code.

```javascript
function multiplier(factor) {
  return function(number) {
    return number * factor;
  };
}

const double = multiplier(2);
const triple = multiplier(3);

console.log(double(4)); // Output: 8
console.log(triple(5)); // Output: 15
```

JavaScript treats functions as first-class citizens, allowing them to be manipulated, passed around, and stored just like other values. This feature enhances the expressive power and flexibility of the language, enabling the creation of more dynamic and functional programming styles.


<!-- Links -->
[javascript.info]:https://javascript.info/