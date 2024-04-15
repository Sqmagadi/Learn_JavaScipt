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

### Escape Characters

Because strings must be written within quotes, JavaScript will misunderstand this string:

`let text = "We are the so-called "Vikings" from the north.";`

The string will be chopped to "**We are the so-called**".

To solve this problem, you can use an backslash escape character.

The backslash escape character (`\`) turns special characters into string characters:


|Code	|Result	|Description|
|---|---|
|\'	|'	|Single quote|
|\"	|"	|Double quote|
|\\	|\	|Backslash|

*Examples*

\" inserts a double quote in a string:

`let text = "We are the so-called \"Vikings\" from the north.";`

\' inserts a single quote in a string:

`let text= 'It\'s alright.';`



\\ inserts a backslash in a string:

`let text = "The character \\ is called backslash.";`



Six other escape sequences are valid in JavaScript:

|Code	|Result|
|---|---|
|\b	|Backspace|
|\f	|Form Feed|
|\n	|New Line|
|\r	|Carriage Return|
|\t	|Horizontal Tabulator|
|\v	|Vertical Tabulator|


>Note: The 6 escape characters above were originally designed to control typewriters, teletypes, and fax machines. They do not make any sense in HTML.




### Breaking Long Lines

For readability, programmers often like to avoid long code lines.

A safe way to break up a statement is after an operator:

*Example*

```
document.getElementById("demo").innerHTML =
"Hello Dolly!";
```

A safe way to break up a string is by using string addition:

*Example*

```
document.getElementById("demo").innerHTML = "Hello " +
"Dolly!";
```

### Template Strings


Templates are strings enclosed in backticks (`This is a template string`).

Templates allow multiline strings:

*Example*

```
let text =
`The quick
brown fox
jumps over
the lazy dog`;
```

> Note: Templates are not supported in Internet Explorer.


