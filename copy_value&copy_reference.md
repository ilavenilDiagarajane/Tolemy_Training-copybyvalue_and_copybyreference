# Copy By Value vs. Copy By Reference in JavaScript

In JavaScript, when a function is called, the arguments can be passed in two ways .

### **1. copy by value**

Primitive data types such as _string, number, null, undefined, boolean,_ are copy by value in Javascript.primitives are immutable .

### **2. copy by reference(address)**

non-primitive data types such as _objects, arrays, and functions_ are copy by reference in Javascript.non-primitives are mutable .

### Copy By Value

- `In Pass by value`, function is called by _directly_ passing the _value_ of the variable as an argument.

- So any changes made inside the function does _not affect_ the original value.

- The original value and the copied value are _independent_ of each other as they both have a different space in memory.

```js
//javascript copy by value
function copybyvalue(x) {
  x = x + x;

  return x;
}

var y = 10;

var result = copybyvalue(y);

console.log(y); // 10 -- there is no change in orginal value
console.log(result); // 100
```

### Copy By Reference

- `In Pass by Reference`, Function is called by _directly_ passing the _reference/address_ of the variable as an argument.

- So changing the value inside the function also _change_ the original value.

- JavaScript does not create a _new space_ in the memory, instead, we pass the reference/address of the actual parameter.


Object example Copy By Reference
```js
function copyByReference(varObj) {
  console.log("Inside Call by Reference Method");

  Obj.a = 100;

  console.log(varObj);
}

let Obj = {
  a: 1,
};
```
```js
console.log("Before copy By Reference Method");
console.log(Obj);
/*output:
Before copy By Reference Method
{a: 1}*/
```
```js
copyByReference(Obj);
/*output:
Inside Copy by Reference Method
{a: 100}*/

```


```js
console.log("After Copy by Reference Method");
console.log(Obj);
/*output:
After Copy by Reference Method
{a: 100}*/
```




Array example Copy By Reference
```js
let originalArray = [1, 2, 3, 4];

function pushArray(tmpArray) {
  console.log("Inside Call by Reference Method");
  tmpArrary.push(5);
  console.log(tmpArrary);
}
```
```js
console.log("Before copy By Reference Method");
console.log(originalArray);
/*output:
Before copy By Reference Method
[1,2,3,4]
*/
```
```js
pushArray(originalArray);
/*output:
Inside Copy by Reference Method
[1,2,3,4,5]
*/
```
```js
console.log("After Copy by Reference Method");
console.log(originalArray);
/*output:
After Copy by Reference Method
[1,2,3,4,5]
*/
```




