# Lab: Refactoring Regular Functions to Arrow Functions

### Introduction:

In this lab, you will explore various scenarios where you can **refactor** regular functions into arrow functions in JavaScript. Arrow functions provide a concise syntax and lexically scoped this, making them a valuable tool for enhancing code readability and maintainability.

### step 1

Create a JavaScript file (e.g., `arrow-functions.js`) in the project directory

### Step 2: Refactor Regular Functions to Arrow Functions:

**Scenario 1**: Basic Function:
Refactor a simple function with no parameters and a single-line return statement:

```js
// Regular function
function sayHello() {
    return "Hello, world!";
}
```

<details>
  <summary>Solution</summary>

`const sayHelloArrow = () => "Hello, world!";`

</details>


**Scenario 2**: Single Parameter:
Refactor a function with a single parameter:

```js
// Regular function
function double(x) {
    return x * 2;
}
```

<details>
  <summary>Solution</summary>

`const doubleArrow = x => x * 2;`

</details>


**Scenario 3**: Multiple Parameters:
Refactor a function with multiple parameters:

```js
// Regular function
function add(x, y) {
    return x + y;
}
```

<details>
  <summary>Solution</summary>

`const addArrow = (x, y) => x + y;`

</details>

**Scenario 4**: Function Inside an Object:
Refactor a function defined inside an object:

```js
// Regular function
const person = {
    name: "Alice",
    sayHi: function() {
        return "Hi, " + this.name + "!";
    }
};
```

<details>
  <summary>Solution</summary>

```js
const personArrow = {
    name: "Alice",
    sayHi: () => "Hi, " + this.name + "!" // 'this' will not work as expected here
};
```

</details> 


**Scenario 5**: Callback Functions:

> Call back functions and map() will be discussed later in the course

Refactor a callback function passed to the map method:

```js
const numbers = [1, 2, 3, 4, 5];

const doubled = [];
numbers.forEach(function(num) {
  doubled.push(num * 2);
});

```

<details>
  <summary>Solution</summary>

```js
const numbers = [1, 2, 3, 4, 5];
const doubled = [];

numbers.forEach((num) => {
  doubled.push(num * 2);
});
```
</details>


### Step 3: Run the Script:

In your terminal or command prompt, execute the script using the Node.js runtime:

```shell
node arrow-functions.js
```






