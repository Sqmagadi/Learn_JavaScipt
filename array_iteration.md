JavaScript Array Iteration	
❮ PreviousNext ❯	
Array Iteration Methods	
    
Array iteration methods operate on every array item:	
    
Array forEach	Array every()
Array map()	Array some()
Array flatMap()	Array from()
Array filter()	Array keys()
Array reduce()	Array entries()
Array reduceRight()	Array with()
See Also:	Array Spread (...)
Basic Array Methods	
Array Search Methods	
Array Sort Methods	
    
JavaScript Array forEach()	
    
The forEach() method calls a function (a callback function) once for each array element.	
    
Example	
const numbers = [45, 4, 9, 16, 25];	
let txt = "";	
numbers.forEach(myFunction);	
    
function myFunction(value, index, array) {	
  txt += value + "<br>";	
}	
Try it Yourself »	
    
Note that the function takes 3 arguments:	
    
The item value	
The item index	
The array itself	
    
The example above uses only the value parameter. The example can be rewritten to:	
    
Example	
const numbers = [45, 4, 9, 16, 25];	
let txt = "";	
numbers.forEach(myFunction);	
    
function myFunction(value) {	
  txt += value + "<br>";	
}	
Try it Yourself »	
    
JavaScript Array map()	
    
The map() method creates a new array by performing a function on each array element.	
    
The map() method does not execute the function for array elements without values.	
    
The map() method does not change the original array.	
    
This example multiplies each array value by 2:	
    
Example	
const numbers1 = [45, 4, 9, 16, 25];	
const numbers2 = numbers1.map(myFunction);	
    
function myFunction(value, index, array) {	
  return value * 2;	
}	
Try it Yourself »	
    
Note that the function takes 3 arguments:	
    
The item value	
The item index	
The array itself	
    
When a callback function uses only the value parameter, the index and array parameters can be omitted:	
    
Example	
const numbers1 = [45, 4, 9, 16, 25];	
const numbers2 = numbers1.map(myFunction);	
    
function myFunction(value) {	
  return value * 2;	
}	
Try it Yourself »	
    
JavaScript Array flatMap()	
    
ES2019 added the Array flatMap() method to JavaScript.	
    
The flatMap() method first maps all elements of an array and then creates a new array by flattening the array.	
    
Example	
const myArr = [1, 2, 3, 4, 5, 6];	
const newArr = myArr.flatMap((x) => x * 2);	
Try it Yourself »	
Browser Support	
    
JavaScript Array flatMap() is supported in all modern browsers since January 2020:	
    
    
    
    
    
    
    
JavaScript Array filter()	
    
The filter() method creates a new array with array elements that pass a test.	
    
This example creates a new array from elements with a value larger than 18:	
    
Example	
const numbers = [45, 4, 9, 16, 25];	
const over18 = numbers.filter(myFunction);	
    
function myFunction(value, index, array) {	
  return value > 18;	
}	
Try it Yourself »	
    
Note that the function takes 3 arguments:	
    
The item value	
The item index	
The array itself	
    
In the example above, the callback function does not use the index and array parameters, so they can be omitted:	
    
Example	
const numbers = [45, 4, 9, 16, 25];	
const over18 = numbers.filter(myFunction);	
    
function myFunction(value) {	
  return value > 18;	
}	
Try it Yourself »	
    
JavaScript Array reduce()	
    
The reduce() method runs a function on each array element to produce (reduce it to) a single value.	
    
The reduce() method works from left-to-right in the array. See also reduceRight().	
    
The reduce() method does not reduce the original array.	
    
This example finds the sum of all numbers in an array:	
    
Example	
const numbers = [45, 4, 9, 16, 25];	
let sum = numbers.reduce(myFunction);	
    
function myFunction(total, value, index, array) {	
  return total + value;	
}	
Try it Yourself »	
    
Note that the function takes 4 arguments:	
    
The total (the initial value / previously returned value)	
The item value	
The item index	
The array itself	
    
The example above does not use the index and array parameters. It can be rewritten to:	
    
Example	
const numbers = [45, 4, 9, 16, 25];	
let sum = numbers.reduce(myFunction);	
    
function myFunction(total, value) {	
  return total + value;	
}	
Try it Yourself »	
    
The reduce() method can accept an initial value:	
    
Example	
const numbers = [45, 4, 9, 16, 25];	
let sum = numbers.reduce(myFunction, 100);	
    
function myFunction(total, value) {	
  return total + value;	
}	
Try it Yourself »	
    
JavaScript Array reduceRight()	
    
