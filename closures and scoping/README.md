### Scoping in JavaScript:

Scoping defines the accessibility or visibility of variables in different parts of your code. In JavaScript, there are two main types of scope: **global scope** and **local (function) scope**.

1. **Global Scope:** Variables declared outside of any function or block have global scope. They can be accessed from anywhere in your code, including within functions.

2. **Local (Function) Scope:** Variables declared within a function have local scope. They are only accessible within that function. Each function creates its own scope.

### Closure in JavaScript:

A closure is a function that retains access to variables from its containing (enclosing) scope even after that scope has finished executing. In other words, a closure "remembers" the variables and parameters of the function where it was created, even if that function has already completed.

Closures are powerful and are often used for creating private data and encapsulation, event handling, and maintaining state in functional programming.

Here's an example:

```javascript
function outerFunction() {
  const outerVar = "I'm from outer function";

  function innerFunction() {
    console.log(outerVar); // innerFunction has access to outerVar
  }

  return innerFunction;
}

const myClosure = outerFunction(); // myClosure now holds the innerFunction

myClosure(); // Output: "I'm from outer function"
```

In this example, `innerFunction` is a closure because it maintains access to the `outerVar` variable from its enclosing `outerFunction`. Even after `outerFunction` finishes executing, `innerFunction` still has access to `outerVar`.

### Practical Uses of Closures:

1. **Data Privacy and Encapsulation:** Closures can be used to create private variables and methods, hiding implementation details from the outside world.

2. **Event Handlers:** Closures are often used to capture the state of a function when used as an event handler. This allows the function to remember the context it was created in.

3. **Factory Functions:** Closures can be used in factory functions to generate instances of objects with unique private states.

4. **Module Pattern:** Closures can be leveraged to implement the module pattern, allowing you to organize code into self-contained modules.
