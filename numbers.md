JavaScript Numbers		
❮ PreviousNext ❯		
        
        
JavaScript has only one type of number. Numbers can be written with or without decimals.		
        
        
Example		
let x = 3.14;    // A number with decimals		
let y = 3;       // A number without decimals		
        
Try it Yourself »		
        
Extra large or extra small numbers can be written with scientific (exponent) notation:		
        
Example		
let x = 123e5;    // 12300000		
let y = 123e-5;   // 0.00123		
        
Try it Yourself »		
        
        
JavaScript Numbers are Always 64-bit Floating Point		
        
Unlike many other programming languages, JavaScript does not define different types of numbers, like integers, short, long, floating-point etc.		
        
JavaScript numbers are always stored as double precision floating point numbers, following the international IEEE 754 standard.		
        
This format stores numbers in 64 bits, where the number (the fraction) is stored in bits 0 to 51, the exponent in bits 52 to 62, and the sign in bit 63:		
        
Value (aka Fraction/Mantissa)	Exponent	Sign
52 bits (0 - 51) 	11 bits (52 - 62)	1 bit (63)
        
Integer Precision		
        
Integers (numbers without a period or exponent notation) are accurate up to 15 digits.		
        
Example		
let x = 999999999999999;   // x will be 999999999999999		
let y = 9999999999999999;  // y will be 10000000000000000		
Try it Yourself »		
        
The maximum number of decimals is 17.		
        
Floating Precision		
        
Floating point arithmetic is not always 100% accurate:		
        
let x = 0.2 + 0.1;		
        
Try it Yourself »		
        
To solve the problem above, it helps to multiply and divide:		
        
let x = (0.2 * 10 + 0.1 * 10) / 10;		
Try it Yourself »		
        
ADVERTISEMENT		
        
Adding Numbers and Strings		
        
WARNING !!		
        
JavaScript uses the + operator for both addition and concatenation.		
        
Numbers are added. Strings are concatenated.		
        
If you add two numbers, the result will be a number:		
        
Example		
let x = 10;		
let y = 20;		
let z = x + y;		
Try it Yourself »		
        
If you add two strings, the result will be a string concatenation:		
        
Example		
let x = "10";		
let y = "20";		
let z = x + y;		
Try it Yourself »		
        
If you add a number and a string, the result will be a string concatenation:		
        
Example		
let x = 10;		
let y = "20";		
let z = x + y;		
Try it Yourself »		
        
If you add a string and a number, the result will be a string concatenation:		
        
Example		
let x = "10";		
let y = 20;		
let z = x + y;		
Try it Yourself »		
        
A common mistake is to expect this result to be 30:		
        
Example		
let x = 10;		
let y = 20;		
let z = "The result is: " + x + y;		
Try it Yourself »		
        
A common mistake is to expect this result to be 102030:		
        
Example		
let x = 10;		
let y = 20;		
let z = "30";		
let result = x + y + z;		
Try it Yourself »		
        
The JavaScript interpreter works from left to right.		
        
First 10 + 20 is added because x and y are both numbers.		
        
Then 30 + "30" is concatenated because z is a string.		
        
        
Numeric Strings		
        
JavaScript strings can have numeric content:		
        
let x = 100;         // x is a number		
        
let y = "100";       // y is a string		
        
JavaScript will try to convert strings to numbers in all numeric operations:		
        
This will work:		
        
let x = "100";		
let y = "10";		
let z = x / y;		
        
Try it Yourself »		
        
This will also work:		
        
let x = "100";		
let y = "10";		
let z = x * y;		
        
Try it Yourself »		
        
And this will work:		
        
let x = "100";		
let y = "10";		
let z = x - y;		
        
Try it Yourself »		
        
But this will not work:		
        
let x = "100";		
let y = "10";		
let z = x + y;		
        
Try it Yourself »		
        
In the last example JavaScript uses the + operator to concatenate the strings.		
        
        
NaN - Not a Number		
        
NaN is a JavaScript reserved word indicating that a number is not a legal number.		
        
Trying to do arithmetic with a non-numeric string will result in NaN (Not a Number):		
        
Example		
let x = 100 / "Apple";		
        
Try it Yourself »		
        
However, if the string is numeric, the result will be a number:		
        
Example		
let x = 100 / "10";		
Try it Yourself »		
        
You can use the global JavaScript function isNaN() to find out if a value is a not a number:		
        
Example		
let x = 100 / "Apple";		
isNaN(x);		
Try it Yourself »		
        
Watch out for NaN. If you use NaN in a mathematical operation, the result will also be NaN:		
        
Example		
let x = NaN;		
let y = 5;		
let z = x + y;		
Try it Yourself »		
        
Or the result might be a concatenation like NaN5:		
        
Example		
let x = NaN;		
let y = "5";		
let z = x + y;		
Try it Yourself »		
        
NaN is a number: typeof NaN returns number:		
        
Example		
typeof NaN;		
Try it Yourself »		
        
Infinity		
        
Infinity (or -Infinity) is the value JavaScript will return if you calculate a number outside the largest possible number.		
        
Example		
let myNumber = 2;		
// Execute until Infinity		
while (myNumber != Infinity) {		
  myNumber = myNumber * myNumber;		
}		
Try it Yourself »		
        
Division by 0 (zero) also generates Infinity:		
        
Example		
let x =  2 / 0;		
let y = -2 / 0;		
Try it Yourself »		
        
Infinity is a number: typeof Infinity returns number.		
        
Example		
typeof Infinity;		
Try it Yourself »		
        
Hexadecimal		
        
JavaScript interprets numeric constants as hexadecimal if they are preceded by 0x.		
        
Example		
let x = 0xFF;		
Try it Yourself »		
        
Never write a number with a leading zero (like 07).		
Some JavaScript versions interpret numbers as octal if they are written with a leading zero.		
        
By default, JavaScript displays numbers as base 10 decimals.		
        
But you can use the toString() method to output numbers from base 2 to base 36.		
        
Hexadecimal is base 16. Decimal is base 10. Octal is base 8. Binary is base 2.		
        
Example		
let myNumber = 32;		
myNumber.toString(32);		
myNumber.toString(16);		
myNumber.toString(12);		
myNumber.toString(10);		
myNumber.toString(8);		
myNumber.toString(2);		
Try it Yourself »		
        
JavaScript Numbers as Objects		
        
Normally JavaScript numbers are primitive values created from literals:		
        
let x = 123;		
        
But numbers can also be defined as objects with the keyword new:		
        
let y = new Number(123);		
        
Example		
let x = 123;		
let y = new Number(123);		
Try it Yourself »		
        
Do not create Number objects.		
        
The new keyword complicates the code and slows down execution speed.		
        
Number Objects can produce unexpected results:		
        
When using the == operator, x and y are equal:		
        
let x = 500;		
let y = new Number(500);		
        
Try it Yourself »		
        
When using the === operator, x and y are not equal.		
        
let x = 500;		
let y = new Number(500);		
        
Try it Yourself »		
        
Note the difference between (x==y) and (x===y).		
        
(x == y) true or false?		
        
let x = new Number(500);		
let y = new Number(500);		
        
Try it Yourself »		
        
(x === y) true or false?		
        
let x = new Number(500);		
let y = new Number(500);		
        
Try it Yourself »		
