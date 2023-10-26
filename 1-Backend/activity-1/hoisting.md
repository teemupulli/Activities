# Hoisting

```js
// function declaration
function square(x) {
  return x * x;
}

// function expression
var square = function(x) {
  return x * x;
};
```

### Step 0

Create a JavaScript file (e.g., `hoisting.js`) in the project directory

### Part 1/3: Refactoring

- Rewrite the following *function declarations* using a *function expression*:

 ```js
 // 1.
 function cube(x) {
   return x * x * x;
 }

 // 2.
 function fullName(first, last) {
   return first + " " + last;
 }

 // 3.
 function power(base, exp) {
   if (exp === 0) {
     return 1;
   }
   return base * power(base, exp - 1);
 }

 // 4.
 function sumCubes(numbers) {
   var total = 0;
   for (var i = 0; i < numbers.length; i++) {
     total = total + cube(numbers[i]);
   }
   return total;
 }
 ```

### Part 2/3: Mechanics of Hoisting

Type out your best answers to the following questions:

1. Why does JavaScript output `undefined` instead of throwing an error in the following code?

  ```js
  console.log(message);

  var message = 'Hi there!';
  ```

2. Why does JavaScript throw an error instead of logging `undefined` in the following code?

    ```js
    console.log(message);

    let message = 'Hi there!';
    ```

3. Explain precisely what happens when the following code is executed.

    ```js
    console.log(showMessage());

    const showMessage = function(){
      return 'Hi there!';
    };
    ```

4. Why does JavaScript *not* throw any errors when the following code is executed?

  ```js
  console.log(showMessage());

  function showMessage(){
    return 'Hi there!';
  }
  ```

### Part 3/3: Code Restructuring

Restructure the following instances of code to work correctly:

 ```js
 // 1.
 for(var i = 0; i < values.length; i++){
   console.log(values[i]);
 }

 var values = [10, 20, 30];
 ```
 ```js
 // 2.
 console.log(welcome('Charlie', 'Munger'));

 function welcome(first, last) {
   return `Welcome, ${first} ${last}! You last logged in on ${lastLogin}.`
 };

 var lastLogin = '1/1/1970';
 ```

 ### Ref
 - [hackreactor](https://github.com/hackreactor/javascript_401)
