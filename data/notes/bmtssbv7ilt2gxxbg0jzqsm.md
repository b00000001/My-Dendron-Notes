
An array is a collection of items.

    `let arr = [1, 2, 3, 4, 5];`

An array can hold any data type (string, number, boolean, etc.)

### Array Declaration

Arrays can be declared as follows:

````
let arr = []

let arr = new Array()```
````

- JavaScript arrays are resizable and can contain a mix of different data types. (When those characteristics are undesirable, use typed arrays instead.)
- JavaScript arrays are not associative arrays and so, array elements cannot be accessed using strings as indexes, but must be accessed using integers as indexes.
- JavaScript arrays are zero-indexed: the first element of an array is at index 0, the second is at index 1, and so on — and the last element is at the value of the array's length property minus 1.
- JavaScript array-copy operations create shallow copies. (All standard built-in copy operations with any JavaScript objects create shallow copies, rather than deep copies).

### Array Methods

| Method        | Description                                                                      |
| ------------- | -------------------------------------------------------------------------------- |
| concat()      | Joins two or more arrays, and returns a copy of the joined arrays                |
| copyWithin()  | Copies array elements within the array, to and from specified positions          |
| entries()     | Returns a key/value pair Array Iteration Object                                  |
| every()       | Checks if every element in an array pass a test                                  |
| fill()        | Fill the elements in an array with a static value                                |
| filter()      | Creates a new array with every element in an array that pass a test              |
| find()        | Returns the value of the first element in an array that pass a test              |
| findIndex()   | Returns the index of the first element in an array that pass a test              |
| forEach()     | Calls a function for each array element                                          |
| from()        | Creates an array from an object                                                  |
| includes()    | Check if an array contains the specified element                                 |
| indexOf()     | Search the array for an element and returns its position                         |
| isArray()     | Checks whether an object is an array                                             |
| join()        | Joins all elements of an array into a string                                     |
| keys()        | Returns a Array Iteration Object, containing the keys of the original array      |
| lastIndexOf() | Search the array for an element, starting at the end, and returns its position   |
| map()         | Creates a new array with the result of calling a function for each array element |
| pop()         | Removes the last element of an array, and returns that element                   |
| push()        | Adds new elements to the end of an array, and returns the new length             |
| reduce()      | Reduce the values of an array to a single value (going left-to-right)            |
| reduceRight() | Reduce the values of an array to a single value (going right-to-left)            |
| reverse()     | Reverses the order of the elements in an array                                   |
| shift()       | Removes the first element of an array, and returns that element                  |
| slice()       | Selects a part of an array, and returns the new array                            |
| some()        | Checks if any of the elements in an array pass a test                            |
| sort()        | Sorts the elements of an array                                                   |
| splice()      | Adds/Removes elements from an array                                              |
| toString()    | Converts an array to a string, and returns the result                            |
| unshift()     | Adds new elements to the beginning of an array, and returns the new length       |
| valueOf()     | Returns the primitive value of an array                                          |
