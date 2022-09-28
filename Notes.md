# isNAN vs Number.isNaN()

`isNaN` is an function used to check whether the value is number or not.if given value is not a number it will return true.coercion will work on inside the isNaN function.

_Syntax of isNaN()_

isNaN(value)

_Parameters of isNaN()_

`value` is the parameter of isNaN()

_Return Value of isNaN()_

Return type of isNaN() method is `boolean`

```js
isNaN(NaN); //  true
isNaN(undefined); //true
isNaN({}); // true
isNaN(true);
/* true will converted to 1 by coercion so function will retrun false.*/
isNaN(null);
/* null  will converted to 0 by coercion so function will retrun false.*/
isNaN(37);
/* parameter is number so it will return false.*/

// strings
isNaN("37"); /*"37" is converted to the number 37 function will retrun false.*/
isNaN("37.37");
/* "37.37" is converted to the number 37.37 function will retrun false.*/
isNaN("37,5");
/* "37,5" is an string so function will retrun true.*/
isNaN("123ABC");
/* "123ABC"is an string so function will retrun true.*/
isNaN(
  ""
); /* false: the empty string is converted to 0 by coercion so function will retrun true.*/
isNaN(" "); // a string with spaces is converted to 0 by coercion so function will retrun false.*/

// dates
isNaN(
  new Date()
); /* new date() will give timestamp so it will be converted to number by coercion so function will retrun false.*/
isNaN(
  new Date().toString()
); /* new date().toSting() will convert to string so function will retrun true.*/
isNaN("blabla"); /* "blabla is  string so function will retrun true"*/
```

`Number.isNaN()` for this method valuse should be NaN and datatype should be Number. doesn't attempt to convert the parameter to a number.
_Syntax of isNaN()_

Number.isNaN()(value)

_Parameters of isNaN()_

`value` is the parameter of Number.isNaN()

_Return Value of isNaN()_

Return type of Number.isNaN() method is `boolean`

```js
Number.isNaN(
  NaN
); /*  is type is number and value is NaN so function return true.*/
Number.isNaN(
  Number.NaN
); /*is type is number and value is NaN so function return true.*/
Number.isNaN(
  0 / 0
); /* is type is number and value is NaN so function return true.*/
Number.isNaN(
  37
); /* is type is number and value is number so function return false.*/
Number.isNaN(
  "NaN"
); /* is type is string  and value string so function return false.*/
Number.isNaN(
  undefined
); /* is type is string  and value is undefined so function return false.*/
Number.isNaN(
  {}
); /* is type is object  and value is empty object so function return false.*/
Number.isNaN(
  "blabla"
); /* is type is string  and value is string so function return false.*/
Number.isNaN(true); /* is type boolean and value is true return false.*/
Number.isNaN(null); /* is type object and value is null return false.*/
Number.isNaN("37"); /* is type string  and value is string return false*/
Number.isNaN("37.37"); /* is type string  and value is string return false*/
Number.isNaN(""); /* is type string  and value is fasly value return false*/
Number.isNaN(" "); /* is type string  and value is empty return false*/
```

# parseInt()

- parseInt() is a function the take string has a parameter and return integer value.
- The radix parameter is used to specify which numeral system to be used.
- radix of 16 (hexadecimal) indicates that the number in the string should be parsed from a hexadecimal number to a decimal number.

_Syntax of parseInt()_

parseInt(string)

parseInt(string, radix)

_Parameters of parseInt()_

`string` is the parameter of parseInt()

`radix` is the parameter of parseInt()

```js
a = parseInt("100");
console.log(a); /* it convert string to number result:100*/

// It returns a Integer until
// it encounters Not a Number character
b = parseInt("2018@geeksforgeeks");
console.log(
  b
); /* it convert string to number and it will return  ]integer until result:2018*/

// It returns NaN on Non numeral character
c = parseInt("geeksforgeeks@2018");
console.log(
  c
); /* it convert string to number and it will return NaN on Non Numeral character result:NaN*/

// It returns Integer value of a Floating point Number
d = parseInt("3.14");
console.log(
  d
); /* it convert string to number and it will return  Integer value of a Floating point Number result:3*/

// It returns only first Number it encounters
e = parseInt("21 7 2018");
console.log(e);
/*It returns only first Number it encounters */
```

# Array Clone

```js
 let numbersCopy = [];

const originalArray = [2,4,6,8,10]

const clone1 = [...originalArray]/*spread method*/

const clone2 = Array.from(originalArray);/*The from() method creates a new array from any array-like or iterable object.*/

const clone3 = originalArray.slice();/*slice method will give shollow copy of original array*/

const clone4 = [].concat(originalArray);

for (i = 0; i < originalArray.length; i++)
{
numbersCopy[i] = originalArray[i];

}
const clone5 = originalArray.map((x) => x);

const clone6  = originalArray.filter(() => true);?
/*filter method return value in new array if it is undefined */
var clone7 = JSON.parse(JSON.stringify(originalArray));
/*“JSON.stringify()” method will convert “originalArray” to string and then it will parse it to an array (object) using the “JSON.parse()” method. The returned array elements will be then copied to “clone7”*/
```
