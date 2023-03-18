---
title: "JavaScript Functions"
datePublished: Sat Mar 18 2023 18:41:39 GMT+0000 (Coordinated Universal Time)
cuid: clfebfccy04ytr3nv4iwq6zt8
slug: javascript-functions
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1679047387931/efbfd537-527a-4644-bccf-ab802639b05e.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1679047635180/e85ed8a9-53e6-498d-b6c1-0d3ae98467a0.gif
tags: javascript, iwritecode, javascript-functions

---

# Introduction

Functions are one of the fundamental building blocks of javascript, it's a group of reusable code that can perform some task and executed when it is been called or invoked.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679047344698/9d40e4a6-6673-45fc-bb04-cfa9c7fcd75b.png align="center")

### Declaration of Function

```javascript
 function function1()
{
   return "John"
}
```

### Calling a Function

`function1()`

```javascript
function function1()
{
   return "John"
}

console.log(function1())
```

Output:

```javascript
John
```

# Types of Functions

* ## Named Function
    

In this function, the function is declared with by `function` keyword along with `function name`.

```javascript
function function1()
{
    console.log("John1")
}
    
function1()
```

Output:

```javascript
John1
```

* ## Hoisting Function
    

Function hoisting is a mechanism in which the JavaScript engine physically `moves function declarations to the top` of the code before executing them.

```javascript
function1()

function function1()
{
    console.log("John1")
}
```

Output:

```javascript
John1
```

* ## Anonymous Function
    

An anonymous function is a function `without a name`. An anonymous function is not accessible after its initial creation.

```javascript
const function2 = function(){
   console.log("John2")
}
    
function2()
```

Output:

```javascript
John2
```

* ## Immediately Invoked Function
    

The immediately invoked function is `execute itself immediately` after the declaration.

```javascript
function1()

function function1()
{
   console.log("John1")
}
const function2 = function(){
   console.log("John2")
}
const function3 = 
  (function(){
   console.log("John3")
})()

function2()
```

Output:

```javascript
John1
John3
John2
```

* ## Arrow Function
    

An arrow function is an anonymous function expression written with the `fat arrow` syntax ( =&gt; ).

> Arrow functions are not hoisted.

```javascript
const function4 = () => {
   console.log("John4")
}

function4()
```

Output:

```javascript
John4
```

# Scope of Function

Variables defined inside a function cannot be accessed from anywhere outside the function, because the variable is defined only in the scope of the function. However, a function can access all variables and functions defined inside the scope in which it is defined.

### Accessing Its Calling Scope

```javascript
let name ='John'
function function1()
{
   console.log(name)
}
function1()
```

Output:

```javascript
John
```

### Function Scope variable

```javascript
function function1()
{
let name ='John'
   console.log(name)
}
function1()

console.log(name)
```

Output:

```yaml
John
ReferenceError: name is not defined
```

# Built-in Functions

## eval()

eval() is used to convert string to executable `arithmetic operations`.

```javascript
let sum = '4+3'
console.log(eval(sum))
```

Output:

```javascript
7
```

## isNaN()

The isNaN() function determines whether a value is NaN or not.

```javascript
let string = 'John'
console.log(isNaN(string))
```

Output:

```javascript
false
```

## parseInt()

The parseInt() function parses a string argument and returns an integer.

```javascript
let string = '6562'
console.log(parseInt(string))
console.log(typeof(parseInt(string)))
```

Output:

```javascript
6562
number
```

## typeof()

The typeof() function parses an argument and returns a data type of element.

```javascript
let string = '6562'
console.log(typeof(parseInt(string)))
```

Output:

```javascript
number
```