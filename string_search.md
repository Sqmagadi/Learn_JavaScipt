# JavaScript String Search

**String Search Methods**

- String indexOf()
- String match()
- String lastIndexOf()
- String matchAll()
- String search()
- String includes()

**String Templates**

*JavaScript String indexOf()*
    
The indexOf() method returns the index (position) of the first occurrence of a string in a string, or it returns -1 if the string is not found:	
    
*Example*

```
let text = "Please locate where 'locate' occurs!";	
let index = text.indexOf("locate");	
```
	
Note:     
JavaScript counts positions from zero.
    
0 is the first position in a string, 1 is the second, 2 is the third, ...
    
    
*JavaScript String lastIndexOf()*
    
The lastIndexOf() method returns the index of the last occurrence of a specified text in a string:	
    
*Example*

```
let text = "Please locate where 'locate' occurs!";	
let index = text.lastIndexOf("locate");	
```
    
Both indexOf(), and lastIndexOf() return -1 if the text is not found:	
    
*Example*

```
let text = "Please locate where 'locate' occurs!";	
let index = text.lastIndexOf("John");	
```
    
Both methods accept a second parameter as the starting position for the search:	
    
*Example*

```
let text = "Please locate where 'locate' occurs!";	
let index = text.indexOf("locate", 15);	
```
    
The lastIndexOf() methods searches backwards (from the end to the beginning), meaning: if the second parameter is 15, the search starts at position 15, and searches to the beginning of the string.
    
*Example*

```
let text = "Please locate where 'locate' occurs!";	
text.lastIndexOf("locate", 15);	
```
    
*JavaScript String search()*
    
The search() method searches a string for a string (or a regular expression) and returns the position of the match:	
    
*Examples*

```
let text = "Please locate where 'locate' occurs!";	
text.search("locate");	

let text = "Please locate where 'locate' occurs!";	
text.search(/locate/);	
```

They accept the same arguments (parameters), and return the same value?	
    
The two methods are NOT equal. These are the differences:	
    
The search() method cannot take a second start position argument.

The indexOf() method cannot take powerful search values (regular expressions).	
    
You will learn more about regular expressions in a later chapter.	
    
    

    
*JavaScript String match()*
    
The match() method returns an array containing the results of matching a string against a string (or a regular expression).	
    
*Examples*
    
Perform a search for "ain":	

```    
let text = "The rain in SPAIN stays mainly in the plain";	
text.match("ain");	
```
        
Perform a search for "ain":	
    
let text = "The rain in SPAIN stays mainly in the plain";	
text.match(/ain/);	
    

Perform a global search for "ain":	
    
```
let text = "The rain in SPAIN stays mainly in the plain";	
text.match(/ain/g);	
``` 

    
Perform a global, case-insensitive search for "ain":	
    
```
let text = "The rain in SPAIN stays mainly in the plain";	
text.match(/ain/gi);	
 ```

Note:     
If a regular expression does not include the g modifier (global search), match() will return only the first match in the string.	
    
Read more about regular expressions in the chapter JS RegExp.	
    
    
*JavaScript String matchAll()*
    
The matchAll() method returns an iterator containing the results of matching a string against a string (or a regular expression).	
    
*Example*	

`const iterator = text.matchAll("Cats");`	

    
If the parameter is a regular expression, the global flag (g) must be set, otherwise a TypeError is thrown.	
    
*Example*

`const iterator = text.matchAll(/Cats/g);`

    
If you want to search case insensitive, the insensitive flag (i) must be set:	
    
*Example*

`const iterator = text.matchAll(/Cats/gi);`

Notes	
    
matchAll() is an ES2020 feature.
    
matchAll() does not work in Internet Explorer.
    
    
*JavaScript String includes()*
    
The includes() method returns true if a string contains a specified value.	
    
Otherwise it returns false.	
    
*Examples*
    
Check if a string includes "world":

```    
let text = "Hello world, welcome to the universe.";	
text.includes("world");	
```

    
Check if a string includes "world". Start at position 12:	
    
let text = "Hello world, welcome to the universe.";	
text.includes("world", 12);	
    
Try it Yourself »	
Notes	
    
includes() is case sensitive.	
    
includes() is an ES6 feature.	
    
includes() is not supported in Internet Explorer.	
    
    
JavaScript String startsWith()	
    
The startsWith() method returns true if a string begins with a specified value.	
    
Otherwise it returns false:	
    
Examples	
    
Returns true:	
    
let text = "Hello world, welcome to the universe.";	
text.startsWith("Hello");	
    
Try it Yourself »	
    
Returns false:	
    
let text = "Hello world, welcome to the universe.";	
text.startsWith("world")	
    
Try it Yourself »	
    
A start position for the search can be specified:	
    
Returns false:	
    
let text = "Hello world, welcome to the universe.";	
text.startsWith("world", 5)	
    
Try it Yourself »	
    
Returns true:	
    
let text = "Hello world, welcome to the universe.";	
text.startsWith("world", 6)	
    
Try it Yourself »	
Notes	
    
startsWith() is case sensitive.	
    
startsWith() is an ES6 feature.	
    
startsWith() is not supported in Internet Explorer.	
    
    
JavaScript String endsWith()	
    
The endsWith() method returns true if a string ends with a specified value.	
    
Otherwise it returns false:	
    
Examples	
    
Check if a string ends with "Doe":	
    
let text = "John Doe";	
text.endsWith("Doe");	
    
Try it Yourself »	
    
Check if the 11 first characters of a string ends with "world":	
    
let text = "Hello world, welcome to the universe.";	
text.endsWith("world", 11);	
    
Try it Yourself »	
    
Notes	
    
endsWith() is case sensitive.	
    
endsWith() is an ES6 feature.	
    
endsWith() is not supported in Internet Explorer.	
    
    
Complete String Reference	
    
For a complete String reference, go to our:	
    
Complete JavaScript String Reference.	
    
The reference contains descriptions and examples of all string properties and methods.	
