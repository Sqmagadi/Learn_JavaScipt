# JavaScript Template Strings

String Templates

Template Strings

Template Literals

Back-Tics Syntax

Template Strings use back-ticks (``) rather than the quotes ("") to define a string:

*Example*

`let text = `Hello World!`;`


**Quotes Inside Strings**

Template Strings allow both single and double quotes inside a string:

*Example*

let text = `He's often called "Johnny"`;


**Multiline Strings**

Template Strings allow multiline strings:

*Example*

```
let text =
`The quick
brown fox
jumps over
the lazy dog`;
```



**Interpolation**

Template String provide an easy way to interpolate variables and expressions into strings.

The method is called string interpolation.

The syntax is:

`${...}`


**Variable Substitutions**

Template Strings allow variables in strings:

*Example*

```
let firstName = "John";
let lastName = "Doe";

let text = `Welcome ${firstName}, ${lastName}!`;
```

Automatic replacing of variables with real values is called string interpolation.


**Expression Substitution**

Template Strings allow expressions in strings:

*Example*

```
let price = 10;
let VAT = 0.25;

let total = `Total: ${(price * (1 + VAT)).toFixed(2)}`;
```

Automatic replacing of expressions with real values is called string interpolation.


**HTML Templates**


*Example*

```
let header = "Template Strings";
let tags = ["template strings", "javascript", "es6"];

let html = `<h2>${header}</h2><ul>`;
for (const x of tags) {
  html += `<li>${x}</li>`;
}

html += `</ul>`;
```
