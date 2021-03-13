# What I Learned In Week 5 At Code Immersives

&nbsp;

## If/Else Continued

Multiple if...else statements can be nested to create an else if clause. Note that there is no elseif (in one word) keyword in JavaScript.

    if (condition1)
    statement1
    else if (condition2)
    statement2
    else if (condition3)
    statement3
    ...
    else
    statementN

&nbsp;

## Arrow Functions

An arrow function expression is a compact alternative to a traditional function expression, but is limited and can't be used in all situations.

    // Traditional Function
    function (a){
    return a + 100;
    }

    // Arrow Function Break Down

    // 1. Remove the word "function" and place arrow between the argument and opening body bracket
    (a) => {
    return a + 100;
    }

    // 2. Remove the body brackets and word "return" -- the return is implied.
    (a) => a + 100;

    // 3. Remove the argument parentheses
    a => a + 100;

&nbsp;

For example, if you have multiple arguments or no arguments, you'll need to re-introduce parentheses around the arguments:

    // Traditional Function
    function (a, b){
    return a + b + 100;
    }

    // Arrow Function
    (a, b) => a + b + 100;

    // Traditional Function (no arguments)
    let a = 4;
    let b = 2;
    function (){
    return a + b + 100;
    }

    // Arrow Function (no arguments)
    let a = 4;
    let b = 2;
    () => a + b + 100;

&nbsp;

## Node.js

JavaScript is used across the web development stack.

Backend developers use a type of JavaScript called Node.js for backend work. The Node.js framework allows a developer to handle data updates from the front end and build scalable network applications able to process many simultaneous user requests, amongst other things.

Node.js is an open-source server side runtime environment built on Chrome's V8 JavaScript engine. It provides an event driven, non-blocking (asynchronous) I/O and cross-platform runtime environment for building highly scalable server-side applications using JavaScript.

&nbsp;

## Understanding module.exports & exports in Node.js

In programming, modules are self-contained units of functionality that can be shared and reused across projects. They make our lives as developers easier, as we can use them to augment our applications with functionality that we haven’t had to write ourselves. They also allow us to organize and decouple our code, leading to applications that are easier to understand, debug and maintain.

The module.exports is a special object which is included in every JavaScript file in the Node.js application by default. The module is a variable that represents the current module, and exports is an object that will be exposed as a module. So, whatever you assign to module.exports will be exposed as a module.

Exports is an object. So it exposes whatever you assigned to it as a module. For example, if you assign a string literal then it will expose that string literal as a module.

The following example exposes simple string message as a module in Message.js.

Message.js

    module.exports = 'Hello world';

Now, import this message module and use it as shown below.

app.js

    var msg = require('./Messages.js');

console.log(msg);

    C:\> node app.js
    Hello World

&nbsp;

## process.argv

process.argv is an array containing the command line arguments. The first element will be node, the second element will be the name of the JavaScript file. The next elements will be any additional command line arguments.

Code Example:

Output sum of all command line arguments

index.js

    var sum = 0;
    for (i = 2; i < process.argv.length; i++) {
        sum += Number(process.argv[i]);
    }

    console.log(sum);

Usage Example:

    node index.js 2 5 6 7
    Output will be 20

A brief explanation of the code:

Here in for loop for (i = 2; i < process.argv.length; i++) loop begins with 2 because first two elements in process.argv array always is ['path/to/node.exe', 'path/to/js/file', ...]

Converting to number Number(process.argv[i]) because elements in process.argv array always is string

It starts on 2 because process.argv contains the whole command-line invocation:

    process.argv = ['node', 'yourscript.js', ...]

Elements 0 and 1 are not "arguments" from the script's point of view, but they are for the shell that invoked the script.
