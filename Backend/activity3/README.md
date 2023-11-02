# JavaScript Lab

In this lab, you'll review some fundamental concepts of JavaScript while working in the Node.js environment.

### Part 1: Template Literals

1. **Create a New File:**
   - create a new file named `node.js`.

2. **Declare a Variable:**
   - Inside `node.js`, write: `const name = "YourName";` (Replace `"YourName"` with your actual name.)

3. **Use Template Literals:**

Below the variable declaration, write: 
```js
const message = `Hello, my name is ${name}.`;
```

1. **Print the Message:**
   - Add: `console.log(message);` on the next line.

2. **Run Your Code:**
   - Open your terminal, navigate to the directory containing `node.js`, and run: `node node.js`.
   - You should see the message printed in the console.

### Part 2: JSON vs JavaScript Objects

1. **Declare an Object:**

After the previous part, write: 
```js
const person = { name: "John", age: 25, email: "john@example.com" };
```

1. **Convert to JSON:**
   - Write: `const jsonPerson = JSON.stringify(person);`
   - `jsonPerson` now holds the JSON representation of the `person` object.

2. **Print JSON:**
   - Add: `console.log(jsonPerson);`

3. **Parse JSON:**
   - Write: `const jsonString = '{"name": "Alice", "age": 30, "email": "alice@example.com"}';`
   - `jsonString` contains JSON-formatted data.

4. **Convert JSON to Object:**
   - Write: `const parsedPerson = JSON.parse(jsonString);`
   - `parsedPerson` is now a JavaScript object.

5. **Print Parsed Object:**
   - Add: `console.log(parsedPerson);`


### Part 3:

**Multi-line Strings using Template Literals:**

1. **Refactor Code for Multi-line Strings:**
   Given the following JavaScript code with multi-line strings using string concatenation, refactor it to use template literals for a more efficient and readable solution:
   ```javascript
   const firstName = "John";
   const lastName = "Doe";
   const address = "123 Main Street\nApt 4B\nCity: Example";
   ```
   
```javascript
const firstName = "John";
const lastName = "Doe";
const address = `123 Main Street
Apt 4B
City: Example`;
```

**Convert Concatenation with Template Literals:**

2. **Refactor Code with Template Literals:**
   Refactor the following JavaScript code with string concatenation to use template literals for a more efficient and readable solution:
   ```javascript
   const name = "Alice";
   const age = 30;
   const greeting = "Hello, my name is " + name + " and I am " + age + " years old.";
   ```


```javascript
const name = "Alice";
const age = 30;
const greeting = `Hello, my name is ${name} and I am ${age} years old.`;
```


**Convert JSON to JavaScript Object:**

3. **Parse JSON to JavaScript Object:**
   Given the following JSON string representing a user, write a JavaScript code snippet that parses the JSON and extracts the user's name:
   ```javascript
   const userJSON = '{"name": "Emily", "age": 25, "city": "San Francisco"}';
   ```


```javascript
const userJSON = '{"name": "Emily", "age": 25, "city": "San Francisco"}';
const userObject = JSON.parse(userJSON);
const userName = userObject.name;
```


**Convert JavaScript Object to JSON:**

4. **Serialize JavaScript Object to JSON:**
   Given a JavaScript object representing a product, write a code example that converts the object into a JSON string. Include the product's name, price, and category in the JSON representation:
   ```javascript
   const product = { name: "Product A", price: 15.99, category: "Electronics" };
   ```

```javascript
const product = { name: "Product A", price: 15.99, category: "Electronics" };
const productJSON = JSON.stringify(product);
```


**Convert JavaScript Array to JSON:**

5. **Serialize JavaScript Array to JSON:**
   You have an array of customer orders in JavaScript. Write a function that converts this array into a JSON string. Provide an example of the JavaScript array and the resulting JSON string:
   ```javascript
   const orders = [
     { orderID: 1, product: "Widget", quantity: 5 },
     { orderID: 2, product: "Gadget", quantity: 3 },
   ];
   ```

```javascript
const orders = [
  { orderID: 1, product: "Widget", quantity: 5 },
  { orderID: 2, product: "Gadget", quantity: 3 },
];
const ordersJSON = JSON.stringify(orders);
```
