# Javascript basics

## Web Dev "Body"

- HTML is the bones/skeleton. It gives us the structure of all of our elements
- Javascript is the muscle. It allows the skeleton (and skin) to move, and makes your page generally more "life-like"
- CSS is the skin. It goes on top of the skeleton and muscles to give a more complete look to your page

## The Four JS Building Blocks

- Variables
- Operators
- Conditionals
- Iterators/loops

## Variables

A variable is a reference to a value. Variables come as one of several types and can be declared with the reserved words `var`, `let`, or `const`. Variables are the most fundamental building block in javascript.

### Variable Types

- [String](#string)
- [Number](#number)
- [Boolean](#boolean)
- [Null](#null)
- [Undefined](#undefined)
- [Object](#object)
- [Array](#array)
- [Function](#function)

The 8 variables can be classified as one of three basic categories of data types => [_primitive_](#primitive-data-types), [_composite/reference_](#composite-or-reference-data-types), and [_special_](#special-data-types). They are explained more in detail below. Every variable has access to properties and methods that are **inherited** depending upon what data type they are (the base data type is considered a `prototype` and this inheritence is reffered to as `prototypical inheritence`).

#### Primitive Data Types

Primitive data types encompass the most basic data types.

- ##### String
  - string values will **always** be wrapped in quotation marks.
  - characters inside of the quotation marks are only limited by your character set and can typically include letters, numbers, special characters, or emojis
  - you can use `'single quotes'`, `"double quotes"`, or `` `backticks` ``
  - strings can be `concattenated` or added together with the `+` operator
    ```javascript
    var firstName = "John";
    var lastName = "Doe";
    var fullName = firstName + " " + lastName; // "John Doe"
    ```
  - if using`` `backticks` ``you can also use a technique called `string interpolation` to join strings together
    ```javascript
    var firstName = "John";
    var lastName = "Doe";
    var fullName = `${firstName} ${lastName}`; // "John Doe"
    ```
  - [Common String methods](https://dev.to/frugencefidel/10-javascript-string-methods-you-should-know-4l76)
- ##### Number
  - number values are **never** wrapped in quotation marks
  - frequently used in conjunction with the various `arithmetic operators`
  - typically will somehow involve some sort of math
    ```javascript
    var firstNumber = 150;
    var secondNumber = 500;
    var sum = firstNumber + secondNumber; // 650
    ```
  - [Common Number methods](https://www.w3schools.com/js/js_number_methods.asp)
- ##### Boolean
  - boolean values will be either `true` or `false`, **nothing else**
  - frequently used in conjunction with the various `logical operators`
    ```javascript
    var isTrue = true;
    var isFalse = false;
    ```
  - there really aren't any "common boolean methods"

#### Special Data Types

Special data types are in a category all their own, and don't inherit anything from a prototype (because they have no prototype).

- ##### Null
  - null is the **intentional** absence of value
  ```javascript
  var nothing = null;
  ```
- ##### Undefined

  - a variable that has not been assigned any value is considered of type undefined
  - a function that does not return any value will also log as undefined

  ```javascript
  var something;
  function doNothing() {
    console.log("what a do nothing function");
  }
  console.log(something); // undefined
  console.log(doNothing()); // undefined
  ```

#### Composite or Reference Data Types

Composite or reference data types are more complex and typically build on some other data types (primitive, special or composite). This means composity data types will (frakly, pretty often) have some kind of nested composite data type. (As these types are significantly more complex, there is a bit more space dedicated to them.)

- ##### Object

  - objects are made up of some kind of key/value pair.
  - a `key` must be either a string or a number
    - most commonly keys are of type string, and will be referenced without any quotation marks
    ```javascript
    var someObject = {
      key: "value",
      "some-other-key": "a different value",
      2: "numbers can also be keys",
    };
    ```
  - a `value` can be of ANY type
    - if a value is a function, then that `key` is referred to as a `method`
    ```javascript
    var someObject = {
      stringKey: "A String Value",
      numberKey: 5,
      booleanKey: true,
      undefinedKey: undefined,
      nullKey: null,
      arrayKey: [],
      objectKey: {},
      method: function () {},
    };
    ```

- ##### Array

  - arrays are collections of values
  - these values can be of ANY type

  ```javascript
  var someArray = [
    "a string",
    5,
    true,
    undefined,
    null,
    [],
    {},
    function () {},
  ];
  ```

- ##### Function

  - a function is a block of code designed to perform a specific task
  - a function is first `defined`, and must be invoked or called to execute the specified task/logic
  - function is a reserved keyword for defining a function
  - the function name can be anything you could name any other variable
  - parameters are values that will be passed into the function, once the function has been invoked/called.
    // these values are called parameters when the function is defined, but will be called arguments when the function is invoked

  ```javascript
  // defining a function called `sum` with 2 parameters `x` and `y`
  function sum(x, y) {
    return x + y;
  }
  // invoking the `sum` function with arguments where x=5 and y=6
  var eleven; // variable `eleven` is currently `undefined`
  eleven = sum(5, 6); // variable `eleven` is reassigned and should now have value of 11
  ```

  - functions either return a value, or do not.
  - if a function does not return a value, it typically interacts with some other variable (like invoking another function)

  ```javascript
  function subtract(x, y) {
    return x - y; // returns a new value of x - y
  }
  function subtractWithNoReturn(x, y) {
    console.log(x - y); // just logs the value of x - y
  }
  ```

> Fun/Stupid fact about composite data types
> technically functions and arrays are `objects`.
> In fact, technically all prototypes
> are objects... super confusing, right?
> But, just like any other object, prototypes have properties (keys) and methods

## Operators

Operators allow us to perform operations on or between variables.

### Assigment Operators

### Arithmetic Operators

### Comparison Operators

### Logical Operators
