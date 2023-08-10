1. **Fat Arrow Functions:**
   Fat arrow functions, also known as arrow functions, provide a concise syntax for writing functions. They also have some important differences in terms of how they handle `this`.

   ```javascript
   // Traditional function
   function add(a, b) {
     return a + b;
   }

   // Arrow function
   const subtract = (a, b) => a - b;
   ```

   Arrow functions are often used for short, concise functions and can be especially useful for avoiding issues with the `this` keyword in certain scenarios, like within callback functions.

2. **Import/Export Modules:**
   ES6 introduced a standardized way to organize and share code between different files using the `import` and `export` keywords. This modular approach helps keep codebase organized and promotes reusability.

   **Example:**
   Let's say you have two JavaScript files: `math.js` and `main.js`.

   ```javascript
   // math.js
   export function add(a, b) {
     return a + b;
   }

   // main.js
   import { add } from './math.js';

   console.log(add(5, 3)); // Output: 8
   ```

   In this example, the `add` function is defined in the `math.js` file and exported using `export`. In the `main.js` file, it's imported using `import` and then used.

3. **Lexical Scoping:**
   Lexical scoping, also known as static scoping, determines the scope of a variable based on its location within the code. This concept affects how variables are accessed and resolved.

   **Example:**

   ```javascript
   function outer() {
     const outerVar = 'I am outside!';

     function inner() {
       console.log(outerVar); // Inner function can access outerVar
     }

     inner();
   }

   outer();
   ```

   In this example, the `inner` function has access to variables defined in the `outer` function's scope due to lexical scoping.

ES6 brought several powerful features to JavaScript that enhance code readability, maintainability, and organization. Arrow functions simplify function syntax, import/export modules allow for modular development, and lexical scoping ensures that variables are resolved based on their location in the code.
