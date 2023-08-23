# Variable Declarations
In javascript we can decalare/use variables using <span style="color:red; font-size:22px"> var, let </span> and <span style="color:red; font-size:22px"> const </span> keywords.
 
## <span style="color : red; font-size : 20px; font-style:italic"> All about var </span>

+ Variables declared with var </span> have global scope, but they can also have local scope depending upon where they are initialized. 
+ Variables declared using var can be redeclared and reassigned. 
``` js
var a = 100;
var a = "Redeclared";
// The above is possible with var declarations

var b = 100;
b="Reassigned"
// Reassignment
``` 
+ var variables are hoisted i.e. they are accessible before there declarations. <span style="font-style: italic"> Remember only the variable declarations are hoisted and not the value of variable 
``` js
console.log(num);
// Hoisted but this will print "undefined" which is the default value of num

var num = 100;
```

## <span style="color : red; font-size : 20px; font-style:italic"> All about let </span>

+ Variables declared with let can have global,local or block scope depening on where they are declared.
``` js
let str = "I am global";

function (){
    let str2 = "I am local";

    if(2 > 1){
        var str3 = "I have a local scope too";
        let str4 = "I have a block scope";

        console.log(str2); // "I am local" because of local scope
    }

    console.log(str3); 
    // "I have a local scope too" variable declared with var has local scope
    
    console.log(str4);
    // Reference Error str4 is not defined. Because str4 has block scope
}
```

+ Variables can not be redeclared, they can only be reassigned. 
+ Variables are hoisted to the top of thier scope but their hoisting works a little different than var. Instead of getting error like variable is not defined or "undefiend", we will get 
```js
console.log(num) //ReferenceError: Cannot access 'num' before initialization
let num = 100;
```
## <span style="color : red; font-size : 20px; font-style:italic"> All about const </span>
+ const variables are same as let variables with regards to scope and hoisting i.e. they are also hoisted but without a default initial value.
+ const variables can neither be redeclared or reassigned.

 
