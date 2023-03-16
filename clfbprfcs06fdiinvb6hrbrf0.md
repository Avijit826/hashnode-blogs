---
title: "A In Depth Information Of JavaScript Object & Its Methods"
datePublished: Thu Mar 16 2023 22:59:38 GMT+0000 (Coordinated Universal Time)
cuid: clfbprfcs06fdiinvb6hrbrf0
slug: a-in-depth-information-of-javascript-object-its-methods
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1678967575494/3f6b9bd6-852a-4890-88ed-875ffd27da31.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1678967730404/b9fddd53-7fb1-4a2a-8953-eb94f760f495.gif
tags: javascript, javascript-objects, javascript-object-methods, iwritecode

---

# Introduction

JavaScript object is a non-primitive data type that allows you to store multiple collections of key/value pairs and more complex entities.

## Object Declaration

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678946671484/681ae8b0-cf09-44ce-ab7d-2fa165cc8efe.png align="center")

Here, an object `Object name` is defined. Each member of an object is a `key`: `value` pair separated by commas and enclosed in curly braces `{}`.

### Example:

```javascript
const user = {
    firstName: 'John',
    lastName: 'Due',
};
```

## Accessing Elements

### To get a Complete Object

```javascript
const user = {
    firstName: 'John',
    lastName: 'Due',
};

console.log(user)
```

Output:

```javascript
{
    firstName: 'John',
    lastName: 'Due',
}
```

### To get an element from an Object

```javascript
const user = {
    firstName: 'John',
    lastName: 'Due',
};

console.log(user.firstName)  // dot notation
        // OR
console.log(user['firstName'])  // bracket notation
```

Output:

```javascript
'John'
```

> Here, it calls the objects `key` to get its value.

### To get an element from an Object of another Object

```javascript
const user = {
    name:{
        firstName: 'John',
        lastName: 'Due',
    }
};

console.log(user.name.firstName)
```

Output:

```javascript
'John'
```

# Methods

The JavaScript method is an object property that has a `function value`.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678950105614/9215e6a7-599c-450e-991c-8682f5923b01.png align="center")

## User Defined Methods

### Declaring Methods

```javascript
const user = {
    name: function(){
        return "John"
    }
};
```

### Accessing Methods

```javascript
const user = {
    name: function(){
        return "John"
    }
};

console.log(user.name())
```

Output:

```javascript
John
```

## Built-In Methods

### Object.create()

The Object.create() method is used to create a new object and link it to the prototype of an existing object.

`Object.create(proto)`

```javascript
const user = {
    firstName: 'John',
    lastName: 'Due',
};
const person1 = Object.create(user);
console.log(person1.firstName)
```

Output:

```javascript
John
```

### Object.values()

Object.values() creates an array containing the values of an object.

`Object.values(obj)`

```javascript
const user = {
    firstName: 'John',
    lastName: 'Due',
};
const name = Object.values(user);
console.log(name)
```

Output:

```javascript
[ 'John', 'Due' ]
```

### Object.keys()

Object.keys() creates an array containing the keys of an object.

`Object.keys(obj)`

```javascript
const user = {
    firstName: 'John',
    lastName: 'Due',
};
const name = Object.keys(user);
console.log(name)
```

Output:

```javascript
[ 'firstName', 'lastName' ]
```

### Object.entries()

Object.entries() creates a nested array of the key/value pairs of an object.

`Object.entries(obj)`

```javascript
const user = {
    firstName: 'John',
    lastName: 'Due',
};
const name = Object.entries(user);
console.log(name)
```

Output:

```javascript
[ 
    [ 'firstName', 'John' ], 
    [ 'lastName', 'Due' ] 
]
```

### Object.fromEntries()

Object.fromEntries() creates an object array a nested array.

`Object.fromEntries(obj)`

```javascript
const user = [ [ 'firstName', 'John' ], [ 'lastName', 'Due' ] ]
const name = Object.fromEntries(user);

console.log(name);
```

Output:

```javascript
{ 
    firstName: 'John', 
    lastName: 'Due' 
}
```

### Object.freeze()

Object.freeze() prevents modification to properties and values of an object.

`Object.freeze(obj)`

```javascript
const user = {
    firstName: 'John',
    lastName: 'Due',
};
const name = Object.freeze(user);
name.firstName= 'Mario'
name.middleName= 'Bros'
console.log(name)
```

Output:

```javascript
{ firstName: 'John', lastName: 'Due' }
```

### Object.seal()

Object.seal() prevents new properties from being added to an object, but allows the modification of existing properties.

`Object.seal(obj)`

```javascript
const user = {
    firstName: 'John',
    lastName: 'Due',
};
const name = Object.seal(user);
name.firstName= 'Mario'
name.middleName= 'Bros'
console.log(name)
```

Output:

```javascript
{ firstName: 'Mario', lastName: 'Due' }
```

### Object.assign()

Object.assign() is used to copy values from one or objects to another object.

`Object.assign(destination_objects, ...source_objects)`

```javascript
const name1 = {
    firstName: 'John',
};
const name2 = {
    lastName: 'Due',
};
Object.assign(name2, name1); // Also returns value of name2
console.log(name2)
```

Output:

```javascript
{ lastName: 'Due', firstName: 'John' }
```

### Object.is()

The Object.is() method determines whether two values are the same or not.

`Object.is(value1, value2)`

```javascript
const user = { firstName: 'John', lastName: 'Due' }
const obj = Object.is(user.firstName, 'John');

console.log(obj);
```

Output:

```javascript
true
```