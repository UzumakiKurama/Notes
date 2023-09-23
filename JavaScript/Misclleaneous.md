# "use strict" 
The purpose of "use strict" is to indicate that the code should be executed in "strict mode". It lets write secure and safe javascript. For ex, it will throw error if we try to use undeclared variables;

Deleting a variable (or object) and a function is not allowed. 
```js
function helloWorld(){
    str = "hello world"
    console.log(str); // This will print hello world without any errors
}
helloWorld()

function helloMars(){
    str = "hello mars"
    console.log(str) // This will give RefferenceError.
}
hellowMars()
```
# Ways to declare objects in Javascripts
There are 4 ways to declare objects in javascript :- 
+ using object literal
+ using Object.create()
+ using constructor (functions) --> constructors are functions that are called using <span style="color : red; ">new</span>
+ using ES6 Classes 

```js 
let employee = {"id" : 1, "name":"Gobind"}; // 1st
employee.address = "Delhi";

let employee2 = Object.create(employee) // 2nd
employee2.name = "Arvind"

function employeeConstructor(){
    this.id = 2;
    this.name = "Ganesh";
}

let employee3 = new employeeConstructor(); //3rd

class Employee{
    constructor(id, name) {
    this.id = id;
    this.name = name;
  }
}

let employee4 = new Employee(1,"Shanko"); // 4th
```


# IIFE (Immediately Invoked Function Expressions)
It is a function that runs as soon as it is defined. This kind of function does not have a name i.e. an anonymous function. 

Use Cases Of IIFE

+ Avoid polluting the global namespace 
+ To create closures
+ Avoid conflict of variable names between libraries and programs.
+ IIFE is used to create private and  public variables and methods
+ It is used to execute the async and await function
+ It is used in JQuery Library
+ It is used to work with require function
