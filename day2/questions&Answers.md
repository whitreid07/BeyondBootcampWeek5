
1. What are the 3 pillars of Object Oriented Programming?
​
  - Encapsulation: Namespacing, putting things in the same object. Organizing things inside of objects by likeness. 
​
  - Abstraction: Predicting things that might happen and taking care of them for the user. Removing unnecessary information (aka implementation details) (usually procedural code).  
​
  - Inheritence: An object gathers properties from a parent object. 
​
2. What does the new keyword do? Creates a new instance of a prototype:
​
- Makes the function that comes after it return an object (aka the instance)
​
- Assigns the 'this' value inside that function to the instance
​
```javascript
​
const simon = new Person() {
​
}
​
```
​
3. What is the name of the type of function that use to create new objects
​
- Constructor function
​
4. How do we customize properties on an object instance?
​
We use the 'this' keyword to set properties on an object instance.
​
```javascript
​
const me = new Person('simon')
​
const Person = function(name) {
​
  this.name = name
​
  this.greet = function() {
​
    console.log(`Hello, ${this.name}`)
​
  }
​
}
​
```
​
5. Why is it problematic to add methods to an object instance inside of a constructor? How can we mitigate that?
​
This is problematic because it creates an identical copy of the greet function on EACH object instance. Which is redundant and expensive.