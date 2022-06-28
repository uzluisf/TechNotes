# Const, Let, and Var in JavaScript

## `const`

`const` declares a block-scoped, read-only named constant.

- `const`-declared entities (i.e., constants) are [[Block Scope]]d.

```JavaScript
const number = 42;

if (true){
	const number = 45;
	console.log(number); // 45
} 

(function () {
	const number = 47;
	console.log(number); // 47
})();

console.log(number); // 42
```

- Constants cannot be changed through reassignment, using the assignment operator.

```JavaScript
const number = 42;

number = 45; // Error: Assignment to constant variable.
```

- Constants cannot be redeclared within the same function or block scope.

```JavaScript
const number = 45;

const number  = 35; // Error: Identifier 'number' has already been declared
```

- If a container such as an array or an object is assigned to a constant, then its items or properties can be changed.

```JavaScript
const evens = [2, 3, 6, 8, 10];
evens[1] = 4;

console.log(evens); // Array [2, 4, 6, 8, 10]

const user = {fname: "rose", lname: "erls" }
user.fname = "Rose"
user.lname = "Erls"

console.log(user);  // Object { fname: "Rose", lname: "Erls" }
```

## `let`

`let` declares a block-scoped, local variable, optionally initializing it to a value.

- `let`-declared variables are [[Block Scope]]d. 
- You cannot **redeclare** the same variable within the same function or block scope. This raises a `SyntaxError`.
- 

```javascript
let x = 1;

if (true) {
  let x = 2;

  console.log(x); // expected output: 2
}

(function () {
  let x = 3;
  console.log(x); // expected output: 3
})()

console.log(x); // expected output: 1
```

## `var`
`var` declares a variable, optionally initializing it to a value.


References:
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var
- https://hacks.mozilla.org/2015/07/es6-in-depth-let-and-const/0
- https://tc39.es/ecma262/multipage/ecmascript-language-statements-and-declarations.html#sec-let-and-const-declarations

Tags: #fleeting 