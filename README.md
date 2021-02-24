# What I Learned In Week 5 At Code Immersives

&nbsp;

## Functions

What is a Function?

A function is a subprogram designed to perform a particular task.

Functions are executed when they are called. This is known as invoking a function. Values can be passed into functions and used within the function.

Functions always return a value. In JavaScript, if no return value is specified, the function will return undefined.

    function nameOfFunction(parameter) {
    // code to be executed
    }

&nbsp;

## Parameters

Function parameters are the names listed in the function definition.

Function arguments are the real values passed to (and received by) the function.

    function  nameOfFunction(parameter1, parameter2) {
     // code to be executed
    }

&nbsp;

## Return Values

Every function in JavaScript returns undefined unless otherwise specified.

When JavaScript reaches a return statement, the function will stop running.

    str = "John";

    function logMyFirstName(str) {
    console.log(str);
    }

    // Will log "John" to the console

&nbsp;

    function test(){
    return true;
    }

    test();
    // true

&nbsp;

## Booleans

JS primitive data types

1. Strings
2. Numbers
3. Booleans = True or False
4. NaN = Not a number
5. Null = The value null represents the intentional absence of any object value. It is one of JavaScript's primitive values and is treated as falsy for boolean operations.
6. Undefined = The undefined property indicates that a variable has not been assigned a value, or not declared at all.

A JavaScript Boolean represents one of two values: true or false.

Very often, in programming, you will need a data type that can only have one of two values, like

- YES / NO
- ON / OFF
- TRUE / FALSE

For this, JavaScript has a Boolean data type. It can only take the values true or false.

&nbsp;

## &&, ||(or), if, else

Conditional Statements

Very often when you write code, you want to perform different actions for different decisions.

You can use conditional statements in your code to do this.

In JavaScript we have the following conditional statements:

- Use if to specify a block of code to be executed, if a specified condition is true
- Use else to specify a block of code to be executed, if the same condition is false
- Use else if to specify a new condition to test, if the first condition is false

      function nameOfFunction(parameter) {
      if (condition) {
      // block of code to be executed if the condition is true
      } else {
      // block of code to be executed if the condition is false
      }

&nbsp;

## Testing With Quokka & Jest

Quokka.js is a rapid prototyping playground in your editor, with access to your project’s files, inline reporting, code coverage and rich output formatting. Runtime values are updated and displayed in your IDE next to your code, as you type

[quokka](https://quokkajs.com/)

&nbsp;

Jest is a delightful JavaScript Testing Framework with a focus on simplicity. It works with projects using: Babel, TypeScript, Node, React, Angular, Vue and more!

[jest](https://jestjs.io/)
