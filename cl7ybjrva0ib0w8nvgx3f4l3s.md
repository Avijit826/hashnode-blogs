# A note on top javascript interview topics

# Scope

The scope of JavaScript is a execution context in which `values` and `expressions` are available. The scope of JavaScript is the set of rules for determining what variables exist in which parts of the program.

>Scopes can also be layered in a hierarchy, so that child scopes have access to parent scopes, but not vice versa.

JavaScript has the following kinds of scopes:
- Global scope: The default scope for all code running in script mode.
- Module scope: The scope for code running in module mode.
- Function scope: The scope created with a function.
- Block scope: The scope created with a pair of curly braces.



![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1662898074561/9A7Ljbdkz.png align="left")


### Global Scope

In JS, the global scope is the scope that contains, and is visible in, all other scopes.

>In client-side JavaScript, the global scope is generally the web page inside which all the code is being executed.

```javascript
let cource = "Angular";
const getCource = () => {
   console.log(cource);
}

getCource();
```

Here `course` variable is declared globally and child elements also access it.

### Function Scope

A function that creates a scope where all the declared methods are work only inside that.

```javascript

const getCource = () => {
  let cource = "Angular"; 
   console.log(cource); // Gives output
}
getCource();
console.log(cource); // Gives ReferenceError: cource is not defined
```

### Block Scope

It is a cope where its characteristic of variables are bound with in that scope.

> This also called as a `local level` scope.

```javascript
{
	let cource="Angular";
  
  console.log(cource); // Gives output
}

console.log(cource);  // Gives ReferenceError: cource is not defined
```

### Lexical Scope

Lexical Scoping defines how variable names are resolved in nested functions.

```javascript
const getFramework = () => {
  let framework = "Angular"; 
  const withVersion = () =>{
  	let version = "v12.3";
  	console.log(framework + " " + version); // accessing parent variable
  }
   withVersion();
}
getFramework();
```

> This also called as `static scope`.

# Single Thread

JavaScript is a single-threaded language because it has one call stack and one memory heap. Because of `synchronization`, it executes code in order and must finish executing a piece code before moving onto the next.

```javascript
function one() {
    for(i=1; i<= 10; i++){
        console.log(i);
}
}
function two() {
       console.log("Two");
}
one();
two();
```
Output:
```
1
2
3
4
5
6
7
8
9
10
"Two"
```

Here function two waits until function one executed completely.

# Call Stack

A call stack is used to track the location of programs, also known as a `execution stack`.
It records what function was called and what function called that one until it gets back to the main function or top of the stack.

> Every time you invoke a function, it’s added to the stack. If it has a nested function, that nested function will get added to the stack too. It's a linear data structure which means that when you call one function, all of its calls are pushed onto the top of the stack and then when you call another one, its calls are pushed on top of those calls.

```javascript
const getFramework = () => {
  let framework = "Angular"; 
   console.log(framework + ' ' + withVersion());
}
const withVersion = () =>{
  	let version = "v12.3";
  	return(version); // accessing parent variable
  }
getFramework();
```

- Add the `getFramework()` function to call stack.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1662955486942/rt1tScxB_.png align="left")

- Execute codes inside function.
- Invoke `withVersion()` function.
- Add the `withVersion()` function to call stack.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1662955700088/bBCNh9F6a.png align="left")

- Execute codes inside function.
- Delete the `withVersion()` function from our call stack list.
- When everything inside the `getFramework()` function has been executed, return to its invoking line to continue executing the rest of the JS code.
-  Delete the `getFramework()` function from the call stack list.

# Hoisting

The JavaScript interpreter moves functions, variables or classes declarations to the top of their current scope so that they are available as soon as possible. The interpreter also moves variable and function declarations within a scope so that they are available.

### Function hoisting
```javascript
getFramework();

function getFramework(){
  let framework = "Angular"; 
   console.log(framework);
}
```
### Variable hoisting

- Hoisting works with variables too, so you can use a variable in code before it is declared and/or initialized.

Using `var`:
```javascript
console.log(a);  // undefined
var a=5;
console.log(a); // 5
```
> Until that point in the execution is reached the variable has its default initialization (undefined for a variable declared using var, otherwise uninitialized).

Using `let` or `const`:
```javascript
console.log(a);  // ReferenceError exception as the variable value is uninitialized
var a=5;
console.log(a); // 5
```
> Variables declared with let and const are also hoisted but, unlike var, are not initialized with a default value. An exception will be thrown if a variable declared with let or const is read before it is initialized.

### Class hoisting
Classes defined using a class declaration are hoisted, which means that JavaScript has a reference to the class. However the class is not initialized by default, so any code that uses it before the line in which it is initialized is executed will throw a ReferenceError.