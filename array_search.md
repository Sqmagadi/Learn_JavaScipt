JavaScript Array Search	
❮ PreviousNext ❯	
Array Find and Search Methods	
Array indexOf()	Array find()
Array lastIndexOf()	Array findIndex()
Array includes()	Array findLast()
See Also:	Array findLastIndex()
Basic Methods	
Sort Methods	
Iteration Methods	
    
JavaScript Array indexOf()	
    
The indexOf() method searches an array for an element value and returns its position.	
    
Note: The first item has position 0, the second item has position 1, and so on.	
    
Example	
    
Search an array for the item "Apple":	
    
const fruits = ["Apple", "Orange", "Apple", "Mango"];	
let position = fruits.indexOf("Apple") + 1;	
    
Try it Yourself »	
Syntax	
array.indexOf(item, start)	
item	Required. The item to search for.
start	Optional. Where to start the search. Negative values will start at the given position counting from the end, and search to the end.
    
Array.indexOf() returns -1 if the item is not found.	
    
If the item is present more than once, it returns the position of the first occurrence.	
    
    
JavaScript Array lastIndexOf()	
    
Array.lastIndexOf() is the same as Array.indexOf(), but returns the position of the last occurrence of the specified element.	
    
Example	
    
Search an array for the item "Apple":	
    
const fruits = ["Apple", "Orange", "Apple", "Mango"];	
let position = fruits.lastIndexOf("Apple") + 1;	
    
Try it Yourself »	
Syntax	
array.lastIndexOf(item, start)	
item	Required. The item to search for
start	Optional. Where to start the search. Negative values will start at the given position counting from the end, and search to the beginning
    
JavaScript Array includes()	
    
ECMAScript 2016 introduced Array.includes() to arrays. This allows us to check if an element is present in an array (including NaN, unlike indexOf).	
    
Example	
const fruits = ["Banana", "Orange", "Apple", "Mango"];	
    
fruits.includes("Mango"); // is true	
Try it Yourself »	
Syntax	
array.includes(search-item)	
    
Array.includes() allows to check for NaN values. Unlike Array.indexOf().	
    
Browser Support	
    
includes() is an ECMAScript 2016 feature.	
    
ES 2016 is fully supported in all modern browsers since March 2017:	
    
    
    
    
    
includes() is not supported in Internet Explorer.	
    
    
ADVERTISEMENT	
    
JavaScript Array find()	
    
The find() method returns the value of the first array element that passes a test function.	
    
This example finds (returns the value of) the first element that is larger than 18:	
    
Example	
const numbers = [4, 9, 16, 25, 29];	
let first = numbers.find(myFunction);	
    
function myFunction(value, index, array) {	
  return value > 18;	
}	
Try it Yourself »	
    
Note that the function takes 3 arguments:	
    
The item value	
The item index	
The array itself	
    
Browser Support	
    
find() is an ES6 feature (JavaScript 2015).	
    
ES6 is fully supported in all modern browsers since June 2017:	
    
    
    
    
    
find() is not supported in Internet Explorer.	
    
    
JavaScript Array findIndex()	
    
The findIndex() method returns the index of the first array element that passes a test function.	
    
This example finds the index of the first element that is larger than 18:	
    
Example	
const numbers = [4, 9, 16, 25, 29];	
let first = numbers.findIndex(myFunction);	
    
function myFunction(value, index, array) {	
  return value > 18;	
}	
Try it Yourself »	
    
Note that the function takes 3 arguments:	
    
The item value	
The item index	
The array itself	
    
Browser Support	
    
findIndex() is an ES6 feature (JavaScript 2015).	
    
ES6 is fully supported in all modern browsers since June 2017:	
    
    
    
    
    
findIndex() is not supported in Internet Explorer.	
    
    
JavaScript Array findLast() Method	
    
ES2023 added the findLast() method that will start from the end of an array and return the value of the first element that satisfies a condition.	
    
Example	
const temp = [27, 28, 30, 40, 42, 35, 30];	
let high = temp.findLast(x => x > 40);	
Try it Yourself »	
Browser Support	
    
findLast() is an ES2023 feature.	
    
It is supported in all modern browsers since July 2023:	
    
    
    
    
    
JavaScript Array findLastIndex() Method	
    
The findLastIndex() method finds the index of the last element that satisfies a condition.	
    
Example	
const temp = [27, 28, 30, 40, 42, 35, 30];	
let pos = temp.findLastIndex(x => x > 40);	
Try it Yourself »	
