# Inheritance 
As we already know objects in javascript has a default hidden property called [[prototype]] which is either null or references another object. Prototypal inheritance uses prototype to extend an object's properties to another object. For example let's consider a Employee function :- 

```js
function employee(name, age){
    this.name = name;
    this.age = age;
}
```

Now a company can have sales, marketing, accounting employees which can inherit the above emplopyee function instead of creating a whole new function

```js
function employeeDepartment(name,age,department){
    employee.call(this, name, age);
    this.department = department;
}

// To inherit the employee function 
Object.setPrototypeOf(employeeDepartment.prototype, employee.prototype);

// To see the prototype of employeeDepartment
console.log(employeeDepartment.prototype); // employee {constructor: ƒ}


console.log(Object.getPrototypeOf(employeeDepartment.prototype)); ////{getName: ƒ, constructor: ƒ}

const Abhijeet = employeeDepartment("Abhijeet", 23, "Engineering");
//At this point we can guess the output 
console.log(Abhijeet.name);
console.log(Abhijeet.age);
console.log(Abhijeet.department);

```