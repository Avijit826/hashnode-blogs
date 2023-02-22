# A In Depth Information Of JavaScript Array & Its Methods

In javascript array is a `built-in global miscellaneous` object, which represents a collection of objects (like string, number, boolean or object etc.).

```javascript
const languages = ["c", "c++", "javascript", "java", "python"]
```

## Declaration

You can create an array using two ways:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676978936291/56043dc3-4e3c-4459-99e1-2d092c3f9531.png align="center")

1. Using an array literal

```javascript
const arr = [] // empty array
const languages = ["c", "c++", "javascript", "java", "python"] // array with elements
```

2. Using Array() constructor

```javascript
const arr = new Array() // empty array
const languages = new Array("c", "c++", "javascript", "java", "python") // array with elements
```

### Different data types in a single array

> JavaScript arrays are `resizable` and can contain a `mix of different data types`.

```javascript
const array1 = ["string", 123, true]
```

Output:

```javascript
["string", 123, true]
```

> Array's length is resized from 3 to 4.

## Accessing array elements

JavaScript arrays elements can accessed via index

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676984262013/97dfcdca-a02a-40b0-aa96-d9ad7943c454.png align="center")

```javascript
const arr = ["L", "C", "O"]
console.log(arr[0])
```

Output:

```javascript
L
```

> Array's index starts with 0, not 1.

### Insert data in an array

```javascript
const arr = new Array()
arr[0] = "data"
```

Output:

```javascript
console.log(arr) // ['data']
```

# Methods

## Array length

With the help of `length` method we get the length of array in number

```javascript
const arr = ["L", "C", "O"]
console.log(arr.length)
```

Output:

```javascript
3
```

> Use of length method

- Iterating over an array
- Shortening an array
- Create empty array of fixed length

## push()

The push() method adds one or more elements to the end of an array.

`push(element0, element1, /* … ,*/ elementN)`

```javascript
const array1 = ["string", 123, true]
array1.push("data")
```

Output:

```javascript
["string", 123, true, "data"]
```

> Use of push() method

- Adding elements to an array
- Merging two arrays

## pop()

The pop() method removes the last element from an array and returns that element.

```javascript
const array1 = ["string", 123, true]
array1.pop()
```

Output:

```javascript
["string", 123]
```

> Use of pop() method

- Removing the last element of an array

## shift()

The shift() method removes the first element from an array and returns that removed element.

```javascript
const array1 = ["string", 123, true]
array1.shift()
```

Output:

```javascript
[123, true]
```

> Use of shift() method

- Removing an element from an array

## unshift()

The unshift() method adds one or more elements to the beginning of an array and returns the new length of the array.

`unshift(element0, element1, /* … ,*/ elementN)`

```javascript
const array1 = ["string", 123, true]
console.log(array1.unshift("data")) //4
```

Output:

```javascript
["data", "string", 123, true]
```

> Use of unshift() method

- Adding elements to an array

## splice()

The splice() method changes the contents of an array by removing or replacing existing elements and/or adding new elements in place.

`splice(start, deleteCount, item1, item2, itemN)`

```javascript
const array1 = ["string", 123, true]
array1.splice(1, 0, "data")
```

Output:

```javascript
["string", "data", 123, true]
```

> Use of splice() method

- Adding elements to an array in any place by with/without replacing existing one.

## slice()

The slice() method returns a shallow copy of a portion of an array into a new array.

`slice(start, end)`

```javascript
const array1 = ["string", 123, true]
array1.slice(1)
```

Output:

```javascript
[123, true]
```

> Use of slice() method

- Creating a new filtered array with originals position.

## map()

The map() method creates a new array populated with the results of calling a provided function on every element in the calling array.

`map((element, index, array) => { /* … */ })`

```javascript
const array1 = ["string", "data", 123]
array1.map((ele) => ele + 4)
```

Output:

```javascript
["string4", "data4", 127]
```

> Use of map() method

- Mapping an array of elements using a function containing an argument.
- To reformat objects in an array.

