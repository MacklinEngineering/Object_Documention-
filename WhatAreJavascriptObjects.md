### Compiled by “Team Moses”: Joshua Wilkerson, Asiah Bennett, Nyah Macklin, Eric Espinoza, Finesse Carter, Zahmir Jacobs, and Vanessa Charles

# OBJECTS in JavaScript

## What is an object?
#### An object is an unordered list of properties, methods, and attributes which are made up of a key and a value associated with it.
#### Example: Think of a car. A car is an object. A car has a color, make, model etc. and those are properties.
#### Properties: are specific characteristics of the object. It is what differentiates two or more objects from each other.

#### Object: Car
#### Make: Chevy
#### Model: Cruz
#### Year: 2018

### Another Example:
#### Here is the JavaScript representation of a blue Bic ballpoint pen.
#### const pen = {
#### type: "ballpoint",
#### color: "blue",
#### brand: "Bic"
#### };

## How are objects useful in JavaScript?
#### JavaScript objects can be created by simply setting their properties within a pair of curly braces: {...}. Each property is a # key/value pair (A Key points to a value stored in memory). This is called an object literal.
#### The advantage is that the things that belong together are put together in code. Such as anything key/value pair associated with the object “pen” should be in that object.
#### Objects allow for leeway to be creative. Nothing is definite.
#### Higher-order Functions- are functions inside of functions (allow for higher abstractions)
#### Object-Oriented Programming (OOP):

## Chapter 1:Primitive and Reference Types

#### Javascript has no classes, instead, it uses types. There are two kinds: Primitive and Reference.
#### References are stored as objects, which in short are pointing to locations in memory.
#### Javascript uses a variable object to track variables in a specific scope.
#### Both of these types are accessed through objects.
### Primitive Types:
#### Types that are primitive are stored as simple data types.
#### The Primitive Types- pieces of data that are stored as; boolean, number, string, Null, undefined, bigInt, symbol.
#### A variable containing primitive value directly holds the primitive value As opposed to using a pointer
#### Typeof operator is the best way to find Typeof primitive value
### Reference Types:
#### Reference objects are the closest thing to classes
#### Reference values are instances of reference types and are synonymous with objects.
#### Reference Types do not store the object directly into the variable but point to the location in memory where the object exists.

#### To instantiate is to create an object
#### You can use a a new operator with a constructor

## Chapter 2: Functions
### What is a function? 
#### Functions are objects. They behave differently than functions in other languages.
### What is a declaration vs. expressions? 
#### They are two literal terms of functions. A declaration starts with a function keyword and includes the name of the function right after it
### Example:
#### 	Function add(num1, num2){
#### 		Return num1 + num2	;
#### }

### An expression is a function that does not require a name after and is considered an anonymous object function.
### Example:
#### 	Var add = function(num1, num2){
#### 		Return num1 + num2
#### };

### Functions as Values:
#### You can use a function anywhere you would use any other reference value.

## Chapter 3: Defining Properties
#### Properties are the specific characteristics of the object. It is what differentiates two or more objects from each other. ex: a car is an object. The properties could be the model, the color, the brand of the car or the weight. Both use the same object but are created to be something new.
#### Var car1 = {brand: toyota};
#### Var car2 = new object()

#### Car1.color = “red”;
#### Car2.color = “blue”;

#### Car1.weight = “805 kg”;
#### Car2.weight = “8o5 kg”;

#### Removing Properties:
#### For removing properties the Delete operator removes the intended property from the table. If at any point you target a property that does not exist the return will be undefined. Lastly, there are some things that cannot be deleted, an example of this is

#### var person1 = {
#### name: "Nicholas"
#### };
#### console.log("name" in person1); // true
#### delete person1.name; // true - not output
#### console.log("name" in person1); // false
#### console.log(person1.name); // undefined

#### The return comes back false when the delete is applied, meaning it didn’t work! When the property comes back truthy or true is when the property has been deleted properly from the object.

### Types of properties:
#### There are two types of properties. First is the data, they contain a value like a name property.

#### The second is the accessor properties. This one defines the function call, but they do not have a value inside of them.

#### For the accessor properties, they can only use getter or setter as well as using both of them at the same time. The getter is when the function is read. The setter is when the function to call is written.
#### The getter: Are expected to return a value.
#### The setter: Received the value being assigned to the property as an argument.

#### Preventing Object Modification:

