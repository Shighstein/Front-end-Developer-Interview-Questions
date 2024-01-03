---
title: JavaScript Questions
layout: layouts/page.njk
permalink: /questions/javascript-questions/index.html
---

* Explain event delegation.
  * uses event bubble
  * instead of having to add `addEventListener()` to multiple tags, we can just add it to a parent and use `event.target`
  * example: a bunch of <button> wrapped in a single `<div>`. listen to `click` event in the `<div>`
* Explain how `this` works in JavaScript.
  * In an object method, this refers to the object.
  * Alone, this refers to the global object.
  * In a function, this refers to the global object.
  * In a function, in strict mode, this is undefined.
  * In an event, this refers to the element that received the event.
  * Methods like call(), apply(), and bind() can refer this to any object.
* Can you give an example of one of the ways that working with `this` has changed in ES6?
  * by default, `this` is bound to window (global)
  * change is because of the introduction of arrow function
* Explain how prototypal inheritance works.
  * inplicit inheritance
  * all `object` inherit `object.prototype`
  * can be set/get using `__proto__`
  * `this` always refers to the object before the `.`
* What is the difference between a variable that is: `null`, `undefined` or undeclared?
  * `undefined` means the value is not assigned to variable
  * `null` indicates an empty value
  * `undefined` is type undefined. `null` is object
* How would you go about checking for any of these states?
  * check with `=== undefined` or `=== null`
* What is a closure, and how/why would you use one?
  * a closure gives you access to an outer function's scope from an inner function. In JavaScript, closures are created every time a function is created, at function creation time.
* What language constructions do you use for iterating over object properties and array items?
  * `for...in`
* Can you describe the main difference between the `Array.forEach()` loop and `Array.map()` methods and why you would pick one versus the other?
  * `array.map()` creates a new array while `array.forEach()` just executes a task and return nothing
* What is a typical use case for anonymous functions?
  * as a parameter to another function
  * `var greet = function() { console.log('hello'); };` assigns an anonymous function to `greet` and invoke it by `greet()`
* What is the difference between host objects and native objects?
   * native objects are the ones provided by JS itself.
     * examples: `String()`, `Number()`, `Array()`
   * host objects are environment specific
     * examples: `window`, `console`, `NodeList`
* Explain the difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?
  * `function Persion(){}` is a constructor function
  * `var person = Person()` assigns the object (function) `Person()` to `person`
  * `var person = new Person()` create an instance of object created by `Person()`
* Explain the differences on the usage of `foo` between `function foo() {}` and `var foo = function() {}`
  * `function foo(){}` is function expression
  * `var foo = function(){}` is anonymous function and it's global scope
* Can you explain what `Function.call` and `Function.apply` do? What is the notable difference between the two?
  * `Function.call()` takes arguments indivisually while `Function.apply()` takes arguments as an array
  * they both takes `this`
* Explain `Function.prototype.bind`.
  * creates a new instance of the function that can be executed later with the new `this` provided
* What is the difference between feature detection, feature inference, and using the UA string?
* Explain "hoisting".
  * initialize variable or function before they are declared
* What is type coercion? What are common pitfalls of relying on type coercion in JavaScript code?
* Describe event bubbling.
  * event that travels up in the DOM tree from the event was fired to its ancestors
* Describe event capturing.
  * event that travels the other direction from bubbling
* What is the difference between an "attribute" and a "property"?
  * An attribute is the additional information defined in an HTML element to be initialized upon creation. A property is a characteristic of a DOM node(object) that you can manipulate. 
* What are the pros and cons of extending built-in JavaScript objects?
  * it can be difficult to maintain in a large scaled project
* What is the difference between `==` and `===`?
  * `==` checks for truthy `===` checks for type as well as value
* Explain the same-origin policy with regards to JavaScript.
  * a critical security mechanism that restricts how a document or script loaded by one origin can interact with a resource from another origin.
* Why is it called a Ternary operator, what does the word "Ternary" indicate?
  * `condition ? true : false;`
* What is strict mode? What are some of the advantages/disadvantages of using it?
* What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript?
* What tools and techniques do you use debugging JavaScript code?
  * `console.log()`
  * use `debugger`
  * running in debug mode from code editor
* Explain the difference between mutable and immutable objects.
  * mutable can be accessed and changed after created while immutable can be accessed but cannot be changed
  * primitives are immutable, referneces (functions, objects) are mutable
* What is an example of an immutable object in JavaScript?
  * primitive data types
  * `const name1 = 'bob';`
    `const name2 = name1;`
    `name1 = 'john';`
    `console.log(name2); // 'bob'`
* What are the pros and cons of immutability?
* How can you achieve immutability in your own code?
  * `object.seal()` (cannot add or remove but can change value), `object.preventExtension()` (cannot add but can remove) and `object.freeze()` (cannot add/remove/change. but subattributes are mutable)
* 
* Explain the difference between synchronous and asynchronous functions.
* What is event loop?
  * What is the difference between call stack and task queue?
* What are the differences between variables created using `let`, `var` or `const`?
* What are the differences between ES6 class and ES5 function constructors?
* Can you offer a use case for the new arrow `=>` function syntax? How does this new syntax differ from other functions?
* What advantage is there for using the arrow syntax for a method in a constructor?
* What is the definition of a higher-order function?
* Can you give an example for destructuring an object or an array?
* Can you give an example of generating a string with ES6 Template Literals?
* Can you give an example of a curry function and why this syntax offers an advantage?
* What are the benefits of using `spread syntax` and how is it different from `rest syntax`?
* How can you share code between files?
* Why you might want to create static class members?
* What is the difference between `while` and `do-while` loops in JavaScript?
* What is a promise? Where and how would you use promise?
* Discuss how you might use Object Oriented Programming principles when coding with JavaScript.

## Coding questions
* Make this work:
```javascript
duplicate([1,2,3,4,5]); // [1,2,3,4,5,1,2,3,4,5]
```
* Create a for loop that iterates up to `100` while outputting **"fizz"** at multiples of `3`, **"buzz"** at multiples of `5` and **"fizzbuzz"** at multiples of `3` and `5`
* What will be returned by each of these?
```javascript
console.log("hello" || "world")
console.log("foo" && "bar")
```
* Write an immediately invoked function expression (IIFE)