## filter()

The filter() method creates a shallow copy of a portion of a given array, filtered down to just the elements from the given array that pass a certain condition provided by the function.

`filter((element, index, array) => { /* … */ })`

```javascript
const array1 = ["string", "data", 123]
array1.filter((ele) => typeof ele == "string")
```

Output:

```javascript
["string", "data"]
```

> Use of filter() method

- Filtering out certain elements from array.

## reduce()

The reduce() method executes a function on each element of the array and returns a single output value.

`reduce((accumulator, currentValue, currentIndex, array) => { /* … */ })`

```javascript
const array1 = ["string", "data", 123]
array1.reduce((total, ele) => total + " | " + ele)
```

Output:

```javascript
"string | data | 123"
```

> Use of reduce() method

- Sum of values in an object array.
- Flatten an array of arrays.
- Grouping objects by a property.
- Remove duplicate items in an array.
- Replace .filter().map() with .reduce().

## forEach()

The forEach() method executes a provided function once for each array element. Unlike map() function its return value is discarded.
`forEach((element, index, array) => { /* … */ })`

```javascript
const array1 = ["string", "data", 123]
array1.forEach((ele) => console.log(ele))
```

Output:

```javascript
string
data
123
```

> Use of forEach() method

- Replaces for loop
- Flatten an array of arrays.
- Replace .map().

## concat()

The concat() method returns a new array by merging two or more arrays.

`concat(value0, value1, /* … ,*/ valueN)`

```javascript
const array1 = ["string", "data", 123]
const array2 = [456, 789]
array1.concat(array2)
```

Output:

```javascript
["string", "data", 123, 456, 789]
```

> Use of concat() method

- Merge two arrays, even nested once.

## fill()

The fill() method returns an array by filling all elements with a specified value within range.

`fill(value, start, end)`

```javascript
const array1 = ["string", "data", 123, 456, 789]
array1.fill(111, 1, 4)
```

Output:

```javascript
["string", 111, 111, 111, 789]
```

## find()

The find() method returns the value of the first array element that satisfies the provided test function.

`find((element, index, array) => { /* … */ })`

```javascript
const array1 = ["string", "data", 123]
array1.find((ele) => typeof ele == "string")
```

Output:

```javascript
"string"
```

## from()

The from() method returns the value of the first array element that satisfies the provided test function.

`Array.from(arrayLike, (element, index) => { /* … */ })`

```javascript
Array.from("string")
```

Output:

```javascript
["s", "t", "r", "i", "n", "g"]
```

## includes()

The includes() method checks if an array contains a specified element or not.

`includes(searchElement, fromIndex)`

```javascript
const array1 = ["string", "data", 123]
array1.includes("data")
```

Output:

```javascript
true
```

## indexOf()

The indexOf() method returns the first index at which a given element can be found in the array. It returns -1 if element is not present.

`indexOf(searchElement, fromIndex)`

```javascript
const array1 = ["string", "data", 123]
array1.indexOf("data")
```

Output:

```javascript
1
```

## join()

The join() method returns a new string by concatenating all of the elements in an array, separated by a specified separator.

`join(separator)`

```javascript
const array1 = ["string", "data", 123]
array1.join(" | ")
```

Output:

```javascript
"string | data | 123"
```

## reverse()

The reverse() method returns the array in reverse order.

`reverse()`

```javascript
const array1 = ["string", "data", 123]
array1.reverse()
```

Output:

```javascript
[123, "data", "string"]
```

## sort()

The sort() method sorts the items of an array in a specific order.

`sort((a, b) => { /* … */ } )`

```javascript
const array1 = ["string", "data", 456, 123, 789]
array1.sort()
```

Output:

```javascript
[123, 456, 789, "data", "string"]
```

## toString()

The toString() method returns a string representing the specified array and its elements.

`toString()`

```javascript
const array1 = ["string", "data", 123]
array1.toString()
```

Output:

```javascript
"string,data,123"
```
