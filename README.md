# Javascript_Documentation

### Introduction
JavaScript is non-blocking, asynchoronous(when task is taking time for processing at that time other lines of code executed and this task is run in background) programming language and it's easy to learn.

### Datatypes
There are two type of datatypes
1. primitive datatype
2. non-primitive datatype

The primitive datatypes are given below:

1. ```Number```  for number
2. ```BigInt```  is for integer numbers of arbitrary length.
3. ```String``` for string.
4. ```Boolean``` for ```true/false```
5. ```null``` for unknown values
6. ```undefined``` for unassigned values

### "use strict"

When we write a "use strict" in top of the script then it should be executed in strict mode which means it shows an error when we use any variable without its declaration.
```JavaScript
"use strict";
name = "Kevin"; // it gives an error name is not declared.
```

### typeof operator
The typeof operator returns the datatype of the given argument.
The typeof operator returns a string with type name.

```JavaScript
typeof undefined // "undefined"

typeof 5 // "number"

typeof 5n // "bigint"

typeof true // "boolean"

typeof "js" // "string"

typeof null // "object"
```
The typeof operator returns object for object, arrays and null because in js arrays and null are object.

### Variables

Variables are used store the data value.
To create variables in JS, use ```var``` ```let``` and ```const``` keywords.
```var``` declarations are globally scoped or function scoped while ```let``` and ```const``` are block scoped.
```var``` variables can be updated and re-declared within its scope; ```let``` variables can be updated but not re-declared; ```const``` variables can neither be updated nor re-declared.
While ```var``` and ```let``` can be declared without being initialized, ```const``` must be initialized during declaration.

### Popup Boxes

#### alert

```alert()``` function is used to show popup message to the user and it will wait for the user to press ```ok```.

#### prompt
```prompt()``` function takes two parameters. the first parameter is input messge to be displayed and second parameter is optional for taking initial value for input field.

#### confirm

```confirm()``` shows a message and waits for the user to press “OK” or “Cancel”. It returns ```true``` for OK and ```false``` for Cancel/Esc.


### Type Conversion

#### String Conversion
JavaScript Variables can be converted to another data types either by automatically js itself or by the use of js function.
```String()``` method converts any values to string.

```
let num = 5
typeof num // number

num = String(num)
typeof num // String
```

#### Numeric Conversion

In mathematical expression the conversion happen automatically.
```
"8"/"2" //4, strings are automatically converted to numbers
```
Using ```Number()``` method we convert value to number.

```
let name = "57"
typeof name //string

name = Number(name)
typeof name //number
```

when we try to convert any invalid string to number than it will give NaN as a result.
```
Number("john") //NaN
Number(null) //0
Number(undefined) //NaN
```

#### Boolean Conversion

Values that are “empty”, like 0, an empty string, null, undefined, and NaN, become false.
Other values become true.

```
Boolean(1); // true
Boolean(0); // false

Boolean("hello"); // true
Boolean(""); // false

Boolean("0") //True, in js non-empty string returns always true
```

### Object.is(value1, value2)

This method compares whether the both value are same or not.
```Object.is()``` method is same as ```===```.
The difference between both the method is ```===``` method is that  ```-0``` and ```+0``` are strictly equal but not same value.

```
-0 === +0 //true
Object.is(-0, +0) //false

NaN === NaN //false
Object.is(NaN, NaN) //true
```
