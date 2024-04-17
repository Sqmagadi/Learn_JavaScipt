# JavaScript BigInt


JavaScript BigInt variables are used to store big integer values that are too big to be represented by a normal JavaScript Number.

*JavaScript Integer Accuracy*

JavaScript integers are only accurate up to 15 digits:

Integer Precision

```
let x = 999999999999999;
let y = 9999999999999999;
```

In JavaScript, all numbers are stored in a 64-bit floating-point format (IEEE 754 standard).

With this standard, large integer cannot be exactly represented and will be rounded.

Because of this, JavaScript can only safely represent integers:

**Up to 9007199254740991 +(253-1)**

and

**Down to -9007199254740991 -(253-1).**

Integer values outside this range lose precision.


*How to Create a BigInt*

To create a BigInt, append n to the end of an integer or call BigInt():

*Examples*

```
let x = 9999999999999999;
let y = 9999999999999999n;
Try it Yourself »
let x = 1234567890123456789012345n;
let y = BigInt(1234567890123456789012345)
```

**BigInt: A new JavaScript Datatype**

The JavaScript typeof a BigInt is "bigint":

```
let x = BigInt(999999999999999);
let type = typeof x;
```

BigInt is the second numeric data type in JavaScript (after Number).

With BigInt the total number of supported data types in JavaScript is 8:

1. String
2. Number
3. Bigint
4. Boolean
5. Undefined
6. Null
7. Symbol
8. Object


**BigInt Operators**

Operators that can be used on a JavaScript Number can also be used on a BigInt.

BigInt Multiplication 

*Example*

```
let x = 9007199254740995n;
let y = 9007199254740995n;
let z = x * y;
```

>Notes: Arithmetic between a BigInt and a Number is not allowed (type conversion lose information).

Unsigned right shift (`>>>`) can not be done on a BigInt (it does not have a fixed width).


**BigInt Decimals**

A BigInt can not have decimals.

*BigInt Division Example*

```
let x = 5n;
let y = x / 2;
// Error: Cannot mix BigInt and other types, use explicit conversion.
let x = 5n;
let y = Number(x) / 2;
```

**BigInt Hex, Octal and Binary**

BigInt can also be written in hexadecimal, octal, or binary notation:

*BigInt Hex Example*

```
let hex = 0x20000000000003n;
let oct = 0o400000000000000003n;
let bin = 0b100000000000000000000000000000000000000000000000000011n;
```

**Precision Curiosity**

Rounding can compromise program security:

*MAX_SAFE_INTEGER Example*

`9007199254740992 === 9007199254740993; // is true !!!`

**Minimum and Maximum Safe Integers**

ES6 added max and min properties to the Number object:

MAX_SAFE_INTEGER

MIN_SAFE_INTEGER

*MAX_SAFE_INTEGER Example*

`let x = Number.MAX_SAFE_INTEGER;`

*MIN_SAFE_INTEGER Example*

`let x = Number.MIN_SAFE_INTEGER;`


**New Number Methods**

ES6 also added 2 new methods to the Number object:

Number.isInteger()

Number.isSafeInteger()


**The Number.isInteger() Method**

The Number.isInteger() method returns true if the argument is an integer.

*Example: isInteger()*

```
Number.isInteger(10);
Number.isInteger(10.5);
```

The Number.isSafeInteger() Method

A safe integer is an integer that can be exactly represented as a double precision number.

The Number.isSafeInteger() method returns true if the argument is a safe integer.

Example isSafeInteger()
Number.isSafeInteger(10);
Number.isSafeInteger(12345678901234567890);
Try it Yourself »

Safe integers are all integers from -(253 - 1) to +(253 - 1).
This is safe: 9007199254740991. This is not safe: 9007199254740992.