The reduceRight() method runs a function on each array element to produce (reduce it to) a single value.	
    
The reduceRight() works from right-to-left in the array. See also reduce().	
    
The reduceRight() method does not reduce the original array.	
    
This example finds the sum of all numbers in an array:	
    
Example	
const numbers = [45, 4, 9, 16, 25];	
let sum = numbers.reduceRight(myFunction);	
    
function myFunction(total, value, index, array) {	
  return total + value;	
}	
Try it Yourself »	
    
Note that the function takes 4 arguments:	
    
The total (the initial value / previously returned value)	
The item value	
The item index	
The array itself	
    
The example above does not use the index and array parameters. It can be rewritten to:	
    
Example	
const numbers = [45, 4, 9, 16, 25];	
let sum = numbers.reduceRight(myFunction);	
    
function myFunction(total, value) {	
  return total + value;	
}	
Try it Yourself »	
    
JavaScript Array every()	
    
The every() method checks if all array values pass a test.	
    
This example checks if all array values are larger than 18:	
    
Example	
const numbers = [45, 4, 9, 16, 25];	
let allOver18 = numbers.every(myFunction);	
    
function myFunction(value, index, array) {	
  return value > 18;	
}	
Try it Yourself »	
    
Note that the function takes 3 arguments:	
    
The item value	
The item index	
The array itself	
    
When a callback function uses the first parameter only (value), the other parameters can be omitted:	
    
Example	
const numbers = [45, 4, 9, 16, 25];	
let allOver18 = numbers.every(myFunction);	
    
function myFunction(value) {	
  return value > 18;	
}	
Try it Yourself »	
    
JavaScript Array some()	
    
The some() method checks if some array values pass a test.	
    
This example checks if some array values are larger than 18:	
    
Example	
const numbers = [45, 4, 9, 16, 25];	
let someOver18 = numbers.some(myFunction);	
    
function myFunction(value, index, array) {	
  return value > 18;	
}	
Try it Yourself »	
    
Note that the function takes 3 arguments:	
    
The item value	
The item index	
The array itself	
    
    
JavaScript Array.from()	
    
The Array.from() method returns an Array object from any object with a length property or any iterable object.	
    
Example	
    
Create an Array from a String:	
    
Array.from("ABCDEFG");	
    
Try it Yourself »	
Browser Support	
    
from() is an ES6 feature (JavaScript 2015).	
    
ES6 is fully supported in all modern browsers since June 2017:	
    
    
    
    
    
from() is not supported in Internet Explorer.	
    
    
JavaScript Array keys()	
    
The Array.keys() method returns an Array Iterator object with the keys of an array.	
    
Example	
    
Create an Array Iterator object, containing the keys of the array:	
    
const fruits = ["Banana", "Orange", "Apple", "Mango"];	
const keys = fruits.keys();	
    
for (let x of keys) {	
  text += x + "<br>";	
}	
    
Try it Yourself »	
Browser Support	
    
keys() is an ES6 feature (JavaScript 2015).	
    
ES6 is fully supported in all modern browsers since June 2017:	
    
    
    
    
    
keys() is not supported in Internet Explorer.	
    
    
JavaScript Array entries()	
Example	
    
Create an Array Iterator, and then iterate over the key/value pairs:	
    
const fruits = ["Banana", "Orange", "Apple", "Mango"];	
const f = fruits.entries();	
    
for (let x of f) {	
  document.getElementById("demo").innerHTML += x;	
}	
    
Try it Yourself »	
    
The entries() method returns an Array Iterator object with key/value pairs:	
    
[0, "Banana"]	
[1, "Orange"]	
[2, "Apple"]	
[3, "Mango"]	
    
The entries() method does not change the original array.	
    
Browser Support	
    
entries() is an ES6 feature (JavaScript 2015).	
    
ES6 is fully supported in all modern browsers since June 2017:	
    
    
    
    
    
entries() is not supported in Internet Explorer.	
    
    
JavaScript Array with() Method	
    
ES2023 added the Array with() method as a safe way to update elements in an array without altering the original array.	
    
Example	
const months = ["Januar", "Februar", "Mar", "April"];	
const myMonths = months.with(2, "March");	
Try it Yourself »	
    
JavaScript Array Spread (...)	
    
The ... operator expands an iterable (like an array) into more elements:	
    
Example	
const q1 = ["Jan", "Feb", "Mar"];	
const q2 = ["Apr", "May", "Jun"];	
const q3 = ["Jul", "Aug", "Sep"];	
const q4 = ["Oct", "Nov", "May"];	
    
const year = [...q1, ...q2, ...q3, ...q4];	
