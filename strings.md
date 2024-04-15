# JavaScript Strings

Strings are for storing text and are written with quotes

A JavaScript string is zero or more characters written inside quotes.

*Example*

`let text = "John Doe";`


You can use single or double quotes:

*Example*

```
let carName1 = "Volvo XC60";  // Double quotes
let carName2 = 'Volvo XC60';  // Single quotes
```


> Note: Strings created with single or double quotes works the same.

There is no difference between the two.

Quotes Inside Quotes

You can use quotes inside a string, as long as they don't match the quotes surrounding the string:

*Example*

```
let answer1 = "It's alright";
let answer2 = "He is called 'Johnny'";
let answer3 = 'He is called "Johnny"';
```

### Template Strings

Templates are strings enclosed in backticks (`This is a template string`).

Templates allow single and double quotes inside a string:

Example

`let text = `He's often called "Johnny"`;`



> Note: Templates are not supported in Internet Explorer.


### String Length

To find the length of a string, use the built-in length property:

*Example*

```
let text = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
let length = text.length;
```

###Escape Characters

Because strings must be written within quotes, JavaScript will misunderstand this string:

let text = "We are the so-called "Vikings" from the north.";

The string will be chopped to "We are the so-called ".

To solve this problem, you can use an backslash escape character.

The backslash escape character (\) turns special characters into string characters:

Code
\'
\"
\\
Examples

\" inserts a double quote in a string:

let text = "We are the so-called \"Vikings\" from the north.";
Try it Yourself »

\' inserts a single quote in a string:

let text= 'It\'s alright.';

Try it Yourself »

\\ inserts a backslash in a string:

let text = "The character \\ is called backslash.";

Try it Yourself »

Six other escape sequences are valid in JavaScript:

Code
\b
\f
\n
\r
\t
\v
Note

The 6 escape characters above were originally designed to control typewriters, teletypes, and fax machines. They do not make any sense in HTML.


ADVERTISEMENT

Breaking Long Lines

For readability, programmers often like to avoid long code lines.

A safe way to break up a statement is after an operator:

Example
document.getElementById("demo").innerHTML =
"Hello Dolly!";
Try it Yourself »

A safe way to break up a string is by using string addition:

Example
document.getElementById("demo").innerHTML = "Hello " +
"Dolly!";
Try it Yourself »

Template Strings

Templates were introduced with ES6 (JavaScript 2016).

Templates are strings enclosed in backticks (`This is a template string`).

Templates allow multiline strings:

Example
let text =
`The quick
brown fox
jumps over
the lazy dog`;

Try it Yourself »

Note

Templates are not supported in Internet Explorer.


JavaScript Strings as Objects

Normally, JavaScript strings are primitive values, created from literals:

let x = "John";

But strings can also be defined as objects with the keyword new:

let y = new String("John");
Example
let x = "John";
let y = new String("John");
Try it Yourself »

Do not create Strings objects.

The new keyword complicates the code and slows down execution speed.

String objects can produce unexpected results:

When using the == operator, x and y are equal:

let x = "John";
let y = new String("John");

Try it Yourself »

When using the === operator, x and y are not equal:

let x = "John";
let y = new String("John");

Try it Yourself »

Note the difference between (x==y) and (x===y).

(x == y) true or false?

let x = new String("John");
let y = new String("John");

Try it Yourself »

(x === y) true or false?

let x = new String("John");
let y = new String("John");

Try it Yourself »
