



# JavaScript Statements

A JavaScript program is a list of programming statements

JavaScript statements are composed of:

Values, Operators, Expressions, Keywords, and Comments.

The statements are executed, one by one, in the same order as they are written.

### Semicolons *;*

Semicolons separate JavaScript statements.

Add a semicolon at the end of each executable statement:

#### JavaScript White Space

JavaScript ignores multiple spaces. You can add white space to your script to make it more readable.

#### avaScript Line Length and Line Breaks

For best readability, programmers often like to avoid code lines longer than 80 characters.

If a JavaScript statement does not fit on one line, the best place to break it is after an operator:

```
document.getElementById("demo").innerHTML =
"Hello Dolly!";
```

### JavaScript Code Blocks

JavaScript statements can be grouped together in code blocks, inside curly brackets {...}.

The purpose of code blocks is to define statements to be executed together.

One place you will find statements grouped together in blocks, is in JavaScript functions:

```
function myFunction() {
  document.getElementById("demo1").innerHTML = "Hello Dolly!";
  document.getElementById("demo2").innerHTML = "How are you?";
}
```

# JavaScript Syntax

JavaScript syntax is the set of rules, how JavaScript programs are constructed:

```
// How to create variables:
var x;
let y;

// How to use variables:
x = 5;
y = 6;
let z = x + y;
```

### JavaScript Values

The JavaScript syntax defines two types of values:

- Fixed values
- Variable values

Fixed values are called **Literals**.

Variable values are called **Variables**.


#### JavaScript Literals

The two most important syntax rules for fixed values are:

1. Numbers are written with or without decimals:

`10.5`

`1001`



2. Strings are text, written within double or single quotes:

`"John Doe"`

`'John Doe'`


#### JavaScript Variables

In a programming language, variables are used to store data values.

JavaScript uses the keywords `var`, `let` and `const` to declare variables.

An equal `=` sign is used to assign values to variables.

In this example, x is defined as a variable. Then, x is assigned (given) the value 6:

`let x;`
`x = 6;`


# JavaScript comments
JavaScript comments can be used to explain JavaScript code, and to make it more readable.

JavaScript comments can also be used to prevent execution, when testing alternative code.


### Single Line Comments

Single line comments start with `//`.

Any text between `//` and the end of the line will be ignored by JavaScript (will not be executed).

```
// Change heading:
document.getElementById("myH").innerHTML = "My First Page"; 

// Change paragraph:
document.getElementById("myP").innerHTML = "My first paragraph.";


let x = 5;      // Declare x, give it the value of 5
let y = x + 2;  // Declare y, give it the value of x + 2
```

### Multi-line Comments

Multi-line comments start with `/*` and end with `*/`.

Any text between `/* `and `*/` will be ignored by JavaScript.


```
/*
The code below will change
the heading with id = "myH"
and the paragraph with id = "myP"
in my web page:
*/
document.getElementById("myH").innerHTML = "My First Page";
document.getElementById("myP").innerHTML = "My first paragraph.";
```

# JavaScript Variables

Variables are containers for storing values.

JavaScript Variables can be declared in 4 ways:

- Automatically
- Using var
- Using let
- Using const


**When to Use var, let, or const?**

1. Always declare variables

2. Always use const if the value should not be changed

3. Always use const if the type should not be changed (Arrays and Objects)

4. Only use let if you can't use const

5. Only use var if you MUST support old browsers.



### JavaScript Identifiers

All JavaScript variables must be identified with unique names. These unique names are called identifiers.

Identifiers can be short names (like x and y) or more descriptive names (age, sum, totalVolume).

The general rules for constructing names for variables (unique identifiers) are:

- Names can contain letters, digits, underscores, and dollar signs.
- Names must begin with a letter.
- Names can also begin with $ and _ (but we will not use it in this tutorial).
- Names are case sensitive (y and Y are different variables).
- Reserved words (like JavaScript keywords) cannot be used as names.


### Declaring a JavaScript Variable

Creating a variable in JavaScript is called **"declaring"** a variable.

You declare a JavaScript variable with the `var` or the `let `keyword:


```
<p id="demo"></p>

<script>
let carName = "Volvo";
document.getElementById("demo").innerHTML = carName;
</script>
```


#### One Statement, Many Variables

You can declare many variables in one statement. Start the statement with let and separate the variables by comma:


`let person = "John Doe", carName = "Volvo", price = 200;`

**A declaration can span multiple lines:**

```
let person = "John Doe",
carName = "Volvo",
price = 200;
```

### Re-Declaring JavaScript Variables

If you re-declare a JavaScript variable declared with `var`, it will not lose its value.

You cannot re-declare a variable declared with `let` or `const`.