#### Object.preventExtensions() is the method that is used to stop any kind of changes to the properties again. This is one of the ways to create a non extensible object.  An example of this:
#### var person1 = {
#### name: "Nicholas"
#### };
#### ❶ console.log(Object.isExtensible(person1)); // true
#### ❷ Object.preventExtensions(person1);
#### console.log(Object.isExtensible(person1)); // false
#### ❸ person1.sayName = function() {
#### console.log(this.name);
#### };
#### console.log("sayName" in person1); // false

#### Number one of the example is showing the extension being checked. Number two is the extension being prevented. It is now non-extensible. Number three will not be added because the method was successful.

## Chapter 4: Constructors and Prototypes:
#### What is a constructor?

### JavaScript uses special functions called constructor functions to define and initialize objects and their features. They are useful because you'll often come across situations in which you don't know how many objects you will be creating; constructors provide the means to create as many objects as you need in an effective way, attaching data and functions to them as required.

#### The only visual difference between a regular function and a constructor is that the function name should be capitalized when it is a constructor.

#### Example: function person(){ vs function Person(){

### What is a Prototype?
#### Think of prototypes as recipes for objects. Every function has a prototype property.

### How do you identify it?
#### [[Prototype]] is a pointer back to the prototype object that the instance is using. -- When you create a new object using new, constructor’s prototype property is assigned to the [[Prototype]] property of that new object.


## Chapter 5: Inheritance

### What is inheritance?

#### In traditional object-oriented languages classes inherit properties from other classes. In Javascript-inheritance can occur between objects with no class like structure defining the relationship...aka prototypes

### What are the two prototypes that are referred to as? What do they do?
#### Prototype chaining, Prototype inheritance: child objects inherit methods and attributes from their parents.

#### Defining these objects and their inheritance structures is a matter of creating classes that extend one another. A class is a definition of attributes and behaviors, an object is an instance of a given class.

#### Example: You might have a base Animal class with methods that allow animals to eat and sleep. Then, your Dog class inherits the eat and sleep methods from its Animal parent class while also defining its own methods like bark and be_undyingly_loyal.

### Why is inheritance important?

#### It helps build reusable and modular components of software applications because we can inherit from and extend the parent class in many different ways.

### What is constructor inheritance?

#### The constructor property returns a reference to the object constructor function that created the instance object. The value is only read-only for primitive values such as 1, true, and "test"
#### Example: 	input
#### function Tree(name) { this.name = name }
#### let theTree = new Tree('Redwood')
#### console.log('theTree.constructor is ' + theTree.constructor)
#### output
#### the Tree.constructor is function Tree(name) { this.name = name }

## Chapter 6: Object Patterns

### In Javascript there are different ways to create objects. You can create your own custom types and generic objects to accomplish your goals. There are Private and Privileged Members, Module Patterns, Scope-Safe Constructors and Mixins to make more complex objects.

### What is a Module Pattern?

#### Module pattern is an object-creation pattern designed to create singleton objects with private data. The basic approach is to use an immediately invoked function expression that returns an object.

#### var yourObject = (function() {
#### // private data variables
#### return {
#### // public methods and properties
#### }; }());

### What is Mixin?

#### The mixin function accepts two arguments: the receiver and the supplier. The goal of the function is to copy all enumerable properties from the supplier onto the receiver.

#### function mixin(receiver, supplier) {
#### for (var property in supplier) {
#### if (supplier.hasOwnProperty(property)) {
#### receiver[property] = supplier[property]
#### }
#### }
#### return receiver;
#### }

### What are Scope-safe constructors?

### Scope-safe constructors are constructors that you can call with or without new to create a new object instance. This pattern takes advantage of the fact that this is an instance of the custom type as soon as the constructor begins to execute, which lets you alter the constructor’s behavior depending on whether or not you used the new operator.

#### function Book(name, year) {
####  if (!(this instanceof Book)) {
####    return new Book(name, year);
####  }
####  this.name = name;
####  this.year = year;
#### }

#### var person1 = new Book("Javascript book", 2014);
#### var person2 = Book("Javascript book", 2014);

#### console.log(person1 instanceof Book);    // true
#### console.log(person2 instanceof Book);    // trueBook(name, year) {
####  if (!(this instanceof Book)) {
####    return new Book(name, year);
####  }
####   this.year = year;
#### }

#### var person1 = new Book("Javascript book", 2014);

#### console.log(person1 instanceof Book);    // true
#### console.log(person2 instanceof Book);    // true

## In conclusion, we’ve discussed how to create objects in Javascript and the main facets of how they work and what intricacies they have.  
