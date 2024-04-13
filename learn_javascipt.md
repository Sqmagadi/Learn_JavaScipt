
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
