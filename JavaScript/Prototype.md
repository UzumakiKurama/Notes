# Prototype 

Every Object in javascript has a built-in-property called prototype. The prototype is itself an object so it has its own prototype object and the chain goes on and on untill when we reach an prototype that has null for its prototype. This is called as <span style="color: red; font-size:16px"> prototype chaining </span>

<span style="font-style: italic"> Note: The property of an object that points to its prototype is not called prototype. Its name is not standard, but in practice all browsers use "\__proto__". The standard way to access an object's prototype is the Object.getPrototypeOf() method. </span>

When we try to access a property of an object, it will first try to find inside the object if the property is not there then it will search inside the prototype object and it will keep doing so untill it finds null as prototype 