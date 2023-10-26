# Hoisting

In JavaScript, there is hoisting, which means variable and function declarations are moved to the top of their containing scope during the compilation phase. However, the hoisting process behaves differently for variables and function declarations.

### Function Declarations vs Variable Declarations

1. **Variable Declarations:** When a variable is declared using `var`, it is hoisted to the top of its containing function or global scope. The variable declaration is "hoisted," but the assignment (initialization) remains in its original place in the code. As a result, the variable is initialized with `undefined` at the top of the scope.

   For example:
   ```javascript
   console.log(x); // Outputs: undefined
   var x = 5;
   ```

2. **Function Declarations:** Function declarations, unlike variable declarations, are fully hoisted. The entire function is moved to the top of its containing scope, so it can be used before its actual declaration in the code.

   For example:
   ```javascript
   sayHello(); // This works
   function sayHello() {
     console.log('Hello');
   }
   ```

In the cases provided in your code examples, both the variable `values` and the function `welcome` are hoisted due to their function declaration and variable declaration nature. However, the issue is that the variable `values` is not assigned any value during hoisting, and the function `welcome` uses a variable (`lastLogin`) that is declared after the function call, which is why they should be reordered to avoid reference errors.

### Function declaration vs function expression

With anonymous function expressions, only the variable declaration is hoisted, not the function itself. This means you cannot use the function before the line where it's defined.

   For example:
   ```javascript
   sayHello(); // Throws an error: "sayHello is not a function"
   var sayHello = function() {
     console.log('Hello');
   };
   ```
