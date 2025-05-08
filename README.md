<h2> What are some differences between interfaces and types in TypeScript? </h2>

Interface:

Interface Primarily defining objects. We can extend other interfaces. It is best for defining objects, classes, and APIs. In the interface, don't use an equal sign.

Example: interface User {

  name: string;

  age: number;

}

interface Admin extends User {

  role: string;

}

Type:

Type can define primitives, unions, intersections, and more. Basically, type can represent anything, not just objects. It can extend via intersections (&) but not via extends keyword. It is more flexible.

Example: type User = {

  name: string;

  age: number;

};

type Admin = User & {

  role: string;

};

<h2> How does TypeScript help in improving code quality and project maintainability? </h2>

TypeScript is an object-oriented programming language. It is built in JavaScript with extra features. TypeScript checks for type-related errors at compile time, long before the code runs in the browser or backend. TypeScript significantly improves code quality and project maintainability, especially in medium- to large-scale applications. 

Example: function add(a: number, b: number): number {

  return a + b;

}

add(5, "3"); 

In this example , we use both types as numbers, but we pass data as numbers and strings. We also tell our executives data-only numbers. That's why it provides an error. Error: Argument of type 'string' is not assignable to 'number.' In JavaScript it is not possible; for this reason, TypeScript is smarter than JavaScript. 


