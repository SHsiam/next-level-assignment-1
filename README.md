<h2> What are some differences between interfaces and types in TypeScript? </h2>

<b>Interface:</b>

Interface Primarily defining objects. We can extend other interfaces. It is best for defining objects, classes, and APIs. In the interface, don't use an equal sign.

Example: interface User {

  name: string;

  age: number;

}

interface Admin extends User {

  role: string;

}

<b>Type:</b>

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

<h2> Provide an example of using union and intersection types in TypeScript. </h2>

<b>Union types</b>

(|) this one called Union types. Union types allow a variable to hold one of multiple possible types. It is working like or. 

Example: type Status = "success" | "error" | "loading";

function showStatus(status: Status) {

  console.log("Status:", status);

}

showStatus("success");


<b>Intersection types</b>

(&) this one called intersection types. Intersection types combine multiple types into one. They are attached to each other. 

Example:

type User = {

  name: string;

  email: string;

};

type Admin = {

  role: string;

};

type AdminUser = User & Admin;

const admin: AdminUser = {

  name: "Siam",

  email: "Siam@example.com",

  role: "superadmin"

};
